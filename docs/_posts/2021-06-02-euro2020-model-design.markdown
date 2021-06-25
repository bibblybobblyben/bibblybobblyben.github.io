---
layout: posts
title:  "Euro 2020 Model details"
date:   2021-06-02 12:00:00 +0000
categories: statistics sports
excerpt: "A simple model for a simple game"
header:
  teaser: /assets/football_euro2020/TeamAttackRankings.png
---

Having introduced our simple reweighting of goals in [my other post]({% post_url 2021-06-02-euro202-model-intro %}), now we'll try and use the scores to predict the winners of football games in the upcoming tournament. I am going to stick to just using attacking metrics to predict the number of goals scored by each team, and will leave a combined analysis of attacking and defensive stats for a later date. 

## The model

I am going to use a simple model that uses the reweighted attacking power metrics, called the "attack only" model, and another which combines both the attacking and defensive evaluations into a single model to predict games. 

### Predicting scores
The model uses the attacking and defensive scores described in the [initial data analysis]{% post_url 2021-06-02-euro202-model-intro %}. Attacking ratings are calculated from a training set of fixtures, according to the team's weighted goals average, and the standard deviation of this score measured to account for the spread in this performance. The same is done for the defensive ratings. The typical difference between this predicted score and the true score is also measured, to get an idea of how noisy a predictor it is. We now have the components we need for our simple simulator.

The steps taken to simulate a game are therefore:
- First, Measure the attacking and defensive powers of each team
- then, For each team, choose a random attack and defence rating based off the historical spread of values for that team
- Thirdly, Calculate the predicted goals for each team based off this measure
- Finally, Produce a final score based off the historical difference between our predicted measure and the true score

For the interested, the distributions are always Gaussian, which is a drastic oversimplification of reality. This is likely to give underdogs an overrated chance of winning and favourites an underweighted chance. Repeating this process many times allows us to produce probabilities for the outcomes. 

## The team rankings
The figure below shows the attacking ratings for every team in the tournament. The histogram shows the distribution of all attacking ratings recorded in their fixtures, and the solid orange lines shows the Gaussian distribution approximation. 

![dghh](/assets/football_euro2020/TeamAttackRankings.png "Team attacking abilities")

Teams such as Finland and Scotland have almost all of their matches having a low attacking ranking, whereas Spain and Belgium have a much higher likelihood of getting a high attack ranking in any given game. The approximation works to different extents for different teams; Austria's true distribution is not too dissimilar to the Gaussian profile, but England, Wales and Slovakia deviate somewhat. Choosing a dsitribution that more accurately reproduces these profiles may result in beter performance. However, the profiles are somewhat close to the truth so we will persist with the use of Gaussians for the time being.    


## Comparing the two models

We compare both the attack - only and the combined defence/attack models, and across different training sets; one training set only considers the qualification games for that tournament, the other considers all games across the previous 2 years. The below tables show the results when measured across the previous 4 tournaments, with the aggregated statistic on the bottom row. The "RSS" statistic is described [https://github.com/mberk/rss-euro-2020-prediction-competition](here) and is included as it gives a way to combine the probability of a match result with the outcome in a weighted way. A lower score for this is better, and it essentially penalises you for events rated as unlikely occurring, or benefits you if events you rate as highly likely do occur. I also use an "Accuracy" statistic, which instead looks at whether the most likely event is actually the one that occurs. Any fixtures containing the host nation are ignored as they do not participate in tournament qualification.



| Tournament | Training Data | RSS Score: Att| RSS Score:Both| RSS: Random | Accuracy:Att |Accuracy:Both|
|--------|-----------|-----------|------------|---|---|--|
Euro 2004|Qualification|25.89|25.34| 27.47|10/25 |11/25|
Euro 2008|Qualification|26.57| 27.75| 27.47|14/25 |8/25|
Euro 2012|Qualification|26.21|26.36 |27.46|13/25|11/25|
Euro 2016|Qualification|51.25|50.59| 48.33|10/44 |16/44|
**Total**|**Qualification**|**129.92**|**130.04**|**130.74**|**47/119**|**46/119**|

This first table details the results when only the qualifying data is used to quantify the ability of the teams. The Attack only model performs slightly better than the combined model, and both have a slight advantage over the score that a completely uninformed model would produce, which would assign 33% likelihood to each of the potential outcomes, but the difference is not huge. Considering accuracy, the attack only model picked the true outcome 39% of the time, whereas the combined model achieved an accuracy of 38.7%. 

| Tournament | Training Data | RSS Score: Att| RSS Score:Both| RSS: Random | Accuracy:Att |Accuracy:Both|
|--------|-----------|-----------|------------|---|---|--|
Euro 2004|All matches|28.90 |25.98 |27.47|9/25|12/25|
Euro 2008|All matches|32.97|27.28| 27.47|4/25 |10/25|
Euro 2012|All matches|32.14|25.26 | 27.47|(5/25 |13/25|
Euro 2016|All matches|53.2| 49.31 |48.33|13/44|16/44)|
**Total**|**All matches**|**147.21**|**127.83**|**130.74**|**31/119**|**51/119**|


In this second table, we instead train the model on all of the fixtures in the preceding two  years. Now, the combined model outperforms the Attack only model by a large margin, with the attack only model doing worse than a completely uninformed model on the RSS statistic. This is reflected in the accuracy, where it has a much worse score of 26.1% compared to the 33.3% of an uninformed model. The combined model gets the best scores seen across any of the tests in this configuration - it has the lowest RSS score and the highest accuracy, reaching 42.9%. 

None of the performances achieved are particularly stellar, with performance generally being only slightly above random chance. Assuming a noise of $$ \sqrt{N}$$ with $$ N = 119$$ games, the error on the measurement of accuracy is 9% - meaning all results are consistent with a performance of chance. Don't say I didn't warn you. 

Such a performance is probably not too surprising - we haven't given the model any information other than historical scores, and the wealth of further data such as possession, shots, shots on target would further improve the modelling approach. Ignoring so many sources of variation is bound to hinder the model, but availability of this data is limited. However, the fact that such a simple model manages to learn <i>something</i> about the teams, by outperforming random chance, suggests that there may be some merit to this approach, and further work could improve it. 
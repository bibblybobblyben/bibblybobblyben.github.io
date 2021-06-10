---
layout: posts
title:  "How dependent are England and Belgium on their star players?"
date:   2021-06-06 12:00:00 +0000
categories: statistics sports
excerpt: "How will the form of Raheem Sterling and fitness of Kevin De Bruyne influence their Euro 2020 prospects?"
header:
  teaser: assets/thumbnails/BayesRule.png
---

As the model used to simulate the tournament relies solely on goal scored data, we can explore how changing performance for a team in qualifying can alter their chances at Euro 2020. Suppose we want to evaluate how a team will do without a certain player - we can re-evaluate the team by removing their goals from their performance rating and see how it affects their team. Similarly we could add new players in in their place. 

As an English Manchester City fan, two players immediately occur to me to consider - Raheem Sterling, and Kevin De Bruyne. Sterling has been in worse form than in previous years, but played a significant part in the qualifying campaign for England, whereas Kevin De Bruyne got injured in the final of the Champions League. This post explores the effect this may have on the chances for each of their national sides. I'll remove 75% of their goals and assists from their team's qualifying statistics, and see how the team likelihood changes.

## England and Reheem Sterling
Firstly, I will change England's attacking weighting to account for the possibility that Raheem Sterling's drop in form could translate to the international side too. In qualifying, he scored 8 goals and provided 6 assists, being involved in 14 of England's 37 goals, or approximately 38%. A drop in his form will therefore leave the team with a significant gap, and I will simulate this by removing 75% of his contribution from the England attacking rating. I do not remove 100% as I assume a replacement provides an amount of attacking threat, but less than Sterling. 

This chart shows the probability of England appearing in each location in the tournament. England have a 12% chance of winning the whole tournament according to our model, based off their historical performance. Below shows how likely they are to reach each possible location in the knockout stages. Only some of the final 16 rounds are possible for them to qualify for, but the third place ranking system means there is a non zero chance of qualifying for a lot of them.

![dghh](/assets/football_euro2020/EnglandWinProbability.png "Probability of England reaching different stages in the Euro 2020 tournament")

Reducing England's attacking potential, reduces their likelihood of winning the tournament.
![dghh](/assets/football_euro2020/EnglandWinProbability_NoSterling.png "Probability of England reaching different stages in the Euro 2020 tournament without Sterling")
# Belgium and Kevin De Bruyne
The below figure shows a full strength Belgium's chances of progressing to different stages. As they have had a very strong qualifying campaign, they are highly rated by the model and expected to win the tournament.

![dghh](/assets/football_euro2020/BelgiumWin.png "Probability of Belgium reaching different stages in the Euro 2020 tournament based off historical performance")

Removing goals from De Bruyne alters their chances of winning by approximately the same fraction as the reduced goals. 

![dghh](/assets/football_euro2020/BelgiumWin_NoKDB.png "Probability of Belgium reaching different stages in the Euro 2020 tournament without Kevin De Bruyne")

Most interestingly, whereas Belgium were originally favourites in the model, Italy are now the favourites for the tournament. The biggest boost to Italy for this summer's tournament may therefore be for Kevin De Bruyne to be unavailable.
![dghh](/assets/football_euro2020/all_tournament_nokdb.png "Most likely tournament positions without Kevin De Bruyne")


---
layout: posts
title:  "Euro 2020 - whole tournament predictions"
date:   2021-06-06 12:00:00 +0000
categories: statistics sports
excerpt: "Find out the teams predicted to do well in Euro 2020 "
header:
  teaser: /assets/football_euro2020/winning_probs.png
---

Through running many simulations of the tournament, probabilities can be calculated for each team's performance at Euro 2020. This page details the predictions made for group winners and overall tournament winners using the Gaussian model. 

## Group Winner
First, we evaluate how likely each team is to appear in each position in their group, shown in the table below.  

|Team|Winner|Runner up|Third|Last| 
 |---|---|---|---|---| 
**Group A**| | | | | 
Turkey|0.14|0.22|0.28|0.35| 
Italy|0.49|0.27|0.16|0.08| 
Wales|0.16|0.25|0.29|0.3| 
Switzerland|0.21|0.26|0.27|0.26| 
**Group B**| | | | | 
Denmark|0.29|0.38|0.22|0.11| 
Finland|0.07|0.19|0.35|0.39| 
Belgium|0.57|0.27|0.11|0.04| 
Russia|0.07|0.16|0.32|0.45| 
**Group C**| | | | | 
Netherlands|0.46|0.27|0.17|0.1| 
Ukraine|0.13|0.21|0.29|0.36| 
Austria|0.28|0.3|0.24|0.18| 
North Macedonia|0.13|0.22|0.3|0.36| 
**Group D**| | | | | 
England|0.65|0.22|0.09|0.04| 
Croatia|0.18|0.34|0.28|0.2| 
Scotland|0.06|0.18|0.3|0.46| 
Czech Republic|0.11|0.26|0.32|0.31| 
**Group E**| | | | | 
Spain|0.56|0.24|0.13|0.07| 
Sweden|0.11|0.23|0.31|0.35| 
Poland|0.2|0.3|0.28|0.23| 
Slovakia|0.13|0.23|0.29|0.35| 
**Group F**| | | | | 
Hungary|0.08|0.16|0.28|0.48| 
Portugal|0.37|0.31|0.21|0.11| 
France|0.4|0.3|0.19|0.1| 
Germany|0.15|0.23|0.32|0.31| 


England are the team most expected to win their group, closely followed by Belgium and Spain who are all over 50% likely to top their groups. Italy and the Netherlands are only slightly less that 50% likely to win their groups, with the competitibe Group F the only one with no clear expected winner. Hungary, Scotland and Russia are all expected to struggle. Group A is particularly competitive, where any of the three teams after Italy have reasons to aim for qualifying for the next round, with Turkey being the weakest of these sides.  

## Tournament Winner 

Including the knockout rounds, we can calculate how likely each team is to win the whole tournament, shown in the table below. 

|Team|% Probability of:| Winning|Finalist|Semi-finalist|Quarter Finalist|R16| 
 |--|-|---|-|-|-|-| 
Belgium| |20.0|31.4|45.8|67.9|93.7|  
Italy| |15.8|25.4|38.3|59.2|88.0|  
England| |12.1|21.5|37.5|61.5|94.8|  
Spain| |10.6|19.6|35.8|61.3|90.9|  
Denmark| |8.5|16.5|29.1|48.7|82.2|  
Portugal| |5.9|12.3|25.8|46.0|84.0|  
Netherlands| |5.3|11.9|24.0|49.8|86.9|  
France| |5.3|11.7|25.4|45.4|84.8|  
Switzerland| |2.6|6.5|14.5|31.3|65.6|  
Austria| |2.0|5.6|13.6|33.8|74.9|  
Wales| |1.8|5.1|12.1|26.5|61.4|  
Poland| |1.8|5.2|13.9|33.3|68.4|  
Germany| |1.4|3.9|10.3|24.3|58.6|  
Turkey| |1.1|3.4|9.2|22.4|55.5|  
Sweden| |1.1|3.0|8.6|22.6|53.2|  
Croatia| |0.8|3.0|9.8|28.0|69.7|  
Russia| |0.8|2.7|7.4|17.2|41.3|  
Finland| |0.7|2.1|6.8|17.5|46.4|  
North Macedonia| |0.6|1.7|5.6|18.3|53.8|  
Ukraine| |0.6|1.8|6.1|18.9|53.9|  
Slovakia| |0.5|2.1|7.5|21.8|54.0|  
Czech Republic| |0.3|1.6|5.9|19.3|56.8|  
Hungary| |0.3|1.0|3.3|11.8|40.8|  
Scotland| |0.2|0.9|3.7|12.9|40.2|  

Belgium and Italy are highly favoured by the model, with their likely clash in the quarter finals. France have quite a low probability, a combination of their mixed results over the past year and their very difficult path out of the group - their 40% probability of winning the group is the lowest of any expected group winner. If they finish second, they also face the task of beating England, who the model rates highly. Denmark are surprisingly rated highly, due to their solid defence and good results against highly ranked teams. They are also in a group they are expected to perform well in, and should avoid the side of the draw with Belgium and Italy in, further increasing their chances of making the final.


# Most likely team to reach a given position

We can also plot the most likely team to appear at any given position in the tournament. As teams can take multiple routes to the final, they can appear in multiple places. For example, Spain is expected to win their group, but in the less likely event that they come second, they are highly likely to win their last 16 game anyway and progress. Another example is Italy - they are expected to win their group, but are more likely to come second than any of the other teams, due to how evenly matched they are.  

![dghh](/assets/football_euro2020/all_tournament.png "Most likely tournament positions")


It is likely that the difficult group that France are in, meaning they face England and Spain if they come second or Italy and Belgium, or possibly still Spain, if they come first, means they have a tough route to the final off the back of a difficult group, reducing their probability of winning. Belgium are highly likely to win their group and last 16 match, before facing the difficult opponents of Italy and France. Further, the fact Belgium have a 20% chance of winning the tournament is not solely due to the 21% chance of reaching the first half final slot - there is a non zero probability they progress through the second half of the draw.
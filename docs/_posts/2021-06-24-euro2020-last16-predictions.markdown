---
layout: posts
title:  "Euro 2020 - Last 16 predictions"
date:   2021-06-24 23:00:00 +0000
categories: statistics sports
excerpt: "Probabilities for each of the last 16 games in the Euro 2020 tournament"
header:
  teaser: /assets/football_euro2020/odds_screenshot.png
---


The conclusion of the group stages brings us to the knockout rounds, with a few surprise qualifiers. The model is updated to included the group stage performance and probabilities for each team winning are displayed below, with a brief discussion. To see the rankings which are used to calculate these probabilites, see [here]({% post_url 2021-06-24-euro2020-last16-predictions_knockout_updated %}).

<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Wales vs Denmark</h1>
The first match sees the runners up in Group A face the second placed side in Group B, and both were beaten by teams which are highly rated by the model. Wales had already qualified by the time they played Italy, whereas Denmark only qualified with their final match of the group, following the distressing events of their first match against Finland. They looked very impressive in that final match, and gave Belgium a difficult game. The odds for each team winning this tie are shown below.

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |3.81|**Wales**|3.75|**Denmark**|2.12| 

Denmark have a slightly less than 50% chance of progressing from this game, aided by having one of the best defences in the tournament and a higher attacking rating than Wales.  

### Bookmakers comparison
These odds compare somewhat similarly to bookmakers, with Denmark typically quoted at around 1.8. Our model gives Wales a higher chance than the bookmakers, who are currently pricing Wales at 5.0. Considering the attacking ranking Gaussian distribution, this is likely due to our model over-estimating the probability of Wales having a high scoring game.

## Form-based model

An alternative form of the model applies a higher weight to more recent results, and a lower weight to older scores. Applying this weighting produces the probabilities below. The probabilities chance very little in this situation.  

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |3.81|**Wales**|3.74|**Denmark**|2.13| 

## Goal scoring probabilities

|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.0|0.01|0.07|0.18|0.29|**0.45**| Wales | | Denmark |**0.32**|0.26|0.23|0.13|0.05|0.01| 

This is further shown in the probabilities above, for the likelihood of each team scoring a specified number of goals. The relatively high probability of Wales failing to score gives Denmark a high chance of progressing. The effect of Christian Eriksen not playing for Denmark are not accounted for, beyond including their results from the group stages.
<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Italy vs Austria</h1>

Next up sees the best defensively ranked side Italy play Austria, who came second in their group. Italy beat all teams in their group and have continued their defensive solidity into the tournament, and Austria beat both Ukraine and North Macedonia to qualify, despite losing to the Netherlands. The model strongly expects Italy to win this game, as shown in the odds below.

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.72|**Italy**|4.23|**Austria**|5.52|

### Bookmakers comparison
Again our odds are quite similar to the bookmakers, in agreeing that there is a strong favourite. Prices for Italy are currently at around 1.45, whereas Austria are at around 8, meaning we are giving Austria a slightly better chance than the bookies. However, unlike Wales in the above example, both Italy and Austria seem to fit our model relatively well, but a good result for Austria is still a long bet. Our likelihood of a draw is almost equivalent to the bookies, which currently price it at 4.2.

## Form-based model

Italy's long running winning streak and consecutive clean sheets mean that the form based reweighting of the model is even more confident of an Italy victory, giving Austria only approximately a 10% chance of winning. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.43|**Italy**|5.1|**Austria**|9.47| 





## Goal scoring probabilities

|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.02|0.07|0.17|**0.25**|0.25|0.23| Italy | | Austria |**0.48**|0.31|0.16|0.04|0.0|0.0| 

 Again, the probability of Austria failing to score is giving Italy their strong chance of progressing, due to Italy's incredibly strong defence. In fact, the model only gives them a 79% probability of scoring less than 1.5 goals, whereas Italy have only a 48% chance of scoring under the same threshold. A result for Italy here would be a very strong upset, and would require a strong defensive performance from them, as chances to score are expected to be scarce.

<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Netherlands vs Czech Republic</h1>

The winners of Group C play the third place team in Group D, who had been leading the group before the final match day. The Czech Republic have been competitive in all of their matches, and the Netherlands have been keen to attack everyone they play. As a first place team playing a third place side, it is perhaps unsurprising that they are emphatic favourites in this match, as shown in the odds below. 

 |Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.57|**Netherlands**|5.88|**Czech Republic**|5.15| 


### Bookmakers comparison
Bookies are currently quoting Netherlands at 1.66, giving them a very slightly smaller chance than our model, whereas Czech Republic are currently priced at 5.5, which is pretty similar to our probability. The main disagreement is in the probability of a draw, which is much more likely in the bookmaker's opinions, priced at 3.75. 


## Form-based model

Considering recent form, the Czech Republic have a slightly improved chance, based off good results in the group stages and a down weighting of early qualifying results, such as the 5-0 defeat to England. They are still an outside bet though, at just under 25% chance of winning. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.66|**Netherlands**|5.82|**Czech Republic**|4.43| 



## Goal scoring probabilities


|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.08|0.15|0.2|**0.21**|0.16|0.14| Netherlands | | Czech Republic |**0.35**|0.28|0.22|0.11|0.03|0.01| 

 The Czech Republic are more likely to score than any other the previous 2 underdog sides, with a 22% chance of scoring 2 goals, although failing to score is still their most likely outcome. The reason they are expected to lose is that the Netherlands are expect to score heavily against them, with the most likely result being 2 goals, but a 15% chance of scoring 4 goals. This is shown in the [rankings]({% post_url 2021-06-24-euro2020-last16-predictions_knockout_updated %}), where the Netherlands are not exceptional defensively. With two sides expected to have the potential to score, it could be quite a lively game.  


<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Belgium vs Portugal</h1>

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.74|**Belgium**|5.15|**Portugal**|4.35| 

The Group B winners, and pre-tournmanent model favourites, Belgium play Portugal, who came third in the group of death, F. Portugal were the only side to beat Hungary in their group, before being comprehensively beaten by Germany and drawing against the world champions France. Belgium beat Denmark in a difficult game, emphatically beating Russia and managing to eventually break down Finland in the final game. On the face of it, it seems quite an even game, but the model strong favours Belgium. If Portugal concede at the rate they have against Germany and France, Belgium are expected to be able to capitalise. 

### Bookmakers comparison
Bookmakers are currently pricing Belgium at 2.45, and Portugal at 3.00, meaning they are very unsure of the outcome. This is in stark contrast to the model we use, which would view any result other than  Belgium win to be quite an upset. In the 
[rankings]({% post_url 2021-06-24-euro2020-last16-predictions_knockout_updated %}), Belgium are significantly strong than Portugal in attack and slightly better defensively, so it is not too surprising the model doesn't rate Portugal's chances. 


## Form-based model
The form based model is slightly less sure of a Belgium win, but they are still odds-on favourites. Portugal had some mixed results in a difficult group, but have been able to score freely, and Belgium have won games that they would have been expected to win, albeit perhaps not by as high margins as expected. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.91|**Belgium**|4.87|**Portugal**|3.69|


## Goal scoring probabilities


|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 | | | | | | | | **Group F** | | | | | | | | 
 |0.05|0.13|0.21|**0.24**|0.19|0.15| Belgium | | Portugal |**0.31**|0.3|0.24|0.11|0.03|0.0|

The attacking ability of Belgium is reflected in the likely goals scored odds. They have a 21% chance of scoring 3 goals, and a 13% chance of scoring 4, compared to 11% and 3% for Portugal for the same figures. Both sides have a good chance of scoring goals in the game, but Portugal only having a 15% chance of keeping Belgium from scoring a goal is what gives the Belgians such a strong chance of winning this tie.  



<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Croatia vs Spain</h1>

Spain were slow to get going in this tournament, playing out two slow draws before obliterating Slovakia 5-0 in their final match, but this could not prevent them coming second in their group. Their strong attack rating is what gives our model its confidence in their ability, so they will need to continue their goalscoring into future games, but if that game signals a return to form for them they could be optimistic. Croati lost to England in their opening game, before drawing with the Czech Republic and beating the team our model considers the worst in the tournament, Scotland. Spain are expected to win this game, in one of the most one sided matches of the round.


|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |5.44|**Croatia**|6.81|**Spain**|1.49| 

### Bookmakers comparison

Bookies are currently quoting prices very similar to our model. with 6.00 for Croatia and 1.6 for Spain, indicating they are similarly confident in the outcome. They rank the draw much more likely than our model, at 3.7.  

## Form-based model

Even though Spain's recent form has been mixed, with a slow start to the group campaign before emphatically beating Slovakia, their form still gives them a slightly improved chance of winning the group. Croatia have also had a poor Euros so far, only qualifying due to a victory against Scotland on the final game. Concededing against Scotland is not likely to have helped them in the model though, where Spain are one of the better attacking sides. They are quite a long shot to win this game, from the model's perspective.

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |6.72|**Croatia**|7.07|**Spain**|1.41|

## Goal scoring probabilities

|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.0|0.03|0.11|0.24|0.3|**0.31**| Croatia | | Spain |0.15|0.13|0.16|**0.17**|0.15|0.11|

 The high attacking ranking of Spain means they are most likely to score 3 goals against Croatia, with 4 goals being as likely as 0 goals. Croatia meanwhile have an 85% chance of scoring fewer than 2.5 goals, expecting the Spanish to outscore them in this match. If their goal scoring continues from the match against Slovakia, this could prove to be the case, but if they play more like how they did in their earlier group matches, Croatia can feel confident about scoring a goal against them. 



<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">France vs Switzerland</h1>

The world champions France, having won the most difficult group, play Switzerland who came third in Group A. Our model doesn't rank France particularly highly for attacking or defensive ability, meaning they are less favoured than in many other models. Switzerland had mixed results in their group games, and this is one of the less unequal ties in the round. France are favourites, but with a slightly less than 50% chance of winning. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |2.05|**France**|5.06|**Switzerland**|3.18| 

### Bookmakers comparison
Bookmakers favour France considerably more strongly than our model does, with them being priced at 1.5 and Switzerland at 7.00, under half the probability we give them of winning. The model does give Switzerland a higher probability of higher attacking performances than the distribution of results suggests, this is skewed by the fact they have had a few high scoring games. For example, a 3-3 against Germany, and have managed to score against both Belgium and Spain. They may therefore have the potential to score against the French, but will need to keep things tight in defence. They did not manage to do so against Italy in the knockout rounds, a similarly ranked team for attacking potential to France.


## Form-based model

France have drawn against Hungary and Portugal and beaten Germany, whereas Switzerland drew against Wales, beat Turkey and lost to Italy. Accounting for this form causes one of the larger shifts in the model output, with France now comfortable favourites to win the game. Switzerland's chances fall from about 33% without considering form, down to almost 20% when form is considered.

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.6|**France**|6.56|**Switzerland**|4.49| 



## Goal scoring probabilities


|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.05|0.11|0.18|0.21|0.19|**0.23**| France | | Switzerland |**0.29**|0.25|0.23|0.14|0.06|0.02|

Switzerland's chances of scoring against France do help their chances in this match, but France are expected to edge the game by outscoring them. 0-0 is considered the most likely score, but with both sides reliant on their attack, a defensive mistake by either side is considered likely.


<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Engand vs Germany</h1>

Another exciting tie in the last 16 sees the winners of Group D England play Germany, who came runners up in Group F. England completed the group stages without conceding a goal, but without scoring particularly freely. They did however take 7 points from a possible 9. Germany lost to France, beat Portugal in a high scoring game, before seeing out a dramatic 2-2 match against Hungary on the final day. The model emphatically expects England to win, with Germany considered signfiicant underdogs. 

 |Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.66|**England**|5.77|**Germany**|4.47| 

### Bookmakers comparison
Our model gives England a much better chance than the bookies, who currently price England at 2.50, and they give Germany a much better chance, pricing their victory at 2.9, suggesting they are very unsure of the outcome. Our model's confidence likely comes from the porous German defence, which has also been shown in the group stages were they conceded in every match.



## Form-based model

England have yet to concede in this tournament, whereas Germany have conceded in every game they have played, leading the model to become even more confident in an England victory.  All signs therefore point to a surprise 1-0 to Germany. Germany are given a staggeringly small chance of only 15.5% of winning this match, and England rated at almost 70% to win.

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |1.44|**England**|6.56|**Germany**|6.45|

## Goal scoring probabilities

|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.09|0.14|0.17|0.18|0.15|**0.2**| England | | Germany |**0.32**|0.29|0.24|0.11|0.03|0.01| 

The goal scoring probabilities further show that England's defence is expected to give them the edge against Germany, with England expected to keep them to 1 goal or fewer. England are expected to score several goals against this defence, but they have not scored highly so far in this tournament. They may need to find their scoring touch in this game to ensure qualifying, or rely on continuing their defensive solidity.  



<h1 style="text-align: center; font-size:32px;background-color:mediumslateblue;padding:20px;">Sweden vs Ukraine</h1>

The final match in the last 16 sees the winners of Group E Sweden play Ukraine, who came third in Group B. Sweden were quite a shock winner in their group, but got a point against Spain before beating both Poland and Slovakie. They have shown defensive strength, which the model did not expect to be so prevalent. Ukraine only managed to beat North Macedonia, but scored a couple against the Netherlands before losing the Austria in the final match, which decided who finished second. The odds are quite split on this one, with Sweden expected to edge it but both sides can be optimistic of making the quarter finals. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |2.4|**Sweden**|4.24|**Ukraine**|2.88| 


### Bookmakers comparison
The bookmakers also consider it to be quite an even contest, pricing Sweden at 2.25 and Ukraine at 3.3, meaning they are slightly more confident in Sweden winning this one. They may be applying more weight to Sweden's recent form and good showings against highly rated sides such as Poland and Spain, whereas our model also considers longer term historical results across the past few years. 


## Form-based model

Sweden's perforances in the group stages give them a slightly better chance of progressing, bringing our odds into closer alignment with that currently offered by the bookmakers. They have been improved defensively and managed to score against both Poland and Slovakia, which suggests they could have the solidity to keep Ukraine at bay whilst getting the goal they ened to progress. 

|Odds of winning | Team 1| Odds of Draw |Team 2|Odds of winning 
 |-|-|-|-|-| 
 |2.21|**Sweden**|4.59|**Ukraine**|3.04|


## Goal scoring probabilities


|5|4|3|2|1|0| Team 1|vs|Team 2|0|1|2|3|4|5 
 |-|-|-|-|-|-|-|-|-|-|-|-|-|-|-| 
 |0.02|0.06|0.14|0.23|0.25|**0.3**| Sweden | | Ukraine |**0.32**|0.28|0.24|0.12|0.04|0.01|

 Sweden has a slightly better defensive rating, whereas Ukraine have a slightly better attacking rating. Both sides will therefore need to play at a high level in order to try and win this match. Both teams have a decent chance of scoring, and there is little to choose between them. The weaker Swedish attack seems to be well matched by the weaker Ukrainian defence, but if the Swedish defensive strength continues into the next round then they may edge this game. 

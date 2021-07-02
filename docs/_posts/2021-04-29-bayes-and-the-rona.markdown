---
layout: posts
title:  "False Positives and False Confidence"
date:   2021-04-29 12:00:00 +0000
categories: statistics
excerpt: "Why you need to pay attention past the Intro to Stats lecture."
header:
  teaser: assets/thumbnails/BayesRule.png
---

<head>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
</head>

One of the side effects of the Covid-19 pandemic has been a widespread erratic interpretation of statistics. 


## It's all false positives?
One idea that gained a lot of coverage in the UK over the pandemic was the idea that most of the cases are due to false positives in the testing. This has a deceptive appeal, especially as it was preceded by a long period of coverage which threw doubt on the performance of the various testing routines, such as the lateral flow test performance vs PCR.  

It gained further credence once these sceptics rediscovered a familiar example in probability, which demonstrates the usefulness of Bayesian methods. This example considers the case of a very rare disease, and a reasonably well performing test for it, and returns the apparently paradoxical result that even if the highly performing test suggests you are a carrier of the disease, it is actually more likely that you do **not** have the disease at all! It is therefore not much of a stretch of imagination to take this example and apply it to the pandemic, lending an apparently expert validation of the false positives thesis. One such sceptic that used their media audience to amplify these claims was Julia Hartley Brewer, tweeting

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">THIS IS VERY IMPORTANT: Matt Hancock told me on <a href="https://twitter.com/talkRADIO?ref_src=twsrc%5Etfw">@talkRADIO</a> that the False Positive Rate of Covid tests in the community is &quot;under 1%&quot;. Sounds good, doesn&#39;t it? WRONG! <br>An FPR of 0.8% when the virus prevalence is so low means that at least 91% of &quot;Covid cases&quot; are FALSE POSITIVES. <a href="https://t.co/f2Z85Lj4cj">https://t.co/f2Z85Lj4cj</a></p>&mdash; Julia Hartley-Brewer (@JuliaHB1) <a href="https://twitter.com/JuliaHB1/status/1306916494773755910?ref_src=twsrc%5Etfw">September 18, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

Initially, the testimony of statistics experts such as David Spiegelhalter was used as further evidence, with the difference between the coronavirus example and the textbook "rare disease" example being lost in the debate. When these experts tried to clarify the truth, such as in the BBC "More or Less" programme, a lot of the damage had already been done. 

 Unfortunately, the case is not as clear cut as the pandemic sceptics would have liked.  

 ## Quantifying false positives

The main issue with this argument is how it hinges on the idea of drawing samples from an *unbiased sampling of the population*. If we reconsider the [Bayesian approach]({% post_url 2021-04-27-bayesian-intro %}), we recall that the probability of somebody testing positive can be viewed as happening through a combination of events:

- Either they have the disease and test positive for it = $$ P(Pos|D=1)P(D=1) $$
- or they do not, but are a false positive = $$ P(Pos|D=0)P(D=0)
where D=0,1 if the patient does not or does have the disease, respectively and P(Pos) is the probability of testing positive.  

The false negatives come from the second contribution here, i.e   
  
P(Pos|D=0)P(D=0)
  
which has two components. The probability of testing positive, given the patient is in fact negative, is usually assumed to be constant. It is a characteristic of the medical test being used. The second term however, is where the problems arose. This defines the **probability of the patient not having the disease**. Across a random sampling of the *whole* population, we would expect this probability to be the prevalence of the disease. However, the people presenting themselves for Covid-19 tests are, usually, not a **random** sampling of the population. These are all people who have exhibited symptoms of Covid-19, or have otherwise been exposed or tested positive with a lateral flow test. The likelihood of somebody in this population having Covid-19 is very different to the probability of anyone randomly selected from the population. Therefore, the probability of them not having the disease, $$P(D=0)$$, will be lower than for the population at large. 

Try playing with the calculator at the end of the [Bayesian introduction page]({% post_url 2021-04-27-bayesian-intro %}). For example, assuming a false positive rate of 1% and and true positive rate of 99%, we can run a few tests with different levels of disease in the population being tested.
- If 1% of the population has the disease, then a positive test still only results in there being a **50%** chance of the individual carrying the disease - the false positives are very high 
- If we assume the people getting tests are a moderate 10x more likely to have Covid than the general population, then the chances of a positive test being a true Covid case becomes **92%** - the false positives are less of an issue.

This highlights the effect of your sampling strategy on the statistics and probabilites you infer at the other end. It's always important to be aware of the assumptions you are making throughout the process; this is one of the advantages of a Bayesian approach, which enforces you codifying each of them. 
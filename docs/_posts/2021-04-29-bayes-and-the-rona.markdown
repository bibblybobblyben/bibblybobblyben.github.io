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

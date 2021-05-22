---
layout: posts
title:  "Bayesian Statistics"
date:   2021-04-27 12:00:00 +0000
categories: statistics
excerpt: "Bayes n that"
header:
  teaser: assets/thumbnails/BayesRule.png
---
<head>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
</head>







Bayesian statistics might be a bit of a buzz word but the concepts behind it can be surprisingly simple, and learning to think in a Bayesian way can allow you to see the world in slightly different ways. This page is a gentle introduction to the subject, recapping conditional probability concepts before defining Bayes' theorem and then working through a popular example of the use of Bayesian techniques. This example is the rare disease scenario, where the situation of testing positive to a rare condition is explored and which presents some surprising results. 

## Conditional probability 

At the core of the issue is the appropriate way to analyse statistics, and the concept of conditional probability. Conditional probability is familiar to most people in how they will intuitively think about the world. Propose I ask "*How likely is Sergio Aguero to score a penalty this weekend?*" When evaluating this question to hazard a guess, it is likely that one would:
* Estimate the probability that Aguero would play in the next game
* Estimate the likelihood of Manchester City being awarded a penalty in their next game
* Estimate the probability of Aguero taking such an awarded penalty 
* Finally, estimate the likelihood of Aguero scoring a given penalty 
  
Whilst we might not formulate the solution so rigorously in our minds this way, these variables would all be being considered and weighed against each other to make our estimate of the probability. Furthermore, this example highlights the concept of **conditional probability**. The probability of Aguero scoring a penalty can be *conditional* on other events - if it transpires that Aguero isn't in the starting line up, our probability would be much lower than if he was in the starting line up.  
  
This concept can be formalised in a relatively simple mathematical equation, which can be carried through to some profound results. The equation is shown below. 

$$ P(A,B)= P(A|B) P(B) $$ 

$$P(A,B)$$ can be read as the probability of two events "A" and "B" both happening, $$ P(A \vert B) $$ is the probability of event "A" happening *conditional* on the fact that event "B" has already happened, and $$ P(B) $$ is the probability of event "B" happening. 
  
Therefore, the equation can be read as "*the probability of event A and B both happening, is the probability of event B happening, times the probability of event A happening considering that event B has happened*".   

Often, the two events are unrelated, such as for two rolls of a fair dice - the number you get on the first roll does not alter the likelihood of the number you will get on the second roll. In this case, the equation simplifies to $$P(A)P(B)$$.  

## Bayes's Theorem
Immediately, there is an apparent symmetry in the probabilities that we calculate this way. We've said  
  
$$ P(A, B) = P(A|B)P(B) $$
  
but we could equally have written:  
  
$$ P(A, B) = P(B|A)P(A)  $$ 
  
i.e, the probability of both events happening should be the same whether we suppose event A happens first or event B happens first. After all, they both come to the same result. Therefore  
  
$$P(A|B) P(B) = P(B|A) P(A)$$
  
Dividing both sides by $$P(B) $$ leads us to an important result of conditional probability, the often quoted <b>Bayes Theorem</b>:  
  
$$ P(A|B) = \frac{P(B|A)P(A)}{P(B)} $$

  
This might seem somewhat trivial but it can lead to some interesting conclusions.  

Particularly, this equation now gives us a way of finding the probability of A given B, from the knowledge of the other terms. This can be <b>incredibly</b> useful - often, it is easier to define the conditional probability of one event given the other than the reverse, and we wish to infer the more difficult conditional probability. 

For example, if you have a model which you believe could explain the data you see, it may be easier to define the probability of the data given the model is correct, than it is to straight away define how likely the model is from the data.  In many scientific applications, we want to learn what the probability of the model is given the data. Bayes' theorem gives us a way to do that.

## Practical example - the rare disease example

Often introductions to Bayesian statistics have this rare disease example somewhere in the beginning of the course as a quick way of showing an accessible and useful application of Bayesian techniques.  
Often these are a bit too brief, so I am including a full discussion of the process below. 

### The problem

This is where the rare diseases example comes in. Consider a disease, which is present in 0.001% of the population, and consider we have a test for the disease. This test is incredibly precise: 99.9% of positive test results correspond to people that have the disease. That is to say, the probability of testing positive if you have the disease is 99.9%. Unfortunately, you've just been to the doctor and found out that you have tested positive, and tell your statistically minded friend, distraught by the 99.9% performance of the test suggesting it is nigh on certain to indicate you have the disease. Fortunately, they have some maths of comfort for you.  

Specifically, your friend reminds you of Bayes's Theorem. Defining our events according to (A="Having disease", B="Testing positive"), we can see that the probability of having the disease can be considered as;  
  
$$ P(\textrm{Disease}\vert \textrm{Positive test}) = \frac{P(\textrm{Positive test}\vert \text {Disease})P(\textrm{Disease})}{P(\textrm{Disease})} $$


and we can now recognise our scenario is exactly one of those for which Bayes's theorem is well designed: we know how likely it is that somebody tests positive given they have the disease, but we don't know how likely it is somebody has the disease given they have tested positive. Therefore, if we can define the terms on the right hand side of the equation, we can calculate how likely it is that somebody has the disease given they have tested positive.  
* The first term, $$ P(\textrm{Positive test} \vert \textrm{Disease})$$, is given to us by the performance of the test. It is the probability of somebody testing positive given they have the disease, which is also known as the *sensitivity* of the test. We have defined this is 99.9% previously, and is a known statistic from testing.
* The second term $$P(\textrm{Disease})$$ can also be quite easily defined. It is the probability of having the disease at all, in the whole population. If we assume the test was carried out at random, the probability of having the disease is just the fraction of the population that have it, i.e 0.0001%.
* The final term $$P(rm{Positive})$$ is a bit more difficult to define, and relates to the tests *specificity*, what is the probability of somebody testing positive? This is sensitive to the number of false positives in the test.

### Defining P(Positive)
P(Positive) is the sum of the probabilities of testing positive given the individual does not have the disease, plus the probability of testing positive given they do not have the disease. Put another way, it is the total fraction of positive tests expected in a population. In this scenario, it is relatively easy to compute. There are two possible routes to testing positive:
* the disease is present, and the test detects it successfully = $$ P(\textrm{Positive test} \vert \textrm {Disease})P(\textrm{Disease})$$
* the disease is not present but the test makes a mistake = $$ P(\textrm{Positive test} \vert \textrm{No disease})P(\textrm{No disease}) $$

Each term in these two possible scenarios can be estimated: 
* $$P(\textrm{Positive test} \vert \textrm{Disease}) $$ and $$ P(\textrm{Positive test} \vert \textrm{Disease})$$ are measured metrics of the test's performance in trials.
* $$P(\textrm{Disease}) $$ and $$P(\textrm{No Disease}) $$ are the prevalence of the disease in the population - we'll need a realistic estimate of this.

and we can define $$ P(\textrm{Positive}) $$ by summing the probabilities for the two possible scenarios.

## Defining the posterior probability

Now we have all the pieces, we can define the probability of having the disease, given a positive test has been observed. For this demonstration, let's define a few numbers for a hypothetical test:
* 99.5% of people with the disease are successfully detected by the disease, meaning 0.5% of cases aren't found
* 1% of people without the disease will test positive. 
* We'll assume the disease is present in 0.1% of the population. 
Therefore we can define all terms we need:

$$ P(\textrm{Positive}) = (0.995*0.001) + (0.01*0.999) = 0.010985$$
$$ P(\textrm{Disease}) = 0.001$$
$$ P(\textrm{Positive} \vert \textrm{Disease}) = 0.995 $$


Plugging those numbers in, we can reach the answer:

$$P(\textrm{Disease} \vert \textrm{Positive test}) = \frac{0.995*0.001}{0.10985} = 0.0091 $$

Even with a positive test, the probability of having the disease is still very small, although the likelihood of having the disease has increase nine times compared to the risk to the bulk of the population. This might look like an error, but the cause is that although the the chances of testing positive are very low if you do not have the disease, the probability of not having the disease is also very high. Therefore, the false positive test results end up being the far more likely outcome, and the true positives are only a fraction of the positive tests. You can calculate this yourself by assuming a population of 200,000 people are tested, and seeing how many tests fall into which category. 

* From 200,000 people, 0.1% have the disease = 200 people
* of those 200, the test catches 199 of them
* Conversely, 199,800 people do not have the disease
* of these, the test returns 1% false positives = 1998

Therefore we have $$ 199 + 1998 = 2197 $$ tests, but only 199 of them actually have the disease. If we work out what fraction of those are true positives, we find:  
$$ P(\textrm{Disease} \vert \textrm{Positive test}) = \frac{199}{2197} = 0.091 $$  
which is the same result we got before, and we can clearly see how the probability of the false positives means that the most likely case is you do not have the disease, even with the positive test. This apparent paradox is reliant on the condition being quite rare, but the general framewokr can be applied anywhere. As a demonstration, it serves of a good mental reminder that  
  
$$P(A \vert B) \neq P(B\vert A) $$

## Try it yourself!

Just to prove that these aren't some contrived numbers I have forced to work to emphasise a freak niche case, use the tool below yourself to explore how changing the probabilities of the different components affects the posterior likelihood. Make sure you enter your probabilities in the range 0-1. 




<html>
<body>

<script>
function myFunction() {
  var posdis = parseFloat(document.getElementById("posdis").value);
  var pdis = parseFloat(document.getElementById("pdis").value);
  var pfpos = parseFloat(document.getElementById("ppos").value);
  var prob =0.0;
  var ppos = 0.0;
  ppos = (posdis*pdis)+(pfpos *(1.-pdis))
  prob = posdis*pdis/ppos; 
  
  document.getElementById("probout").innerHTML = "The probability of the positive test meaning that the disease is actually present in the individual is <b>" +prob +"</b>";

}
</script>


<form id = "frm1">
<label for="posdis">$$P(\textrm{Positive} \vert \textrm{Disease})=$$</label><br>
  <input type="text" id="posdis" name="posdis"><br>
<label for="pdis">$$P(\textrm{Disease})= $$</label><br>
  <input type="text" id="pdis" name="pdis"><br>
<label for="ppos">$$ P(\textrm{Positive} \vert \textrm{No Disease}) =$$ </label><br>
  <input type="text" id="ppos" name="ppos"><br>
</form>
<button type="button" onclick = "myFunction();">Calculate</button>
<p id="probout"></p>


</body>
</html>
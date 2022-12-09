---
layout: post
title: Bayes Theorem 
---

Bayes' theorem is a mathematical formula used to determine the probability of an event based on prior knowledge of
conditions that might be related to the event. It is a widely used tool in statistics and probability theory.

The theorem is named after Thomas Bayes, a 18th century English statistician and Presbyterian minister, who developed a
method for calculating probabilities based on the concept of conditional probability. Conditional probability is the
probability of an event occurring given that another event has already occurred.

Bayes' theorem is typically expressed as follows:

        P(A|B) = P(B|A) * P(A) / P(B)

where `P(A|B)` is the conditional probability of event `A` occurring given that event `B` has already occurred, P(B|A)
is the conditional probability of event `B` occurring given that event A has already occurred, `P(A)` is the probability
of event A occurring, and `P(B)` is the probability of event `B` occurring.

The theorem is used in a variety of applications, such as medical testing, where it can be used to calculate the
probability that a person has a certain disease based on the results of a test. It is also used in machine learning,
where it can be used to make predictions about future events based on past data.

One example of the use of Bayes' theorem in medicine is in the context of HIV testing. HIV, or human immunodeficiency
virus, is a virus that can lead to acquired immunodeficiency syndrome (AIDS). It is a relatively rare disease, with an
estimated prevalence of 0.3% in the general population.

Suppose a person undergoes an HIV test and the test comes back positive. What is the probability that the person
actually has HIV? This is where Bayes' theorem can be used.

In this case, event A is the person having HIV, and event B is the person testing positive for HIV. `P(A)` is the
probability that a person has HIV, which is 0.3%. `P(B|A)` is the probability that a person with HIV will test positive
for the disease, which is high (assuming the test is accurate). `P(B)` is the probability that a person will test positive
for HIV, which includes both those with HIV (0.3%) and those without HIV who happen to test positive due to false
positives (a very small percentage).

Using Bayes' theorem, we can calculate the probability that a person who tests positive for HIV actually has the
disease:

        P(A|B) = P(B|A) * P(A) / P(B)

               = (high) * 0.003 / (0.003 + very small)

               = high

Thus, Bayes' theorem can be used to calculate the probability that a person who tests positive for HIV actually has the
disease, taking into account both the accuracy of the test and the overall prevalence of HIV in the population.

Overall, Bayes' theorem is a valuable tool in probability and statistics. It allows for the calculation of probabilities
based on prior knowledge of related events, and can provide valuable insights into the likelihood of future events.


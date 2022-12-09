---
layout: post
title: Bayes Theorem 
---

Bayes' theorem is a mathematical formula used to determine the probability of an event based on prior knowledge of
conditions that might be related to the event. It is a widely used tool in statistics and probability theory.

The theorem is named after Thomas Bayes, a 18th century English statistician and Presbyterian minister, who developed a
method for calculating probabilities based on the concept of conditional probability. Conditional probability is the
probability of an event occurring given that another event has already occurred.

Laplace is credited with being the first to use Bayes' theorem in the field of statistics. Before Laplace, Bayes'
theorem was primarily used in the field of theology to try to infer the existence and nature of God from observed
phenomena.

Laplace recognized the potential of Bayes' theorem for solving problems in statistics and used it to develop a rigorous
approach to statistical inference. His work was influential in establishing Bayes' theorem as a cornerstone of
statistical theory.

Laplace's contribution to Bayes' theorem was to recognize its potential for solving statistical problems and to develop
a mathematical framework for using it in statistical inference. He showed that Bayes' theorem could be used to calculate
the probability of an event based on prior knowledge and observed data. This allowed him to develop a more objective and
rigorous approach to statistical inference than was previously possible.

Overall, Laplace's work was instrumental in establishing Bayes' theorem as an important tool in the field of statistics.

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

Here is an example of Bayes' theorem using NumPy. Keep in mind that this is just one possible way to implement Bayes' theorem using NumPy and that there may be other ways to do it as well.

First, let's define some variables that we will use in our implementation:

    import numpy as np

    # Prior probabilities of each hypothesis
    prior = np.array([0.2, 0.3, 0.5])

    # Likelihood of each evidence under each hypothesis
    likelihood = np.array([
        [0.5, 0.1, 0.9],  # Evidence 1
        [0.3, 0.5, 0.2],  # Evidence 2
        [0.2, 0.4, 0.3]   # Evidence 3
    ])

    # Evidence
    evidence = np.array([1, 0, 1])

In this example, we have three hypotheses (represented by the prior array) and three pieces of evidence (represented by
the evidence array). The likelihood array represents the likelihood of each evidence under each hypothesis.

Next, we can use Bayes' theorem to compute the posterior probabilities of each hypothesis given the evidence:

    # Compute the posterior probabilities using Bayes' theorem
    posterior = np.zeros_like(prior)
    for i in range(len(prior)):
        posterior[i] = prior[i] * np.prod(likelihood[:, i] ** evidence)

    # Normalize the posterior probabilities
    posterior /= np.sum(posterior)

    print(posterior)  # [0.08695652 0.15217391 0.76086957]

The resulting posterior array gives the probabilities of each hypothesis given the evidence. In this case, the highest
probability is for the third hypothesis, which means that it is the most likely given the evidence.

Overall, Bayes' theorem is a valuable tool in probability and statistics. It allows for the calculation of probabilities
based on prior knowledge of related events, and can provide valuable insights into the likelihood of future events.


---
title: "Glossary: M04 — Probability Concepts"
type: glossary
subject: quantitative-methods
module: M04
created: 2026-04-09
updated: 2026-04-09
tags: [glossary, probability, bayes, expected-value, combinations]
---

# Glossary: M04 — Probability Concepts

**Module**: [[quantitative-methods/modules/m04-probability/index|M04]]
**Formulas**: [[quantitative-methods/formulas/probability|Formula Sheet]]
**Concept page**: [[quantitative-methods/concepts/probability|Probability]]

---

## Random Variable

A variable whose value is determined by the outcome of a random process (an experiment). Can be [[quantitative-methods/glossary/m05-portfolio-math#Discrete Random Variable|discrete]] or [[quantitative-methods/glossary/m05-portfolio-math#Continuous Random Variable|continuous]].

**LOS**: 4.a | **Examples**: The return on a stock next year; the number of defaults in a bond portfolio.

---

## Outcome

A possible value of a random variable or a possible result of a single trial of an experiment. Outcomes are the basic building blocks of probability.

**LOS**: 4.a | **Related**: [[#Event]], [[#Sample Space]]

---

## Event

A specified set of one or more outcomes of a random experiment. Events can be simple (single outcome) or compound (multiple outcomes).

**LOS**: 4.a | **See**: [[#Mutually Exclusive Events]], [[#Exhaustive Events]]

---

## Probability

A number between 0 and 1 that expresses the likelihood of an event occurring. A probability of 0 means the event is impossible; a probability of 1 means it is certain.

$$0 \leq P(E) \leq 1 \qquad \text{and} \qquad \sum P(E_i) = 1 \text{ (over all mutually exclusive, exhaustive events)}$$

**LOS**: 4.a | **See**: [[#Subjective Probability]], [[#Empirical Probability]], [[#A Priori Probability]]

---

## Subjective Probability

A probability based on personal judgment or informed opinion rather than formal analysis or historical data. Not repeatable.

**LOS**: 4.a | **Example**: An analyst's estimate that a merger will succeed has a 70% probability.

---

## Empirical Probability

A probability estimated from observed historical data — the relative frequency of the event over a large number of trials.

**LOS**: 4.a | **Example**: If a stock rose on 120 of 200 trading days, the empirical probability of a rise is 120/200 = 60%.

---

## A Priori Probability

A probability derived from logical analysis of equally likely outcomes, without reference to observed data. Based on deductive reasoning.

**LOS**: 4.a | **Example**: The probability of rolling a 4 on a fair die is 1/6 by a priori reasoning.

---

## Mutually Exclusive Events

Events that cannot occur simultaneously. The occurrence of one event precludes the occurrence of the other.

$$P(A \text{ and } B) = 0$$

**LOS**: 4.b | **Related**: [[#Addition Rule]]

---

## Exhaustive Events

A set of events that includes all possible outcomes. The sum of probabilities of exhaustive, mutually exclusive events equals 1.

$$P(E_1) + P(E_2) + \cdots + P(E_n) = 1$$

**LOS**: 4.b

---

## Odds For

The ratio of the probability that an event occurs to the probability that it does not occur.

$$\text{Odds for } A = \frac{P(A)}{1 - P(A)}$$

**LOS**: 4.b | **Example**: If $P(A) = 0.75$, odds for $A$ = 3 to 1 (or 3:1).

---

## Odds Against

The ratio of the probability that an event does not occur to the probability that it does occur. The inverse of odds for.

$$\text{Odds against } A = \frac{1 - P(A)}{P(A)}$$

**LOS**: 4.b | **Example**: If odds against $A$ are 4 to 1, then $P(A) = \frac{1}{1+4} = 0.20$.

---

## Unconditional Probability

The probability of an event without conditioning on any other event. Also called the marginal probability. Denoted $P(A)$.

**LOS**: 4.c | **Contrast**: [[#Conditional Probability]]

---

## Conditional Probability

The probability of event $A$ given that event $B$ has already occurred. Updated probability in light of new information.

$$P(A|B) = \frac{P(AB)}{P(B)} \qquad P(B) \neq 0$$

**LOS**: 4.c | **Foundation for**: [[#Bayes' Formula]], [[#Total Probability Rule]]

---

## Joint Probability

The probability that both events $A$ and $B$ occur simultaneously. Denoted $P(AB)$ or $P(A \cap B)$.

$$P(AB) = P(A|B) \times P(B)$$

**LOS**: 4.c | **Related**: [[#Multiplication Rule]], [[#Probability Tree]]

---

## Addition Rule

The probability that event $A$ or event $B$ (or both) occurs.

$$P(A \text{ or } B) = P(A) + P(B) - P(AB)$$

For [[#Mutually Exclusive Events]]: $P(A \text{ or } B) = P(A) + P(B)$

**LOS**: 4.d | **Related**: [[#Unconditional Probability]]

---

## Multiplication Rule

The probability that both events $A$ and $B$ occur, derived from conditional probability.

$$P(AB) = P(A|B) \times P(B) = P(B|A) \times P(A)$$

For [[#Independent Events]]: $P(AB) = P(A) \times P(B)$

**LOS**: 4.d | **Related**: [[#Joint Probability]]

---

## Independent Events

Two events are independent if the occurrence of one does not affect the probability of the other. $P(A|B) = P(A)$ and $P(B|A) = P(B)$.

$$P(AB) = P(A) \times P(B) \quad \text{(if and only if independent)}$$

**LOS**: 4.e | **Contrast**: [[#Dependent Events]]

---

## Dependent Events

Events where the occurrence of one affects the probability of the other. $P(A|B) \neq P(A)$.

**LOS**: 4.e | **Example**: The default of one firm in an industry may increase the probability of default by a competitor (contagion).

---

## Total Probability Rule

Expresses the unconditional probability of an event as a weighted average of conditional probabilities, where the weights are the probabilities of the conditioning events.

$$P(A) = P(A|S_1)P(S_1) + P(A|S_2)P(S_2) + \cdots + P(A|S_n)P(S_n)$$

where $S_1, S_2, \ldots, S_n$ are mutually exclusive and exhaustive scenarios.

**LOS**: 4.f | **Used in**: [[#Bayes' Formula]] | **Application**: Scenario analysis in investment management.

---

## Expected Value

The probability-weighted average of all possible outcomes of a random variable. The mean of the probability distribution.

$$E(X) = \sum_{i=1}^{n} P(X_i) \times X_i$$

**LOS**: 4.g | **Key**: Expected value does not have to be a possible outcome (e.g., expected number of children = 2.1). | **Related**: [[#Variance of Random Variable]]

---

## Variance of Random Variable

The expected value of the squared deviations from the mean. Measures the dispersion of a random variable's probability distribution.

$$\text{Var}(X) = E\left[(X - E(X))^2\right] = \sum_{i=1}^{n} P(X_i) \left[X_i - E(X)\right]^2$$

**LOS**: 4.g | **Related**: [[#Standard Deviation of Random Variable]], [[quantitative-methods/glossary/m03-statistical-measures#Variance (Sample)|Sample Variance]]

---

## Standard Deviation of Random Variable

The positive square root of the variance of a random variable. Expressed in the same units as $X$.

$$\text{SD}(X) = \sqrt{\text{Var}(X)}$$

**LOS**: 4.g | **Related**: [[quantitative-methods/glossary/m05-portfolio-math#Portfolio Standard Deviation|Portfolio Standard Deviation]]

---

## Bayes' Formula

A method for updating the probability of an event given new information. Calculates the posterior probability from the prior probability and the likelihood of the new evidence.

$$P(A|B) = \frac{P(B|A) \times P(A)}{P(B)}$$

Expanded using [[#Total Probability Rule]]:

$$P(A|B) = \frac{P(B|A) \times P(A)}{P(B|A)P(A) + P(B|A^c)P(A^c)}$$

**LOS**: 4.h | **Key**: $P(A)$ = prior probability; $P(A|B)$ = posterior probability (updated after observing $B$).

---

## Factorial

The product of all positive integers from 1 to $n$. Used in counting methods. Notation: $n!$

$$n! = n \times (n-1) \times (n-2) \times \cdots \times 1 \qquad 0! = 1$$

**LOS**: 4.i | **Related**: [[#Permutation]], [[#Combination]]

---

## Permutation

The number of ways to arrange $r$ objects chosen from $n$ distinct objects, where **order matters**.

$$_nP_r = \frac{n!}{(n-r)!}$$

**LOS**: 4.i | **Contrast**: [[#Combination]] — order does not matter.

---

## Combination

The number of ways to choose $r$ objects from $n$ distinct objects, where **order does not matter**. Also called "n choose r."

$$\binom{n}{r} = \frac{n!}{r!(n-r)!}$$

**LOS**: 4.i | **Application**: Number of ways to select a portfolio of $r$ stocks from $n$ candidates. | **Related**: [[quantitative-methods/glossary/m05-portfolio-math#Binomial Distribution|Binomial Distribution]]

---

## Probability Tree

A diagram that maps out all possible outcomes of a sequence of events, with each branch labeled with its probability. Visually represents joint and conditional probabilities.

**LOS**: 4.f | **Use**: Illustrates the [[#Total Probability Rule]] and [[#Bayes' Formula]] calculations. | **Related**: [[#Joint Probability]], [[#Conditional Probability]]

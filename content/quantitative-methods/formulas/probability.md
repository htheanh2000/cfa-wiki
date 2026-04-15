---
title: "Formulas: Probability"
type: formula
subject: quantitative-methods
module: M04
created: 2026-04-09
updated: 2026-04-09
tags: [formulas, probability, bayes, expected-value, counting]
---

# Formulas: Probability

**Module**: [[quantitative-methods/modules/m04-probability-trees/index|M04]]

## Odds

$$\text{Odds for } E = \frac{P(E)}{1 - P(E)} \qquad \text{Odds against } E = \frac{1 - P(E)}{P(E)}$$

## Conditional Probability

$$P(A|B) = \frac{P(AB)}{P(B)}$$

## Addition Rule

$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

If mutually exclusive: $P(A \cup B) = P(A) + P(B)$

## Multiplication Rule

**Dependent**: $P(AB) = P(A|B) \cdot P(B)$

**Independent**: $P(AB) = P(A) \cdot P(B)$

## Total Probability Rule

$$P(A) = \sum_{i=1}^{N} P(A|B_i) \cdot P(B_i)$$

## Bayes' Formula

$$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$$

## Expected Value

$$E(X) = \sum_{i=1}^{n} P(X_i) \cdot X_i$$

## Variance of a Random Variable

$$\sigma^2(X) = \sum_{i=1}^{n} P(X_i) \cdot [X_i - E(X)]^2$$

## Standard Deviation

$$\sigma(X) = \sqrt{\sigma^2(X)}$$

## Factorial

$$n! = n \times (n-1) \times \cdots \times 2 \times 1$$

## Permutation

$$P(n,r) = \frac{n!}{(n-r)!}$$

## Combination

$$C(n,r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}$$

## Binomial Probability

$$P(X = x) = \binom{n}{x} p^x (1-p)^{n-x}$$

where $n$ = trials, $x$ = successes, $p$ = probability of success

# tnnr48.github.io

---
layout: default
title: Lindberg-Levy Central Limit Theorem
---

# Lindberg-Levy Central Limit Theorem (CLT)

The **Lindberg-Levy Central Limit Theorem** states that suppose we have a sample of random variables \( X_1, X_2, X_3, \dots \) drawn from a population, which are **independent and identically distributed (i.i.d.)**. This means:

- The value of one random variable does not affect the value of any other.
- All random variables share the same distribution.

Let:
- \( \bar{X} \) denote the **sample mean**.
- \( E[X_i] = \mu \) denote the **population mean**.
- \( \text{Var}(X_i) = \sigma^2 < \infty \) denote the **population variance** (which is finite).

Then, as the sample size \( n \) approaches infinity, the **standardized sample means**

\[
\frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
\]

converge in distribution to the **standard normal distribution** \( \mathcal{N}(0, 1) \).

## Mathematical Representation

\[
\frac{\sqrt{n}(\bar{X} - \mu)}{\sigma} \xrightarrow{d} \mathcal{N}(0, 1) \quad \text{as} \quad n \to \infty
\]

## Explanation

- **Independent and Identically Distributed (i.i.d.)**: Each random variable \( X_i \) is independent of the others and follows the same probability distribution.
- **Sample Mean (\( \bar{X} \))**: The average of the sample \( X_1, X_2, \dots, X_n \).
- **Standardized Sample Mean**: The expression \( \frac{\sqrt{n}(\bar{X} - \mu)}{\sigma} \) normalizes the sample mean, scaling it by the square root of the sample size and the population standard deviation.
- **Convergence in Distribution**: As \( n \) increases, the distribution of the standardized sample mean approaches the standard normal distribution \( \mathcal{N}(0, 1) \), regardless of the original distribution of \( X_i \), provided certain conditions (like finite variance) are met.

## Implications of the CLT

- **Approximation of Distributions**: The CLT allows us to approximate the distribution of the sample mean \( \bar{X} \) with a normal distribution, which is especially useful for large sample sizes.
- **Facilitates Statistical Inference**: Many statistical methods and confidence interval calculations rely on the assumption of normality, which the CLT justifies under the i.i.d. and finite variance conditions.

## Example

Suppose we have a population with mean \( \mu = 50 \) and variance \( \sigma^2 = 25 \). We take a sample of size \( n = 100 \).

The standardized sample mean is:

\[
\frac{\sqrt{100}(\bar{X} - 50)}{5} = \frac{10(\bar{X} - 50)}{5} = 2(\bar{X} - 50)
\]

According to the Lindberg-Levy CLT:

\[
2(\bar{X} - 50) \xrightarrow{d} \mathcal{N}(0, 1) \quad \text{as} \quad n \to \infty
\]

This means that for large \( n \), \( 2(\bar{X} - 50) \) approximately follows a standard normal distribution.

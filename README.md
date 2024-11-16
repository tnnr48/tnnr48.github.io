<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>{{ page.title }}</title>
  <!-- Existing styles and scripts -->
  
  <!-- MathJax CDN -->
  <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" async></script>
  
  <!-- Optional: MathJax Configuration -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['$', '$'], ['\\(', '\\)']],
        displayMath: [['$$', '$$'], ['\\[', '\\]']]
      },
      svg: {
        fontCache: 'global'
      }
    };
  </script>
</head>
<body>
 ## Lindberg-Levy Central Limit Theorem

The Lindberg-Levy CLT states that suppose we have some sample of random variables \( X_1, X_2, X_3 \dots \) drawn from a population, which are **independent and identically distributed** (the value of one does not change the value of any other and all have the same distribution), with sample mean \( \bar{X}_i \), population mean \( E[X_i] = \mu \), and population variance \( \text{Var}(X_i) = \sigma^2 < \infty \) (finite variance). Then, as the sample size \( n \) approaches infinity, the standardized sample means

$$
\frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
$$

converge in distribution to the standard normal distribution \( \mathcal{N}(0,1) \).

In other words, the distribution of the sample mean, with samples drawn from some population that has a mean and variance (first and second moments), will be normally distributed for large enough sample size \( n \). To prove the CLT, we consider the sample mean

$$
\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i
$$

which, on average, equals

$$
E\left[\bar{X}\right] = E\left[\frac{1}{n} \sum_{i=1}^{n} X_i\right] = \frac{1}{n} \sum_{i=1}^{n} E[X_i] = \frac{1}{n} \cdot n\mu = \mu
$$

and thus the average of the sample means is the population mean. The variance of the sample mean is

$$
\text{Var}\left(\bar{X}\right) = \text{Var}\left(\frac{1}{n} \sum_{i=1}^{n} X_i\right) = \frac{1}{n^2} \sum_{i=1}^{n} \text{Var}(X_i) = \frac{1}{n^2} \sum_{i=1}^{n} \sigma^2 = \frac{\sigma^2}{n}
$$

Thus, the mean of the **sampling distribution of sample means** \( \bar{X}_i \) is equal to the population mean with variance \( \frac{\sigma^2}{n} \). To **standardize the sample mean**, we center it around the mean of the sample means (the population mean) and divide by its standard deviation, which gives

$$
\frac{(\bar{X} - \mu)}{\frac{\sigma}{\sqrt{n}}} = \frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
$$

$$
= \frac{\sqrt{n}\left(\frac{1}{n} \sum_{i=1}^{n} X_i - \mu\right)}{\sigma}
$$

$$
= \frac{\frac{1}{\sqrt{n}} \sum_{i=1}^{n} X_i - \sqrt{n}\mu}{\sigma}
$$

We can call the standardized sample mean by a new random variable \( \bar{X}_s \) (where \( s \) indicates 'standardized') and our goal is to show that this converges in distribution to the standard normal for large enough \( n \). That is, 

$$
\bar{X}_s \xrightarrow{d} \mathcal{N}(0,1)
$$

Now, rather than dealing with sample means directly, we can discuss \( S \), the sum of our sample of i.i.d. random variables, \( \sum_{i=1}^{n} X_i \). The **sampling distribution of the sample sums** \( S \) has mean 

$$
E[S] = E\left[\sum_{i=1}^{n} X_i\right] = \sum_{i=1}^{n} E[X_i] = n\mu
$$

and variance 

$$
\text{Var}(S) = \sum_{i=1}^{n} \text{Var}(X_i) = n\sigma^2
$$

respectively. **Standardizing the sample sum** gives 

$$
S^* = \frac{S - n\mu}{\sqrt{n}\sigma}
$$

$$
= \frac{\sum_{i=1}^{n} X_i - n\mu}{\sqrt{n}\sigma}
$$

$$
= \frac{\frac{1}{\sqrt{n}} \left(\sum_{i=1}^{n} X_i - n\mu\right)}{\sigma}
$$

$$
= \frac{\frac{1}{\sqrt{n}} \sum_{i=1}^{n} X_i - \sqrt{n}\mu}{\sigma}
$$

which we can see is equivalent to the standardized sample mean. Thus, proving that sample sums converge to the standard normal distribution also proves that the distribution of sample means does and proves the CLT.
</body>
</html>

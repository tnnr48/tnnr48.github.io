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

The **Lindberg-Levy Central Limit Theorem (CLT)** states that suppose we have a sample of random variables \( X_1, X_2, X_3, \dots \) drawn from a population, which are **independent and identically distributed (i.i.d.)** (the value of one does not affect the value of any other, and all have the same distribution), with sample mean \( \bar{X} \), population mean \( E[X_i] = \mu \), and population variance \( \text{Var}(X_i) = \sigma^2 < \infty \) (finite variance). Then, as the sample size \( n \) approaches infinity, the standardized sample means

$$
\frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
$$

converge in distribution to the **standard normal distribution** \( \mathcal{N}(0,1) \).

In other words, the distribution of the sample mean, with samples drawn from a population that has a mean and variance (first and second moments), will be **normally distributed** for sufficiently large sample sizes \( n \). To prove the CLT, we consider the sample mean

$$
\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i
$$

which, on average, equals \( \mu \). Thus, the average of the sample means is the population mean. The **variance of the sample mean** is

$$
\text{Var}(\bar{X}) = \text{Var}\left(\frac{1}{n} \sum_{i=1}^{n} X_i\right) = \frac{1}{n^2} \sum_{i=1}^{n} \text{Var}(X_i) = \frac{1}{n^2} \sum_{i=1}^{n} \sigma^2 = \frac{\sigma^2}{n}
$$

Thus, the mean of the **sampling distribution of sample means** \( \bar{X}_i \) is equal to the population mean with variance \( \frac{\sigma^2}{n} \). To **standardize the sample mean**, we center it around the mean of the sample means (the population mean) and divide by its standard deviation, which gives:
</body>
</html>

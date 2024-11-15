# tnnr48.github.io

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Your Page Title</title>
    
    <!-- MathJax Configuration (Optional) -->
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
    
    <!-- Include MathJax from CDN -->
    <script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js" async></script>
    
    <!-- Your other head elements -->
</head>
<body>
   The Lindberg-Levy CLT states that suppose we have some sample of random variables $X_1, X_2, X_3\dots$ drawn from a population, which are independent and identically distributed (the value of one does not change the value of any other and all have the same distribution), with sample mean $\bar{X_i}$, population mean $E[X_i] = \mu$, and population variance $Var(X_i) = \sigma^2 < \infty$ (finite variance). Then as the sample size $n$ approaches $\infty$, the standardized sample means

\[
\frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
\]

converge in distribution to the standard normal distribution $\mathcal{N}(0,1)$.

In other words, the distribution of the sample mean, with samples drawn from some population that has a mean and variance (first and second moments), will be normally distributed for large enough sample size $n$. To prove the CLT we consider the sample mean
$\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i$ which, in the average equals

\[
$E[\bar{X}] = E\left[\frac{1}{n} \sum_{i=1}^{n} X_i\right] = \frac{1}{n} \sum_{i=1}^{n} E[X_i] = \frac{1}{n} n\mu = \mu$
\]

<p>
and thus the average of the sample means is the population mean. The variance of the sample mean is
</p>

\[
$Var(\bar{X}) = Var\left(\frac{1}{n} \sum_{i=1}^{n} X_i\right) = \frac{1}{n^2} \sum_{i=1}^{n} Var(X_i) = \frac{1}{n^2} \sum_{i=1}^{n} \sigma^2 = \frac{\sigma^2}{n}$
]\

<p>
thus the mean of the sampling distribution of sample means $\bar{X}_i$ is equal to the population mean with variance $\frac{\sigma^2}{n}$. To standardize the sample mean we center it around the mean of the sample means (the population mean) and divide by its standard deviation, which gives 
</p>

</body>
</html>

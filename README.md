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

</body>
</html>

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
E[\bar{X}] = E\left[\frac{1}{n} \sum_{i=1}^{n} X_i\right] = \frac{1}{n} \sum_{i=1}^{n} E[X_i] = \frac{1}{n} n\mu = \mu
\]

<p>
and thus the average of the sample means is the population mean. The variance of the sample mean is
</p>

\[
Var(\bar{X}) = Var\left(\frac{1}{n} \sum_{i=1}^{n} X_i\right) = \frac{1}{n^2} \sum_{i=1}^{n} Var(X_i) = \frac{1}{n^2} \sum_{i=1}^{n} \sigma^2 = \frac{\sigma^2}{n}
\]

<p>
thus the mean of the sampling distribution of sample means $\bar{X}_i$ is equal to the population mean with variance $\frac{\sigma^2}{n}$. To standardize the sample mean we center it around the mean of the sample means (the population mean) and divide by its standard deviation, which gives 
</p>

\[
\frac{(\bar{X} - \mu)}{\frac{\sigma}{\sqrt{n}}} = \frac{\sqrt{n}(\bar{X} - \mu)}{\sigma}
\]

\[
= \frac{\sqrt{n}(\frac{1}{n} \sum_{i=1}^{n} X_i - \mu)}{\sigma}
\]

\[
= \frac{\frac{1}{\sqrt{n}} \sum_{i=1}^{n} X_i - \sqrt{n}\mu}{\sigma}
\]

We can call the standardized sample mean by a new random variable $\bar{X}_s$ (where s indicates 'standardized') and our goal is to show that this converges in distribution to the standard normal for large enough $n$. That is, $\bar{X}_s \xrightarrow{d} \mathcal{N}(0,1)$

Now rather than dealing with sample means directly we can discuss $S$, the sum of our sample of iid random variables, $\sum_{i=1}^{n} X_i$. The sampling distribution of the sample sums $S$ has mean $E[S] = E[\sum_{i=1}^{n} X_i] = \sum_{i=1}^{n} E[X_i] = n\mu$ and variance $Var(S) = \sum_{i=1}^{n} Var(X_i) = n\sigma^2$ respectively. Standardizing the sample sum gives 

\[
S^* = \frac{S - n\mu}{\sqrt{n}\sigma}
\]

\[
= \frac{\sum_{i=1}^{n} X_i - n\mu}{\sqrt{n}\sigma}
\]

\[
= \frac{\frac{1}{\sqrt{n}} (\sum_{i=1}^{n} X_i - n\mu)}{\sigma}
\]

\[
= \frac{\frac{1}{\sqrt{n}} \sum_{i=1}^{n} X_i - \sqrt{n}\mu}{\sigma}
\]

which we can see is equivalent to the standardized sample mean. Thus proving that sample sums converge to the standard normal distribution also proves that the distribution of sample means does and proves the CLT.

We now consider the standard normal distribution and its moment generating function. The density function for the standard normal distribution is given by $f_Z(x) = f(x| \mu=0, \sigma^2=1) = \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}$ for some standard normal random variable $Z$. Then $M_Z(t) = E[e^{Xt}] = \int_{-\infty}^{\infty} e^{xt} \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}} dx$. We can simplify this like so

\[
\int_{-\infty}^{\infty} e^{xt} \frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}} dx
\]

\[
= \int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{xt - \frac{x^2}{2}} dx
\]

\[
= \int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2}(x^2 - 2xt)}
\]

\[
= \int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2}(x^2 - 2xt + t^2) + \frac{1}{2}t^2}
\]

\[
= \int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2}(x-t)^2 + \frac{1}{2}t^2}
\]

and since $e^{\frac{1}{2}t^2}$ is a constant as there is no $x$ term (the integral is with respect to x) then we can factor it out of the integral which gives

\[
M_Z(t) = e^{\frac{1}{2}t^2} \int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}} e^{-\frac{1}{2}(x-t)^2} = e^{\frac{1}{2}t^2}(1) = e^{\frac{1}{2}t^2}
\]

as our moment generating function for the standard normal distribution. Note that the integral simplifies to $1$ as it integrates the probability density function over all possible values of $Z$, which is $1$. In order to prove the CLT we need to show that the moment generating function for $S$ converges to $e^{\frac{1}{2}t^2}$. There are several properties of moment generating functions that are useful for this purpose and we will list here. If any two random variables $A, B$ are independent with moment generating functions $M_A(t), M_B(t)$ then $C = A + B$ has moment generating function $M_C(t) = M_A(t)M_B(t)$. This is easily demonstrated by $M_C(t) = E[e^{Ct}] = E[e^({A + B)t}] = E[e^{At + Bt}] = E[e^{At}e^{Bt}] = E[e^{At}]E[e^{Bt}] = M_A(t)M_B(t)$. Another property that we have already stated is that the $k^{th}$ derivative of the moment generating function gives the $k^{th}$ moment, which is evident from the expectation of the Taylor polynomial of $e^(x)$. 

Recall that the standardized sample sum $S^* = \frac{S - n\mu}{\sqrt{n}\sigma} = \frac{\sum_{i=1}^{n} X_i - n\mu}{\sqrt{n}\sigma}$ then

\[
S^* = \frac{\sum_{i=1}^{n} X_i - n\mu}{\sqrt{n}\sigma}
\]

\[
= \frac{(X_1 + X_2 + ... + X_n) - n\mu}{\sqrt{n}\sigma}
\]

\[
= \frac{(X_1 - \mu) + (X_2 - \mu) + ... + (X_n - \mu)}{\sqrt{n}\sigma}
\]

\[
= \frac{(X_1 - \mu)}{\sqrt{n}\sigma} + \frac{(X_2 - \mu)}{\sqrt{n}\sigma} + ... + \frac{(X_n - \mu)}{\sqrt{n}\sigma}
\]

and the moment generating function of $S^*$, $M_{S^*}(t) = E[e^{S^*t}]$ where

\[
E[e^{S^*t}] = E[e^{t(\frac{(X_1 - \mu)}{\sqrt{n}\sigma} + \frac{(X_2 - \mu)}{\sqrt{n}\sigma} + ... + \frac{(X_n - \mu)}{\sqrt{n}\sigma})} = E[e^{t(\frac{(X_i - \mu)}{\sqrt{n}\sigma}}]^n
\]

as the sum of $n$ terms in the exponent is equal to the product of $n$ exponential terms. Note that each $E[e^{t(\frac{(X_i - \mu)}{\sqrt{n}\sigma}}]$ is a moment generating function for the standardized random variable $\frac{(X_i - \mu)}{\sqrt{n}\sigma}$ which we can denote as $M_{\frac{(X_i - \mu)}{\sqrt{n}\sigma}}(t)$. Also note that since $cM_A(t) = M_A(ct)$ for some scaling constant $c$ then $M_{\frac{(X_i - \mu)}{\sqrt{n}\sigma}}(t) = M_{(X_i - \mu)}(\frac{t}{{\sqrt{n}\sigma}})$ as $\frac{1}{\sqrt{n}\sigma}$ is a constant. We then have

\[
M_{S^*}(t) = (M_{(X_i - \mu)}(\frac{t}{{\sqrt{n}\sigma}}))^n
\]

This is a fairly complex function and we can make it easier to work with by expanding it as a Taylor polynomial. We have

\[
M_{(X_i - \mu)}(\frac{t}{{\sqrt{n}\sigma}}) = E[1 + (\frac{t}{{\sqrt{n}\sigma}})(X - \mu) + (\frac{t^2}{{2n\sigma^2}})(X - \mu)^2 + ...]
\]

where we can disregard the remaining terms. We then have

\[
M_{(X_i - \mu)}(\frac{t}{{\sqrt{n}\sigma}}) \approx E[1] + \frac{t}{{\sqrt{n}\sigma}}E[(X - \mu)] + \frac{t^2}{{2n\sigma^2}})E[(X - \mu)^2]
\]







</html>

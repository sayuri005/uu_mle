# Problem Set 6: MLE

1. Let $\ell = -\log(\sigma) - \frac{1}{2\sigma^2} \sum_{i=1}^n(y_i - x_i \beta)^2$. Find the value of $\mu$ that maximizes $\ell$ by setting $\ell'(\mu) = 0$ and solving. Check that the second derivative of $\ell(\mu)$ is negative at that value of $\mu$; why do we care? Find the value of $\sigma$ that maximizes $\ell$ by setting $\ell'(\sigma)=0$ and solving.

2. Let $X_1,\ldots,X_n$ be i.i.d. $N(\mu,\sigma^2)$, and you have drawn a sample with observed values $ (3.0,5.0,9.0)$.

    **a.** Write the log-likelihood $\ell(\mu,\sigma^2)$ for this sample. Then maximize it to find $\hat{\mu}$ and $\widehat{\sigma^2}$

    **b.** Compute a 95% confidence interval for $\mu$

    **c.** Provide a 90% prediction interval for $X$.

3. Let $y$ be an $n\times 1$ vector with $y\sim N(X\beta,\sigma^2 I)$, where $X$ is $n\times p$: $n$ observations of $p$ predictors.

    **a.** Write the log-likelihood $\ell(\beta,\sigma^2)$ in matrix form.

    **b.** Show that maximizing $\ell$ over $\beta$ is the same as minimizing $(y-X\beta)^\top(y-X\beta)$, and that $\hat{\beta} = (X^\top X)^{-1}X^\top y$.

    **c.** Take $n = 3$, $y = (2,3,5)^\top$, and

    $$
    X = \begin{pmatrix}
    1 & 1 \\
    1 & 2 \\
    1 & 3
    \end{pmatrix}.
    $$

    Compute $\hat{\beta}$. *Hint:* for a $2\times 2$ matrix,

    $$
    \begin{pmatrix}
    a & b \\
    c & d
    \end{pmatrix}^{-1}
    = \frac{1}{ad-bc}
    \begin{pmatrix}
    d & -b \\
    -c & a
    \end{pmatrix}.
    $$

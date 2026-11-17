# Problem Set 7: MLE for Binary and Count Outcomes

Assume observations are independent (conditional on the regressors, when present). Show your work; a calculator or a few lines of Python are fine. Use $1.96$ for approximate 95% confidence intervals. These small samples are for practicing the calculations; the normal approximations may be poor.

1. **Bernoulli likelihood.** Let $Y_1,\ldots,Y_n$ be i.i.d. Bernoulli $(p)$, with

    $$
    \Pr(Y_i=y_i)=p^{y_i}(1-p)^{1-y_i},\qquad y_i\in\{0,1\}.
    $$

    Assume the sample contains both zeros and ones.

    **a.** Write the log-likelihood $\ell(p)$ and find its first and second derivatives with respect to $p$.

    **b.** Set the first derivative equal to zero and solve for $\hat p$. Check that the second derivative is negative. Why does that matter?

    **c.** Now write $p=1/(1+e^{-\beta})$. Differentiate $\ell$ with respect to $\beta$, and express $\hat\beta$ in terms of $\hat p$. Explain the connection to logistic regression.

2. **Poisson likelihood.** Let $Y_1,\ldots,Y_n$ be i.i.d. Poisson $(\lambda)$, with

    $$
    \Pr(Y_i=y_i)=\frac{e^{-\lambda}\lambda^{y_i}}{y_i!},\qquad y_i\in\{0,1,2,\ldots\}.
    $$

    Assume at least one observed count is positive.

    **a.** Write the log-likelihood $\ell(\lambda)$ and find its first and second derivatives with respect to $\lambda$.

    **b.** Set the first derivative equal to zero and solve for $\hat\lambda$. Check that the second derivative is negative at your answer.

    **c.** Now write $\lambda=e^\beta$. Differentiate $\ell$ with respect to $\beta$, and express $\hat\beta$ in terms of $\hat\lambda$. Explain the connection to Poisson regression.

3. **Fit an intercept-only logistic model.** Five customers were offered a subscription. Their purchase decisions were

    $$
    y=(0,1,1,0,1),\qquad p=\frac{1}{1+e^{-\beta}}.
    $$

    **a.** Write the sample log-likelihood and find $\hat p$ and $\hat\beta$.

    **b.** Using

    $$
    \operatorname{SE}(\hat\beta)=\frac{1}{\sqrt{n\hat p(1-\hat p)}},
    $$

    compute an approximate 95% confidence interval for $\beta$. Transform its endpoints through the logistic function to obtain an interval for $p$.

    **c.** For one new customer under the same conditions, predict the probabilities of purchase and no purchase. Which outcome is more likely? Explain why the interval for $p$ is not a prediction interval for this customer's binary outcome.

4. **Fit an intercept-only Poisson model.** The numbers of support requests received during five equal-length shifts were

    $$
    y=(0,1,2,2,5),\qquad \lambda=e^\beta.
    $$

    **a.** Write the sample log-likelihood and find $\hat\lambda$ and $\hat\beta$.

    **b.** Using

    $$
    \operatorname{SE}(\hat\beta)=\frac{1}{\sqrt{n\hat\lambda}},
    $$

    compute an approximate 95% confidence interval for $\beta$. Exponentiate its endpoints to obtain an interval for $\lambda$.

    **c.** For a new shift of the same length, predict the expected count, the probability of zero requests, and the probability of at least two requests. Treat the fitted parameters as fixed when predicting.

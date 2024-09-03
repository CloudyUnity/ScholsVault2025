Given a set of i.i.d. observed values in a sample of size $n$, what is an estimation for a population parameter (e.g. $\mu$)

Population parameter estimations have a hat $(\hat \mu)$
# Point Estimation

When a population parameter is estimated using a single value
When observations are i.i.d. then:
	 $\mu = E(X)$
	 $\sigma^2 = \dfrac{V(X)}{n}$
	 Large $n \to \bar{X}_n \sim$ N$(\mu, \dfrac{\sigma^2}{n})$
Otherwise
	$\hat \mu = \bar{x}_n$
	$\hat{\sigma}^2 = n^{-1} \sum (x_i - \bar{x}_n)^2$

$X \sim$ Bern$(\pi) \to E(\bar{X}_n) = \pi$

Repeated Sampling
	If we gather multiple samples of size $n$ then the distribution of the sample statistics provides info on the population parameters

Standard Error $(SE)$
	$SE = \dfrac{\hat{\sigma}^2}{\sqrt n}$
	This is the standard error of the mean
	Assumes that $n$ is much smaller than $N$

Finite Population Correction (FPC)
	This is a correction to $SE$ when $\dfrac{n}{N} > 0.1$ or sometimes $\dfrac{n}{N} > 0.05$
	$SE = \dfrac{\hat{\sigma}^2}{\sqrt n} \sqrt{\dfrac{N - n}{N - 1}}$
	This is only for finite populations

Estimators
	These are used to obtain estimate quantities of interest in the population from observations in a sample 
	An estimator for the generic population parameter $\theta$ is a function of the sample observations $T = t(X_1, X_2, \dots, X_n)$
	The value of the estimator is called the estimate: $t = t(x_1, x_2, \dots, x_n)$
	Equivalent to sample statistics and their values but with the focus on finding estimators for $\theta$

r.v. $X \ \ \ \ \ \ \ \ \ \ \longrightarrow$ Observation $x$
Estimator $T \longrightarrow$ Estimate $t$

Unbiased Estimators
	The bias of an estimator $T$ for $\theta$ is
		$B(T) = E(T) - \theta$
	An estimator is thus unbiased if $B(T) = 0$ and $E(T) = \theta$

Mean Squared Error $(MSE)$
	A measure for how far $T$ is from $\theta$ 
	$MSE(T) = E[(T - \theta)^2]$
	$MSE(T) = V(T) + B(T)^2$
	When unbiased $MSE(T) = V(T)$
	$T_1$ is more efficient than $T_2$ when
		$MSE(T_1) < MSE(T_2)$	

Example
	$T_1 = n^{-1} \sum X_i$
	$T_2 = \dfrac{1}{n-1} \sum X_i$
	$E(T_1) = n^{-1} \sum E(X_i) = \mu$
	$E(T_2) = \dfrac{1}{n - 1} \sum E(X_i) = \dfrac{n}{n-1} \mu$
	Only $T_1$ is unbiased for $\mu$

Unbiased Sample Variance Estimator $(S^2)$
	$S^2 = \dfrac{1}{n-1} \sum (X_i - \bar{X}_n)^2$
	$S^2$ is unbiased therefore
		$E(S^2) = \sigma^2$	

# Interval Estimation

Point estimation is based on repeated sampling of decent sample sizes
Sometimes the point estimate value is far from the actual parameter value

We know that for large sample sizes the distribution of the standardized sample mean is approx the standard normal
	$Z = \dfrac{\bar{X}_n - \mu}{\sigma / \sqrt n} \sim$ N$(0, 1)$

We can construct interval estimates for population parameters called confidence intervals

$1 - a$ is the confidence level

For the sample mean with a known population variance
	$\bar{X}_n \pm z_{\frac{a}{2}} \dfrac{\sigma}{\sqrt n}$

For an observed sample
	$\bar{x}_n \pm z_{\frac{a}{2}} \dfrac{\sigma}{\sqrt n}$

#todo 
	What is the difference between a sample $\{X_1, X_2, \dots, X_n\}$ and an observed sample $\{x_1, x_2, \dots, x_n\}$

$Pr(\bar{x}_n - z_{\frac{a}{2}} \dfrac{\sigma}{\sqrt n} \leq \mu \leq \bar{x}_n + z_{\frac{a}{2}} \dfrac{\sigma}{\sqrt n} )) = 1 - a$
There is a $(1-a)$ probability that the interval for the sample mean will contain $\mu$

When $X \sim$ N$(\mu, \sigma^2)$ and the population variance is not known
	$\bar{X}_n \pm t_{\frac{a}{2}} \dfrac{S}{\sqrt n}$
	$\bar{x}_n \pm t_{\frac{a}{2}} \dfrac{S}{\sqrt n}$
	Where $v = n -1$

For estimating population proportion $\pi$
	$\bar{X}_n \pm z_{\frac{a}{2}} \dfrac{\sqrt{\bar{X}_n (1 - \bar{X}_n)}}{\sqrt n}$
	$\bar{x}_n \pm z_{\frac{a}{2}} \dfrac{\sqrt{\bar{x}_n (1 - \bar{x}_n)}}{\sqrt n}$

When is data considered normal?
	Histogram
		One mode, symmetric, bell shaped
	QQ Plot (Normal Probability Plot)
		Shows standardized observed $n$ values against those of a standard normal distribution with sample size $n$
	Statistical Tests
		You can formally check normality with tests like the Kolmogorov-Smirnov or Shapiro-Wilk tests

Minimum Sample Size
	This is the minimum sample size that guarantees the maximum width of the confidence interval
	$\delta = 2 z_{\frac{a}{2}} SE$
	If the variance is known
		$n \geq (2 z_{\frac{a}{2}} \dfrac{\sigma}{\delta})^2$
	For proportions
		$\sigma^2 = \hat \pi (1 - \hat \pi)$
		Remember to account for this in the $SE$



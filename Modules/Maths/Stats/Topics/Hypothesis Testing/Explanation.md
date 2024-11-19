
# Parametric Context

A statement concerning the parameters or form of the probability distribution for a population has been formulated. We need to test it	

When making assumptions on the probability distribution, and we'd like to test those assumptions we are in the context of parametric hypothesis testing

Test Statistic $(T_{s})$
	A standardized value calculated from sample data
	Measures deviation from the null hypothesis
	Has a sampling distribution ($Z, T, \mathscr{X}^2,$ etc)

How to test a statement
	Quantify the evidence supporting it using appropriate $T_{s}$ and a significance level $a$

Hypothesis
	A statement regarding a parameter $\theta$ in a population of interest

Neyman-Pearson Approach
	Null hypothesis and Alternative hypothesis
	The null $H_0$ corresponds with the statement we wish to test, we're looking to see if we have evidence to reject this hypothesis
	The alternative $H_1$ corresponds with an alternative to $H_0$ 

One-Sided Hypothesis
	Appropriate when missing an effect in the untested direction isn't relevant (e.g. A cheaper drug is developed and you only care about if it's less effective. Not appropriate if the drug is intended to be an improvement)
	$H_0 : \theta =\theta_0$
	$H_1 : \theta > \theta_0$
	or
	$H_1 : \theta < \theta_0$

Two-Sided Hypothesis
	$H_0 : \theta = \theta_0$
	$H_1 : \theta \neq \theta$

# Repeated Sampling Context

Here a hypothesis test is a rule allowing us to discriminate samples between those agreeing with $H_0$ and those which do not
$a$ represents the fraction of samples we expect to be in disagreement with $H_0$
$T_{s}$ is computed using sample data, used to quantify information supporting $H_0$ in a sample

Rejection Region $(RR)$
	Given $a$ we can define this as the region with the set of values of $T_{s}$ that reject $H_0$ 
	It has an area of $a$

Rejection rule $(Rr)$
	A boolean expression which if true, you must reject $H_0$
	(I made this term up, but it's useful later)

Acceptance region $(AR)$
	Set of values of $T_{s}$ that fail to reject $H_0$ 
	It has an area of $1-a$

![[Pasted image 20240904151809.png]]

P-Value ($p$)
	Given an observed sample and $t$ computed in the sample, $p$ is the probability of observing a value of $T_{s}$ more extreme than $t$ under $H_0$
	These are not fixed values
	$p < a \to H_1$
		"If $p$ is low, reject $H_0$"
	This does not measure the size of an effect or the importance of a result
	$p$ being closer to 0 does not make it more significant
	$p$ only has meaning based on whether it is higher or lower than $a$

P-Hacking
	Manipulation of researcher decisions to bias data
	For example when to stop collecting data, whether or not the data is transformed, which tests/parameters to use

![[Pasted image 20240904152214.png]]

Errors
	If we reject $H_0$ but $H_0$ was true, that's a **type 1 error**
	If we don't reject $H_0$ but $H_0$ was false, that's a **type 2 error**
	![[Pasted image 20240904152340.png]]
	$a$ is the probability of a type 1 error
	$\beta$ is the probability of a type 2 error
		This value depends on $a$ 
	$1 - \beta$ is the power of the test, we want this to be large as fuck

![[Pasted image 20240904152714.png]]

# One Population Tests

Test for the mean (Known $\sigma^2$)
	$T_{s} \sim N(\mu_0, \sigma)$
	$z = \dfrac{\bar{X}_n - \mu_0}{\sigma / \sqrt n}$
	$\mu_0$ is the population mean under $H_0$
	If $H_1$ is...
		$\mu > \mu_0$
			$Rr = z \geq z_a$
			$Rr = \bar{X}_n \geq \mu_0 + z_a SE$
			$p = Pr(Z \geq z)$
		$\mu < \mu_0$
			$Rr = z \leq -z_a$
			$Rr = \bar{X}_n \leq \mu_0 - z_a SE$
			$p = Pr(Z \leq z)$
		$\mu \neq \mu_0$
			$Rr = |z| \geq z_{\frac{a}{2}}$
			$Rr = (\bar{X}_n \geq \mu_0 + z_{\frac{a}{2}} SE) \lor (\bar{X}_n \leq \mu_0 - z_{\frac{a}{2}} SE)$
			$p = 2 Pr(Z \geq |z|)$

Test for a proportion
	$T_{s} \sim N(\pi_0, \pi_0 (1 - \pi_0))$
	Follow same rules as Test for a mean (Known $\sigma^2$)
		$\mu_0 = \pi_0$
		$\sigma^2 = \pi_0 (1 - \pi_0)$
		$z_a = z_a$

Test for the mean (Unknown $\sigma^2$)
	$T_{s} \sim T(n - 1)$
	$t = \dfrac{\bar{X}_n - \mu_0}{S / \sqrt n}$
	$S$ is the sample standard deviation
	This holds when $X$ is normally distributed or $n$ is very large
	Follow same rules as Test for a mean (Known $\sigma^2$)
		$Z = T$
		$z = t$
		$z_a = t_a$

Test for proportions
	Consider if $X$ can take $K$ different values
	We want to test if observed frequencies $f_1, f_2, \dots, f_K$ match those expected under $H_0$
	$H_0 : \pi_1, \pi_2, \dots, \pi_K$
	$H_1 :$ Any proportion different
	$T_{s} \sim \mathscr{X}^2(K - 1)$
	When given frequencies, test with frequencies
		$\mathscr{x}^2 = \overset{K}\sum \dfrac{(f_k - n \pi_k)^2}{n \pi_k}$
	Otherwise test with proportions
		$\mathscr{x}^2 = \overset{K}\sum \dfrac{(\tilde f_k - \pi_k)^2}{\pi_k}$
	$\mathscr{x}^2 = \overset{K}\sum \dfrac{(O - E)^2}{E}$
		$O$ = Observed Value
		$E$ = Expected Value
	$Rr = \mathscr{x}^2 \geq \mathscr{x}^2_a$
	$p = Pr(\mathscr{X^2} \geq \mathscr{x}^2)$

# Two Population Tests

Test between means (Known $\sigma^2$)
	$T_{s} \sim N$
	$z = \dfrac{\bar{X}_1 - \bar{X}_2 - d_0}{\sqrt{\sigma^2_1 / n_1 + \sigma^2_2 / n_2}}$
	$d_0 = \mu_1 - \mu_2$
	If $H_1$ is...
		$d_0 > 0$ or $\mu_1 > \mu_2$
			$Rr = z \geq z_a$
			$p = Pr(Z \geq z)$
		$d_0 < 0$ or $\mu_1 < \mu_2$ 
			$Rr = z \leq -z_a$
			$p = Pr(Z \leq z)$
		$d_0 \neq 0$ or $\mu_1 \neq \mu_2$
			$Rr = |z| \geq z_{\frac{a}{2}}$
			$p = 2 Pr(Z \geq |z|)$
	#NeedsFactCheckingByTrueAmericanPatriots 
		Are these p values correct?

Pooled Variance Estimator ($S_p^2$)
	$S_p^2 = \dfrac{(n_1 - 1)S_1^2 + (n_2 - 1)S_2^2}{n_1 + n_2 - 2}$

Test between means (Unknown $\sigma^2$)
	$T_{s} \sim T(n_1 + n_2 - 2)$
	$t = \dfrac{\bar{X}_1 - \bar{X}_2 - d_0}{\sqrt{S^2_p (1/n_1 + 1/n_2)}}$	
	Follow same rules as Test between means (Known $\sigma^2$)
		$z = t$
		$z_a = t_a$

Joint Proportion Estimator ($\bar{X}_p$)
	$\bar{X}_p = \dfrac{n_1 \bar{X}_1 + n_2 \bar{X}_2}{n_1 + n_2}$

Test between proportions
	$T_{s} \sim N$
	$z = \dfrac{\bar{X}_1 - \bar{X}_2 - d_0}{\sqrt{\bar{X}_p (1 - \bar{X}_p)(1/n_1 + 1/n_2)}}$
	Follow same rules as Test between means (Known $\sigma^2$)
		$\mu = \pi$

Independence Test
	$X$ is a categorical variable taking $K$ different values
	$Y$ is a categorical variable taking $J$ different values
	We want to test if $X$ and $Y$ are independent 
	$H_0 : \dfrac{f_{1,1}}{n} = \dfrac{f_{1,2}}{n} = \dots = \dfrac{f_{K,J}}{n}$
	$H_1 :$ Any proportion different
	![[Pasted image 20240904171942.png]]
	
	$T_{s} \sim \mathscr{X}^2 ((K-1)(J-1))$
	$\mathscr{x}^2 = \overset{K}{\sum} \overset{J}{\sum} \dfrac{(f_{kj} - f_{k.} f_{.j} / n)^2}{f_{k.} f_{.j} / n}$
	$\mathscr{x}^2 = \overset{K}{\sum} \dfrac{(O - E)^2}{E}$
	$E = \dfrac{row \times column}{n}$
	
	$Rr = \mathscr{x}^2 \geq \mathscr{x}^2_a$
	$p = Pr(\mathscr{X}^2 \geq \mathscr{x}^2)$
	Given a joint frequency table ($O$) you need to calculate $E$ for each non-margin cell
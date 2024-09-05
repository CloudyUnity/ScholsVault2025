What is a distribution
	 **"The simplest useful numerical description of a distribution
consists of both a measure of center and a measure of spread."** - *David. S. Moore* himself
	 A distribution is a method of visualizing the spread, variability and frequencies of outcomes in an probabilistic event we can observe, the useful thing about observations is that they can have patterns we can use to describe them.
	 Normal Distribution is bell shaped
	 Uniform Distribution is a flat block

$X \sim$ R(...)
	The r.v. X is distributed in the R distribution

`C` = Continuous r.v.
`D` = Discrete r.v.

$f(x)$ is the PDF for continuous r.v.s
$Pr(x_i \leq X \leq x_j) = \int^{x_j}_{x_i} f(w) dw$
	PDF = Probability Density Function
	
$F(x)$ is the CDF for a discrete or continuous r.v.
For an interval `[a, b]`
	$x < a \to F(x) = 0$
	$x > b \to F(x) = 1$
	 CDF = Cumulative Distribution Function
	 
For discrete r.v.s 
	$E(X) = \sum x_i Pr(x_i)$
	$V(X) = \sum [x_i - E(X)]^2 Pr(x_i)$

For continuous r.v.s 
	$E(X) = \int^{b}_a x f(x) dx$
	$V(X) = \int^b_a [x - E(X)]^2 f(x) dx$

# Distributions

`D` Discrete Uniform:
	$X \sim$ U(a, b)
	$n$ = b - a + 1
	$Pr(X = x) = \dfrac{1}{n}$
	$E(X) = \dfrac{1}{n} \sum x_i$
	$V(X) = \dfrac{n^2 - 1}{12}$

`C` Continuous Uniform:
	$X \sim$ Unif(a, b)
	$f(x) = \dfrac{1}{b-a}$
	$F(x) = \dfrac{x - a}{b - a}$
	$E(X) = 0.5 (a+b)$
	$V(X) = \dfrac{(b-a)^2}{12}$

`D` Bernoulli:
	$X \sim$ Bern($\pi$)
	x = {0, 1}
	$Pr(X = x) = \pi ^x (1-\pi)^{1-x}$
	$E(X) = \pi$
	$V(X) = \pi (1-\pi)$

`D` Binomial:
	$X \sim$ Binom($\pi, n$)
	Trials must be independent 
	$Pr(X = x) = \binom{n}{x} \pi ^x (1-\pi)^{n-x}$
	$E(X) = n \pi$
	$V(X) = n \pi (1 - \pi)$
	$\overline{x}_{a} \approx n \pi$

`D` Poisson:
	$X \sim$ Pois($\lambda$)
	$\lambda > 0$
	$Pr(X = x) = \dfrac{\lambda ^x}{x!} \ exp(-\lambda)$
	$E(X) = V(X) = \lambda$
	$V(\hat X) = \dfrac{\lambda}{n}$
	#todo 
		Is this ^ necessary? Come back after writing estimation notes
	Given $X_1 \sim Pois(\lambda_1), \dots, X_P \sim Pois(\lambda_P)$
		$\sum X_i \sim Pois(\sum \lambda_i)$

Given $X \sim Binom(\pi, n)$
	For large $n$ and small $\pi$ : $X \sim$ Pois($n\pi$)
	Guidelines:
		$n > 100 \land \pi \leq 0.05$
		$\pi \leq 0.01$

`C` Exponential:
	$X \sim$ Exp($\lambda$)
	X intervals $[0, \infty]$		
	$\lambda > 0$
	$f(x) = \lambda \ exp(-\lambda x)$
	$F(x) = 1 - exp(-\lambda x)$
	$E(X) = \dfrac{1}{\lambda}$
	$V(X) = \dfrac{1}{\lambda ^2}$

`C` Normal/Gaussian:
	$X \sim$ N($\mu, \sigma ^2$)	
	$f(x) = \dfrac{1}{\sqrt{\sigma ^2 2 \pi}} exp(\dfrac{-(x - \mu)^2}{2 \sigma ^2})$
	$F(x) = #todo
	$E(X) = \mu$
	$V(X) = \sigma ^2$
	Unimodal and Symmetric around mean
	Given $Y = a + bX$
		$Y \sim$ N($a + b\mu, b^2 \sigma^2$)		
	Given $X \sim$ N($\mu_X, \sigma_X^2$) and $Y \sim$ N($\mu_Y, \sigma_Y^2$)
		$X + Y \sim$ N($\mu_X + \mu_Y, \sigma_X^2 + \sigma_Y^2$)
	Observations:
		68% fall between $\mu \pm \sigma$ 
		95% fall between $\mu \pm 1.96 \sigma$
		99.7% fall between $\mu \pm 3\sigma$

`C` Standard Normal:
	$Z \sim$ N(0, 1)
	Given $X \sim$ N($\mu, \sigma^2$)
		$Z = \dfrac{X - \mu}{\sigma}$
		$z = \dfrac{x- \mu}{\sigma}$
	$f(z) = \dfrac{1}{\sqrt{2 \pi}} exp(-0.5 x^2)$
	$f(z) = f(-z)$
	$F(-z) = 1 - F(z)$
	$F(z) \equiv \upphi(z)$
	Cumulative/Z-Scores:
		$\int^z_0 f(w) dw =$ Use P Tables ($P$)
		$Pr(0 \leq Z) = 0.5$
		$Pr(0 \le Z \le z) = P$
		$Pr(Z \le z) = P + 0.5$
		$Pr(z_1 \le Z \le z_2) = Pr(Z \le z_2) - Pr(Z \le z_1)$
		$Pr(Z \ge z) = 1 - Pr(Z \le z)$
		$Pr(Z \le -z) = 1 - Pr(Z \le z)$

`C` Student's T:
	$X \sim$ T($v$)
	$v =$ degrees of freedom
	$v > 0$
	$v < 2 \to E(X) = UB$
	$v \geq 2 \to E(X) = 0$
	$v < 3 \to V(X) = UB$
	$v \geq 3 \to V(X) = \dfrac{v}{v - 2}$		
	Use tables to calculate $Pr(T \leq t)$

`C` Chi-Squared:
	$X \sim \mathscr{X}^2(v)$
	$v =$ degrees of freedom
	$v > 25 \to X \sim N$
	#todo 
		Check if $E(X), V(X),$ etc are important/readable

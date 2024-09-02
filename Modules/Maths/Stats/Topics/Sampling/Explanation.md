
$N$ = Population size
$n$ = Sample size

Finite populations are countable
Population parameters can be used on finite populations
	These are constant variables such as the mean/variance
	For example $\mu = N^{-1} \sum x_i$

Infinite populations are uncountable
Parameters can be used to describe infinite populations
	These are not constant
	For example $E(X) = \mu$
	Characteristics are taken to be r.v.s

A sample survey is the selection and analysis of a set of units from a population with the goal of gaining information on some of the population parameters

For finite populations you can collect all data with a census for all $N$ units

$\dfrac{n}{N}$ is the sampling fraction
$\ohm$ is the sample space, the set of all possible samples that can be drawn from a population
$p_S$ is the probability a sample $S$ is taken from $\ohm$ 
For $\ohm$ of ordered samples of size $n$, $|\ohm| = \underset{i=0}{\overset{n + 1}{\prod}} (N - i)$
For $\ohm$ of ordered samples of size $n$, $|\ohm| = \binom{N}{n}$

Sampling design is the pair of $\ohm$ and $p_S$
Sampling errors are inaccuracies carries out at the sampling stage, generally when the sample does not properly represent the population
	Random Errors
		Errors happen randomly and independently, normally distributed
	Systematic Errors
		The error systemically depends on some external factor with a direct impact on the quantity recorded in the sample. The samples become biased

Simple Random Sampling Design:
	When each sample has the same probability of being selected
	![[Pasted image 20240902164419.png]]
	When sampling with no repetition the values in the sample are dependant 
		$X \sim$ U(1, 3)
		$Pr(X_2 = 2) \neq Pr(X_2 = 2 | X_1 = 1)$
		#todo 
			Does it make sense to use $X \sim \dots$ for discrete populations?

Stratified Random Sampling Design:
	The population is divided into subgroups according to different criterion
	Units are extracted using simple random sampling from each of the subgroups
	Useful when the population is not homogenous with respect to 1+ characteristic 
	Allows for collection of information at population and subgroup level

Systematic Sampling Design
	The units in an ordered population are selected at a regular interval $K$ 
	Easy to implement but large risk of data manipulation when ordering the population or choosing $K$

Independent and Identically Distributed (i.i.d.)
	#todo

Sampling from infinite populations
	Census is not an option, you must always sample
	Given a population characteristic $X$, $n$ i.i.d. observations form a sample
	It does not make sense here to distinguish between sampling with or without repetition 

Sample Statistic
	A function of the sample observations $t(X_1, X_2, \dots, X_n)$
	Sample Mean:
		$\bar{X} = n^{-1} \sum X_i$
	Sample Variance:
		$\hat{\sigma}^2 = n^{-1} \sum (X_i - \bar{X})^2$
	The value of the sample statistic evaluated on the observed sample is $t(x_1, x_2, \dots, x_n)$
	#todo 
		Huh? What does that even mean

Sampling Distribution
	The probability distribution of $t(X_1, X_2, \dots, X_n)$ 

Remember that $\mu$ is the population mean
$E(\bar X) = E(X_i) = \mu$
$V(\bar X) = \dfrac{\sigma^2}{n}$
$X \sim$ N$(\mu, \sigma^2)$ $\to \bar X \sim$ N$(\mu, \dfrac{\sigma^2}{n})$
$X \sim$ Bern$(\pi) \to \bar X \sim \dfrac{1}{n}$ Binom$(\pi, n)$

Central Limit Theorem (CLT)
	$\underset{n \to \infty}{\lim} Pr(\dfrac{\bar{X}_n - \mu}{\dfrac{\sigma}{\sqrt n}} \leq z) = Pr(Z \leq z)$


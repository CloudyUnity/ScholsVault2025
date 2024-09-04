A random variable (r.v.) is a function defined over $\ohm$ that associates a real value to each of the elementary events

There are discrete and continuous r.v.s

r.v.s use upper case ($X$)
r.v. realizations use lower case ($x$)

Probability Distribution Function (No Acronym):
	A Probability Distribution Function of a discrete r.v. is a function which associates a probability $Pr(X = x_i)$ to each of the values $X$ may take
	$Pr(X = x_i) \geq 0$
	$Pr(X = x_i) = Pr(x_i)$

Discrete Cumulative Distribution Function (CDF):
	The CDF of a discrete r.v. is a function which associates a cumulative probability $Pr(X \leq x_i)$ to each of the values $X$ may take
	$F(x_i) = Pr(X \leq x_i)$
	$F(x)$ is non-decreasing
		$x_1 < x_2 \to F(x_1) \leq F(x_2)$
	For a discrete r.v. in `[a, b]`
		$x \leq a \to F(x) = 0$
		$a \leq x \leq b \to 0 \leq F(x) \leq 1$
		$x \geq b \to F(x) = 1$

![[Pasted image 20240902123130.png]]


Probability Density Function (PDF)
	The PDF for a continuous r.v. $X$ is a function whose underlying area in a given interval corresponds to the probability $X$ takes a value in that said interval
	$Pr(xi \leq X \leq x_j) = \int^{x_j}_{x_i} f(x) dx$
	$f(x)$ is the PDF
	$f(x) \geq 0$
	If a continuous r.v. $X$ takes values in `[a, b]
		$\int^{b}_a f(x) dx = 1$
	$Pr(X = x_i) = 0$
	$Pr(x_i \leq X \leq x_j) = Pr(x_i < X < x_j)$

Continuous Cumulative Distribution Function (CDF)
	$F(x) = Pr(X \leq x) = \int^{x}_a f(w) dw$
	Where $X$ is in the range `[a, b]`
	$F(x)$ is still non-decreasing
		$x_1 < x_2 \to F(x_1) \leq F(x_2)$

Expected Value ($E(X)$)
	The expected value of a r.v. is the mean/average value over a large number of trials

Variance ($V(X)$)
	The variance of a r.v. measures the average of the differences between the possible values of $X$ and $E(X)$ weighted by the probabilities 
	$V(X) = E([X - E(X)]^2)$
	$V(X) = E(X^2) - E(X)^2$

See [[Trinity/Schols/Modules/Maths/Stats/Topics/Distributions/Explanation|Explanation]] for more info on $E(X)$ and $V(X)$ for various distributions

Standard Deviation ($Sd(X)$)
	$Sd(X) = \sqrt{V(X)}$

Equations for the Y axis
	$E(Y) = E(d + sX) = d + sE(X)$
	$V(Y) = V(d + sX) = s^2 V(X)$
	#todo
	What is d and s?
	Add more info in general

Standardization ($Z$)
	$Z = \dfrac{X - E(X)}{Sd(X)}$
	$Z$ is a r.v. corresponding to the standardized $X$ r.v.
	$E(Z) = 0$
	$V(Z) = 1$

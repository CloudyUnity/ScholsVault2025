
See distributions from Stats [[Trinity/Schols/Modules/Maths/Stats/Topics/Distributions/Explanation|Explanation]] 

$E(X^2)$ is the expected value of the square of $X$ 
Remember that $E(X^2) = V(X) + E(X)^2$ 
Poisson:
	$E(X^2) = \lambda + \lambda^2$ 
$E(X^n) = \sum x^n P(X =x )$ 

For two independent discrete r.v.s $X$ and $Y$ 
	$E(XY) = E(X)E(Y)$

For two dependent discrete r.v.s $X$ and $Y$
	$E(XY) = \underset{x}{\sum} \underset{y}{\sum} xy P(X=x, Y=y)$

For two continuous r.v.s $X$ and $Y$ 
	$E(XY) = \int \int xy \  f(x, y)\  dx \ dy$ 

Stirling Number of the Second Kind
	$S(n, k) = \{{{n}\atop{k}}\}$ 
	Returns the number of ways to partition a set of $n$ objects into $k$ non-empty subsets
	$\{{n \atop n}\} = 1, n \geq 0$ 
	$\{{n \atop 1}\} = 1, n \geq 1$ 
	$k = 0 \land n \neq 0 \to S(n, k) = 0$
	$k = 1 \to S(n, k) = 1$
	$k > n \to S(n, k) = 0$
	Example: 	
		$S(3, 2) = |\{\{\{0, 1\}, \{2\}\}, \{\{0\},\{1, 2\}\}, \{\{1\}\{0,2\}\}\}| = 3$

Poisson Moments
	$E(X!) = \lambda^n$ 
	$E(X^n) = \sum S(n, k) \lambda^k$ 
		$E(X) = S(1, 0) \lambda = \lambda$
		$E(X^2) = S(2, 0) \lambda + S(2, 1) \lambda^2 = \lambda + \lambda^2$
		$E(X^3) = S(3, 0) \lambda + S(3, 1) \lambda^2 + S(3, 2) \lambda^3 = \lambda + 3\lambda^2 + \lambda^3$ 

Remember that for independent variables the joint distribution function $f_{X,Y} = f_X f_Y$ 
$X_{min} < g(X) < h(Y) < Y_{max}$
$g(X) < X_{max}$
$Y_{min} < h(Y)$ 
$P(g(X) > h(Y)) = \int^{X_{max}} _{X_{min}} \int^{Y_{max}} _{Y_{min}} f_{X, Y} (x, y) \ dy \ dx$ 
IDFK try more examples and figure it out
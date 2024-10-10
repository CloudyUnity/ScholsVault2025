The domain is the set of input values
The codomain is the set of output values
The rule is an association between how to map the domain to the codomain

A function consists of a domain, codomain and a rule

A function cannot map an element in the domain to multiple elements in the codomain

$y = f(x)$
	$x$ is independent
	$y$ is dependent 

The image is the set of all elements of the codomain associated with an element of the domain
	Domain = $A \to$ Image = $\{f(x) | x \in A \}$

A graph of a function is the set of ordered pairs $(x, f(x))$
	If a vertical line intersects a curve more than once, it is not a function

A piecewise function has a different rule depending on where in the domain $x$ lies

Interval Notation:
	$[a, b]$ is inclusive
	$(a, b)$ is exclusive

$(f + g)(x) = f(x) + g(x)$
$(f - g)(x) = f(x) - g(x)$
$(fg)(x) = f(x)g(x)$
Domain = $D_f \cap D_g$

$(\dfrac{f}{g})(x) = \dfrac{f(x)}{g(x)}$.
	Domain = $D_f \cap \{ x \in D_g | g(x) \neq 0 \}$

Composition:
	($g \circ f)(x) = g(f(x))$
		Assuming $f(x) \in D_g$
	Assume the codomain is $\mathbb{R}$

Translations:
	To translate by $(h, v)$
	$f(x - h) + v$

Scaling:
	To scale by $(h, v)$
	$vf(\dfrac{x}{h})$

Reflections:
	x-axis flip:
		$-f(x)$
	y-axis flip:
		$f(-x)$

$f(x) = f(-x) \to f(x)$ is even
$-f(x) = f(-x) \to f(x)$ is odd

Polynomials with degree $n$:
	$f(x) = a x^n + \dots + b x^2 + c x + d$
	Turning points $< n$

Rational Functions:
	$f(x) = \dfrac{g(x)}{h(x)}$
	Where $g(x), h(x)$ are polynomials

Sinusoidal:
	$f(\theta) = a sin(b \theta + c)$
	Frequency = $\dfrac{|b|}{2 \pi}$
	Period = $\dfrac{2 \pi}{|b|}$

Surjective: $\forall y \in$ Codomain, $\exists x (f(x) = y)$
	Horizontal Line hits at least once
	Every output is mapped
Injective: $\forall y \in$ Codomain, $\exists^{\leq 1} x (f(x) = y)$
	Horizontal Line hits at most once
	No output is mapped more than once
Bijective: $\forall y \in$ Codomain, $\exists !x (f(x) = y)$
	Horizontal Line hits once
	Every output is mapped once

Inverse Functions:
	$f(x)$ must be bijective
	$f : A \to B$
		$x \mapsto f(x)$
	$f^{-1} : B \to A$
		$f(x) \mapsto x$
	$f^{-1}$ is the reflection of $f(x)$ across $y = x$
	How to solve:
		$y = kx + c$
		$x = \dfrac{y - c}{k}$
		$f^{-1} = \dfrac{x - c}{k}$


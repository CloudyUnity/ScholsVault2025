See the functions section in Maths 1

Domain = $D$
Codomain = $C_d$
$f : D \to C_d$

Boolean Function:
	A function where $C_d = \{T, F\}$

Graph $(\Upgamma(f))$
	$\Upgamma (f) \subset D \times C_d$
	$\Upgamma (f) = \{(x, f(x)) | x \in D\}$

$f^{-1} \circ f(x) = x$
Inverse functions only exist for bijective functions

Assume $D$ is finite
$f$ is injective $\leftrightarrow |f(D)| = |D|$
Proof:
	$D = \{a_1, a_2, \dots, a_n\} \to f(D) = \{f(a_1), f(a_2), \dots, f(a_n)\}$
	$f$ is injective $\leftrightarrow f(a_i) \neq f(a_j)\ |\ i \neq j \leftrightarrow |f(D)| = |D|$

Assume $D, C_d$ are finite and $|D| = |C_d|$
$f$ is injective $\leftrightarrow f$ is bijective
Proof:
	Suppose $f$ is injective
	$|D| = |f(D)| \to |f(D)| = |C_d|$
	$f(D) \subseteq C_d \to f(D) = C_d$
	Therefore $f$ is surjective
	Therefore $f$ is bijective

The Pigeonhole Principle
	Suppose $D, C_d$ are finite
	$|C_d| < |D| \to \exists a, a' \in D, a \neq a'$ such that $f(a) = f(a')$
	Proof:
		$f(D) \subseteq C_d \land |C_d| < |D| \to |f(D)| < |D|$
		$f$ is not injective
		
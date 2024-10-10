Binary Operation (BO) $(*)$:
	Given a set $A$,
	 $*$ on $A$ is an operation to any two elements $x, y \in A$ that yields an element $(x*y) \in A$ 
	 $\forall x, y \in A, x*y \in A$

$\div$ on $\mathbb{R}$ is not a BO as $\exists x \in \mathbb{R}, \dfrac{x}{0}$ is undefined

A BO is commutative if $\forall x, y \in A, x *y = y*x$ 
A BO is associative if $\forall x, y, z \in A, (x*y)*z = x*(y*z)$

Semigroup $(A, *)$:
	A set endowed with an associative BO 

Generic Exponents
	$a^p = a * a^{p-1}$

General Associative Law
	Given $(A, *). \forall a_1, \dots, a_s \in A, a_1 * a_2 * \dots * a_s$ has the same value regardless of brackets

Identity Elements
	Given $(A, *)$. $e \in A$ is an identity element if $\forall x \in A, e*x = x*e = x$
	You cannot have more than one identity element as $e_1 * e_2$ cannot be equal to both
	0 for $(\mathbb{R}, +)$
	1 for $(\mathbb{R}, \times)$
	$\emptyset$ for $(P(A), \cup)$
	$A$ for $(P(A), \cap)$
	$I_n$ for $(M_n, *)$

Monoids
	A semigroup with an identity element
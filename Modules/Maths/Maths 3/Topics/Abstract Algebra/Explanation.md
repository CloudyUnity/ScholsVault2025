Binary Operation (BO) $(*)$:
	Given a set $A$,
	 $*$ on $A$ is an operation to any two elements $x, y \in A$ that yields an element $(x*y) \in A$ 
	 $\forall x, y \in A, x*y \in A$

All BOs are closed by definition 
$\div$ on $\mathbb{R}$ is not a BO as $\exists x \in \mathbb{R}, \dfrac{x}{0}$ is undefined

A BO is commutative if $\forall x, y \in A, x *y = y*x$ 
A BO is associative if $\forall x, y, z \in A, (x*y)*z = x*(y*z)$

Semigroup $(A, *)$
	A set endowed with an associative BO 

Generic Exponents
	$a^p = a * a^{p-1}$

General Associative Law
	Given $(A, *). \forall a_1, \dots, a_s \in A, a_1 * a_2 * \dots * a_s$ has the same value regardless of brackets

Identity Elements $(e)$ 
	Given $(A, *)$. $e \in A$ is an identity element if $\forall x \in A, e*x = x*e = x$
	You cannot have more than one identity element as $e_1 * e_2$ cannot be equal to both
	0 for $(\mathbb{R}, +)$
	1 for $(\mathbb{R}, \times)$
	$\emptyset$ for $(P(A), \cup)$
	$A$ for $(P(A), \cap)$
	$I_n$ for $(M_n, *)$

$a^0 = e$

Monoids
	A semigroup with an identity element $e$ 

Inverses
	$x$ is the inverse of $y$ $\leftrightarrow x * y = y*x = e$
	$a^{-n}$ where $n \geq 0 = (a^{n})^{-1}$	
	Any monoid with an invertible element $a \in A$ has a unique inverse 
		Proof:
			Assume $a$ has two inverses
			$a * b = b * a = a * c = c * a = e$
			$b \neq c$ 
			$b = b * e = b* (a * c) = (b * a) * c = e * c = c$
			Contradiction
	For any monoid with invertible elements $a, b \in A$, $a*b$ is also invertible and $(a*b)^{-1} = b^{-1} * a^{-1}$ 
		Proof:
			$(a*b) * (b^{-1} * a^{-1}) = a * (b * b^{-1}) * a^{-1} = a*e*a^{-1} = e$
			$(b^{-1} * a^{-1}) * (a*b) = b^{-1} * (a^{-1}  * a) * b = b^{-1} * e * b = e$
	For any monoid with elements $a,b,x \in A$ where $x$ is invertible, $a = b * x \leftrightarrow b = a * x^{-1}$
		Proof:
			$"\to"$ 
				Assume $a = b*x$ 
				$a * x^{-1}= (b*x) * x^{-1} = b$
			$"\leftarrow"$ 
				Assume $b = a * x^{-1}$ 
				$b * x = (a * x^{-1}) * x = a$

Group $(G)$
	A set of elements
	A closed associative BO
	An identity element
	Valid Inverses

Group/Monoid syntax is $(A, *, e)$

Groups are called Abelian if they're commutative 

Order $(|G|)$
	New name for cardinality just dropped

Subgroup $(H)$
	$H$ is a subgroup of $G \leftrightarrow H \leq G$ 
	$H \neq G \land H \leq G \to H < G$

Cayley Tables
	Imagine multiplication tables but generic
	Headers contain the elements
	Cells contain $Row_i * Col_j$ 
	If you start the headers with $e$ then the first row/column match their respective headers
	All cells containing $e$ show that $Row_i$ and $Col_j$ are inverses
	Every row and column should contain $e$ at least once as all elements have inverses
	Row/Columns cannot have duplicates
		Proof:
			If row $a$ has duplicate on col $x$ and $y$ where $x \neq y$ 
			$a * x = a* y$
			$x = y$
	All rows/columns must contain all elements, use sudoku to solve tables

Trivial Group
	$\{e\}$
	Is a subgroup of all other groups

Cyclic Group
	Given $(A, *, e), a \in A$
	$A' = \{a^m | m \in \mathbb{Z}\}$
	$(A', *, e)$ is a cyclic group and abelian regardless of whether $(A, *, e)$ is abelian

Homomorphism
	Let $(A, *), (B, \diamond)$ be semigroups
	$f: A \to B$ is a homomorphism iff $\forall x, y \in A, f(x * y) = f(x) \diamond f(y)$
	Example:
		$G = (\mathbb{R}, +, 0)$
		$H = (\mathbb{R}^+, \times, 1)$
		$f: G \to H, x \mapsto e^x$
		$f(x+y) = f(x) \times f(y)$
		$e^{x+y} = e^x \times e^y$

Isomorphic
	Two semigroups are isomorphic if you can map all elements from one to another where all products also maps correctly
	$\exists$ isomorphism $f: A \to B$ 
	Same Mary, different hat

Isomorphism
	A homomorphism which is bijective
	This shows the semigroups are identical in shape
	Example:
		$G := (\mathbb{R}^+, \times, 1)$
		$H := (\mathbb{R}, +, 0)$
		$f: G \to H, x \mapsto log(x)$
		$log(x \times y) = log(x) + log(y)$ 
		$log(x) = log(y) \to e^{log(x)} = e^{log(y)} \to x = y \to$ Injective
		$log(x) \in \mathbb{R} \to$ Surjective

The inverse of any isomorphism is also an isomorphism
Proof:
	$f: A \to B$ is bijective $\to f^{-1}: B \to A$ is bijective
	$\forall u, v \in B, \exists x, y \in A, \ \  x = f^{-1}(u) \land y = f^{-1}(v) \to \ \  u = f(x) \land v = f(y)$
	$f(x * y) = f(x) * f(y) = u * v$
	$f^{-1}(u * v) = x*y = f^{-1}(u) * f^{-1}(v)$ 

Rings

Vector Spaces
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

Identity Elements $(e)$ 
	Given $(A, *)$. $e \in A$ is an identity element if $\forall x \in A, e*x = x*e = x$
	You cannot have more than one identity element as $e_1 * e_2$ cannot be equal to both
	0 for $(\mathbb{R}, +)$
	1 for $(\mathbb{R}, \times)$
	$\emptyset$ for $(P(A), \cup)$
	$A$ for $(P(A), \cap)$
	$I_n$ for $(M_n, *)$

Monoids
	A semigroup with an identity element

Group $(G)$
	A set of elements
	A closed associative BO
	An identity element
	Valid Inverses

Order $(|G|)$
	New name for cardinality just dropped

Subgroup $(H)$
	$H$ is a subgroup of $G \leftrightarrow H \leq G$ 
	$H \neq G \land H \leq G \to H < G$

Cayley Tables
	Imagine multiplication tables but abstract
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
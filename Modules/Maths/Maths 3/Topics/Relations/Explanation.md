Relations are a way to abstract the idea of comparing elements together
Some examples of relations are $=, \equiv mod \ n, <, >, \sim, \to, \leftrightarrow, \subseteq$
	But you can make them whatever you want
Relations are functions that always return a boolean value, either they are related or not

We use Cartesian Products to define these relations

$R$ is equality $\to (xRy \leftrightarrow (x, y) \in \{(x, x) | x \in \mathbb{R}\}$

$R = \{(1, 1), (1, 5), (3, 2)\} \to 1R1, 1R5, 3R2$

A subset of $A \times B$ is a relation between $A$ and $B$
A subset of $A \times A$ is a relation on $A$

A relation is reflexive iff $\forall x \in A, xRx$
A relation is symmetric iff $\forall x, y \in A, xRy \to yRx$
A relation is transitive iff $\forall x, y, z \in A, xRy \land yRz \to xRz$
An equivalence relation is reflexive, symmetric and transitive 
	Often denoted with $\equiv$ or $\sim$ 

Partition
	A collection of disjoint non-empty sets such that their union is $A$

Equivalence Class $([x]_R)$
	Given an equivalence relation $R$ and $x \in A$
	$[x]_R = \{y \in A | xRy\}$
	The collection of all equivalence classes is called $A$ modulo $R$, denoted $A \backslash R$ 
	$\forall x \in A, \exists y \in A, x \in [y]$
	$xRy \leftrightarrow [x] = [y]$	
	Proof:		
		Let $y = x, x \in [x], xRy$
		$[y] = \{w \in A, yRw\}$
		$\forall w \in [y], yRw$
		$xRy \land yRw \to xRw \to w \in [x] \to [y] \subseteq [x]$
		$xRy \to yRx \to [x] \subseteq [y]$
		$xRy \to [x] = [y]$
	$\lnot (xRy) \leftrightarrow [x] \cap [y] = \emptyset$	
	Proof:
		Assume $[x] \cap [y] \neq \emptyset$
		$\exists z \in [x] \cap [y]$
		$z \in [x] \to xRz$
		$z \in [y] \to yRz$
		$xRz \land yRz \to xRy$
		Contradiction with $\lnot (xRy)$

Equivalence classes always partition a set in two

If $xRy \land yRx \to x = y$ then $R$ is anti-symmetric

A function can be symmetric and anti-symmetric for example:
	Equality 
	$R = \emptyset$
	$|R| = 1$

Partial Order
	A relation on $A$ that is reflexive, anti-symmetric and transitive
	Such as <, >, $\subseteq$ 
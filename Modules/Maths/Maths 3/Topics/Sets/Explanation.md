For basic set theory stuff see Maths 2 section

Show $Term_1 \cup Term_2 = Term_3$
	First show $Term_1 \cup Term_2 \subseteq Term_3$
		Show $\forall x, Term_1 \subseteq Term_3 \lor Term_2 \subseteq Term_3$
	Show $Term_3 \subseteq Term_1 \cup Term_2$

$\wp(\{\{\emptyset \}\}) = \{ \emptyset, \{\{\emptyset \}\} \}$

$(x_1, x_2) \in \mathbb{R}^2$ (Ordered Pair)

$A \times B = \{ (x, y) | x \in A \land y \in B \}$

$\#A = |A|$

Hilbert's Hotel:
	Given a hotel with infinite booked rooms you can accommodate an additional guest by moving guest $n$ to room $n+1$ 
	The hotel $H = \{x_1, x_2, \dots x_n \}$
	$f : H \to H$
		$f(x_n) = x_{n+1}$
		$f(H) = H\  \backslash \  \{x_1\}$
	$f$ is injective and not surjective 	

A set $A$ is finite iff $\forall f : A \to A$ an injective function is also bijective
Proof:
	Prove Forwards:
		If $A$ is finite it follows from corollary 1 that every injective function is bijective
	Prove Backwards:
		Contrapositive
		Suppose $A$ is infinite, therefore there is a non-bijective injective function
		Since $A$ is infinite there is a sequence $\{x_1, x_2, x_3, \dots \}$ of the elements of $A$ where each appears at most once
		There then exists a function $f : A \to A$ such that $f(x_n) = x_{n+1}$ for all integers $n \geq 1$ 
		$f(x) = x$ if $x$ is an element of $A$ not in the sequence
		If $x = x_n$ where $n > 1$ then the only element that maps to $x$ is $x_{n-1}$ 
		It follows that $f$ is injective 
		It cannot be surjective as no element of $A$ gets mapped to $x_1$ 
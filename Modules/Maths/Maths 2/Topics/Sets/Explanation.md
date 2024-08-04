A set in an unordered collection of elements

|S| defines the size/cardinality of a set S
Some sets are infinite ($\mathbb{R}$)
A is cardinal to B if |A| = |B|

Naïve Set Theory:
	Leads to a contradiction 
	Let $A = \{B | B \centernot\in B \}$
	$A \in A$ is a paradox

A set is normal/ordinary if it does not contain itself

ZFC Set Theory:
	Most widely used modern set theory
	Only allows normal sets among other axioms
	We use naïve set theory for this module

Local Universal Set $U$ contains everything under consideration
Empty Set $\emptyset$ = {}
	$\emptyset \neq \{\emptyset \}$
Sets can be elements of other sets

Describe sets either by enumerating over all values or define a formula to generate all elements of the set

Half Plane Set Formula:
	y > mx + c
Disc Set Formula:
	$x^2 + y^2 < 1$
Use solid/hollow dots and solid/broken lines for inclusion when graphing	

Normal/Ordinary sets do not contain themselves

Axiom of Choice:
	Given a set of non-empty sets $A$
	You should be able to come up with a rule that gets specific elements from $A$ even if the size is infinite
	In an infinite shoe shop you can select one shoe out of every pair by selecting the left shoe
	In an infinite sock shop you cannot select one sock out of every pair as they are identical

Subset:
	$A \subseteq B \leftrightarrow \forall x, (x \in A \to x \in B)$
	Prove by assuming $x \in A$ and showing $x \in B$
	Disprove by counter-example

Prove sets are equal:
	To show S = T
	Prove $S \subseteq T$
	Prove $T \subseteq S$

Proper Subsets:
	$A \subset B$ = $A \subseteq B \land A \neq B$

Sets are disjoint if $A \cap B = \emptyset$

Complement:
	$\overline{A} = A' = U \backslash A$
	$A' - B' = B - A$

DeMorgan:
	$\overline{(A \cup B)} = \overline{A} \cap \overline{B}$
	$\overline{(A \cap B)} = \overline{A} \cup \overline{B}$

Collections:
	A collection of sets is an object in the form:
	$\mathscr{A} = \{ A_a | a \in I \}$
		Where $A_a$ is a set and $I$ is the indexing set
		$I = \{1, 2, ..., n\}$
	$\bigcap_{a} A_a = \{x | \forall a \in I, x \in A_a\}$
	$\bigcup_{a} A_a = \{x | \exists a \in I, x \in A_a \}$

$B \cup (\bigcap_a A_a) = \bigcap_a (B \cup A_a)$
$B \cap (\bigcup_a A_a) = \bigcup_a (B \cap A_a)$

DeMorgan Collections:
	$\overline{(\bigcap A_a)} = \bigcup \overline{A_a}$
	$\overline{(\bigcup A_a)} = \bigcap \overline{A_a}$

The Cantor Set:
	$A_1 = [0, 1]$
	$A_2 = [0, \frac{1}{3}] \cup [\frac{2}{3}, 1]$
	$A_3 = [0, \frac{1}{9}] \cup [\frac{2}{9}, \frac{1}{3}] \cup [\frac{2}{3}, \frac{7}{9}] \cup [\frac{8}{9}, 1]$
	$C = \bigcap_{i \in \mathbb{N}^*} A_i$
	Cut the middle third of each segment each time

Tuples:
	An ordered collection of n elements
	($a_1, a_2, ..., a_n$)
	$a = b \leftrightarrow (a_1 = b_1) \land (a_2 = b_2) \land ... \land (a_n = b_n)$
	Cartesian Product:
		$|A| = |B| = 1$
		$A \times B = \{(a, b) | a \in A \land b \in B\}$
		$|A \times B| = |A| + |B|$
		Appends a tuple onto another

Karnaugh Maps / Veitch Diagram:
	Sets are disjoint IFF $A \cap B = \emptyset$
	$X \oplus Y = (X \cap \bar Y) \cup (\bar X \cap Y)$
	Example:
		Out of 100 students and 3 modules (A, B, C):
			3 failed all
				111=3
			9 failed B and C
				011=9-3=6			
			10 failed A and C
				101=10-3=7
			12 failed A and B
				110=12-3=9
			32 failed A
				100=32-3-7-8=13
			30 failed B
				010=30-3-6-9=12
			46 failed C
				001=46-3-6-7=30
			100-30-12-6-13-7-9-3=20
				000=20
		Write Karnaugh map where A = row 2, B = column 3-4, C = column 1-2
		Fill in table with info above
		Profit

Power Set:
	$\wp(A)$ is the power set of A
	$A = \{0, 1\} \to \wp(A) = \{\emptyset, \{0\}, \{1\}, \{0, 1\}\}$
	$A = \{0, 1, 2\} \to \wp(A) = \{\emptyset, \{0\}, \{1\}, \{2\}, \{0, 1\}, \{0, 2\}, \{1, 2\}, \{0, 1, 2\}\}|$
	$A = \emptyset \to \wp(A) = \{\emptyset\} \to \wp(\wp(A)) = \{\emptyset, \{\emptyset\}\}$	
	$|A| = n \to |\wp(A)| = 2^n$
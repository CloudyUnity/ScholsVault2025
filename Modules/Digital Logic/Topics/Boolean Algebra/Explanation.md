AND: $A \& B = A \cdot B = AB$
OR:   $A | B = A + B$
NOT: $\overline{A} = A' = \ !A = ¬A$ 
XOR: $A \land B = A \oplus B$

By manipulating boolean expressions it is sometimes possible to simplify the function and thus reduce the gate count

A&1 = A
A&0 = 0
A|1 = 1
A|0 = A

A&A = A
A|A = A
A&A' = 0
A|A' = 1
A'' = A

Associativity:
	A&B = B&A
	A|B = B|A
	ABC = (AB)C

Distributivity:
	A+B+C = (A+B)+C
	A(B+C) = AB+AC
	A+BC = (A+B)(A+C)

DeMorgan Transformations:
	AB = (A' + B')'
	A+B = (A'B')'
	A+1 = (A' & 0)'

AND has higher operator precedence than OR

Use DeMorgan to convert a circuit into cheaper gates (NAND), try and cancel NOTs

Duality Principle:
	Every algebraic expression deducible from the postulates of boolean algebra remains valid if operators and identity elements are interchanged
	AB + C $\to$ C'(A' + B')
	0 and 1 are dual pairs
	& and | are dual pairs

To solve problems first form the truth table and convert it to gates

Sum Problems:
	S(x, y) = $\sum (1, 2)$
	S = x'y + xy'
	S = x $\oplus$ y
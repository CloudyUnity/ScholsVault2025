Mathematical Logic is a tool for working with compound statements
Propositional Logic is the logic of compound statements built from boolean connectives
A proposition is a statement that's either true or false

Connectives:
	Operators combining operand expressions
	Unary: -5
	Binary: 4 + 5
	Propositional/Boolean: A $\to$ B
	Examples:
		¬ = NOT/Opposite
		$\land$ = AND
		$\lor$ = OR
		$\oplus$ = XOR
		$\to$ = Implies
		$\leftrightarrow$ = IFF

Predicate Logic is an extension of propositional logic that permits reasoning about classes of entities. It distinguishes the subject of a sentence from its predicate

Gödel's Incomplete Theorem:
	Given any finitely describable consistent proof procedure, there will always remain some true statements that will never be proven by that procedure

A subject is the noun performing the verb in a sentence
A predicate is the part of the sentence that provides info on the subject
	Has at least 1 free variable

Lowercase denotes objects/variables
Uppercase represents predicates/functions

Universe of Discourse (UD):
	The collection of values a variable can take

Quantifier:
	Notation for quantifying objects in a UD
	($\forall , \exists$)

For an implication $p \to q$
	Converse: $q \to p$
	Inverse: $¬p \to q$
	Contrapositive: $¬q \to ¬p$
		This one is always equivalent to the original
	$((p \to q) \land (q \to p)) \to (p \leftrightarrow q)$

Free Variable:
	An undefined variable such as in a predicate
Bound Variable:
	A variable found in a quantifier
Example:
	$\forall x, P(x, y)$ has 1 free and 1 bound

A statement not made from simpler ones is atomic/simple as opposed to compound
A Tautology/Law is a compound proposition that is always true
A contradiction is a compound proposition that is always false
Propositional Equivalence is when a tautology results due to a biconditional operator ($\leftrightarrow$) between two statements

Remember "Some" = $\exists$, "Only Some" = $\exists \land ¬\exists$

DeMorgan:
	¬$\exists$ = $\forall$
	¬$\forall$ = $\exists$

#bonus 
In probability propositions can have percentage values to represent more complex uncertainties 
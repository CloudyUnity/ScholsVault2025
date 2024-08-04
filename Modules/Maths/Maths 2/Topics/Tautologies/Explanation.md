A tautology is a compound proposition true no matter the truth values of its atomic propositions

A statement Q is a propositional consequence of statement(s) P IFF $P \to Q$ is a tautology

Proofs using tautologies
	Show hypotheses and conclusions
	Draw intermediate steps from hypotheses to conclusion using named tautologies and previous steps

Some Tautologies:
	Modus Ponens:
		$( P \land (P \to Q) ) \to Q$
	Modus Tollens:
		$(¬Q \land (P \to Q)) \to ¬P$
	
	$P \lor ¬P$
	$¬(P \land ¬P)$
	$¬¬P \leftrightarrow P$
	
	$(P \land Q) \to P$
	$(P \land Q) \to Q$
	$P \to (P \lor Q)$
	$Q \to (P \lor Q)$
	$Q \to (P \to Q)$
	$¬P \to (P \to Q)$
	
	$(¬P \land (P \lor Q)) \to Q$
	$P \to (Q \to (P \land Q))$
	$((P \to Q) \land (Q \to R)) \to (P \to R)$
	$(P \to Q) \to ((P \lor R) \to (Q \lor R))$
	$(P \to Q) \to ((P \land R) \to (Q \land R))$
	$((P \leftrightarrow Q) \land (Q \leftrightarrow E)) \to (P \leftrightarrow R)$
	
	$¬(P \land Q) \leftrightarrow (¬P \lor ¬Q)$
	$¬(P \lor Q) \leftrightarrow (¬P \land ¬Q)$
	$¬(P \to Q) \leftrightarrow (P \land ¬Q)$
	
	$(P \to Q) \leftrightarrow (¬P \lor Q)$
	$(P \leftrightarrow Q) \leftrightarrow ((P \to Q) \land (Q \to P))$
	$(P \leftrightarrow Q) \leftrightarrow ((P \land Q) \lor (¬Q \land ¬P))$
	
	$(P \to Q) \leftrightarrow (¬Q \to ¬P)$
	$((P \to Q) \land (P \to R)) \leftrightarrow (P \to (Q \land R))$
	$((P \to R) \land (Q \to R)) \leftrightarrow ((P \lor Q) \to R)$
	$(P \to (Q \to R)) \leftrightarrow ((P \land Q) \to R)$
	$(P \to (Q \land ¬Q) \leftrightarrow ¬P$
	$(P \land (Q \lor R)) \leftrightarrow ((P \land Q) \lor (P \land R))$
	$(P \lor (Q \land R)) \leftrightarrow ((P \lor Q) \land (P \lor R))$
	$(P \land Q) \leftrightarrow (Q \land P)$
	$(P \lor Q) \leftrightarrow (Q \lor P)$
	$(P \lor (Q \lor R)) \leftrightarrow ((P \lor Q) \lor R)$
	$(P \land (Q \land R)) \leftrightarrow ((P \land Q) \land R)$

Alternating Qualifiers:
	$\forall x > 0, P(x)$
		For all x is greater than 0, P(x) is true
	Qualifiers have higher operator precedence than all logical operators
	You can chain qualifiers together
		$\forall x \exists y, z \ \ P(x, y, z)$

A mathematical variable is a combination of symbols that stand for an unspecified number or object
Variables from the same UD are of the same sort
A symbol that stands for a fixed number or object is a constant
An expression representing a value or object is a term
$=, >, <$ are predicate symbols
$+, -, \times, \div, log, sin$ are functions/operators

A law of logic is a symbolic statement true for all possible interpretations of the variables
Logical connectives, quantifiers and the equal sign are not subject to re-interpretation
Every tautology is a law of logic but not the other way around

Universal formula with empty domain is always true
Existential formula with empty domain is always false

$\forall x < t P(x) \equiv \forall x, (x < t \to P(x))$
$\exists x < t P(x) \equiv \exists x, (x < t \land P(x))$

The Following Are Equivalent (TFAE):
	Statements proved in a circular fashion ($a \to b \to c \to d \to a$)

Uniqueness:
	$\exists x (P(x) \land \forall y (P(y) \to x = y))$	
	$\exists ! x P(x)$ means exactly 1 exists
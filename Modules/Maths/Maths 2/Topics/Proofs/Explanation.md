Definitions:
	Axiom:
		A statement accepted as true without proof
		Logical:
			Axioms based in propositional or predicate logic 
		Mathematical:
			Axioms based on properties of a mathematical object (e.g. real numbers, sets, etc)
	Inference Rule:
		A rule describing how a new statement can be asserted in a proof on the basis of its relationship to previous statements in the proof
	Axiomatic System:
		A list of axioms and inference rules		
	Formal Proof:
		A finite sequence of statements in which every statement is either an axiom, previously proven statement, definition or application of an inference rule	
	Theorem:
		A statement that can be proven formally 
	Proposition:
		A simple theorem
	Lemma:
		A theorem that's main use is to prove another theorem
	Corollary:
		A theorem easily proven from another theorem is a corollary to it

Tips:
	Use forward reasoning and/or reverse reasoning 
	Replace terms with their definitions
	Try random/special cases to get an intuition for the problem
	Attempt a simplified version of the problem to gain insight

Proof by Exhaustion:
	If a statement relates to a small finite set it can be proved or disproved by considering all elements in the set

Proof by Counter-Example:
	You can disprove a universal statement by finding an example

Proof by Contraposition:
	Some problems $p \to q$ are easier to solve as $¬q \to ¬p$

Proof involving IFF:
	To prove $p \leftrightarrow q$ you must prove $p \to q$ and $q \to p$

Proof by Contradiction:
	To prove $p$ assume $¬p$ is true and find a contradiction

Proof by Induction:
	Prove a statement $P(0)$ or $P(1)$ depending on the set
	Prove for any $n$ 
	Assume $P(n)$
	Prove $P(n + 1)$
		Prove $P(n) \to P(n + 1)$
	Examples:
		Series:
			$1 + 3 + 5 + \dots + (2n - 1) = n^2$
			$1 + 3 + 5 + \dots + (2n - 1) + (2(n+1) - 1) = (n+1)^2$
			$n^2 + (2n + 1) = n^2 + 2n + 1$
		Equality:
			TODO
		Division:
			TODO

Inference Rules:
	Propositional Consequence:
		Any statements that are propositional consequences of previous statements can be asserted
	Tautologies:
		A statement proven using a tautology can be asserted
	Conditional Proof:
		Assume $P$. If $Q$ can then be proven then $P \to Q$ can be asserted
		Assume ¬$P$. If ¬$Q$ can then be proven then $Q \to P$ can be asserted
	Proof by Contradiction:
		Assume ¬$P$ and prove any contradiction to prove $P$
	Substitution:
		If $P \leftrightarrow Q$ and $S(P)$ then $S(Q)$ can be asserted
	Conjunction Rule:
		$P$ and $Q$ allows us to conclude $P \land Q$	
	Universal Specification Axiom (US):
		If UD is not empty $\forall x, P(x) \to P(t)$ can be asserted
	Universal Generalization Axiom (UG):
		If $P(x)$ where x is a free variable then $\forall x, P(x)$ can be asserted
	Existential Specification Axiom (ES):
		If $\exists x, P(x)$ then $P(c)$ can be asserted where $c$ is a constant
	Existential Generalization Axiom (EG):
		$P(t) \to \exists x, P(x)$ where $t$ is in the domain of $x$

Proof $\sqrt 2$ is irrational:
	Use proof by contradiction
	Assume $\sqrt 2 = \dfrac{m}{n}$
	Assume $\dfrac{m}{n}$ is in its simplest form
	$n \sqrt 2 = m$
	$2 n^2 = m^2 \to m^2$ is even $\to$ m is even $\to m = 2k$
	$2n^2 = (2k)^2 = 4k^2$
	$n^2 = 2k^2 \to n$ is even $\to n$ is even $\to n = 2p$
	$\sqrt 2 = \dfrac{2k}{2p}$
	$\dfrac{m}{n}$ is not in its simplest form
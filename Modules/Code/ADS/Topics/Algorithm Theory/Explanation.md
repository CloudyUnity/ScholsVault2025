Brute-Force
	Typically takes $O(2^n)$
	Normally fucking dogshit

Desirable Scaling Property (Poly-Time)
	When the input size doubles, the algo should only slow down by a constant factor $C$
	These algos are "efficient"
	$C = aN^b$

Worst Case
	Running time guarantee for any input
	Some exponential algos are used widely in practice because worst-case instances are rare

Which problems can we solve in practise?
	Those with poly-time algos
	![[Pasted image 20240915215229.png]]

Oracle
	Computational model supplemented by hardware that solves instances of a problem in a single step

Reduction
	Poly-time problem $X$ reduces to problem $Y$ if arbitrary instances of $X$ can be solved using polynomial number of standard computational steps plus polynomial number of calls to an oracle for $Y$
	$X \leq pY$

$X \leq pY \neq Y \leq pX$

If $X \leq pY$ and $Y$ is poly-time then $X$ is poly-time
If $X \leq pY$ and $X$ is not poly-time then $Y$ is not poly-time

$(X \leq pY \land Y \leq pX) \leftrightarrow (X \equiv pY)$

Literal
	$x$
	$\overline x$

Clause
	Disjunction of literals
	$C_j = x_1 \lor \overline{x}_2 \lor x_3 \lor \dots$

Conjunctive Normal Form
	Propositional formula that is the conjunction of clauses
	$\Phi = C_1 \land C_2 \land C_3 \land \dots$

Satisfying Truth Assignment (SAT)
	#todo 

Pg 17 of final slides
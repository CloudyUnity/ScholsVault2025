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

Conjunctive Normal Form (CNF)
	Propositional formula that is the conjunction of clauses
	$\Phi = C_1 \land C_2 \land C_3 \land \dots$

SAT
	The first problem proven to be NP-Complete
	Given $\Phi$ does it have a satisfying truth assignment 

3-SAT
	SAT where each clause contains exactly 3 literals
	$\Phi = (\overline x_1 \lor x_2 \lor x_3) \land (x_1 \lor \overline  x_2 \lor x_3) \land (\overline  x_1 \lor x_2 \lor x_3)$

Ham-Cycle
	Given an undirected graph $G=(V, E)$
	Does there exist a cycle $\Upgamma$ that contains every vertex in $V$
	Dir-Ham-Cycle
		Given a digraph does there exist a directed cycle $\Upgamma$ that contains every vertex
		Dir-Ham-Cycle $\leq p$ Ham-Cycle
	Given a digraph $G$ construct a graph $G'$ with 3$n$ nodes
	Lemma
		$G$ has a directed ham cycle iff $G'$ has a ham cycle
		$G$ has $\Upgamma \to G'$ has $\Upgamma'$
		$G'$ has $\Upgamma' \to$
			$\Upgamma'$ must visit nodes in either $\dots, B, G, R, B, \dots$ or $\dots, B, R, G, B, \dots$
			Blue nodes in $\Upgamma'$ make up directed ham-cycle in $G$ or reverse of one

Dir-Ham-Cycle Reduction
	#todo 
		Simplify this once understand
	3-SAT $\leq p$ Dir-Ham-Cycle
	Given an instance of $\Phi$ we construct an instance of dir-ham-cycle with a ham-cycle iff $\Phi$ is satisfiable
	First create graph with $2^n$ ham-cycles which correspond to $2^n$ truth assignments
	Given $n$ variables and $k$ clauses
	Traverse path $i$ from left to right $\leftrightarrow$ set $x_i$ to true
	For each clause add a node and 6 edges
	![[{FD561060-09D0-42D6-854F-FFA9C7386A43}.png]]
	Suppose $\Phi$ has satisfying argument $x^*$
	Define ham-cycle as follows
		$x^*_i \to$ Traverse row $i$ left to right
		$\overline{x^*_i} \to$ Traverse row $i$ right to left
	For each clause there will be at least one row $i$ in which we are going in the correct direction to splice node into cycle
	Since $\Upgamma$ visits each clause node at least one path is traversed in correct direction and clause is satisfied

Longest Path Reduction
	3-SAT $\leq p$ Longest-Path
	Given a graph $G$ does there exist a simple path consisting of at least $k$ edges
	Proof 1:
		Redo proof for dir-ham-cycle ignoring back-edge from $t$ to $s$
	Proof 2:
		Show Ham-Cycle $\leq p$ Longest-Path

Traveling Salesperson Problem (TSP)
	Given a set of nodes and pairwise distance function $d(u, v)$
	$d(u, v) = (u, v) \in E\  ? \ 1 : 2$
	Is there a path that connects all nodes of length $\leq D$
	TSP $\leq p$ Ham-Cycle
	Reduction
		Given a undirected graph $G$ does there exist a cycle $\Upgamma$ that contains every node in $V$
		Create $n$ nodes with distance function
		TSP has tour of length $\leq n$ iff $G$ has a ham-cycle

Decision problems
	Problem $X$ is a set of strings
	Instance $s$ is one string
	Algo $A$ solves $X$ 
	$A(s) =$ solves $s$ iff $s \in X$
	$A$ runs in poly-time if $\forall s, A(s)$ terminates in at most $p(|s|)$ where $p()$ is some polynomial and $|s|$ is the length of $s$

Problems
	Is $x$ a multiple of $y$
		Division
	Are $x$ and $y$ relatively prime
		Euclid's
	Is $x$ prime
		AKS
	Is the edit distance between $x$ and $y$ less than 5
		Dynamic Programming
	Is there a vector $x$ that satisfies $Ax = b$
		Gaussian Elimination
	Is there a path between $x$ and $t$ in a graph $G$
		Depth-First Search

Certifier
	Checks a proposed proof $t$ that $s \in X$
	Algo $C(s, t)$ is a certifier for problem $X$ if $\forall s, s \in X$ iff exists string $t$ such that $C(s, t) =$ yes

Certificate
	A nontrivial factor $t$ of $s$
	A certificate exists iff $s$ is composite 
	$|t| \leq |s|$

Polynomial (P)
	Problems for which exists a poly-time algorithm

Nondeterministic Polynomial (NP)
	Set of problems for which exists a poly-time certifier 
	$|t| \leq p(|s|)$

Exponential Polynomial (EXP)
	Problems for which exists an exponential time algorithm

Composite
	Is a given integer $s$ composite 
	Certifier:
		Check that $1 < t < s$ and $s$ is a multiple of $t$
	Composites $\in$ NP

3-SAT $\in$ NP
P $\subseteq$ NP
NP $\subseteq$ EXP

Does P = NP?
	If so we have efficient algos for 3-SAT, TSP, 3-Color, Factor, etc
	If not we don't
	Consensus is probably no
	Other outcomes
		P = NP but only $\ohm(n^{100})$ for 3-SAT
		P $\neq$ NP but $O(n^{log^* \ N})$ for 3-SAT
		P = NP is independent

NP-Complete
	A problem $Y \in$ NP  with the property that for every problem $X \in$ NP, $X \leq pY$

$Y \in$ NP-Complete $\to (Y \in P \leftrightarrow$ P = NP$)$

Circuit-SAT
	Given a combinational circuit built from AND, OR and NOT gates, can you set the inputs such that the output is 1
	The first proven NP-Complete problem

3-SAT $\in$ NP-Complete 
Circuit-SAT $\leq p$ 3-SAT
Proof
	Create a 3-SAT variable for each circuit element
	Make circuit compute correct values at each node by adding clauses
	Hard code input and output values
	Turn clauses of length 1 or 2 into clauses of length 3
	#todo 
		Redo this section (pg 57 P=NP lecture)
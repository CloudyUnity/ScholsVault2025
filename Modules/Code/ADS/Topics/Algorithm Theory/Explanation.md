Brute-Force
	Typically takes $O(2^n)$
	Normally dogshit in practice 

Desirable Scaling Property (Polytime Algorithms)
	When the input size doubles, the algo should only slow down by a constant factor $C$
	These algos are "efficient"
	$C = aN^b, a > 0, b > 0$
	Goal is to have low constant factors. Some algos have 
	high constant factors and are useless in practise 
	These algorithms scale to huge problems 

Examples of polytime algos
	![[Pasted image 20240915215229.png]]

Worst Case
	Running time guarantee for any input
	Some exponential algos are used widely in practice because worst-case instances are rare	

Oracle
	Computational model supplemented by hardware that solves instances of a problem in a single step

Problem
	A question that needs answering. Not an algorithm! Solved by algorithms

Reduction ($X \leq_p Y$)
	Polytime problem $X$ reduces to problem $Y$ if:
		Arbitrary instances of $X$ can be solved using
		- Polynomial number of standard computational steps 
		- Polynomial number of calls to an oracle for $Y$	
	Instances of $Y$ must be of polynomial size 

$X \leq_p Y \neq Y \leq_p X$

$X \leq_p Y$ $\land$ $Y$ is polytime $\to X$ is polytime
$X \leq_p Y \land X$ is not polytime $\to Y$ is not polytime

$(X \leq_p Y \land Y \leq_p X) \leftrightarrow (X \equiv_p Y)$.
	$X \equiv_p Y \leftrightarrow (X$ is polytime $\leftrightarrow Y$ is polytime) 
# Algorithms Explained

## Satisfaction Problems

Literal
	A boolean variable or its negation $(x, \overline x)$ 

Clause
	Disjunction of literals
	$C_j = x_1 \lor \overline{x}_2 \lor x_3 \lor \dots$

Conjunctive Normal Form (CNF)
	Propositional formula that is the conjunction of clauses
	$\Phi = C_1 \land C_2 \land C_3 \land \dots$

Satisfiability (SAT)
	The first problem proven to be NP-Complete
	Problem:
		Given $\Phi$ does it have a satisfying truth assignment? 
		Aka are there values for $x_1, x_2, \dots x_n$ where $\Phi$ is true? 

3-SAT
	SAT where each clause contains exactly 3 literals
	Example:
		$\Phi = (\overline x_1 \lor x_2 \lor x_3) \land (x_1 \lor \overline  x_2 \lor x_3) \land (\overline  x_1 \lor x_2 \lor x_4)$

## Sequencing Problems

Ham-Cycle $(HC)$
	Problem:
		Given an undirected graph $G=(V, E)$	
		Does there exist a cycle $\Upgamma$ that contains every vertex in $V$
	Dir-Ham-Cycle $(DHC)$ 
		Given a digraph does there exist a directed cycle $\Upgamma$ that contains every vertex
		Dir-Ham-Cycle $\leq_p$ Ham-Cycle
	How To Reduce:
		Given a digraph $G$ construct a graph $G'$ with 3$n$ nodes
		![[{FE348C78-9BC9-4368-AAD5-1C88EA150774}.png]]
	Lemma
		$G$ has a DHC $\leftrightarrow$ $G'$ has a HC
		Proof:
			$G$ has $\Upgamma \to G'$ has $\Upgamma'$
			$G'$ has $\Upgamma' \to$
				$\Upgamma'$ must visit nodes in either $\dots, B, G, R, B, \dots$ or $\dots, B, R, G, B, \dots$
				Blue nodes in $\Upgamma'$ make up DHC in $G$ or reverse of one	

Dir-Ham-Cycle Reduction	
	3-SAT $\leq_p$ DHC
	Proof:
		Given an instance of $\Phi$ we construct an instance of DHC that has a HC $\leftrightarrow$ $\Phi$ is satisfiable
			$\Phi$ has $n$ variables and $k$ clauses
		First create graph $G$ with $2^n$ ham-cycles which correspond to $2^n$ truth assignments
			Traversing path $i$ from left to right sets variable $x_i$ to true
			Traversing path right to left sets as false 
		For each clause add a node and 6 edges
		![[{FD561060-09D0-42D6-854F-FFA9C7386A43}.png]]
		Proving $\Phi$ is satisfiable $\to G$ has a HC 
			Suppose $\Phi$ has satisfying argument $x^*$
			Define ham-cycle as follows
				$x^*_i \to$ Traverse row $i$ left to right
				$\overline{x^*_i} \to$ Traverse row $i$ right to left
			For each clause there will be at least one row $i$ in which we are going in the correct direction to splice clause node $C_j$ into cycle
			We splice in $C_j$ exactly once 
		Proving $G$ has a HC $\to \Phi$ is satisfiable 
			If $\Upgamma$ enters clause node $C_j$ it departs on mate edge
				Nodes before and after $C_j$ are connected with an edge
				Removing $C_j$ from cycle and replacing with an edge yields HC on $G \backslash C_j$ 
			$\therefore$ We have a HC $\Upgamma'$ in $G \backslash \{C_1, C_2, \dots, C_k\}$ 
			Set $x^*_i$ to true $\leftrightarrow \Upgamma'$ traverses row $i$ left to right
			Since $\Upgamma$ visits each clause node at least one path is traversed in correct direction and each clause is satisfied
	I don't really understand this one. Why does the graph not look different for each clause/variable?? 

Longest Path Reduction
	3-SAT $\leq_p$ Longest-Path
	Problem:
		Given a graph $G$ does there exist a simple path consisting of at least $k$ edges
	Proof 1:
		Redo proof for DHC ignoring back-edge from $t$ to $s$
	Proof 2:
		Show HC $\leq_p$ Longest-Path

Traveling Salesperson Problem (TSP)
	HC $\leq_p$ TSP
	Problem:
		Given a set of $n$ nodes and pairwise distance function $d(u, v)$		
		Is there a path that connects all nodes of length $\leq D$	
	Reduction Proof:
		Create distance function:
			$d(u, v) = (u, v) \in E\  ? \ 1 : 2$
		Given a undirected graph $G$ does there exist a cycle $\Upgamma$ that contains every node in $V$
		Create $n$ nodes with distance function
		TSP has tour of length $\leq n \leftrightarrow G$ has a HC

# P vs NP

Decision problems
	Problem $X$ is a set of strings
	Instance $s$ is one string
	Algo $A$ solves $X$ 
	$A(s) =$ true $\leftrightarrow s \in X$
	$A$ runs in polytime if $\forall s, A(s)$ terminates in at most $p(|s|)$ where $p()$ is some polynomial 

Certifier
	Checks a proposed proof $t$ that $s \in X$
	Algorithm $C(s, t)$ is a certifier for problem $X$ if 
		$\forall s, s \in X \leftrightarrow \exists$ certificate string $t$ such that $C(s, t) =$ true

Polynomial (P)
	Problems for which exists a polytime algorithm

Nondeterministic Polynomial (NP)
	Set of decision problems for which exists a polytime certifier 
	$t$ is polynomial size if
		$|t| \leq p(|s|)$ for some $p()$ 

Exponential Polynomial (EXP)
	Problems for which exists an exponential time algorithm
	These are brute force algorithms usually 

Composites
	Problem:
		$s \in \mathbb{Z}$
		Is $s$ composite?
	Certificate $t$ is a nontrivial factor of $s$ 
	$\exists t \leftrightarrow s$ is composite
	$|t| \leq |s|$ 
	Certifier:
		Check that $1 < t < s$
		Check that $s = tM$ 
	$\therefore$ Composites $\in NP$ 

3-SAT (with Certifiers)
	Given $\Phi$ is there a satisfying assignment 
	Certificate $t$ is an assignment of truth values to the $n$ variables
	Certifier:
		Check that each clause in $\Phi$ has at least one true literal 
	$\therefore$ 3-SAT $\in NP$ 

Problems & Algorithms
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

P $\subseteq$ NP
	$A(s)$ solves $X \in P$ 
	Certificate $t = \epsilon$ 
	Certifier $C(s, t) = A(s)$ 

NP $\subseteq$ EXP
	$C(s, t)$ exists for $X \in NP$ 
	To solve $s$, run $C(s, t)$ for all $t, |t| \leq p(|s|)$ 
	Return true if any certifiers return true

Does P = NP?
	If so we have efficient algos for 3-SAT, TSP, 3-Color, Factor, etc
	Consensus is probably no
	Other outcomes
		P = NP but only $\ohm(n^{100})$ for 3-SAT
		P $\neq$ NP but $O(n^{log^* \ N})$ for 3-SAT
		P = NP is independent of axiomatic set theory

NP-Complete (NPC)
	A problem $Y \in$ NP  with the property that for every problem $X \in$ NP, $X \leq_p Y$

$Y \in$ NPC $\to (Y \in P \leftrightarrow$ P = NP$)$

Circuit-SAT
	Given a combinational circuit built from AND, OR and NOT gates, can you set the inputs such that the output is 1
	The first proven NPC problem
	![[{94E511CF-A547-40F2-8E8F-EF70D79F1436}.png]]

3-SAT $\in$ NPC
Proof
	Circuit-SAT $\leq_p$ 3-SAT
	Goal:
		Given a circuit $K$ construct an instance $\Phi$ 
		$\Phi$ is satisfiable $\leftrightarrow K$ has a solution
	Create a variable $x_i$ for each circuit element $i$ 
	Make circuit compute correct values at each node
		$x_2 = \lnot x_3 \leftrightarrow (x_2 \lor x_3) \land (x_2' \lor x_3')$ 
		$x_1 = x_4 \lor x_5 \leftrightarrow (x_1 \lor x_4') \land (x_1 \lor x_5') \land (x_1' \lor x_4 \lor x_5)$ 
		$x_0 = x_1 \land x_2 \leftrightarrow (x_0' \lor x_1) \land (x_0' \lor x_2) \land (x_0 \lor x_1' \lor x_2)$ 
	Hard code input values
		$x_5 = 0 \leftrightarrow x_5'$ 
		$x_0 = 1 \leftrightarrow x_0$ 
	Make all clauses length 3
		Create $z_1, z_2, z_3, z_4$
		Create 8 clauses to force $z_1 = z_2 =$ false
		Add $z_1$ and $z_2$ to any clauses with less than 3 variables
Automaton
	Mathematical model of a computing device

Inputs cause automata to either stay in their current state or transition to another
The current state is one of the inputs

$S$ is the finite set of all possible states
$t$ is the transition mapping
	May or may not be a function
$a$ is the input datum 
$i \in S$ is the initial state
$s' = t(s, a)$

$F \subseteq S$ is the finishing states 

Finite State Acceptor $(S, A, i, t, F)$ 
	Returns true to input datum $w$ if $w \in L$ 
	A word $a_1 \dots a_n$ is accepted if:
		$\exists s_0, s_1, \dots, s_n \in S$
		$s_0 = i$, $s_n \in F$
		$s_k = t(s_{k-1}, a_k) \ \forall 1 \leq k \leq n$
	A language $L$ over $A$ is accepted if all words in $L$ are accepted 

Deterministic FSA (DFSA)
	Every state has exactly one transition for each possible input. $t$ is a function

Non-Deterministic FSA (NDFSA)
	An input can lead to multiple transitions due to multithreading or randomness. $t$ is not a function

There exists an algo to transform a NDFSA into a DFSA using power set construction

$L$ over $A$ is a regular language $\leftrightarrow$ $L$ is accepted by a DFSA with input $A$ $\leftrightarrow$ $L$ is accepted by a NDFSA with input $A$ 

Myhill-Nerode Theorem
	Let $x, y \in L$ over $A$ 
	$(\forall w \in A^*, x \circ w \in L \leftrightarrow y \circ w \in L) \to x \equiv_L y$ 
	$L/\equiv$ is the set of equivalence classes determined by the relation $\equiv_L$ 
	If $L/\equiv$ is infinite then $L$ is not a regular language 
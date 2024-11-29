 
Regular/Finite State Languages
	Languages which are recognized by a finite state acceptor
	Regular languages over $A$ constitute the smallest collection $C$ where
		$C \subseteq P(A^*)$ 
		$M \in C \to M^* \in C$ 
		$M \in C \land N \in C \to M \circ N \in C$ 
		$M \in C \land N \in C \to M \cup N \in C$ 
	$L$ is a regular language over $A$ iff $L = L_m$ for some finite sequence $L_1, L_2, \dots, L_m$ where
		$L_i$ is finite
		$\exists j, k, 1 \leq j,k < i$ s.t.
		$L_i = L_j ^*$ 
		$L_i = L_j \circ L_k$
		$L_i = L_j \cup L_k$ 
	Basically by taking the elements of $A$ can you get to $L$ by applying the above operations
	Example:
		$A = \{0, 1\}$
		$L = \{0^m 1^n | m,n \in \mathbb{N}, m \geq 0, n \geq 0\}$ 
		$L$ is a regular language over $A$ 
		Proof:
			$L_1 = \{0\}$
			$L_2 = \{1\}$
			$L_3 = L_1 ^*$
			$L_4 = L_2 ^*$
			$L = L_5 = L_3 \circ L_4$ 

Regular languages correspond to problems solvable with finite memory

$L', L''$ are regular languages $\to L' \cap L''$ is a regular language 
$L$ is a regular language $\to A^* \backslash L$ is a regular language

Regular Grammar (Left)
	A context-free grammar where every production rule is of one of the forms:
		1. $\langle A \rangle \to b \langle B \rangle$
		2. $\langle A \rangle \to b$
		3. $\langle A \rangle \to \epsilon$ 
	Where $\langle A \rangle, \langle B \rangle$ are nonterminals, $b$ is a terminal and $\epsilon$ is the empty word
	A regular grammar is in normal form if it only uses rule forms 1 and 3

Right Regular Grammar
	Production rule form 1 is instead:
		$\langle A \rangle \to \langle B \rangle b$ 

Regular Expressions (Regex)
	$\emptyset, \epsilon, a \in A$ are all regexes 
	$w, w'$ are regexes $\to w \circ w', w \cup w', w^*$ are regexes
	Regexes are single line strings which form a language
	Example:
		$L = \{011, 011011, 011011011, \dots\}$
		$L = (\{0\} \circ \{1\} \circ \{1\}) \circ ((\{0\} \circ \{1\} \circ \{1\}) \cup \epsilon) \circ \dots \circ ((\{0\} \circ \{1\} \circ \{1\}) \cup \epsilon)$

Operator Precedence 
	$* > \circ > \cup$ 
	$w_1 \circ w_2 \equiv w_1 w_2$ 

$A^*1A^* = \{ w \in A^* | w$ contains a $1\}$ 
$(AA)^* = \{ w \in A^* | w$ is a word of even length$\}$ 
$(A^*A^*)^* = A^*$ 

$L$ is regular $\leftrightarrow$ A regex describes $L$ 
Proof:
	Given the definition of a reg lan we can construct a regex that uses only union/concat/kleene
	Given a regex we can form a finite sequence of $L_i$s such that each is a finite set of words or obtained from previous $L_i$s via union/concat/kleene

$L$ is regular $\leftrightarrow L$ is accepted by a DFSA/NDFSA
$L$ is regular $\leftrightarrow L$ is produced by a regular grammar

How to determine whether $L$ is regular 
	Given $L \subset A^*$ 
	$L$ is finite $\to \exists$ FSA to accept $L \to L$ is regular
	$L = A^* \to L$ is regular
	Proof:
		$A = \{a_1, \dots, a_m\}$ 
		The FSA has just one state
		![[{48A29163-E3CC-4D8E-BAB8-F875C3EC6151}.png]]

The Pumping Lemma
	$L$ is infinite $\land \ L \neq A^*$ 
	The Myhill-Nerode theorem can get complicated so we use the pumping lemma
	$p =$ Pumping Length
	$w \in L \land |w| \geq p \to w = xuy$
		$\forall u, x, y$ s.t.
		$|u| > 0$
		$|xu| \leq p$
		$xu^n y \in L, \forall n \geq 0$ 
	Proof:
		If $L$ is regular then all its words can be pumped through a FSA that recognizes $L$
		Assume it's a DFSA with $p$ states
		$|w| = l \to$ DFSA processes $l$ pieces of info
			The DFSA passes through $l+1$ states
		$l \geq p \to$ DFSA passes through $l+1 \geq p+1$ states
		$\therefore$ A state is repeated among the first $p+1$ 
			States = $\{s_1, s_2, \dots, s_{l+1}\}$
			$l \geq p \to \exists i, j$ s.t. 
				$i < j \leq p+1$
				$s_i = s_j$ 		 
		$x$ is the part of $w$ that gets the DFSA through the first $i$ states
			$x = a_1 a_2 \dots a_{i-1}$
		$u$ is the part of $w$ that gets the DFSA through the $i+1$ to $j$ states
			$u = a_{i}a_{i+1} \dots a_{j-1}$ 
			$i < j \to |u| > 0$ 
		$y$ is the part of $w$ that gets the DFSA through the $j+1$ to $p+1$ states
			$y = a_j a_{j+1} \dots a_{l}$ 
			$j \leq p + 1$
			$j - 1 \leq p \land xu = a_1 a_2 \dots a_{j-1} \to |xu| \leq p$ 
		$s_i = s_j \to$ Beginning and end of $u$ the acceptor is in the same state
		$\therefore x u^n y$ is accepted $\forall n \geq 0$ 

Pumping Lemma Applications
	$P$ = $L$ is regular
	$Q$ = $\forall w \in L, |w| \geq p \to w = xuy$
	$P \to Q$ 
	We can use the contrapositive to find non-regular languages
	$\lnot Q \to \lnot P$ 
	Example:
		$L = \{0^m 1^m | m \in \mathbb{N}, m \geq 0\}$
		$w = 0^m 1^m = xu^ny$
		$x \in 0^*$
		$y = 0^s 1^m$
		Let $u \in 0^*$			
			$n \geq 2 \to xu^n y \notin L$ as there are more 0s than 1s
		Let $u \in 1^*$
			Same contradiction, more 1s than 0s
		Let $u \in 0^*1^*$
			$xu^2y \notin L$ for any $x, y$ 
		$\therefore L$ is irregular
	Example:
		$L = \{0^m | m$ is prime$\}$ 
		$w = 0^m = xu^ny$
		$x = 0^i, u=0^j, y=0^k$
		$i + nj + k$ is prime $\forall n \geq 0$ 
		This is impossible
		$\therefore L$ is irregular
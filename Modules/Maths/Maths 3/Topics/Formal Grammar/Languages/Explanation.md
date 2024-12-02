Alphabet
	A finite set

Letters
	Elements of an alphabet

Word
	$a_1, a_2, \dots, a_n | a_i \in A$ 
	$A^n$ is the set of all words of length $n$ over $A$ 

Words are a 1-1 correspondence with $n$-ordered tuples $A \times \dots \times A$ 

$A^p$
	Set of all words of length $p$ over alphabet $A$ 

$A^+$
	$\overset{\infty}{\underset{n=1}{\bigcup}} A^n$
	Set of all words of positive length over alphabet $A$ 

$A = \{0, 1\} \to A^+ = \{0, 1, 00, 01, 10, 11, \dots \}$ 

The Empty String
	$\epsilon = \{\}$ 
	$A^0 = \{\epsilon\}$	

$\emptyset$ is the language that does not contain any strings
	$A^0 = \{\}$ 

Kleene Star $(*)$
	$A^* = \epsilon \cup A^+$ 

$\epsilon^* = \emptyset^* = \{\epsilon\}$ 

$w_1 \circ w_2$ is the concatenation of words
	$|w_1 \circ w_2 | = |w_1| + |w_2|$ 
	Associative and not commutative 
	$\epsilon$ is the identity for $(A^*, \circ)$ 
	$A = \{x, y\}, B = \{a, b\} \to A \circ B = \{xa, xb, ya, yb\}$ 

Language
	A language $L$ over $A$ is a subset of $A^*$ 

Formal Language
	A language where there exists a set of rules of algorithms that generates exactly $L$ 
	$(L, \cup), (L, \cap), (L, \circ)$ are closed
	$L_1 \circ L_2 = \{ w_1 \circ w_2 \in A^* | w_1 \in L_1 \land w_2 \in L2 \}$ 

$L^n$
	$L^n = L \circ L^{n-1}$
	All the possible combinations of $n$ words

Formal Grammar:
	Set of production rules for strings in a language 
	To generate a language you need a alphabet, start symbol $\langle s\rangle$ and a set of production rules 
	$V$ is the set of terminals and non-terminals 
	$A$ is the set of terminals 
	$P$ is the set of production rules
	Terminal elements are those that also exist in the alphabet		
	Non-Terminals:
		$\langle T \rangle$ $\in V \backslash A$ 

Production rules have the form:
	$\langle T\rangle \to w$ 
	$w \in V^*$ 
	$(\langle T\rangle , w) \in (V\backslash A) \times V^*$ 

Example: 
	$A = \{0, 1\}$ 
	$\langle s\rangle \to 01$
	$\langle s\rangle  \to 0 \langle s \rangle 1$ 
	$L = \{01, 0011, 000111, \dots \}$ 
	
Context-Free Grammar $(V, A, \langle s \rangle , P)$ 
	You can replace any instance of $\langle T \rangle$ with $w$ if $\langle T \rangle \to w$ 
	$P \subset (V \backslash A) \times V^*$ 
	Generates context-free languages 

Context-Sensitive Grammar
	Only certain replacements are allowed, governed by the syntax of $L$ 

Ambiguous Grammars
	Grammars that generate the same string in multiple ways 
	Unambiguous grammars are better for computers 

Direct Yields $(\Rightarrow)$ 
	$w'$ directly yields $w''$ $\leftrightarrow$ $w''$ can be gotten from $w'$ by applying a single production rule
	$w', w'' \in V^*$ 
	$\exists u, v \in V^* \land \exists (\langle T \rangle \to w)$ s.t  $w' = u \langle T \rangle v \land w'' = uwv \to w'$ yields $w''$ 
	Denoted by $w' \Rightarrow w''$ 

Yields $(\overset{*}{\Rightarrow})$ 
	$w'$ yields $w''$ $\leftrightarrow$ $w''$ can be gotten from $w'$ by applying zero or more production rules
	$w' = w'' \lor \exists w_0, w_1, \dots, w_n \in V^* s.t w_0 \Rightarrow w_1 \Rightarrow \dots \Rightarrow w_{n}$
	Denoted by $w' \overset{*}{\Rightarrow} w''$ 

Phase Structure Grammar 
	Also called Type 0 Grammars 
	Production rules may have more than one nonterminal
	$r \to w$ 
	$L = \{w \in A^* | \langle s \rangle \overset{*}{\Rightarrow} w\}$ 
	Example:
		$A = \{0, 1\}$ 
		$V \backslash A = \{\langle s \rangle, \langle N \rangle, \langle D \rangle \}$ 
		$0 \langle s \rangle 0 \langle s  \rangle 0 \to 00010$
		$\langle s \rangle \to \langle N \rangle \langle D \rangle$
		$\langle N \rangle \to$ "Mice" 
		$\langle D \rangle \to$ "Died" 

#bonus 
Recursive Language
	A language where there exists a turing machine halts on every input and either accepts or rejects. Boolean output 

#bonus 
Recursively Enumerable Language
	A language where there exists a turing machine that either accepts or rejects/runs forever on every input
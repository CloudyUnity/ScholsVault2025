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

$\epsilon = \{\}$ 

$A^* = \epsilon \cup A^+$ 

$w_1 \circ w_2$ is the concatenation of words
	$|w_1 \circ w_2 | = |w_1| + |w_2|$ 
	Associative and not commutative 
	$\epsilon$ is the identity for $(A^*, \circ)$ 

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
	To generate a language you need a alphabet, start symbol $<s>$ and a set of production rules 
	$V$ is the set of terminals and non-terminals 
	$A$ is the set of terminals 
	$P$ is the set of production rules
	Terminal elements are those that also exist in the alphabet		
	Non-Terminals:
		$<T>$ $\in V \backslash A$ 

Production rules have the form:
	$<T> \to w$ 
	$w \in V^*$ 
	$(<T>, w) \in (V\backslash A) \times V^*$ 

Example: 
	$A = \{0, 1\}$ 
	$<s> \to 01$
	$<s> \to 0<s>1$ 
	$L = \{01, 0011, 000111, \dots \}$ 
	
Context-Free Grammar $(V, A, <s>, P)$ 
	You can replace any instance of $<T>$ with $w$ if $<T> \to w$ 

Context-Sensitive Grammar
	Only certain replacements are allowed, governed by the syntax of $L$ 

Ambiguous Grammars
	Grammars that generate the same string in multiple ways 
	Unambiguous grammars are better for computers 

Direct Yields
	$w', w'' \in V^*$ 
	$\exists u, v \in V^* \land \exists (<T> \to w)$ s.t  
	$w' = u <T> v \land w'' = uwv \to w'$ yields $w''$ 
	Denoted by $w' \Rightarrow w''$ 
	#todo 
		I DONT GET THIS

Yields
	$w' = w'' \lor \exists w_0, w_1, \dots, w_n \in V^* s.t w_0 \Rightarrow w_1 \Rightarrow \dots \Rightarrow w_{n}$
	Denoted by $w' \overset{*}{\Rightarrow} w''$ 
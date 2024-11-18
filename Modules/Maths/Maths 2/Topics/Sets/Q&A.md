
> [!question]- #schols  ![[Pasted image 20240805115154.png]]
 $A \backslash B = A \cap B'$ 
 $A \backslash (B \backslash C) = A \backslash (B \cap C')$ 
 $(A \backslash B) \cup (A \backslash C')$ 
 $(A \backslash B) \cup (A \cap C)$ 

#todo
Make strict by proving it's subset not subseteq 
> [!question]- #schols  ![[Pasted image 20240805115443.png]]
 Prove forwards:
 Assume $S \subset T$, prove $P(S) \subset P(T)$ 
 $X \subseteq S \to X \in P(S)$ 
 $X \subseteq S \to X \subset T$ 
 $X \subset T \to X \in P(T)$ 
 $\forall X \subseteq S, X \in P(S) \land X \in P(T) \to P(S) \subset P(T)$ 
 Prove backwards:
 Assume $P(S) \subset P(T)$, prove $S \subset T$ 
 $X \in P(S) \to X \subseteq S$ 
 $X \in P(S) \to X \in P(T)$ 
 $X \in P(T) \to X \subset T$ 
 $\forall X \in P(S), X \subseteq S \land X \subset T \to S \subset T$ 

> [!question]- #schols  ![[Pasted image 20240805115742.png]]
 $A = [-2, 2]$ 
 $B = [0, 3]$ 
 $A \cap B = [0, 2]$
 $A \cup B = [-2, 3]$ 
 (i)
 $X \oplus Y = (X \cup Y) \cap (X \cap Y)'$
 $A \oplus B = [-2, 3] \cap [0, 2]'$ 
 $A \oplus B = \{n \in \mathbb{Z} | -2 \leq n < 0 \lor 2 < n \leq 3\}$
 (ii)
 $X \sim Y = (X \cap Y) \cup (X \cup Y)'$ 
 $A \sim Y = [0, 2] \cup [-2, 3]'$
 $A \sim Y = \{n \in \mathbb{Z} | n < -2 \lor n > 3 \lor 0 \leq n \leq 2\}$ 

> [!question]- #schols  ![[Pasted image 20240805120116.png]]
 Prove forwards:
 $\forall x \in B$ 
 $(B \subseteq A) \land x \in B \to x \in A$ 
 $x \in B \land x \in A \to x \in (A \cap B)$ 
 Proved that all elements of $B$ are also in $A \cap B$ 
 $x \in B \to x \notin A \backslash B$ 
 $x \in B \land x \in (A \cap B) \land x \notin A \backslash B \to A \cap B = B$ 
 $B \subseteq A \to A \cap B = B$ 
 Prove backwards:
 $\forall x \in B$
 $x \in B \land x \in A \cap B$
 $x \in A \cap B \to x \in A$ 
 $A \cap B = B \to x \notin A \backslash B$ 
 All elements of $B$ are in $A$ and not $A\backslash B$ thus $B \subseteq A$ 

> [!question]- #schols  ![[Pasted image 20240805120255.png]]
 (a)
 (i)
 $A \times B = \emptyset$ 
 If $m=0$ then the elements in $B$ have no elements to pair with from $A$
 If $n=0$ then the elements in $A$ have no elements to pair with from $B$ 
 (ii)
 Base Case:
 $m = 1, n = 1$
 $A_1 = \{a_1\}$
 $B_1 = \{b_1\}$ 
 $A_1 \times B_1 = \{(a_1, b_1)\}$
 $|A_1 \times B_1| = 1 = mn$ 
 .
 Assume true for $m=k, n=p$
 $A_k = \{a_1, a_2, a_3, \dots, a_k\}$
 $B_p = \{b_1, b_2, b_3, \dots, b_p\}$
 $A_k \times B_p = \{(a_1, b_1), (a_1, b_2), \dots, (a_1, b_p), (a_2, b_1), (a_2, b_2), \dots, (a_2, b_p), \dots, (a_k, b_p)\}$
 $|A_k \times B_p| = kp$ 
 .
 Prove for $m=k+1, n=p$
 $A_{k+1} = \{a_1, a_2, a_3, \dots, a_k, a_{k+1}\}$
 $B_p = \{b_1, b_2, b_3, \dots, b_p\}$
 $A_{k+1} \times B_p = \{(a_1, b_1), (a_1, b_2), \dots, (a_1, b_p), (a_2, b_1), (a_2, b_2), \dots, (a_2, b_p), \dots, (a_k, b_p), (a_{k+1}, b_1), (a_{k+1}, b_2), \dots, (a_{k+1}, b_p)\}$
 $A_{k+1} \times B_p = A_k \times B_p \cup \{(a_{k+1}, b_1), (a_{k+1}, b_2), \dots, (a_{k+1}, b_p)\}$ 
 $A_{k+1} \times B_p \backslash A_k \times B_p = \{(a_{k+1}, b_1), (a_{k+1}, b_2), \dots, (a_{k+1}, b_p)\}$ 
 $|A_{k+1} \times B_p \backslash A_k \times B_p| = p$ 
 $|A_{k+1} \times B_p| = |A_k \times B_p| + |A_{k+1} \times B_p \backslash A_k \times B_p| = kp + p = (k+1)p$ 
 $|A_{k+1} \times B_p| = mn$ 
.
 Prove for $m=k, n=p+1$
 As $m$ and $n$ are interchangeable the proof is the same
 (b)
 (i)
 Prove forwards
 Let $x \in P(A \cap B)$, prove $x \in P(A) \cap P(B)$ 
 $x \subseteq A \cap B$ 
 $x \subseteq A \land x \subseteq B$ 
 $x \in P(A) \land x \in P(B)$ 
 $x \in P(A) \cap P(B)$ 
 Prove backwards
 Let $x \in P(A) \cap P(B)$, prove $x \in P(A \cap B)$ 
 $x \in P(A) \land x \in P(B)$
 $x \subseteq A \land x \subseteq B$ 
 $x \subseteq A \cap B$ 
 $x \in P(A \cap B)$ 
 (ii)
 Yes
 $P(A \cap B) = P(A) \cap P(B)$
 LHS: $P(P(A \cap B))$
 RHS: $P(P(A) \cap P(B))$
 RHS: $P(P(A \cap B))$
 LHS = RHS
 
> [!question]- #schols ![[Pasted image 20240805120442.png]]
 (i)
 $A - B = A \cap B'$ 
 $x \in A \cap B'$ 
 $x \in A \land x \notin B$ 
 $\exists x \to A \nsubseteq B$ 
 $A - B = \emptyset \to \nexists x \to A \subseteq B$ 
 (ii)
 Contrapositive:
 $|A| \neq 0 \lor |B| \neq 0 \to A \cup B \neq \emptyset$ 
 $|A| \neq 0 \to \exists a \in A \to |A \cup B| \neq 0 \to A \cup B \neq \emptyset$ 
 $|B| \neq 0 \to \exists b \in B \to |A \cup B| \neq 0 \to A \cup B \neq \emptyset$ 

> [!question]- #schols  ![[Pasted image 20240805120456.png]]
 (i)
 $(\emptyset - B) \cup (B - \emptyset)$
 $\emptyset - B = \emptyset$
 $B - \emptyset = B$
 $\emptyset \cup B = B$ 
 .
 $(A - A) \cup (A - A)$
 $A - A = \emptyset$ 
 $\emptyset \cup \emptyset = \emptyset$ 
 .
 $(A - B) \cup (B - A) = \emptyset$
 $A - B = \emptyset$
 $B - A = \emptyset$ 
 $A - B = B - A$ 
 $B \cup (A - B) = B \cup (B - A)$
 $A = B- A$
 $A \cup A = A \cup (B - A)$
 $A = B$ 
 (ii)
Easiest with diagram
 Show $B \oplus C, A \oplus B, A \oplus (B \oplus C), (A \oplus B) \oplus C$ 
 (iii)
 $(A - B) \cup (B - A) = (A - C) \cup (C - A)$
 $A \cup (A - B) \cup (B - A) = A \cup (A - C) \cup (C - A)$
 $(A - B) \cup B = (A - C) \cup C$ 
 $A \cup B = A \cup C$ 
 $(A \cup B) \backslash A = (A \cup C) \backslash A$ 
$B = C$ 

> [!question]- #scholc ![[Pasted image 20240805120833.png]]
 (i)
 Use a kmap, it's like sudoku 
 AB / C
 $\begin{array}{|c| c| c| c| c|} \hline & 00 & 01 & 10 & 11 \\ \hline 0 & 0 & 8 & 7 & 4 \\ \hline 1 & 5 & 1 & 2 & 3 \\ \hline \end{array}$ 
 $7$ want to take only athletics 
 (ii)
 I'll prove by induction
 Base Case:
 $n =1$
 $S_1 = \{s\}$
 $P(S_1) = \{\emptyset, \{s\}\}$ 
 $|P(S_1)| = 2 = 2^1 = 2^n$ 
 .
 Assume true for $n=k$
 $S_k = \{s_1, s_2, s_3, \dots, s_k\}$
 $|P(S_k)| = 2^k$
  .
 Prove for $n = k+1$ 
 $S_{k+1} = \{s_1, s_2, s_3, \dots, s_k, s_{k+1}\}$ 
 $\forall q \in P(S_k), q \cup \{s_{k+1}\} \in P(S_{k+1})$ 
 This will double the size of $P(S_k)$ 
$|P(S_{k+1})| = 2 |P(S_k)| = 2 \times 2^k = 2^{k+1}$ 

#schols #bonus 
![[Pasted image 20240805120346.png]]

#schols #bonus 
![[Pasted image 20240805120647.png]]
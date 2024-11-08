
![[{5902FCF1-41BD-45C9-BF08-60155E2BB6A5}.png]]

> [!question]- #schols  ![[Pasted image 20240805115758.png]]
 $\begin{array}{| c | c | c | c | c |} \hline P & Q & P \to Q & (P \to Q) \to P & ((P \to Q) \to P) \to P \\ \hline F & F & T & F & T \\ F & T & T & F & T \\ T & F & F & T & T \\ T & T & T & T & T \\ \hline \end{array}$

#NeedsFactCheckingByTrueAmericanPatriots 
> [!question]- #schols  ![[Pasted image 20240805115318.png]]
 $2n + 7 = p$
 $n = \dfrac{p - 7}{2}$ 
 $p = 2 \to n = -2.5$
 Proven false by counter example

> [!question]- #schols  ![[Pasted image 20240805115539.png]]
 $UD =$ Students
 $C(x) = x$ completed the exam in under two hours
 $s =$ Sebastian
 Hypotheses:
 $s \in UD$ 
 $\forall x, C(x)$ 
 Conclusion:
 $C(s)$ 
 Workings:
 $(s \in UD \land \forall x, C(x)) \to C(s)$ (Universal Specification Axiom)
 $C(s)$ 

> [!question]- #schols  ![[Pasted image 20240805115611.png]]
 $(p \lor q \to p \land q) \equiv (p \equiv q)$
 Prove forwards:
 $p \lor q \to p \land q$      (Hypothesis)
 $p \land q \equiv p$      (TX)
 $p \lor q \to p$     (Substitution on 1 from 2)
 $p \land q \equiv q$     (TX)
 $p \lor q \to q$     (Substitution on 1 from 4)
 $(p \lor q \to p) \land (p \lor q \to q)$    (3 + 5)
  $p \lor q \equiv \lnot(\lnot p \land \lnot q)$      (DeMorgan)
$(\lnot(\lnot p \land \lnot q) \to p) \land (\lnot(\lnot p \land \lnot q) \to q)$      (Substitution on 6 from 7)
 $(\lnot p \to \lnot p \land \lnot q) \land (\lnot q \to \lnot p \land \lnot q)$            (Contrapositive)
 $(\lnot p \to \lnot p) \land (\lnot p \to \lnot q) \land (\lnot q \to \lnot p) \land (\lnot q \to \lnot q)$      (TX)
 $(\lnot p \to \lnot q) \land (\lnot q \to \lnot p)$       (TX)
 $(q \to p) \land (p \to q)$              (Contrapositive)
 $p \equiv q$         (TX)
 $\therefore (p \lor q \to p \land q) \to (p \equiv q)$
 .
 Prove backwards:
 $p \equiv q$   (Hypothesis)
 $p \equiv p \lor p$     (TX)
 $p \lor p \equiv q$   (Substitution on 1 from 2) 
 $q \equiv q \land q$     (TX)
 $p \lor p \equiv q \land q$   (Substitution on 4 from 3)  
 $p \lor q \equiv p \land q$   (Substitution on 5 from 1) 
 $p \lor q \to p \land q$  (Conclusion)
 $\therefore (p \equiv q) \to (p \lor q \to p \land q)$
 .
 $\therefore (p \lor q \to p \land q) \equiv (p \equiv q)$ 

> [!question]- #schols  ![[Pasted image 20240805115626.png]]
 $p \oplus q \to \lnot p \lor \lnot q$
 $(p \land \lnot q) \lor (\lnot p \land q) \to \lnot p \lor \lnot q$ 
 $(p \land \lnot q) \to \lnot q$
 $(\lnot p \land q) \to \lnot p$
 $\lnot q \lor \lnot p \to \lnot p \lor \lnot q$
 $\lnot p \lor \lnot q \to \lnot p \lor \lnot q$

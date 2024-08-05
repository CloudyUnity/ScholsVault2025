Pre-requisite Knowledge:
	Maths 2 Sets: [[Trinity/Schols/Modules/Maths/Maths 2/Topics/Sets/Explanation|Explanation]]

Probability is the study of randomness
It's a value in the range `[0, 1]` to measure the degree on uncertainty associated with the realisation of the event
0 is impossible
1 is certain

$Pr(E) \approx \tilde{f}_E$

Sample Space ($\ohm$):
	A defined set of 2 or more outcomes

Experiment:
	An experiment is a procedure which can be replicated an infinite number of times with a sample space

Deterministic:
	An experiment with only 1 outcome

Trial:
	Repetitions of the same experiment 

Event ($E$):
	A set of outcomes from an experiment with corresponding probability values $Pr(E)$
	An event with 1 outcome is elementary, otherwise compound

#NeedsFactCheckingByTrueAmericanPatriots 
Set of all subsets in $\ohm$:
	$\mathcal{E} = \{\emptyset, E_1, \dots, E_R \} = \wp(\ohm)$
	All possible variations on all combinations of the events

Complement:
	$\bar{E}$ = $E$ does not happen
	$Pr(\bar E) = 1 - Pr(E)$

$E_1 \cup E_2$ = Either happens
$E_1 \cap E_2$ = Both happen
$Pr(\ohm) = 1$

$Pr(A \cup B) = Pr(A) + Pr(B) - Pr(A \cap B)$

Mutually Exclusive:
	$E_1 \cap E_2 = \emptyset \to$ Incompatible/Mutually Exclusive
	Two events that cannot happen together
	$Pr(A \cap B) = 0$

Conditional Probability:
	Event B is conditional on event A
	What is $Pr(B | A)$
		Probability of B given A
	$Pr(B|A) = \dfrac{Pr(A \cap B)}{Pr(A)}$
	This is the chance of getting A and B, ignoring the chance it took to get A
	Note:
		$Pr(A) = 0 \to Pr(B|A) = 0$

Independence:
	Two events are independent if one has no effect on the other
	$Pr(B | A) = Pr(B)$

Bayes Theorem:
	$Pr(B_i|A) = \dfrac{Pr(B_i) Pr(A|B_i)}{\sum Pr(B_i)Pr(A|B_i)}$
	Example:
		Given $Pr(A), Pr(B|\bar A), Pr(\bar B | A)$
		Find $Pr(A|B)$
		Solution:
		$Pr(\bar B | \bar A) = 1 - Pr(B | \bar A)$
		$Pr(B | A) = 1 - Pr(\bar B | A)$
		$Pr(A|B) = \dfrac{Pr(A)Pr(B|A)}{Pr(A)Pr(B|A) + Pr(\bar A)Pr(B|\bar A)}$
		
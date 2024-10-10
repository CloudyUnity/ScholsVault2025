Strong Induction
	Where you assume not just $P(n)$ but $P(1), P(2), \dots, P(n)$
	For example:
		Proving the fundamental theorem of arithmetic $(\forall n \in \mathbb{N}, n \geq 2, n$ can be expressed as a product of two prime numbers$)$ 

Abusing Induction
	All horses are the same color
		$P(1):$ One horse, one color
		Assume $P(n)$ horses are the same color
		Consider a group of $n+1$ horses. If you exclude the first horse we have $n$ horses thus they are the same color. If you exclude the last horse we have $n$ horses thus they are all the same color. Thus the first, middle and last horses are the same color
		Fails due to $P(2)$ being false, there are no middle horses
	The Hilbert Hotel Cigar Mystery
		No cigars may be taken into the hotel
		Guest in room $n$ goes to room $n+1$ to get $n$ cigars and smoke one
		This fails due to no base case

Given $(A, *)$. $\forall a \in A, a^m * a^n = a^{m+n}, \forall m, n \in \mathbb{N}^*$
	$m=1$
		$a^1 * a^n = a*a^n = a^{1 + n}$
	Assume true for $m=p$
		$a^p * a^n = a^{p+n}$
	Prove 
		$a^{p+1} * a^n = (a*a^p)*a^n = a*(a^p*a^n) = a*a^{p+n} = a^{p+n+1}$

Given $(A, *)$. $\forall a \in A, (a^m)^n = a^{mn}, \forall m, n \in \mathbb{N}^*$
	$n=1$
		$(a^m)^1 = a^m = a^{m(1)}$
	Assume true for $n=p$
		$(a^m)^p = a^{mp}$
	Prove
		$(a^m)^{p+1} = (a^m)^p * a^m = a^{mp + m} = a^{m(p+1)}$
		
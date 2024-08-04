Two numbers are congruent modulo n if they have the same remainder on division by n
	$a \equiv b$ (mod n)
	$(a-b)|n$

Congruence/Residue Class:
	A set of numbers congruent to each other modulo n

Least Residue:
	Smallest positive member of a residue class

Modular Arithmetic:
	$a \equiv b \to a + k \equiv b + k$ (mod n) 
	$a \equiv b \to ak \equiv bk$ (mod n)
	$a \equiv b \to a^n \equiv b^n$ (mod n)

Multiplicative Inverse:
	The inverse for a number a is the number v where $av \equiv 1$ (mod n)
	a and n must be co-prime
	Finding the inverse:
		Get Bezouts Identity ($d = a v + nw$)		
		$nw \equiv 0$ (mod n)
		Co-Prime $\to d = 1$
		$\to av \equiv 1$ (mod n)

Linear Congruence:
	$ax \equiv b$ (mod n) where x is unknown
	If a and n are co-prime then $x \equiv vb$ (mod n)
	Else try $\dfrac{a}{d} x \equiv \dfrac{b}{d}$ (mod $\dfrac{n}{d}$) where d = HCF(a, n)
		If ¬($d|b$) there are no solutions

Chinese Remainder Theorem:
	$x \equiv a_1$ (mod $m_1$)
	$x \equiv a_2$ (mod $m_2$)
	$\dots$
	$x \equiv a_n$ (mod $m_n$)
	Solving:
		$m_i$ are all co-prime with each other and greater than 1
		$m = \prod m_i$
		$M_i = \frac{m}{m_i}$
		$v_i$ = inverse of $M_i$ (mod $m_i$)
		$x_0 \equiv (\sum a_i v_i M_i)$ (mod m)	

Fermat's Little Theorem:
	If $p$ is a prime number co-prime with $a$
	$a^{p-1} \equiv 1$ (mod $p$)
	Use FLT to find the least residue of a high power. Split the power into a prime

#bonus 
Fermat's Last Theorem:
	No positive integers $a, b, c$ for any value of $n > 2$ satisfy:
		$a^n + b^n = c^n$


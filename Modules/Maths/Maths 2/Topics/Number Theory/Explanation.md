a|b = a divides into b (a $\neq$ 0)
	b is a multiple of a
	a is a factor of b

Division Theorem:
	$a|d \to a = dq + r$
		q = quotient
		r = remainder

Prime numbers are numbers with no factors other than 1 and itself
Non-primes are composite numbers

Fundamental Theorem of Arithmetic:
	Every integer greater than 1 can be written as a unique product of primes

Finding the HCF/GCD (d):
	Primes Method:
		The common prime factors multiplied together
		1890 = 2x3x3x3x5x7
		9450 = 2x3x3x3x5x5x7
		HCF = 2x3x3x3x5x7 = 1890
	Euclids Algo:
		![[Pasted image 20240802165947.png]]
		HCF = the smallest quotient with no remainder
		Back Substitution:
			Rearrange each equation to have the remainder by itself
			Starting from `d = ...` substitute until $d = a_0 v + bw$
			This equation is Bezouts Identity

LCM:
	LCM of a and b is the common factors multiplied together

Co-Primes:
	Two number with no common factors together
A IEEE-754 float is composed of 3 parts, the mantissa, exponent and sign bit
	f = $(-1)^S \times 1.M \times 2^e$
It's often better to have a biased exponent rather than two's complement exponent due to easier computation
	f = $(-1)^S \times 1.M \times 2^{e - b}$

If you are encoding a float add the bias
If you are decoding a float subtract the bias

16-bit: Half
32-bit: Float
64-bit: Double

Unnormalized floats are when M $\geq$ 2 or M $\lt$ 1
You can normalise a float by shifting left/right and adding/subtracting the multiplier to the exponent

$\pm 0$ = s 00000000 00000000000000000000000
$\pm \infty$ = s 11111111 00000000000000000000000
NaN = 0 11111111 M
	Where M != 0

Addition:
	To add floats you need to make their exponents the same
	Shift the fraction of the value with the smaller exponent
	Remember the hidden bit
	Add the mantissas (Account for sign bit)
	If it overflowed that's an exception
	Normalise it
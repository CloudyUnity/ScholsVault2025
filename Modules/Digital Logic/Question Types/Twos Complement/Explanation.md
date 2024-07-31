A way to bias numbers so there's both positive and negative numbers

The most significant bit is always negative, if it is on/true/1 then the number is negative

For example:
	1011 = -8(1) + 4(0) + 2(1) + 1(1) = -5	
	10 = -2(1) + 1(0) = -2
	111111 = -1

Overflow:
	Adding two positive numbers and receiving a negative
	011 + 001 = 100 
	3 + 1 = -4

Underflow:
	Adding two negative numbers and receiving a positive
	101 + 100 = 001
	-3 + -4 = 1

Sometimes "Overflow" is used to refer to cases of both overflow and underflow

One's Complement:
	Negate the bits
	01101101 => 10010010

Negating a number:
	Negate the bits and add 1
	0110 (6) => 1001 + 0001 = 1010 (-6)
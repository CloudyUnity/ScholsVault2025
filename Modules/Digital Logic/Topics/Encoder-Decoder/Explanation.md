Decoder:
	![[Pasted image 20240731120305.png]]
		Converts a n-bit binary number to an output line
		Has $2^n$ output lines
		A decoder with an enable input is the same as a demux
	One-Hot:
		A group of bits is one-hot if there's only a single 1
		A group of bits is one-cold if there's only a single 0		
		One-cold is more economical due to using NAND 	
		Commonly used for address selection in memory chips
		Decoders can be binary to one-hot or binary to one-cold
	BCD to 7SD:
		![[Pasted image 20240731120746.png]]
	Expanding Decoders:
		![[Pasted image 20240731122324.png]]
	Using a decoder to solve a sum problem:
		![[Pasted image 20240731122450.png]]

Barrel Shifter:
	![[Pasted image 20240731120818.png]]
	A circuit for shifting a number using a sequence of multiplexors
	This one rotates (wraps) bits by default
	y = x >> s

Encoder:
	![[Pasted image 20240731132124.png]]
		Converts $2^n$ input lines to n output lines
		If more than 1 input line is active at a time it is undefined behaviour (UB)
		Sometimes includes an enable bit to resolve the discrepancy between all 0s and $D_0$ = 1
	Priority Encoder:
		If multiple bits are 1 then the highest priority takes precedence 
Propagation Delay:
	The time after an input signal is applied before the output signal changes

Nibble:
	4 bit binary number
	Half a byte

Active High/Low:
	![[Pasted image 20240731121234.png]]
	Bobbles on the input indicate active-low
	High chips are considered "on" when a high voltage is applied
	Low chips are considered "on" when a low voltage is applied

XOR3:
	An XOR gate with 3 inputs, how does it work?
	Option 1:
		Odd-parity function
	Option 2:
		IFF one of the inputs is 1

Minterms:
	A boolean function of n unique variables multiplied together
	Minimal conditions where expression is true
	Same as SOP
	For example:
		AB'C
		X'Y'ZW'

Maxterms:
	A boolean function of n unique variables summed together
	Maximal conditions where expression is false
	Same as POS
	For example:
		A+B'+C
		X'+Y'+Z+W'

Complement Form:
	A' = NOT A

Canonical Form:
	A basic representation
	Sum-of-Products and Product-of-Sums are different canonical forms
	To compare two boolean expressions you must coerce them into the same canonical form

Programmable Logic Arrays:
	![[Pasted image 20240731133906.png]]

Three-state Gates:
	A gate which either has a value of 1 (High V), 0 (Ground) or High-Impedance (Hi-Z)
	In Hi-Z the output appears to be disconnected, no logical significance 
	Prevents short circuits and makes for efficient multiplexors
	![[Pasted image 20240731140948.png]]

Also learn:
	EIT Transistors: [[Trinity/Schols/Modules/EIT/Electronics/Topics/Transistor/Explanation|Explanation]]
	EIT Chemistry: [[Trinity/Schols/Modules/EIT/Electronics/Topics/Chemistry/Explanation|Explanation]]
	EIT Conductors: [[Trinity/Schols/Modules/EIT/Electronics/Topics/Conductors & Dielectrics/Explanation|Explanation]]


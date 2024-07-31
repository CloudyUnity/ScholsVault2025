Addend:
	A number that's added to another

Augend:
	A number that has an addend added to it

Half-Adder:
	![[Pasted image 20240718174546.png]]
	Adds two bits to form a sum and carry bit

Full-Adder:
	![[Pasted image 20240718174744.png]]
	![[Pasted image 20240718174701.png]]
	Two half adders and an OR gate
	Adds 3 bits to form a sum and carry bit

4-bit Adder:
	![[Pasted image 20240718174807.png]]
	Chain together full adders to form n-bit adders
	Remember to carry the carry bit

4-bit Adder-Subtractor:
	![[Pasted image 20240731111905.png]]
	If M' then S = A + B
	If M then S = A - B
		M inverts B to get its one's complement
		M acts as the first carry bit to add 1
		Thus negating B
	Condition Code Flags:
		N (Is Negative) = $S_3$
		Z (Is Zero) = $S_0' S_1' S_2' S_3'$
		C (Carry) = $C_4$
		V (Overflow) = $C_4 \oplus C_3$
			Look for if `sign(A) == sign(B) != sign(S)`

Decimal Adder:
	Binary Coded Decimal (BCD):
		Each decimal digit is represented by an unsigned nibble
		After 1001 (9) it becomes 0 and sends a carry to the next BCD
	Binary to BCD:
		![[Pasted image 20240731113256.png]]
		K = Carry out
		If Z > 9 then Z + 6 = S
		C = K + $Z_8 (Z_4 + Z_2)$
		If C then S = Z + 6
		S = Z + 0CC0
	![[Pasted image 20240731113822.png]]
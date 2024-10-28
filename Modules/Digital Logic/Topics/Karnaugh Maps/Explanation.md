
In a kmap there's a box for each line in a truth table
The rows and columns represent the input
The value of the box represents the output

Gray Code:
	The columns are ordered in `00 01 11 10` so that only 1 bit changes between columns

Kmaps are used to solve or minimise truth tables

![[Pasted image 20240731130439.png]]
![[Pasted image 20240731130459.png]]

Group adjacent 1 bits together in groups of sizes of powers of two
Wrapping is allowed
	This means you can make the 4 corners a 4-bit group
4-bit groups must be either squares or straight line shapes
All groups must be as large as possible, always overlap

All variables that have both their uncomplemented and complemented forms included get cancelled out
Create a Sum-of-Products

Incomplete Functions:
	![[Pasted image 20240731131210.png]]
	Incomplete cells can be used however you wish to simplify further
	Commonly seen in 7SDs as binary greater than 9 does not occur

Product-of-Sums Method:
	![[Pasted image 20240731131348.png]]
	Use 0 cells instead and form a product of sums
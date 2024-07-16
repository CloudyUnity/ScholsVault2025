Given a system of linear equations:
![[Pasted image 20240702171231.png]]

This system is consistent if it has at least one solution

Rewrite this equation where $A \mathbf x = \mathbf b$
![[Pasted image 20240702171352.png]]

The augmented matrix of the system is the concatenated matrix $[A \mathbf b]$

Row-Echelon Form:
	All zero rows are at the bottom
	All non-zero rows start with more zeros than the previous

Reduced-Row-Echelon Form (RRE):
	Row-Echelon Form
	All non-zero rows leftmost non-zero is a 1
	All columns with a 1 only have 0s for the other entries

Elementary Row Operations (ERO):
	Swap two rows
	Multiply a row by a non-zero scalar
	Add a multiple of a row to another row

A matrix is row-equivalent to another if it can be obtained using ERO
Subroutines use labels with syntax "Label:"
Subfunction branches use labels with syntax ".LLabel:"

Call a subroutine using `BL Label`
All subroutines use registers `R0-R3` for arguments
All subroutines must push and pop the contents of it's non-arg registers 
If it is a non-leaf subroutine it must also push and pop `LR`
`BX LR` to return from a function
	Alternatively you can pop `LR` into `PC`

ARM Architecture Procedure Call Standard (AAPCS):
	A technical document dictating how a high-level interface is implemented in ARM assembly

Be aware recursion may be required I guess

If you need more than 4 args then use the system stack to hold more
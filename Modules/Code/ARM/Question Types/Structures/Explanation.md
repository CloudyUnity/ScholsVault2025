Arrays:
	Byte arrays:
		LDRB Ro, [Ra, i]
	Halfword arrays:
		LDRH Ro, [Ra, i, LSL #1]
	Word arrays:
		LDR Ro, [Ra, i, LSL #2]

Matrices:
	2D Word Matrix:
		MUL r, row, size(row)
		ADD i, r, column
		LDR Ro, [Ra, i, LSL #2]
	Assume row-major for ARM problems

Stack:
	A LIFO data structure
	A full stack has the pointer on the last added value
	An empty stack has the pointer after the last added value
	An ascending stack has the stack grow up the addresses
	A descending stack has the stack grow down the addresses
		We use a full descending stack
	The system stack must be word aligned so don't push bytes onto it

#bonus 
DirectX uses row-major matrices
OpenGL/Vulkan use column-major matrices
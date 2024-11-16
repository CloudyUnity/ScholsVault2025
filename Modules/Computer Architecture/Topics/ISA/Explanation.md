Instructions can be split into 3 parts
	OPCODE
		Function
	DESTINATION
		Almost always datapath register 
	OPERANDS
		Comes from datapath registers

Opcodes select the ASM in the control memory which determines how the rest of the instruction is laid out
	Aka what DR, SA, SB represent in our case

For our processor we have the basic layout
	OPCODE(31:15)
	DR(14:10)
	SA(9:5)
	SB(4:0)

OPCODES get converted by the CAR and control memory into a bunch of 1 bit flags which are used all over the processor 

Decoder
	Splits a binary number length $n$ into $2^n$ outputs
	Each possible value corresponds to one output
	One wire will always be on
	Made by:
		Create SOP minterms and lead them to outputs

Multiplexor
	Sends one of many $m$ inputs length $n$ to a single output length $n$ based on $2^m$ select inputs
	Select is a binary number representing the index of the data input to output
	Made by:
		Convert each select state to a wire, AND them with corresponding data input
		OR everything together

SR Latch
	Set - Q=1
	Reset - Q=0
	Made by:
		Have two parallel NOR gates 
		NOR1.in0 = R
		NOR1.in1 = NOR2.out
		NOR2.in0 = S
		NOR2.in1 = NOR1.out
		Q = NOR1.out

D Latch
	C - Enables modification
	D - Value to set Q as
	Made by:
		Take SR latch
		Set = CD
		Reset = CD'

D-Type PE Flip Flop
	Uses a Clk instead of C
	Only changes on PE
	Made by:
		Too complicated to memorize 

Half Adder -> Full Adder -> RippleAdder -> ALU

RAM
	Inputs:
		CLK, RW
		Address[31:0]
		DataIn[31:0]
	Outputs:
		DataOut[31:0]

Functional Unit
	Contains an ALU and Shifter
	These are the inputs for the FU
		FS(5:0) - FU op codes
			Split into:
			G(3:0) - ALU op codes
			H(1:0) - Shifter op codes
			MF - Selects between ALU and Shifter for output
			H = G(3:2) when MF

Datapath
	The functional unit requires 5 bits to select ALU/Shift micro-ops
	3 bits control the datapath itself
		RW, MB, MD
		MB selects between ConstantIn and RegisterFileOut to go into functional unit B
		MD selects between DataIn and FunctionalOut to go into RegFile D
	Most datapath inputs can be combined into the Control Word
		0 - RW
		1 - MD
		2:6 - FS
		7 - MB
		8:10 - BA (B Reg Address)
		11:13 - AA (A Reg Address)
		14-16 - DA (D Reg Address)
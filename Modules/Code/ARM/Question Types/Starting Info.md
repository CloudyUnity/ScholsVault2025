Reduced Instruction Set Computing (RISC):
	A type of processor with 100 instructions or less
	More general purpose, faster execution
	Only Load/Store instructions can access memory

Complex Instruction Set Computing (CISC):
	TODO

ARM Mode vs Thumb Mode:
	Thumb instructions can be either 2 or 4 bytes
	TODO

Least Significant Bit (LSB):
	Bit of value 1 in a n-bit number

Most Significant Bit (MSB):
	Bit of value $2^n$ in a n-bit number

Little Endian:
	LSB is closer to address 0x0

Big Endian: 
	MSB is closer to address 0x0

Intel x86 and x86-64 processors are little endian
ARM was little endian before v3 but is now bi-endian

Operands:
	The registers an instruction uses

Registers:
	R0-R11 General Purpose
	R12(IP) Intra Procedural Call
	R13(SP) Stack Ptr
	R14(LR) Link Register
	R15(PC) Program Counter
	R16(CPSR) Current Program Status Register

![[Pasted image 20240731173911.png]]
	Jazelle is related to executing java bytecode

#bonus
ARM Versions:
	ARM7 (v4)
	ARM9 (v5)
	ARM11 (v6)
	Cortex-A (v7-A)
	Cortex-R (v7-R)
	Cortex-M (v7-M)

#bonus 
Cortex-M:
	Has only 16 registers as opposed to 30
	Other ARM versions use registers 17-29 for privileged software execution 
	Runs at 24 MHz
	128KB Flash Memory
	8KB RAM

#bonus
Understand how languages are compiled, linked, assembled and executed, there will probably be info on this in the C section

#bonus 
ROP Chains:
	TODO
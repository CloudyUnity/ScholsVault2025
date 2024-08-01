Ro = Register Copy Destination
Ra = Register With Address

Some values are invalid to use as constants so you have to load them into a register first

Appended Shift
	LSL Rn*
	LSR Rn*
	ASL Rn*
	ASR Rn*
	ROR Rn*
	ROL Rn*

Arithmetic Shift (ASL) brings in 1s to the left if the MSB is a 1
	Allows quick division for signed numbers

Rotates (ROR) brings the LSB back around to the MSB while shifting
Basically wrapping the number

Rx* = Register or Register + Appended Shift or Constant Value
~ = Discarded value
{x} = x is optional (Excluding `R List`)
[x] = value at address x
@ = Comment
$\#$ = Constant Value
0x = Hex value
0b = Binary value

.Label = A symbol exchanged for an address in the pre-processing stage
.Label* = A label or constant address value

{`R List`}
	A list of registers separated by commas or connected with dashes
	{R0, R4, R8}
	{R2-R6, R7}
	They will be ordered by the pre-processor if you don't
	These are not optional

Extensions (E):
	B = Byte
	H = Halfword
	S/SB/SH = Modify Condition Code Flags

Variations (V):
	IA = Increment After (Default)
	IB = Increment Before
	DA = Decrement After
	DB = Decrement Before
	FD = Full Descending Stack
		IA for LDM
		DB for STM 
	All increment/decrement by 4

Condition Code Extensions (CC):
	Execute the instruction if the condition code flags are met
	EQ = Rn == Rm
	NE = Rn != Rm
	LE = Rn <= Rm (Signed)
	LT = Rn < Rm (Signed)
	GE = Rn >= Rm (Signed)
	GT = Rn > Rm (Signed)
	LS = Rn <= Rm (Unsigned)
	LO = Rn < Rm (Unsigned)
	HS = Rn >= Rm (Unsigned)
	HI = Rn > Rm (Unsigned)
	VS = Signed Overflow

MOV{S} Ro, Rn*
	Copies Rn* into Rd
	Cycles: 1

ADD{S} Ro, Rn, Rm
	Ro = Rn + Rm
	Cycles: 1

SUB{S} Ro, Rn, Rm
	Ro = Rn - Rm
	Cycles: 1

AND{S} Ro, Rn, Rm
	Ro = Rn & Rm
	Cycles: 1

BIC{S} Ro, Rn, Rm
	Ro = Rn & ~Rm
	Cycles: 1

ORR{S} Ro, Rn, Rm
	Ro = Rn | Rm
	Cycles: 1

EOR{S} Ro, Rn, Rm
	Ro = Rn ^ Rm
	Cycles: 1

MUL{S} Ro, Rn, Rm
	Ro = Rn * Rm
	Cycles: 2-5

UDIV{S} Ro, Rn, Rm
	Ro = Rn / Rm
	Cycles: 4

SDIV{S} Ro, Rn, Rm
	Ro = Rn / Rm
	Cycles: 4

NOT Ro, Rn
	Ro = ~Rn
	Cycles: 1

NEG Ro, Rn
	Ro = -Rn
	Cycles: 1

CMP Rn, Rm
	SUBS ~, Rn, Rm
	Updates CPSR
	Cycles: 1

B{CC} .Label
	Sets the PC to the label address
	Cycles: 3

BX LR
	Sets the PC to the LR
	Cycles: 3

BL{CC} .Label
	Sets the LR to the PC
	Sets the PC to the label address	
	Cycles: 3

CBZ Rn, .Label
	Branches to label if Rn == 0
	Cycles: 3

IT {CC}
	Activates conditional execution for thumb mode
	Example:
		`ITTE EQ`
		`ADDEQ R0, R0, R1`
		`SUBEQ R2, R2, R3`
		`MOVNE R4, R5`
	Cycles: 1

LDR{E} Ro, [Ra, Rn*]{!}
	Loads a word/halfword/byte from [Ra + Rn*] into Ro
	If (!) then Ra += Rn*
	Cycles: 3

LDR{E} Ro, [Ra], Rn*
	Loads a word/halfword/byte from [Ra] into Ro
	Ra += Rn*
	Cycles: 3

LDR{E} Ro, =.Label*
	Loads a word/halfword/byte from [.Label*] into Ro
	Cycles: 3

STR{E} Rn, [Ra, Rn*]{!}
	Stores a word/halfword/byte from Rn into [Ra + Rn*] 
	If (!) then Ra += Rn*
	Cycles: 2

STR{E} Rn, [Ra], Rn*
	Stores a word/halfword/byte from Rn into [Ra]
	Ra += Rn*
	Cycles: 2

STR{E} Ro, =.Label*
	Stores a word/halfword/byte from Rn into [.Label*]
	Cycles: 2

LDM{V} Ra{!}, {`R List`}
	Loads n words from [Ra] into `R List`
	If (!) then Ra saves the new address
	Cycles: 2 + n

STM{V} Ra{!}, {`R List`}
	Stores n words from each in `R List` into [Ra]
	If (!) then Ra saves the new address
	Cycles: 2 + n

PUSH {`R List`}
	LDMDB! SP, {`R List`}
	Cycles: 2 + n

POP {`R List`}
	STMIA! SP, {`R List`}
	Cycles: 4 + n
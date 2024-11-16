
Control Unit (CU)
	Supplies control signals to datapath 
	Responds to NZCV
	Takes in instructions from memory 
	Two approaches:
		Hard-wired
		or
		Micro-coded

Hard-wired Binary Multiplier ASM:
	$G$ = Go
	$Z$ = Zero status
	$Q_0$ = ?
	![[{8535EC64-8B8A-4874-8C30-DFC6BCA36BBC}.png]]

Hard-wired CUs are compact and have low prop delay but as they get bigger they become more costly to design, debug and upgrade 
Micro-coded are more flexible 

Erasable Programmable ROM = EPROM

Micro-coded approach:
	Store control words together with next-state info in a control memory (ROM/EPROM)
	Use control inputs and status signals to select appropriate address of next state
	As control words are stored it prevents from depending dynamically on the value of the control input
	![[{F8F1DE98-F1D2-4B2D-96D9-4F91EAAF125F}.png]]

Binary Multiplier to Micro-coded ASM
	You need to replace conditional output boxes with state boxes
	Before:
	![[{45CB4751-BB19-4264-85FC-943A085E6AE5}.png]]
	After:
	![[{BF26C1D1-0614-43D8-BD9A-38A2ED3A9ACF}.png]]

Control Address Register (CAR)
	$s$ = Number of states in the ASM
	The control memory must store $s$ control words
	You will need a $n$ bit CAR where $n$ is the least number of bits to store up to $s$ in binary 

SEL bits
	Keep track of which status bits your ASM needs to respond to (NZCV, $Q_0$ )
	Also look at your control inputs (G)
	You need a select bit for each status bit used in the control word

Next Address Field
	Have the form NXTADDN where N is the next-address field index
		0 indexed
	The address of the instruction after the current one
	In a sequential program you only need one NXTADD
	In a conditional program you need enough NXTADD in the control word for the highest branch conditional (Generally just 2)
	Each NXTADD bit length is the size of the CAR
		The NXTADD needs to be big enough to refer to the binary codes on the state boxes

The SEL bits determine which conditional function to apply
![[{F4055C07-3C61-4795-B02E-962B2E4F5856}.png]]

The control word also needs 1 bit for each state box register transfers. If multiple state boxes do the same register transfers they can share a bit


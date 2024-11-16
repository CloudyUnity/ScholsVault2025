
Compute System Architecture (CSA)
	Conceptual design and structure of a computer system
	Layout of hardware, design of ISA, techniques for data handling

Control Unit
	Determines the sequence of operations

Datapath
	Preforms data-processing operations

Control inputs enter the control unit
Control outputs exit the control unit
Control signals enter the datapath
Data inputs enter the datapath
Status signals exit the datapath and enter the control unit
Data outputs exit the datapath

Shared Signals
	Signals driven by 1+ sources (Buses)

Signal Values
	U = Uninitialized
	X = Unknown
	0, 1, Z
	W = Weak Unknown
	L = Weak 0
	H = Weak 1
	- = Don't Care

Transaction
	A time-value pair representing the future value of a signal
	signal $<=$ expression after time;

Process
	Sequentially executed process of HDL code
	Doesn't have the parallelism of regular HDL
	Sensitivity List
		List of inputs (Clock)
		In a TB there is no sensitivity list

Stim_Proc Process
	Runs constantly, loops when completed 
	Similar to a while (true) loop

Unit Under Test (UUT)
	Self explanatory 

Register Transfer Language (RTL)
	Level of abstraction used in DLD to describe functionality of digital system
	$C : RD * RS$ 
		$C$ = Control function 
		$RD$ = Dest Reg
		$RS$ = Src Reg
		$*$ = Operation
	$RN(k)$ = kth bit of $RN$
	$RN(k:p)$ = kth to pth bits of $RN$ 
	$M[RN]$ = Memory pointed to by $RN$ 
	$\leftarrow$ = Operation for data transfer 

Micro-Operation
	Operation accomplished within few gate prop delays upon data stored in adjacent registers and memory 

$A + \overline{B} + 1 \equiv A - B$ 

Transfer Micro-Ops
	Two approaches are used:
		Multiplexor based transfer for speed
			We use this one
		Bus based transfer for flexibility and economy 
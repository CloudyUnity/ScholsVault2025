A finite state machine (FSM) is a mathematical model of computation
An abstract machine that can be in exactly one of a finite number of states at any given time

Example:
	![[Pasted image 20240731145216.png]]
	Circles are states
	d, n, q, s are all inputs that transition states	

State/Transition equations specifies the next state as a function of the current state and inputs

![[Pasted image 20240731145914.png]]
	The binary inside the circle represents the state of the flip-flops
	The transition line numbers represent the input value and output value
	If there's no slash or second number, there's no output

Mealy Model:
	A Mealy machine is a FSM whose output is determined by its current state and inputs

Moore Model:
	A Moore machine is a FSM whose output is only determined by its current state

State Reduction:
	These algorithms try to reduce the number of states and flip flops in circuit while keeping external requirements unchanged
	Two states are equivalent if for each input they give the same output and send the circuit to equivalent states
		One of these states can be removed
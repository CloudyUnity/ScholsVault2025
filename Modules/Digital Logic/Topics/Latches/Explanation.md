Latches are level sensitive, they change based on the input level
Flip Flips are edge sensitive, then change based on input level changes
Latches and flip flops are bistable multivibrators (Two stable states)

S-R Latch:
	A Set-Reset latch has two inputs
	If Set then the latch stores a 1
	If Reset then the latch stores a 0
	![[Pasted image 20240731141458.png]]
	If both inputs are low then there's a race condition and whichever gate changes first with assert itself
	Manufacturing methods have made it so one gate will always win
	S = R = 1 is UB

Gated S-R Latch:
	Has an enable bit that must be high for the stored bit to change
	![[Pasted image 20240731142458.png]]

D-Latch:
	Has Data and Enable inputs
	When enable bit is high the state of D is stored
	![[Pasted image 20240731142514.png]]
	Level sensitivity causes chaos in large circuits due to output feedback within clock cycles

Master-Slave D-Flip-Flop:
	Only stores state of D on falling clock edge
	![[Pasted image 20240731142851.png]]
	Toggle Mode:
		![[Pasted image 20240731143420.png]]
		Wire the Q' into D to have it toggle every cycle

7474 Positive-Edge D-Flip-Flop:
	![[Pasted image 20240731143146.png]]

J-K Flip-Flop:
	If K then store 0
	If J then store 1
	If JK then toggle stored value
	![[Pasted image 20240731143240.png]]
	Async Inputs:
		These are independent of the clock
		Preset: ($\overline{PRE}$) forces Q to 1
		Clear: ($\overline{CLR}$) forces Q to 0
		![[Pasted image 20240731143507.png]]

Set-up time and hold time are times required before and after a clock transition for data to present and remain in a flip-flop

Frequency Division:
	Flip flops can divide a signal frequency by two
	![[Pasted image 20240731144629.png]]

Simple Binary Counters:
	![[Pasted image 20240731144727.png]]

#bonus
Register:
	Just a bunch of flip flops where each represents a bit of a bit vector. Shrimple stuff
Before 1950 electronics used vacuum tubes/valves as transistors. They were large and created lots of heat
I don't know if more information is needed on the history

Enhancement Metal Oxide Semiconductor Field Effect Transistor (E-MOSFET):
	These have fast switching speeds which is good for processors
	Easy to manufacture, can be used as a resistor or capacitor 
	Less gain than the Bipolar Junction Transistor however
	N-Channel E-MOSFET:
		![[Pasted image 20240715162507.png]]
		![[Pasted image 20240715162616.png]]
		N-Channel is also called an inversion layer
		Why does the dielectric become negative closer to the gate though? 
			#todo find an answer

Building Logic Gates:
	![[Pasted image 20240715163158.png]]
		When the gate is HIGH the transistor connects to ground and the voltage leaving X is LOW
		When the gate is LOW the voltage goes straight from Vcc to X HIGH
	![[Pasted image 20240715163353.png]]

Class A Amplifiers:
	![[Pasted image 20240715163530.png]]
	$V_{in}$ is AC
	$V_{DD}$ is DC
	Capacitors prevent backflow of DC while allowing AC 
	$V_{out}$ is inverted amplified AC voltage
	$R_S$ is the emitter resistor
	$R_1$ is the base resistor
	$R_0$ is the collector resistor
	$V_S$ should be $0.5 V_{DD}$ for maximum efficiency   
	Gain
		How much the signal amplitude is multiplied
	#todo
		Solve for each variable, idfk how it's confusin
Resistor:
	A two terminal element which impedes flow of electrical current
	Converts electrical energy into another form (Heat, light, etc)
	Unit = Ohms (Scalar)
	Every material has at least some resistance, "Resistors" are "Ohmic Materials"
		These have a linear relationship between applied voltage and current

Ohms ($\ohm$):
	Unit of electrical resistance
	$\ohm = \dfrac{V}{A} = \dfrac{W}{A^2} = \dfrac{V^2}{W} = \dfrac{H}{s} = \dfrac{Wb}{C}$

Ohm's Law:
	$V = IR$

Joules Law:
	$P = VI = \dfrac{V^2}{R} = I^2 R$

Non-ideal power sources can be modelled using a resistor 
	In series for voltage sources
	In parallel for current sources

Batteries have internal resistance
	If $R_{internal}$ is very small we can consider the source ideal

Resistors in Series:
	$R = R_1 + R_2 + \dots + R_n$

Resistors in Parallel:
	$\dfrac{1}{R} = \dfrac{1}{R_1} + \dfrac{1}{R_2} + \dots + \dfrac{1}{R_n}$

The Potential Divider:
	A circuit that divides a voltage into smaller voltages
	Has two resisters in series
	$V_o = V_i \dfrac{R_2}{R_1 + R_2}$
	Used for volume controls in audio equipment
	![[Pasted image 20240911132118.png]]

Current Split
	Given a current $I$ being split into two branches with resistance $R_1$ and $R_2$
	$I_1 = I \dfrac{R_2}{R_1 + R_2}$
	$I_2 = I \dfrac{R_1}{R_1 + R_2}$

Superposition Theorem
	Used to solve circuits with multiple batteries
	Can only be used on circuits reducible to series/parallel combinations. Not unbalanced bridge circuits
	For each power source	
		For every other power source
			Replace voltage sources with short circuits (Wire)
			Replace current sources with open circuits (Break)
		Calculate all voltages and current for the circuit
		Add voltages and currents into circuit drawing
	Add voltage drops across all resistors
		Opposite polarities subtract
	Add currents across all branches
		Opposite directions subtract

Mesh Current
	Also used for multi-battery circuits
	Label all current loops
	![[{B0D87BE8-628C-43AF-B031-96D83B2BCACE}.png]]
	Then label all voltage drops across resistors according to assumed directions of mesh currents
	Apply KVL to each loop, replace $V$ with $IR$
	Solve for each $I$,  $I < 0 \to$ Change rotation of loop
	Where loops touch the same branch, sum individual currents
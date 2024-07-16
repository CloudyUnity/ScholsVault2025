Electric Field:
	An electric field forms between two points with an electrical potential difference
	Its intensity at a point is the force per unit positive charge at that point
	$\mathbf E = \dfrac{\mathbf F}{q}$
	Unit = N/C or V/m (Vector)
	Represented by gauss lines radiating from a charge
	$\mathbf{E} = k \dfrac{|q_{1} - q_{2}|}{|AB|^2}$

Electric Flux ($\phi_E$):
	The measure of an electric field through a surface
	$\phi_{E} = \mathbf E \cdot \mathbf{\hat{n}} = ||\mathbf E|| A cos(\theta) = \mathbf{\hat n} \mathbf D A$
	![[Pasted image 20240715143557.png]]

Electric Flux Density ($\mathbf D$):
	Corresponds to the electric field strength (Number of gauss lines per unit area)
	$\mathbf D = \epsilon \mathbf E$
		$\epsilon$ = Electrical Permittivity

Electrical Current and Magnetism:
	Currents attract if moving in the same direction, repel if opposite
	This phenomenon is defined by the ampere ($A$)
	When charges move (electric current) they each exert forces, aka have a magnetic field
	The magnetic field rotates around the current axis right-handed
		Point thumb in current direction, follow wrapping of fingers

Magnetic Pole/Charge:
	A pole of 1 $Wb$ takes 1 $J$ to move around 1 $A$
	Magnetic poles are an abstraction, not physical

Magnetic Field Strength ($\mathbf H$):
	 MFS at a point is the force per unit positive magnetic pole at that point
	 Unit = $A$ (Vector)

Magnetic Flux Density ($\mathbf B$):
	MFD at a point is the force per unit positive electric charge moving at 1m/s normal to the magnetic field direction
	$\mathbf B = \dfrac{\mathbf F}{I l}$
		$\mathbf F$ = Force (Vector)
		$l$ = Length of wire
	$\mathbf B = \mu H$
		$\mu$ is the magnetic permeability 
	$\mathbf{B} = \dfrac{\mu I}{2 \pi r} \mathbf{\hat{I}} \times \mathbf{\hat{r}}$
		$r$ is the radial distance to the wire
	Unit = Tesla (Vector)

Weber ($Wb$):
	Unit of magnetic flux
	Equal to Volt-Second or $\mathbf T m^2$

Magnetic Flux ($\phi_B$)
	Number of magnetic field lines passing through a closed surface
	$\phi_B = \mathbf B \cdot \hat{n} = ||\mathbf B|| A cos(\theta) = \mathbf{\hat n} \mathbf B A$
		$\mathbf B$ is the magnetic field density
		$A$ is the area
	Unit = $Wb$ or $Tm^2$ (Scalar)

Tesla ($\mathbf T$):
	$\mathbf{T} = Wb/m^2$
	$\mathbf T$ is a Vector

In electric fields the force on a charge points in the direction of positive to negative
In magnetic fields the force on a moving charge is perpendicular to the direction of the magnetic field

Lorentz Force Law:
	Lorentz force is the electric and magnetic force on a point charge from electromagnetic fields
	$\mathbf F = q(\mathbf E + \mathbf v \times \mathbf B)$
	$\mathbf F = \mathbf{B} I L$

Ampere's Law for an Infinite Straight Wire:
	Ampere's Circuital Law says that for a straight current-carrying wire:
		Magnetic field lines encircle the wire
		The lines lie in the normal plane to the wire
		If the current reverses, the field reverses
		The field strength is proportional to the current magnitude
		The field strength at any point is inversely proportional to the distance from the wire

Faraday's Law:
	A changing magnetic flux threading a conductor induces an $emf$ according to:
		$emf = -\dfrac{d \phi_B}{dt}$
	For a tightly would coil of wire with N turns:
		$emf = -N \dfrac{d \phi_B}{dt}$
	Applications:
		Electric guitars have a magnet to induce magnetism in the strings, vibrating strings cause a changing flux in the coil resulting in small varying voltage fed into an amplifier and speaker
		Microphones have a coil and magnet which vibrate from sound waves inducing voltage 
		Electrical power generation has a coil rotated by kinetic energy (Turbines) through a magnetic field. EMF appears at the brushes powering the circuit. Makes an AC power supply

Lenz's Law:
	An induced electric current flows in a direction such that the current opposes the change that induced it
	For example if you thrust a pole magnet into a coil the induced current would match the charge repelling it, when retracting the pole the current swaps signs to attract it back
	$emf = -N \dfrac{\partial \phi_B}{\partial t}$

A random number generator (RNG) is a device designed to generate a sequence of pseudo-random numbers

Linear Congruential Method (LCM):
	$X_0$ is the seed
	a is the multiplier
	c is the increment
	m is the modulo
	$R_i$ is in the range `[0, 1)`	
	$X_{i+1} = aX_i + c$ (mod m)
	$R_i = \frac{X_i}{m}$

Combined Linear Congruential Method (CLCM):
	Have LCMs:
		$Y_{i+1, 1} = a_1 Y_{i, 1} + c_1$ (mod $m_1$)
		$Y_{i+1, 2} = a_2 Y_{i, 2} + c_2$ (mod $m_2$)
		$...$
		$Y_{i+1, j} = a_j Y_{i, j} + c_j$ (mod $m_j$)
	$m_j$ must be prime
	$a_j$ must ensure the period is $m_j - 1$
	$X_i = Y_{i, 1} - Y_{i, 2} + Y_{i, 3} - \ ... \ + Y_{i, j}$ (mod $m_1 - 1$)
	$R_i = \dfrac{X_i}{m_1}$		
		If $X_i = 0$ then $R_i = \dfrac{m_1 - 1}{m_1}$
	Max Period:
		$\dfrac{(m_1 - 1)(m_2 - 1) \dots (m_j - 1)}{2^k - 1}$

Random-Number Streams (RNS):
	I don't understand
	![[Pasted image 20240804140216.png]]
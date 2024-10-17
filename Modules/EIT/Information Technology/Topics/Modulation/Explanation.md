Modulating involved changing a property of the carrier signal
Wireless transmission is more efficient at high frequencies and there's more bandwidth available 
Also allows for multiplexing 

Remember that phase is the derivative of frequency
$B_m$ is the bandwidth
$B_b$ is the baseband
$I(t)$ is the information signal
$m(t)$ is the modulated signal 

Amplitude Modulation (AM):
	The modulated signal is gotten from multiplying the carrier signal with the information signal
	$B_m$ is the difference between the upper and lower band
	Example: AM Radio

Frequency Modulation (FM):
	$m(t) = sin(\omega t + \beta \int_0^t I(t) dt)$
		$\omega$ is the carrier angular frequency
		$\beta$ is the frequency modulation index
			The ratio of frequency deviation to the modulating frequency
	Example: FM Radio 
	Bandwidth:
		$B_m = 2(1 + \beta) B_b$			
		$\beta \approx 4$

Phase Modulation (PM):
	$m(t) = sin(\omega t + \alpha I(t))$
		$\alpha$ is the phase modulation index
	Not often used in analog signals
	Bandwidth:
		$B_m = 2(1 + \beta) B_b$
		$1 \leq \beta \leq 3$

Negative Spectrum:
	Any spectrum has a mirrored negative side
	This matters when translating signals up the frequency domain
	Baseband:
		![[Pasted image 20240717142233.png]]
	Bandwidth:
		![[Pasted image 20240717142518.png]]

Examples:
	AM:
		![[Pasted image 20240717141659.png]]
	FM:
		![[Pasted image 20240717141725.png]]
	ASK/FSK/PSK:
		![[Pasted image 20240717141844.png]]

If you modulate a signal and part of its spectra is below zero you will experience distortion and aliasing
You may also lose data due to interference with the positive frequencies 
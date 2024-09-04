Transducers convert signals to electrical signals

Periodic signals repeat a pattern within a time frame
Aperiodic signals do not
The period ($T$) of a signal is the time to complete a cycle
In the space domain period is called wavelength ($\lambda$), measured in meters	

Angular Frequency ($\omega$):
	$\omega = \dfrac{2 \pi}{T}$

Frequency ($f$):
	$f = \dfrac{1}{T} = \dfrac{\omega}{2 \pi}$
	$\lambda = \dfrac{c}{f}$
		$c$ is the speed of light in the medium considered

Sum of Sines:
	Composite periodic signals are generated with a Fourier series
	$s(t) = c + \sum A_i \ sin(\omega_i t + \varphi_i)$

Square Wave:
	Square wave is estimated by:
	$S_q (t) = \sum_{i = 1, i=odd} \dfrac{1}{i} sin(2 \pi i f_1 t)$

Amplitude Domain/Spectrum:
	For a Fourier series plot point $(f_i, A_i)$ for each $i$

Phase Domain/Spectrum:
	For a Fourier series plot point $(f_{i}, \varphi_i)$ for each $i$

These spectrums are discrete 
If the spectra of two channels don't overlap they won't interfere with each other

Bandwidth:
	The range of frequencies composing a signal
	Scalar value, Difference between highest and lowest

Information that needs to be transmitted is aperiodic which can't be represented with a Fourier series

Fourier Transform:
	$F(\omega) = \int^{\infty}_{-\infty} f(t) e^{-2 \pi \omega i t} dt$
	#todo
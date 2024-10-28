To convert a continuous signal to discrete you need to sample values 

Nyquist-Shannon theorem:
	Sample at twice the max frequency for lossless sampling
	Oversampling is often done to account for non-ideal components
	![[Pasted image 20240718150931.png]]

Fast Fourier Transform (FFT) is used to compute the signal from samples
	$F_k = \sum_{n=0}^{N-1} s_n e^{-i \dfrac{2 \pi kn}{N}}$
	Also see Discrete Fourier Transform (DFT)
	Applications:
		Sobel Edge Detection
		Signal filters
	FFT is most efficient when $N$ is a power of 2

Quantisation:
	Converting a continuous set to a discrete set
	8-Bit Quantisation:
		With 8 bits you can represent 256 levels
		$L = 2^n$
	Quantisation will always lead to some data loss / noise

Bits per sample ($n$):
	$n = log_2 L$

Bitrate ($R$):
	Bits per second = Bits per sample * Samples per second
		$R = nS$	
	$R = 2n B_m$

HDTV:
	Resolution: 1920x1080
	Hertz: 25
	Pixel Format: R8G8B8A8 

Latency / Propagation Speed:
	The time taken for a signal to move through space
	Not related to bitrate, limited by the speed of light
	Influences the time until the first bit reaches its destination

$0 \leq d \leq 1$

Baud ($S$):
	How many slots/signals/samples per second
	If a signal transmits 12 b/s with 2-bits per sample the baud is 6
	$S = \dfrac{R}{n}$
	$S = 2B_b = (1+d)B_m$
	$S =$ Samples per channel * Channels per second

Amplitude Shift Keying (ASK):
	On-Off Keying (OOK):
		2-bit ASK
		null amplitude for 0b0
		$A$ amplitude for 0b1		
	M-ASK:		
		M = $L$
		$B_m = (1 + d)R$ 
		null amplitude for 0
		$A_1, A_2, \dots, A_M$ amplitudes for $1, 2, \dots,M$ 

Frequency Shift Keying (FSK):
	M-FSK:
		$B_m = S(M + d)$
		Ideally $d=0$

Phase Shift Keying (PSK):
	$B_m = (1 + d) S$ 
	Isn't affected by noise as much as ASK
	At high M levels it becomes difficult to distinguish between them
	BPSK = 2-PSK
	QPSK = 4-PSK

Quadrature Amplitude Modulation (QAM):
	$B_m = (1+ d)S$
	Merge of ASK and PSK
	Has 2 carriers, one in-phase and one in quadrature (90 degrees off) with different amplitudes
	One of the most widely used modulations	

Constellation Diagram:
	Graphical representation of modulated signals (ASK, PSK, QAM)
	Magnitude is the amplitude
	Angle is the phase
	![[Pasted image 20240718164738.png]]
	![[Pasted image 20240718165032.png]]

Reducing the bandwidth:
	Don't oversample
	Compress data
	Undersample
	Use more efficient modulation schemes like PSK/QAM
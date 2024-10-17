
> [!question]- ![[Pasted image 20240905141016.png]]
> Upper band $= f_c + f_I = 100 + 20 = 120Hz$
Lower band = $f_c - f_I = 100 - 20 = 80Hz$
$B_m = 120 - 80 = 20Hz$ 

> [!question]- ![[Pasted image 20240905141043.png]]
 (a)
 $B_m = 10 \ KHz$
 $f_{min} = 20 - 5 = 15 \ KHz$
 $f_{max} = 20 + 5 = 25 \ KHz$ 
(b)
 $f_{min} = 2 - 5 = -3 \ KHz$ 
 If you modulate a signal and part of its spectra is below zero you will experience distortion and aliasing
 You may also lose data due to interference with the positive frequencies 

> [!question]- ![[Pasted image 20240905141339.png]]
> (a)
 Line from x axis to points $(10, 1)$ and $(30, 1/3)$
 (b)
 $m(t) = sin(2 \pi 100 t) \sum_{n = 1, 3}\dfrac{1}{n} sin(2 \pi n f t)$ 
 (c)
 Min frequency of $I(t)$ is $10Hz$
 $B_b = 20 Hz$
 Min carrier frequency for $AM$ is $10Hz$ as $10 - 10 = 0$ 

> [!question]-  ![[Pasted image 20240905141449.png]]
> (a)
 $n = 16$
 2 Channels
 $B_b = 22 \ KHz$ 
 $S = 2 * B_b = 44,000$
 $R = 16 * 44,000 * 2 = 1.408 \ Mb/s$ 
 (b)
 $L = log_2 \ n = 4$
 $1.2306 - 1.23 = 0.0006 \ GHz = 0.6 \  MHz = 600 \ KHz$
 Spectral Efficiency = $1.408 \ M / 600 \ K \approx 2.35\  b/Hz$ 
 $QPSK$ and $4QAM$ has $2\ b/Hz$, not enough
 $8PSK$ has $3 \ b/Hz$ thus is enough

> [!question]- ![[Pasted image 20240905141502.png]]
 (a)
 $L = 8 \to n = 3$
 $100 \ 110 \ 010 \ 111 \ 001 \ 011$
 Draw square wave with 8 levels 
 (b)
 Draw sin wave with 8 levels of amplitude 
 (c)
 $B_m = (1 + 1)(1M) = 2MHz$
 Draw box from $99MHz$ to $101MHz$ 

> [!question]- ![[Pasted image 20240905141539.png]]
(a)
Digital modulations occur within wires/electronics and are more resilient against noise. This encodes binary data directly using shift keying
Analog signals occur as waves and as such as subject to noise from external factors. This encodes analog data as the amplitude/frequency/phase of a carrier wave
(b)
Digital is more resilient against noise as it is more discrete, and error handling can be implemented such as parity checks
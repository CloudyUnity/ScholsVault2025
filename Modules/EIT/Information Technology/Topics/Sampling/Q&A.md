
> [!question]- #schols  ![[Pasted image 20240731165554.png]]
 (i)
 Channels = 8
 $B_b = 22KHz$
 Oversample 2x
 Sample $n = 16$
 $n=4$
 16-QAM
 $C = 100MHz$
 $R = 16 * 8 * 22K * 2 * 2 = 11,264Kb/s$ 
 $S = R/n = 2816Kbaud$ 
 $B_m = (1 + d)S = 2816 \ KHz$ 
 (ii)
 $9 * 60K = 540KHz$
 $B_{req} = 10 * 2816K + 540K = 28.7 \ MHz$ 
Too high
 $20M - 0.54M = 19.46M$
 $19.46M / 10 = 1.946MHz = 1946KHz$ per system
 $11,264K/1946K = 5.78 \ b/Hz$ 
 We need at least 6 bits per $Hz$ 
 $L = 2^6 = 64$
 64-QAM
 (iii)
 Stop oversampling and reduce guard bands
 $n = 6$
 $10 * B_m + 9 * G = 10,000K$
 $S = 16 * 8 * 22K * 2 / 6 = 938.7Kbaud$
 $10 * 938.7K + 9 * G = 10,000K$
 $9 * G = 613K$
 $G \approx 68.1 \ KHz$ 
 Reducing guard bands are unnecessary 

> [!question]- #schols ![[Pasted image 20240801193949.png]]
 (a)
 $f_{sample} = 2B_b = 10MHz$
 (b)
 $01 \ 10 \ 01 \ 01 \ 00 \ 11$
 Draw wave with 4 levels of amplitudes
 $011 \ 001 \ 010 \ 011$
 Draw wave with 8 levels of phase
 (c)
 $R = 100Mb/s$ 
 $n =2$
 $S = R/n = 50Mbaud$
 $B_m = (1 +d)S = 50MHz$
 Draw bandwidth from $475MHz$ to $525MHz$ 
 (d)
 $B_{m1} = 100M/1 = 100MHz$
 $B_{m2} = 50MHz$
 $B_{m3} = 100M/3 = 33.33MHz$
 $B_{m4} = 100M/4 = 25MHz$
 $100 + 50 + 33.33 + 25 + 3G = 250$
 $3G = 41.67MHz$
 $G = 13.89MHz$ 

> [!question]- ![[Pasted image 20240905141105.png]]
 $10*4K + 9*0.5K = 44.5KHz$

> [!question]- ![[Pasted image 20240905141317.png]]
 The first one experiences undersampling thus losing information
 The second one samples at twice the maximum frequency and does not lose information
 The third oversamples and does not lose information but is not efficient 

#NeedsFactCheckingByTrueAmericanPatriots 
> [!question]- ![[Pasted image 20240905141353.png]]
 $10 * 2M * 2 + 9 * 0.01M = 40.09MHz$ 
 Max = $40.09 / 10 = 4.009 MHz$ 

> [!question]- ![[Pasted image 20240905141426.png]]
 (a)
 $f_{max} = 12KHz$
 $C = 500MHz$
 $L = 64$
 $n = 6$
 $S = 2f_{max} = 24Kbaud$
 $R = 6 * 24K = 144Kb/s$ 
 Using 64-ASK
 $B_m = (1+d)R = 144KHz$ 
 (b)
 You can undersample or compress the data or use more efficient modulation like QAM

> [!question]-  ![[Pasted image 20240905141523.png]]
 (1)
 $n = 16$
 $f_{max} = 32KHz$ 
 $S = 2 * f_{max} = 64Kbaud$
 $R = nS = 1024Kb/s$
 (2)
 $A = 6V$
 $L = 4$
 $6/4 = 1.5V$ per level
 (3)
 It gets clamped down to the highest amplitude level, in this case 0b1111


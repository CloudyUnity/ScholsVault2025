
> [!question]- ![[Pasted image 20240804181713.png]]
> ![[Pasted image 20240804181725.png]]![[Pasted image 20240804181738.png]]![[Pasted image 20240804181753.png]]![[Pasted image 20240804181818.png]]

> [!question]- #schols  ![[Pasted image 20240805115010.png]]
 Base Case:
 $n = 1$
 $1^2 + 4(1) + 3 = 1 + 4 + 3 = 8$
 $8 = 8m, m \in \mathbb{Z}$ 
 .
 Assume true for $n=2k+1$ 
 $(2k+1)^2 + 4(2k+1) + 3 = 8m$
 $4k^2 + 4k + 1 + 8k + 4 + 3 = 8m$
 $4k^2 + 12k + 8 = 8m$ 
 .
 Prove for $n = 2k+3$ 
 $(2k+3)^2 + 4(2k+3)+3$
 $4k^2 + 12k + 9 + 8k + 12 + 3$
 $(4k^2 + 12k + 8) + 8k + 16$
 $8m + 8k + 16$
 $8(m + k + 2)$ 
 QED 

> [!question]- #schols  ![[Pasted image 20240805115020.png]]
 Assume true for $|x + x^{-1}| < 2$
 $(x + x^{-1})^2 < 2(x + x^{-1})$ 
 $x^2 + 2 + x^{-2} < 2x + 2x^{-1}$ 
 $x^2 - 2x + 2 - 2x^{-1} + x^{-2} < 0$ 
 $x^4 - 2x^3 + 2x^2 - 2x + 1 < 0$ 
 $(-1)^4 - 2(-1)^3 + 2(-1)^2 - 2(-1) + 1$
 $1 + 2 + 2 + 2 + 1 = 8$
 8 < 0
 Contradiction
 $\therefore |x + x^{-1}| \geq 2$ 

> [!question]- #schols  ![[Pasted image 20240805115121.png]]
 $(5^2)^n - 1$
 $25^n - 1$
 $(8(3) + 1)^n - 1$ 
  See workings for how I got to the next line
 $-1 + [1 + n(8(3)) + n(8^2 (3^2)) + \dots + n(8^{n-1}(3^{n-1}) +8^n (3^n)]$
 $-1 + 1 + 8[n(3) + n(8(3^2)) + \dots + n(8^{n-2}(3^{n-1}) + 8^{n-1}(3^n)]$
 $8[n(3) + n(8(3^2)) + \dots + n(8^{n-2}(3^{n-1}) + 8^{n-1}(3^n)]$
 $8m$ 
 .
 Workings:
 	Let $n = 1$
 	$-1 + (8(3) + 1)$
 	Let $n = 2$
 	$-1 + (8(3) + 1)(8(3) + 1) = -1 + 8^2(3^2) + 2(8)(3) + 1$
 	Let $n = 3$
 	$-1 + (8(3) + 1)(8^2(3^2) + 2(8(3)) + 1)$
 	$-1 + 8^3 (3^3)  + 2(8^2(3^2)) + 8(3) + 8^2(3^2) + 2(8(3)) + 1$
 	$-1 + 8^3 (3^3) + 3(8^2 (3^2)) + 3(8(3)) + 1$ 
 .
 Can this be done easier with prime number theory, modulo, FLT, something else?

#schols 
![[Pasted image 20240805115137.png]]

#schols 
![[Pasted image 20240805115328.png]]

#schols 
![[Pasted image 20240805115930.png]]

#schols 
![[Pasted image 20240805120535.png]]

#schols 
![[Pasted image 20240805120732.png]]

#schols 
![[Pasted image 20240805120916.png]]

#schols [2024]
![[Pasted image 20241027191313.png]]

#schols [2024]
![[Pasted image 20241027191323.png]]

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

> [!question]- #schols  ![[Pasted image 20240805115137.png]]
 $n = 1$
 $LHS = 1/2$
 $RHS = 1 - \dfrac{1}{1 + 1} = 1 - 1/2 = 1/2$ 
 $n = k$
 $\frac{1}{2} + \frac{1}{6} + \frac{1}{12} + \dots + \dfrac{1}{k(k+1)} = 1 - \dfrac{1}{k + 1}$ 
 $n = k+1$
 $\frac{1}{2} + \frac{1}{6} + \frac{1}{12} + \dots + \dfrac{1}{k(k+1)} + \dfrac{1}{(k+1)(k+2)} = 1 - \dfrac{1}{(k+1) + 1}$ 
 $1 - \dfrac{1}{k+1} + \dfrac{1}{(k+1)(k+2)} = 1 - \dfrac{1}{k+2}$ 
 $-\dfrac{1}{k+1} + \dfrac{1}{k+1} - \dfrac{1}{k+2} = - \dfrac{1}{k+2}$ 
 $LHS = RHS$

> [!question]- #schols  ![[Pasted image 20240805115328.png]]
Prove Forwards:
$n+3 = 2k+1$
$n = 2k - 2$
$3n = 3(2k - 2)$
$6k - 6 = 6(k - 1)$
$k - 1 \in \mathbb{Z}$
$\therefore$ QED
.
Prove backwards
$3n = 6M$
$n = 2M$
$n + 3 = 2M + 3$
$n + 3 = 2(M + 1) + 1$
$M + 1 \in \mathbb{Z}$
$\therefore$ QED 

> [!question]- #schols  ![[Pasted image 20240805115930.png]]
 (i)
 $f(5) = 43 \times 7 \times 3 \times 2 + 1 = 1807$
 $13 | 1807 \to 1807$ is not prime
 (ii)
 $m = max(j, k)$
 $n = min(j, k)$
 $m \neq n$ 
 $f(n)$ is a factor of $f(m) - 1$ 
 $\therefore f(n)$ is not a factor of $f(m)$ 
 $\therefore gcd(f(m), f(n)) =1$ 
 (iii)
  $f(n) = f(1) f(2) \dots f(n-1) + 1$
 $f(n+1) = f(1)f(2) \dots f(n-1) f(n) + 1$
 $f(n+1) = (f(n) - 1) f(n) +1$
 $f(n+1) = f(n)^2 - f(n) + 1$ 

> [!question]- #schols  ![[Pasted image 20240805120535.png]]
 $n = 1$
 $1 = 2^1 - 1 = 2 -1 = 1$
 $n = k$
 $1 + 2 + 4 + \dots + 2^{k-1} = 2^k - 1$ 
 $n = k+1$ 
 $LHS = 1 + 2 + 4 + \dots + 2^{k-1} + 2^k$
 $RHS = 2^{k+1} - 1$ 
 $2^k - 1 + 2^k$
 $2(2^k) - 1$
 $2^{k+1} - 1$ 
 $LHS = RHS$ 

> [!question]- #schols  ![[Pasted image 20240805120732.png]]
 $1 + 2 + 3 + \dots + n-1 = 0.5n(n - 1)$ 
 $n = 1$
 $0 = 0.5(1)(1-1) = 0.5(0) = 0$ 
 $n = k$
 $1 + 2 + 3 + \dots + k - 1 = 0.5k(k-1)$
 $n = k+1$
 $LHS = 1 + 2 + 3 + \dots + k - 1 + k$
 $RHS = 0.5(k+1)(k)$
 $LHS = 0.5k(k-1) + k$ 
 $0.5k(k-1) + 2(0.5k)$
 $0.5k(k-1 + 2) = 0.5k(k+1)$ 
 $LHS = RHS$

> [!question]- #schols  ![[Pasted image 20240805120916.png]]
 (i)
 $m = 2k+1$
 $n = 2p+1$ 
 $mn = (2k+1)(2p+1)$
 $4kp + 2k + 2p + 1$
 $2(2kp + k + p) + 1$ 
 (ii)
 $2^y = 3$
 $log_2 3 = y$ 
 Proof by contradiction
 Assume $log_2 3 = \frac{a}{b}$ 
 $a, b \in \mathbb{Z}$
 $b \neq 0$ 
 $b log_2 3 = a$ 
 $log_2 3^b = a$ 
 $3^b = 2^a$ 
 $3^b = 2k+1$
 $2^a = 2p$
 $2k + 1 \neq 2p \to$ Contradiction
 $\therefore \frac{a}{b} \notin \mathbb{Z} \to y \notin \mathbb{Z}$ 

> [!question]- #schols [2024] ![[Pasted image 20241027191313.png]]
 $m^2 = 102 - n^2$
 $m = \sqrt{102 - n^2}$ 
 Values of $k$ for which $\sqrt{102 - k} \in \mathbb{Z}$ 
 	$k = \{ 2, 21, 53, 66, 77, 86, 93, 98\}$
 	$n^2 = k$ 
 $\forall k_i \in k, \sqrt{k} \notin \mathbb{Q}$
 $\therefore n^2 \notin \mathbb{Q}$ 

> [!question]- #schols [2024] ![[Pasted image 20241027191323.png]]
 $a + b = 4M \to a - b = 4N$ 
 Assumptions to break:
 $a$ is odd
 $b$ is odd
 $a > b$ 
 Starting Point:
 $a + b = 4M$
 $a - b = 4N$
 .
 $2a = 4M + 4N$
 $a = 2(M + N)$
 $a$ is not odd
$\to$ Contradiction 


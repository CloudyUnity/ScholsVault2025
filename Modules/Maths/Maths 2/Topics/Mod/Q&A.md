
> [!question]- #schols  ![[Pasted image 20240805115407.png]]
I use euclids algorithm and bezouts identity to find the possible solution(s)
(i)
$15x + 25y \equiv 70$
 $-15x - 27y \equiv -18$
 $-2y \equiv 58$
 $26y \equiv 58$ 
 Make coprime
 $13y \equiv 29$ (mod 14)
 Find inverse of 13 mod 14
 $14 = 13 + 1$
 $1 = 14 - 13$
 $v = -1$ 
$y \equiv 29(-1)$ (mod 14)
 ! $y \equiv 13$ 
$3x + 5(13) \equiv 14$ (mod 28)
 $3x \equiv 5$ 
$5 = 3 + 2$
$3 = 2 + 1$
$1 = 3 - 2$
$2 = 5 - 3$
$1 = 3 - (5 - 3)$
$1 = (2)3 - 5$
$v = 2$
! $x \equiv 5(2) \equiv 10$ 
(ii)
$-x - 5y \equiv -3$
$3x \equiv -2$ (mod 9)
$9 = 3(3) + 0$
$gcd(9, 3) = 3$
Not coprime, and -2 is not divisible by 3 therefore there is no solution
(iii)
 $a = \{6, 17\}$ 
Mods are coprime and greater than 1 :)
 $m = 8 \times 25 = 200$ 
 $M = \{ 25, 8 \}$ 
Find inverse of 25 mod 8
Find inverse of 1 mod 8
$v = 1$
Find inverse of 8 mod 25
$25 = 3(8) + 1$
 $1 = 25 - (3)8$ 
 $v = -3$ 
 $v = \{1, -3\}$ 
 $x \equiv 6(1)(25) + 17(-3)(8)$ (mod 200)
 $x \equiv -258 \equiv 142$ (mod 200)

> [!question]- #schols  ![[Pasted image 20240805115637.png]]
$10^{241}$ mod 7
This is FLT
$10^{241} \equiv 10^{6(40) + 1} \equiv (10^{6})^{40}(10^1)$
 $10^6 \equiv 1$
 $1^{40} (10) = 10$ 
$r = 10$ 

> [!question]- #schols  ![[Pasted image 20240805120713.png]]
(i)
 $-12 \leq 0 \to 51 | -12 = \lceil \dfrac{51}{-12} \rceil = -4$ 
 $51 = (-4)(-12) + 3$
 $-12 = (-4)(3) + 0$
 $d = 3$ 
 (ii)
 $-12 \leq 0 \to -51 | -12 = \lceil \dfrac{-51}{-12} \rceil = 4$ 
 $-51 = 4(-12) - 3$ 
 $-12 = 4(-3) + 0$
 $d = -3$ 

> [!question]- #schols  ![[Pasted image 20240805121119.png]]
Find the inverse of 55 mod 34
Find the inverse of 21 mod 34
$34 = 21 + 13$
$21 = 13 + 8$
$13 = 8 + 5$
$8 = 5 + 3$
$5 = 3 + 2$
$3 = 2 + 1$
$d = 1$
Co-prime therefore there is an inverse
$13 = 34 - 21$
$8 = 21 - 13$
$5 = 13 - 8$
$3 = 8 - 5$
$2 = 5 -3$
$1 = 3-2$
$1 = 3 - (5 - 3) = (2)3 - 5$
$1 = (2)(8 - 5) - 5 = (2)8 - 3(5)$
$1 = (2)8 - 3(13 - 8) = (5)8 - 3(13)$
$1 = (5)(21 - 13) - 3(13) = (5)21 - 8(13)$
$1 = (5)21 - 8(34 - 21) = (13)21 - 8(34)$
$v = 13$
$55 (13) \equiv_{34} 1$ 

> [!question]- #schols  ![[Pasted image 20240805121135.png]]

> [!question]- #schols  ![[Pasted image 20240805121156.png]] ![[Pasted image 20240805121202.png]]
 See question above

> [!question]- #schols [2024] ![[Pasted image 20241027191433.png]]
 $a = \{2, 3, 10\}$
 $m_i = \{5, 7, 11\}$ 
 $m = 385$ 
 $M = \{77, 55, 35 \}$
 Inverse of 77 mod 5
 Inverse of 2 mod 5
 $5 = 2(2) + 1$
 $2 = (2)1 + 0$
 $1 = 5 - (2)2$ 
 $v = -2$
 Inverse of 55 mod 7
 Inverse of 6 mod 7
 $7 = 6 + 1$
 $1 = 7 - 6$
 $v = -1$ 
 Inverse of 35 mod 11
 Inverse of 2 mod 11
 $11 = (5)2 + 1$
 $1 = 11 - (5)2$
 $v = -5$ 
 $v = \{-2, -1, -5\}$ 
 $x \equiv_{385} 2(77)(-2) + 3(55)(-1) + 10(35)(-5) \equiv_{385} -2223 \equiv_{385} 87$ 

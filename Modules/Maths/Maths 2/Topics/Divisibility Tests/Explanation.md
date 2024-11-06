
$a = a_0 + a_1 \times 10 + a_2 \times 10^2 + \dots + a_n \times 10^n$

2:
	Last digit is even
4:
	Last two digits are divisible by 4
$2^n$:
	Last n-1 digits are divisible by $2^n$

3:
	$\sum_{i} a_{i}$ $\equiv$ 0 (mod 3)
	Repeatedly sum digits until 1 digit remains
	How it works:
		$10 \equiv 1$ (mod 3)
		$a = a_0 + a_1 + a_2 + \dots + a_n$
9:
	$\sum_{i} a_{i}$ $\equiv$ 0 (mod 9)

11:
	$\sum_i a_{i}(-1)^i \equiv 0$ (mod 11)
	Repeatedly alternating digit sum starting at unit digit
	How it works:
		$10 \equiv -1$ (mod 11)
		$a = a_0 - a_1 + a_2 - \dots$

n:
	Is divisible by 2 factors $f_1, f_2$ of n
	$r$ is the remainder on mod
	$r_n = f_{1} (r_{f_{2}}) - f_{2} (r_{f_{1}})$ (mod n)

7,13:
	$\sum_i (-1)^i [a_{i} + 10^i a_{i+1} + 10^{i+1} a_{i+2}] \equiv 0$ (mod 7)
	$\sum_i (-1)^i [a_{i} + 10^i a_{i+1} + 10^{i+1} a_{i+2}] \equiv 0$ (mod 13)
	How it works:
		$1001 = 7 \times 11 \times 13$
		$1000 \equiv -1$ (mod 7)
		$1000 \equiv -1$ (mod 13)
		$a = a_0 + (10) a_1+(10^2) a_2 - 1[a_3 + (10)a_4 + (10^2)a_5] + 1[...]$
		$a = a_2 \circ a_1 \circ a_0 - [a_5 \circ a_4 \circ a_3] + \dots$



Uses shift-and-add algorithm

$a$ is the multiplicand 
$B$ is the multiplier 
$P$ is the product 
$P_n$ is the nth step towards the product
	$P_0 = a$ 

Bit Products:
	$0 \leq i \leq n-1$ 
	$P_i = a_i \land B$
	$PP_j = \overset{j}{\sum} 2^i P_i = 2^j P_j + PP_{j-1}$ 
	$P = PP_{n-1}$ 

Algo Explained:
	$P = 0$
	while ($B \neq 0$)
		If $B_0 = 1$
			$P = P + a$ 
		$a <<= 1$ 
		$B >>= 1$
	or
	$P_i = B_i \land (a << i)$ 
	$P = \sum P_i$ 

Quick Head Maths:
	Write out each $i$ where $B_i = 1$ 
	Write out $a \circ (i\  0s)$ for each $i$  
	Sum all numbers, one at a time is probably least error prone

Example:
	$a = 10111$
	$B = 10011$
		$P_0 = 10111$
		$P_1 = 101110$
		$P_2 = 0$
		$P_3 = 0$
		$P_4 = 101110000$
	$P = 10111 + 101110 + 101110000$
	$P = 110110101$ 

Hardware Multiplication
	Keep track of rolling $a, B, P$ 
	Add to $P$ after each iteration
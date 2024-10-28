
> [!question]- #schols  ![[Pasted image 20240731152910.png]]
(a)
Construct a not gate using NAND gates
$A' = (AA)'$ 
Construct an or gate using NAND gates
 $A + B + C + \dots = (A'B'C' \dots)'$ 
Pretty simple from there, just connect the decoder outputs with ORs
Make sure to reuse the (4 or 6) between F1 and F3
(b)
$Y_0 = XNOR(A_0, B_0)$
$Y_1 = XNOR(A_1, B_1)$
$\dots$
 $Y_7 = XNOR(A_7, B_7)$ 
Seems too easy hmmmm

> [!question]- #schols  ![[Pasted image 20240731153414.png]]
xyzw - abcdefg
0000 - 1111110
0001 - 0110000
0010 - 1101101
0011 - 1111001
0100 - 0110011
0101 - 1011011
0110 - 1011111
0111 - 1110000
1000 - 1111111
1001 - 1111011
1010 - 0000000
1011 - 0000000
1100 - 0000000
1101 - 0000000
1110 - 0000000
1111 - 0000000
Make KMaps for each a, b, c, d, e, f, g to find boolean expressions in terms of x, y, z, w
Then just make the circuit. It's a lot of work but not too hard

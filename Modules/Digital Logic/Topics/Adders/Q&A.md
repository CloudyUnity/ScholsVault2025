
> [!question]- #schols  ![[Pasted image 20240731153723.png]]
(i)
000 - 001
001 - 010
010 - 011
011 - 100
100 - 010
101 - 011
110 - 100
111 - 101
KMAP:
![[{29CBE6E2-A7FD-4549-8B65-BD72B6B8E7ED}.png]]
![[{096FF6A2-B2C1-4CF1-BCE5-0994A1D43FCE}.png]]
![[{08765AE5-261D-4D57-A24B-EB3FC3C08DD2}.png]]
A = xy + yz
B = xy' + zy' = y'(x+z)
C = x'z' + xz = XNOR(x, z)
Now draw the circuit
(ii)
I0 I1 $C_i$ - S $C_o$ 
000 - 00
001 - 10
010 - 10
011 - 01
100 - 10 
101 - 01
110 - 01
111 - 11
Let I0 I1 be select bits for the muxes
Mux 1 will output into S
Mux 2 will output into $C_o$ 
Sel 0:
S = $C_i$ 
$C_o$ = 0
Sel 1:
S = $C_i$'
$C_o$ = $C_i$
Sel 2:
S = $C_i$'
$C_o$ = $C_i$ 
Sel 3:
S = $C_i$
$C_o$ = 1
S Mux takes in inputs ($C_i, C_i', C_i', C_i$)
C Mux takes in inputs ($0, C_i, C_i, 1$)



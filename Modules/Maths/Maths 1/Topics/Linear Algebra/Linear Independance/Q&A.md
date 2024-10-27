
> [!question]- #schols  ![[Pasted image 20240703145039.png]]
 (i)
 $n_{1, 2} = cross(v_1, v_2) = \begin{bmatrix} 4 - 3 \\ 3 + 2 \\ -1 - 2 \end{bmatrix} = (1, 5, -3)$
 $n_{2, 3} = cross(v_2, v_3) = \begin{bmatrix} 1 - 0 \\ 6 - 1 \\ 0 - 3 \end{bmatrix} = (1, 5, -3)$
 $n_{1, 2} = n_{2, 3} \to$ co-planar
 (ii)
Independent when $k_1 v_1 + k_2 v_2 + k_3 v_3 = 0 \leftrightarrow k_1, k_2, k_3 = 0$ 
 $Vk = \mathbf{0}$
 $\begin{bmatrix} 2 & 1 & 0 & 0 \\ 3 & 2 & 1 & 0 \\ -1 & 1 & 3 & 0 \end{bmatrix}$
 R1 <=> R3
 R1 <= -R1
 R2 <= R2 - 3R1
 R3 <= R3 - 2R1
 $\begin{bmatrix} 1 & -1 & -3 & 0 \\ 0 & 5 & 10 & 0 \\ 0 & 3 & 0 & 0 \end{bmatrix}$
 R3 <= R3 / 3
 R1 <= R1 + R3
 R2 <= R2 / 5
 R2 <= R2 - R3
 R2 <= R2 / 2
 R1 <= R1 + 3R2
 $\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \end{bmatrix}$
 $k_1 = k_2 = k_3 = 0 \to$ Linear Independent 

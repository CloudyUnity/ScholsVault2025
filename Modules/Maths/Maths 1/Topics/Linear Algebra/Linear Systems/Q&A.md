
> [!question]- #schols  ![[Pasted image 20240703145333.png]]
$x_1 + (c+1)x_3 + 3x_4 = c$
$x_1 + 3x_3 + 3x_4 = -c$
$(c+1 - 3)x_3 = 2c$
$x_3 = \dfrac{2c}{c-2}$
$c = 2$ 

> [!question]- #schols ![[Pasted image 20240703145535.png]]
$\begin{bmatrix} \gamma - 2 & 1 & -1 & -1 \\ 2 & \gamma - 2 & 2 & 1 \\ \gamma & -1 & 1 & 1 \end{bmatrix}$
R3 <= R3 - R1
$\begin{bmatrix} \gamma - 2 & 1 & -1 & -1 \\ 2 & \gamma - 2 & 2 & 1 \\ 0 & -2 & 2 & 2 \end{bmatrix}$
R3 <= R3 / 2
R1 <= R1 + R3
R2 <= R2 - 2R3
$\begin{bmatrix} \gamma - 2 & 0 & 0 & 0 \\ 2 & \gamma & 0 & -1 \\ 0 & -1 & 1 & 1 \end{bmatrix}$
R2 <= R2 + R1
$\begin{bmatrix} \gamma - 2 & 0 & 0 & 0 \\ \gamma & \gamma & 0 & -1 \\ 0 & -1 & 1 & 1 \end{bmatrix}$
$\gamma = 0 \to$ No Solutions (R2)
.
$\gamma = 2 \to$ Infinite Solutions (R1)
$\begin{bmatrix} 2 & 2 & 0 & -1 \\ 0 & -1 & 1 & 1 \\ 0 & 0 & 0 & 0 \end{bmatrix}$
$2a + 2b = -1$
$a = \dfrac{-1 - 2b}{2}$
$-b + c = 1$
$c = 1+b$
 $v = \begin{bmatrix} \dfrac{-1 - 2t}{2} \\ t \\ 1 + t \end{bmatrix}$ 
.
Let $\gamma = 1$
$\begin{bmatrix} 1 & 0 & 0 & 0 \\ 1 & 1 & 0 & -1 \\ 0 & -1 & 1 & 1 \end{bmatrix}$
R2 <= R2 - R1
R3 <= R3 + R2
$\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & -1 \\ 0 & 0 & 1 & 0 \end{bmatrix}$
$a = 0, b = -1, c = 0$
$\gamma = 1 \to$ One Solution

> [!question]- #schols ![[Pasted image 20240703145644.png]]
 It has at least one solution for $\mathbf{x}$ 

> [!question]- #schols  ![[Pasted image 20240703150302.png]]
$\begin{bmatrix} 1 & a & -1 & 1 \\ -1 & a - 2 & 1 & -1 \\ 2 & 2 & a - 2 & 1 \end{bmatrix}$
R1 <= R1 + R2
R3 <= R3 + 2R2 
R2 <= -R2
$\begin{bmatrix} 0 & 2a - 2 & 0 & 0 \\ 1 & 2 - a & -1 & 1 \\ 0 & 2a - 2 & a & -1 \end{bmatrix}$
R3 <= R3 - R1
$\begin{bmatrix} 0 & 2a - 2 & 0 & 0 \\ 1 & 2 - a & -1 & 1 \\ 0 & 0 & a & -1 \end{bmatrix}$
$a = 0 \to$ No Solution (R3)
$a = 1 \to$ Infinite Solutions
$\begin{bmatrix} 1 & 1 & -1 & 1 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{bmatrix}$
$\begin{bmatrix} 1 & 1 & 0 & 0 \\ 0 & 0 & 1 & -1 \\ 0 & 0 & 0 & 0 \end{bmatrix}$
$x = -y$
$z = -1$
 $v = \begin{bmatrix} t \\ -t \\ -1 \end{bmatrix}$ 
$a = 2 \to$ One Solution
$\begin{bmatrix} 1 & 0 & -1 & 1 \\ 0 & 2 & 0 & 0 \\ 0 & 0 & 1 & -0.5 \end{bmatrix}$
$\begin{bmatrix} 1 & 0 & 0 & 0.5 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & -0.5 \end{bmatrix}$
$x = 0.5, y = 0, z = -0.5$ 

> [!question]- #schols  ![[Pasted image 20240703150314.png]]
$x_1 = x^2, x_2 = xy, x_3 = y^2$
$\begin{bmatrix} 1 & 1 & -1 & 1 \\ 2 & -1 & 3 & 13 \\ 1 & 3 & 2 & 0 \end{bmatrix}$
R2 <= R2 - 2R1
R3 <= R3 - R1
$\begin{bmatrix} 1 & 1 & -1 & 1 \\ 0 & -3 & 5 & 11 \\ 0 & 2 & 3 & -1 \end{bmatrix}$
R3 <= R3 / 2
R1 <= R1 - R3
R2 <= R2 + 3R3
$\begin{bmatrix} 1 & 0 & -2.5 & 1.5 \\ 0 & 0 & 9.5 & 9.5 \\ 0 & 1 & 1.5 & -0.5 \end{bmatrix}$
R2 <= R2 / 9.5
R1 <= R1 + 2.5R2
R3 <= R3 - 1.5R2
$\begin{bmatrix} 1 & 0 & 0 & 4 \\ 0 & 0 & 1 & 1 \\ 0 & 1 & 0 & -2 \end{bmatrix}$
$x^2 = 4 \to x = \pm 2$
 $xy = -2$ 
 $y^2 = 1 \to y = \pm 1$ 
$x = 2, y=-1 \lor x=-2, y=1$ 

> [!question]- #schols  ![[Pasted image 20240703150210.png]]
R2 <= R2 - R3
R1 <= R1 - R2
$\begin{bmatrix} 0 & 0 & b - 2 & b -2 \\ a & 0 & 2 & 4 - b \\ 0 & a & 2 & b \end{bmatrix}$
R1 <= R1 / (b-2)
R2 <= R2 - 2R1
R3 <= R3 - 2R1
 $\begin{bmatrix} 0 & 0 & 1 & 1 \\ a & 0 & 0 & 3 - b \\ 0 & a & 0 & b - 1 \end{bmatrix}$ 
$a = 1 \to$ One Solution
$\begin{bmatrix} 1 & 0 & 0 & 3 - b \\ 0 & 1 & 0 & b - 1 \\ 0 & 0 & 1 & 1 \end{bmatrix}$
$v = \begin{bmatrix} 3 - b \\ b - 1 \\ 1 \end{bmatrix}$
For any value of b there is one solution
$a = 0, b =0 \to$ No Solution
$\begin{bmatrix} 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & 3 \\ 0 & 0 & 0 & -1 \end{bmatrix}$
R2 and R3 are contradictions thus there is no solution


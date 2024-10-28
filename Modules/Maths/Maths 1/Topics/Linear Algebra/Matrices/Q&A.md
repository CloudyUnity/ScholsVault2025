
> [!question]- #schols ![[Pasted image 20240703144527.png]]
> $det(A) = 1 \begin{vmatrix} b & b^2 \\ c & c^2 \end{vmatrix} - a \begin{vmatrix} 1 & b^2 \\ 1 & c^2 \end{vmatrix} + a^2 \begin{vmatrix} 1 & b \\ 1 & c \end{vmatrix}$
> $det(A) = b c^2 - b^2 c - a (c^2 - b^2) + a^2 (c - b)$
> 1: $b = c \to det(A) = c c^2 - c^2 c - a(c^2 - c^2) + a^2 (c - c) = 0$
> 2: $a = b \to det(A) =  a c^2 - a^2 c - a(c^2 - a^2) + a^2 (c - a)$
> $ac^2 - a^c - ac^2 + a^3 + a^2 c - a^3 = 0$
> 3: $a = c \to det(A) = b a^2 - b^2 a - a(a^2 - b^2) + a^2 (a - b)$
> $b a^2 - b^2 a - a^3 + a b^2 + a^3 - ba^2 = 0$
> $\Rightarrow (det(A) = 0) \leftrightarrow (a = b) \lor (b = c) \lor (a = c)$

> [!question]- #schols ![[Pasted image 20240703145316.png]]
> $4A (A' B) B' A^T (A^T)' B' B B^T - 2A B^T (A' B')^T A^T (B')^T B^T ((A^T)')^T$
> $4 B^T - 2 I$
> $4 \begin{bmatrix} 3 & 2 & 1 \\ -1 & 2 & -1 \\ 2 & -1 & 0 \end{bmatrix}^T - 2 \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$
> $\begin{bmatrix} 10 & -4 & 8 \\ 8 & 6 & -4 \\ 4 & -4 & -2 \end{bmatrix}$

> [!question]- #schols ![[Pasted image 20240703145734.png]]
> $A^{-1} = \dfrac{1}{det(A)} (\tilde A)^T$
> $A^T det(A) = (\tilde A)^T$
> $det^T (A) A = \tilde A$
> $det(A) A = \tilde A$

> [!question]- #schols ![[Pasted image 20240703145352.png]]
> Key to this question is to ignore any expressions that look like they won't contain $x^4$ or $x^3$
> 1: $x \begin{vmatrix} x & 1 & 2 \\ x & 2 & 3 \\ 1 & 2 & 2x \end{vmatrix}$
> $x(x(x^2 - 6) - (2x - 3) + 2(4 - x))$
> $x^4$
> 2: $\begin{vmatrix} x & 1 & 2 \\ 1 & x & 3 \\ x & 2 & 2x \end{vmatrix}$
> $x(2x^2 - 6) - (2x - 3x) + 2(2 - x^2)$
> $2x^3$
> 3: $2 \begin{vmatrix} x & x & 2 \\ 1 & 2 & 3 \\ x & 1 & 2x \end{vmatrix}$
> $2(x(4x - 3) - x(2x - 3x) + 2(1-2x))$
> None
> 4: $3 \begin{vmatrix} x & x & 1 \\ 1 & 2 & x \\ x & 1 & 2 \end{vmatrix}$
> $3(x(4 - x) - x(2-x^2) + (1-2x))$
> $3x^3$
> $x^4 + 2x^3 + 3x^3$
> $x^4 + 5x^3$

> [!question]- #schols  ![[Pasted image 20240703145548.png]]
> $\begin{vmatrix} 1 & x \\ x & 1 \end{vmatrix} - x \begin{vmatrix} x & x \\ x & 1 \end{vmatrix} + x \begin{vmatrix} x & 1 \\ x & x \end{vmatrix} = 0$
> $(1 - x^2) - x(x - x^2) + x(x^2 - x) = 0$
> $2x^3 - 3x^2 + 1 = 0$
> Use tables in calculator (Hopefully allowed)
> $x = 1$
> $(2x^3 - 3x^2 + 1) \div (x - 1) = 2x^2 + x + 1$
> $x = -\dfrac{1}{4} \pm \dfrac{7}{4} i$

> [!question]- #schols ![[Pasted image 20240703150031.png]]
> $-1 \begin{vmatrix} -1 & 1 \\ 1 & -1 \end{vmatrix} - 1 \begin{vmatrix} 1 & 1 \\ 1 & -1 \end{vmatrix} + 1 \begin{vmatrix} 1 & -1 \\ 1 & 1 \end{vmatrix}$
> $-(1-1) - (-1-1) + (1+1) = 2 + 2 = 4$

> [!question]- #schols  ![[Pasted image 20240703150103.png]]
> $\tilde B = \begin{bmatrix} \begin{vmatrix} -1 & 1 \\ 1 & -1 \end{vmatrix} & -\begin{vmatrix} 1 & 1 \\ 1 & -1 \end{vmatrix} & \begin{vmatrix} 1 & -1 \\ 1 & 1 \end{vmatrix} \\ -\begin{vmatrix} 1 & 1 \\ 1 & -1 \end{vmatrix}  & \begin{vmatrix} -1 & 1 \\ 1 & -1 \end{vmatrix} & -\begin{vmatrix} -1 & 1 \\ 1 & 1 \end{vmatrix} \\ \begin{vmatrix} 1 & 1 \\ -1 & 1 \end{vmatrix} & -\begin{vmatrix} -1 & 1 \\ 1 & 1 \end{vmatrix} & \begin{vmatrix} -1 & 1 \\ 1 & -1 \end{vmatrix} \end{bmatrix}$
> $\tilde B = \begin{bmatrix} 0 & 2 & 2 \\ 2 & 0 & 2 \\ 2 & 2 & 0 \end{bmatrix}$
> $(\tilde B )^T = \tilde B$
> $det(\tilde B) = 0 - 2(-4) + 2(4) = 16$

> [!question]- #schols  ![[Pasted image 20240703150424.png]]
> $Q Q^T = (a^2 + b^2 + c^2 + d^2) I$
> $Q Q^T = kI$
> $Q Q^T Q^{-T} = kI Q^{-T}$
> $Q = k Q^{-T}$
> $Q^{-1} = k^{-1} Q^T$
> $Q^{-1} = \dfrac{1}{a^2 + b^2 + c^2 + d^2} Q^T$

> [!question]- #schols [2024] ![[Pasted image 20241027191051.png]]
 $\begin{bmatrix} -4 + \lambda & -4 & 4 \\ -1 & \lambda & 1 \\ -7 & -6 & 7 + \lambda \end{bmatrix}$
 Determinant must be zero
 $(-4 + \lambda)(\lambda (7 + \lambda) + 6) + 4 (-(7 + \lambda) + 7) + 4 (6 + 7 \lambda ) = 0$
 $(-4 + \lambda) (\lambda^2 + 7\lambda + 6) - 28 - 4 \lambda + 28 + 24 + 28 \lambda = 0$
  $-4 \lambda^2 - 28 \lambda - 24 + \lambda^3 + 7 \lambda^2 + 6 \lambda - 4 \lambda + 24 + 28 \lambda = 0$
 $\lambda^3 + 3 \lambda^2 + 2 \lambda = 0$
  $\lambda = 0$
 $\lambda^2 + 3\lambda + 2 = 0$
 $\lambda = -1, -2$ 
 

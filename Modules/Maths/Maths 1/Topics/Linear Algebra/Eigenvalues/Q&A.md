
> [!question]- #schols  ![[Pasted image 20240703145054.png]]
 $\begin{bmatrix} a - \lambda_1 & 1 & b & 0 \\ c & 7 - \lambda_1 & 0 & 0 \\ 3 & d & 2 - \lambda_1 & 0 \end{bmatrix}$
 $x_1 = 1$
 $x_2 = 0$
 $x_3 = 3$
 $a - \lambda_1 + 3b = 0$
 ! $c = 0$
 $3 + 3(2 - \lambda_1) = 0$
 $2 - \lambda_1 = -1$
 ! $\lambda_1 = 3$
 $\begin{bmatrix} a - \lambda_2 & 1 & b & 0 \\ 0 & 7 - \lambda_2 & 0 & 0 \\ 3 & d & 2 - \lambda_2 & 0 \end{bmatrix}$
 $x_1 = 3$
 $x_2 = 4$
 $x_3 = 1$
 $3(a - \lambda_2) + 4 + b = 0$
 $0 + 4(7 - \lambda_2) + 0 = 0$
 ! $\lambda_2 = 7$
 $9 + 4d + (2 - 7) = 0$
 ! $d = -1$
 $a - 3 + 3b = 0$
 $a + 3b = 3$
 $3(a - 7) + 4 + b = 0$
 $3a + b = -4 + 21 = 17$
 $-3a - 3b = -9$
 $-2b = 8$
 ! $b = -4$
 $a + 3(-4) = 3$
 ! $a = 15$ 

There must be a better way of doing this one, right?
> [!question]- #schols  ![[Pasted image 20240703145431.png]]
 $\begin{bmatrix} - \lambda & 1 & 0 & 0 &  \dots & 0 & 0 \\ 0 & -\lambda & 1 & 0 & \dots & 0 & 0 \\ 0 & 0 & -\lambda & 1 & \dots & 0 & 0 \\ \dots & \dots & \dots & \dots & \dots & \dots & \dots \\ 0 & 0 & 0 & 0 & \dots & -\lambda & 1 \\ 10^{10} & 0 & 0 & 0 & \dots & 0 & -\lambda \end{bmatrix}$
 $C_2 = \begin{vmatrix} -\lambda & 1 \\ 0 & -\lambda \end{vmatrix} = \lambda^2$
 $C_3 = \begin{vmatrix} -\lambda & 1 & 0 \\ 0 & -\lambda & 1 \\ 0 & 0 & -\lambda \end{vmatrix}$
 $C_3 = -\lambda (C_2) - 1(0) = -\lambda^3$
 $C_4 = \begin{vmatrix} -\lambda & 1 & 0 & 0 \\ 0 & -\lambda & 1 & 0 \\ 0 & 0 & -\lambda & 1 \\ 0 & 0 & 0 & \lambda \end{vmatrix}$
 $C_4 = -\lambda (C_3) - 1(0) = \lambda^4$
 $C_n = (-\lambda)^n$ 
 $C_{10} = -\lambda (C_9) - 1 \begin{vmatrix} 0 & 1 & 0 & \dots & 0 & 0 \\ 0 & -\lambda & 1 & \dots & 0 & 0 \\ \dots & \dots &\dots & \dots & \dots & \dots \\ 0 & 0 & 0 & \dots & -\lambda & 1 \\ 10^{10} & 0 & 0 & \dots & 0 & -\lambda \end{vmatrix}$
 Get determinant from column 1 rather than row 1
 Matrix of Signs for $10^{10} \to -1$ 
 $C_{10} = -\lambda (C_9) - (-10^{10} V_8)$ 
 $V_8 = \begin{vmatrix} 1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\ -\lambda & 1 & 0 & 0  & 0 & 0 & 0 & 0 \\ 0 & -\lambda & 1 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & -\lambda & 1 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & -\lambda & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & -\lambda & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & -\lambda & 1 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & -\lambda & 1 \end{vmatrix}$
 $V_8 = 1 V_7$
 $V_7 = 1V_6$
 ...
 $V_3 = 1$ 
 $C_{10} = -\lambda(-\lambda^9) + 10^{10}(1)$
 $\lambda^{10} + 10^{10} = 0$  

> [!question] #schols  ![[Pasted image 20240703145601.png]]
 $Av = \lambda v$
 $B v = \mu v$ 
 $mAv = m\lambda v$
 $n Bv = n \mu v$
 $mAv + nBv = m \lambda v + n \mu v$
 $(mA + nB)v = (m\lambda + n \mu)v$
 Eigenvalue = $m\lambda + n\mu$ 

> [!question]- #schols  ![[Pasted image 20240703145946.png]]
 (i)
 $A^{-1} = \begin{bmatrix} -1 & -1 \\ -2 & 1 \end{bmatrix} / (-1 - 2)$
 $A^{-1} = \begin{bmatrix} 1/3 & 1/3 \\ 2/3 & -1/3 \end{bmatrix}$ 
 $A^{-1} B = \begin{bmatrix} 1/3(5) + 1/3 (-6) & 1/3(-3) + 1/3(2) \\ 2/3(5) + 1/3(6) & 2/3(-3) - 1/3(2) \end{bmatrix}$
 $A^{-1} B = \begin{bmatrix} -1/3 & -1/3 \\ 16/3 & -8/3 \end{bmatrix}$
 $A^{-1} BA = \begin{bmatrix} -1/3 - 2/3 & -1/3 + 1/3 \\ 16/3 - 16/3  & 16/3 + 8/3 \end{bmatrix}$
 $A^{-1} BA = \begin{bmatrix} -1 & 0 \\ 0 & 8 \end{bmatrix}$
 $(A^{-1}BA)^8 = \begin{bmatrix} 1 & 0 \\ 0 & 8^8 \end{bmatrix}$ 
 (ii)
 $\begin{vmatrix} 5 - \lambda & -3 \\ -6 & 2 - \lambda \end{vmatrix} = 0$
 $(5 - \lambda) (2 - \lambda) - (-3)(-6) = 0$
 $10 - 7 \lambda + \lambda^2 - 18 = 0$
 $\lambda^2 - 7\lambda - 8 = 0$
 $\lambda = 8, -1$
 Equal to the non-zero entries in $A^{-1} BA$ 
 (iii)
 $\begin{bmatrix} -3 & -3 & 0 \\ -6 & -6 & 0 \end{bmatrix}$
 $x_1 = -x_2$
 $v = t \begin{bmatrix} 1 \\ -1 \end{bmatrix}$ 
 $\begin{bmatrix} 6 & -3 & 0 \\ -6 & 3 & 0 \end{bmatrix}$
 $2x_1 = x_2$
 $v = t \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ 
 Eigenvectors equal to columns of $A$ 
 (iv)
 $\begin{bmatrix} 1 & 0 \\ 0 & 8^8 \end{bmatrix} = A^{-1} B^8 A$
 $A \begin{bmatrix} 1 & 0 \\ 0 & 8^8 \end{bmatrix} A^{-1} = A A^{-1} B^8 A A^{-1} = B^8$
 $B^8 = \begin{bmatrix} 1 & 8^8 \\ 2 & -8^8 \end{bmatrix} A^{-1}$
 $B^8 = \begin{bmatrix} 1(1/3) + 8^8 (2/3) & 1(1/3) + 8^8 (-1/3) \\ 2/3 - 8^8 (2/3) & 2/3 - 8^8 (-1/3) \end{bmatrix}$
 $B^8 = \begin{bmatrix} 11184811 & -5592405 \\ -11184810 & 5592406 \end{bmatrix}$ 
 #NeedsFactCheckingByTrueAmericanPatriots 

> [!question]- #schols  ![[Pasted image 20240703150221.png]]
 (i)
 $\begin{vmatrix} -7 - \lambda & -6 & -12 \\ 5 & 5 - \lambda & 7  \\ 1 & 0 & 4 - \lambda  \end{vmatrix} = 0$
 $A = (-7 - \lambda)((5-\lambda)(4 - \lambda) - 0)$
 $A = (-7 - \lambda)(20 - 9 \lambda + \lambda^2)$
 $A = -140 + 63 \lambda - 7 \lambda^2 - 20 \lambda + 9 \lambda^2 - \lambda^3$
 $B = 6 (5(4 - \lambda) - 7)$
 $B = 6(20 - 5 \lambda - 7)$
 $B = 78 - 30 \lambda$
 $C = -12 (0 - (5 - \lambda))$
 $C = 60 - 12 \lambda$ 
 $A + B + C = 0$
 $-\lambda^3 + 2 \lambda^2 + 43 \lambda  - 30 \lambda - 12 \lambda - 140 + 78 + 60 = 0$
 $\lambda^3 - 2 \lambda^2 - \lambda + 2 = 0$
 $\lambda = -1, 1, 2$ 
 .
 $\begin{bmatrix} -6 & -6 & -12 & 0 \\ 5 & 6 & 7 & 0 \\ 1 & 0 & 5 & 0 \end{bmatrix}$
 $\begin{bmatrix} 1 & 1 & 2 & 0 \\ 0 & 1 & -3 & 0 \\ 0 & 0 & 3 & 0 \end{bmatrix}$
 $\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \end{bmatrix}$
 $v = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$
 $\begin{bmatrix} -8 & -6 & -12 & 0 \\ 5 & 4 & 7 & 0 \\ 1 & 0 & 3 & 0 \end{bmatrix}$
 $\begin{bmatrix} 2 & 3 & 6 & 0 \\ 0 & 4 & -8 & 0 \\ 1 & 0 & 3 & 0 \end{bmatrix}$
 $\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \end{bmatrix}$
 $\begin{bmatrix} -9 & -6 & -12 & 0 \\ 5 & 3 & 7  & 0 \\ 1 & 0 & 2 & 0 \end{bmatrix}$
 $\begin{bmatrix} 3 & 2 & 4 & 0 \\ 0 & 3 & -3 & 0 \\ 1 & 0 & 2 & 0 \end{bmatrix}$
 $\begin{bmatrix} 1 & 0 & 2 & 0 \\ 0 & 2 & -2 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}$
 $x_1 = -2x_3$
 $x_2 = -x_3$ 
 $v = t\begin{bmatrix} -2 \\ -1 \\ 1 \end{bmatrix}$ 
 (ii)
   $\tilde{S} = \begin{bmatrix}  2 - 1 & -(3 - 1) & 3 - 2 \\ -(-3 + 2) & -5 + 2 & -(-5 + 3) \\ -3 + 4 & -(-5 + 6) & -10 + 9 \end{bmatrix}$
 $\tilde{S} = \begin{bmatrix} 1 & -2 & 1 \\ 1 & -3 & 2 \\ 1 & -1 & -1 \end{bmatrix}$
 $\tilde{S}^T = \begin{bmatrix} 1 & 1 & 1 \\ -2 & -3 & -1 \\ 1 & 2 & -1 \end{bmatrix}$
  $det(S) = -5(2 - 1) + 3(3 - 1) - 2(3 - 2) = -5 + 6 - 2 = -1$
 $S^{-1} = \begin{bmatrix} -1 & -1 & -1 \\ 2 & 3 & 1 \\ -1 & -2 & 1   \end{bmatrix}$
 $S^{-1} B = \begin{bmatrix} 7 -5 - 1 & 6 - 5 & 12 - 7 - 4 \\ -14 + 15 + 1 & -12 + 15 & -24 + 21 + 4 \\ 7 - 10 + 1 & 6 - 10 & 12 - 14 + 4  \end{bmatrix}$
 $S^{-1}B = \begin{bmatrix} 1 & 1 & 1 \\ 2 & 3 & 1 \\ -2 & -4 & 2 \end{bmatrix}$
 $S^{-1}BS = \begin{bmatrix} -5 + 3 + 1 & -3 + 2 + 1 & -2 + 1 + 1 \\  -10 + 9 + 1 & -6 + 6 + 1 & -4 + 3 + 1 \\ 10 - 12 + 2 & 6 - 8 + 2 & 4 - 4 + 2 \end{bmatrix}$
 $S^{-1}BS = \begin{bmatrix} -1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 2 \end{bmatrix}$ 

> [!question]- #schols  ![[Pasted image 20240703150328.png]]
 $\begin{bmatrix} 5 - \lambda & -3 & 2 \\ 6 & -4 - \lambda & 4 \\ 4 & -4 & 5 - \lambda \end{bmatrix}$
 $(5- \lambda)((-4 - \lambda)(5 - \lambda) + 16) + 3(6(5 - \lambda) - 16) + 2(-24 - 4(-4 - \lambda))$
 $(5 - \lambda)(-20 + 4 \lambda - 5 \lambda + \lambda^2 + 16) + 3(30 - 6 \lambda - 16) + 2(-24 + 16 + 4 \lambda)$
 $(5 - \lambda) (\lambda^2 - \lambda - 4) + 42 - 18 \lambda -16 + 8 \lambda$
 $5 \lambda^2 - 5 \lambda - 20 - \lambda^3 + \lambda^2 + 4\lambda + 26 - 10 \lambda = 0$
 $-\lambda^3 + 6 \lambda^2 - 11 \lambda + 6 = 0$
 $\lambda^3 - 6\lambda^2 + 11\lambda - 6 = 0$ 
 $\lambda = 1, 2, 3$ 
 .
 $\begin{bmatrix} 4 & -3 & 2 \\ 6 & -5 & 4 \\ 4 & -4 & 4 \end{bmatrix}$
 $\begin{bmatrix} 0 & 1 & -2 \\ 0 & 1 & -2 \\ 1 & -1 & 1 \end{bmatrix}$
 $\begin{bmatrix} 0 & 1 & -2 \\ 1 & 0 & -1 \\ 0 & 0 & 0 \end{bmatrix}$ 
 $x_2 - 2x_3 =0$
 $x_1 - x_3 = 0$
 $v = t \begin{bmatrix} 1 \\ 2 \\ 1 \end{bmatrix}$
 $\begin{bmatrix} 3 & -3 & 2 \\ 6 & -6 & 4 \\ 4 & -4 & 3 \end{bmatrix}$
 $\begin{bmatrix} 1 & -1 & 1 \\ 0 & 0 & -1 \\ 0 & 0 & 0 \end{bmatrix}$
 $\begin{bmatrix} 1 & -1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix}$
 $x_1 - x_2 = 0$
 $x_3 = 0$
  $v = t \begin{bmatrix} 1 \\ 1 \\ 0 \end{bmatrix}$
 $\begin{bmatrix} 2 & -3 & 2 \\ 6 & -7 & 4 \\ 4 & -4 & 2 \end{bmatrix}$
 $\begin{bmatrix} 2 & -3 & 2 \\ 0 & 2 & -2 \\ 0 & -10 & -2 \end{bmatrix}$
 $\begin{bmatrix} 2 & 0 & -1 \\ 0 & 1 & -1 \\ 0 & 0 & -12 \end{bmatrix}$
$\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$
 $v = \mathbf{0}$ 

> [!question]- #schols  ![[Pasted image 20240703150437.png]]



> [!question]- #schols #bonus  ![[Pasted image 20240703150125.png]]


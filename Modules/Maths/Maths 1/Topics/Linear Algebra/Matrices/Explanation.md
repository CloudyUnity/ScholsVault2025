$A A^{-1} = I$

For any matrix transformation the inverse is the opposite transformation
	For example a matrix representing a translation of (0, 5, 0), the inverse is a translation of (0, -5, 0). Multiply them together and they cancel out

If a matrix has an inverse then we say it is invertible

Calculating the inverse:
	$2 \times 2$ matrix:
		$A^{-1} = \dfrac{1}{det(A)} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$
		Flip main diagonal
		Negate others

Inverse from the matrix of cofactors:
	$A^{-1} = \dfrac{1}{det(A)} (\tilde{A})^T$
	This is the only way to get 3x3 inverses

$(ABC)^{-1} = C^{-1} B^{-1} A^{-1}$

$2 \times 2$ determinant:
	$\begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - bc$

$3 \times 3$ determinant:
	$\begin{vmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{vmatrix} = a_{11} M_{11} - a_{12} M_{12} + a_{13} M_{13}$
	Remember to follow the matrix of signs
	You can choose any row or column in the matrix to calculate the determinant from

$det(A) = 0 \to$ A is a singular matrix
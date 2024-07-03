$A A^{-1} = I$

For any matrix transformation the inverse is the opposite transformation
	For example a matrix representing a translation of (0, 5, 0), the inverse is a translation of (0, -5, 0). Multiply them together and they cancel out

If a matrix has an inverse then we say it is invertible

Calculating the inverse:
	$2 \times 2$ matrix:
		$A^{-1} = \dfrac{1}{det(A)} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$
		Flip main diagonal
		Negate others
	$3 \times 3$ matrix:
		TODO

Inverse from the matrix of cofactors:
	$A^{-1} = \dfrac{1}{det(A)} (\tilde{A})^T$

$(ABC)^{-1} = C^{-1} B^{-1} A^{-1}$

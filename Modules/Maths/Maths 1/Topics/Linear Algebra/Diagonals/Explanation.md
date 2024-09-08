A diagonal matrix is a square matrix with values only on the main diagonal
	$D = diag(3, 6, 4) = \begin{bmatrix} 3 & 0 & 0 \\ 0 & 6 & 0 \\ 0 & 0 & 4 \end{bmatrix}$

A scalar matrix is a multiple of the identity matrix
	For example:
		$0.5I =\begin{bmatrix} 0.5 & 0 \\ 0 & 0.5 \end{bmatrix}$

Diagonal matrices are easily raised to a power
	$diag(k_1, k_2, \dots, k_n)^p = diag(k_1^p, k_2^p, \dots, k_n^p)$

A square matrix A is diagonalisable if there exists an invertible matrix P such that:
	$D = P^{-1} A P$

A square matrix is diagonalisable IFF:
	Its eigenvectors are linearly independent IFF:
		Each eigenvalues geometric multiplicity equals its algebraic multiplicity

P is formed from a matrix where each column is an eigenvector
	If the eigenvector has parameter t, assume t is a constant. Pick one that makes the maths easy

$D = diag(\lambda_1, \lambda_2, \dots, \lambda_n)$

$D^k = (P^{-1} A P)^k = (P^{-1} A P)(P^{-1} A P) \dots (P^{-1} A P) = P^{-1} A^k P$
$A^k = P D^k P^{-1}$

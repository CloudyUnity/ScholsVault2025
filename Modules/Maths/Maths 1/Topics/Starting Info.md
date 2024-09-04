Dot Product:
	Two Component Vectors:
		$p \cdot q = p_{x} q_{x} + p_{y} q_{y}$
	Three Component Vectors:
		$p \cdot q = p_{x} q_{x} + p_{y} q_{y} + p_{z} q_{z}$
	CosTheta:
		$p \cdot q = ||p|| ||q|| cos(\theta)$
	Results:
		1 = Parallel (Same Direction)
		0 = Perpendicular
		-1 = Parallel (Opposite Direction)

Cross Product:
	$\begin{bmatrix} a_{1} \\ a_{2} \\ a_3 \end{bmatrix} \times \begin{bmatrix} b_1 \\ b_2 \\ b_3 \end{bmatrix} = \begin{bmatrix} a_1 b_2 - a_2 b_1 \\ a_2 b_3 - a_3 b_2 \\ a_3 b_1 - a_1 b_3 \end{bmatrix}$
	Works with any n sized vectors. Always start with $a_1$ 
	Cross two vectors to find a new vector perpendicular to the two:
		$v_1 \times v_2 = v_{\perp}$

Matrix:
	$\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix}$
	An $m \times n$ grid of numbers used for representing the state of a graph or transformation in space
	m rows and n columns

Square Matrix:
	Matrix with the same number of rows and columns

Transpose:
	$\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} ^T = \begin{bmatrix} a_{11} & a_{21} \\ a_{12} & a_{22} \end{bmatrix}$
	$(ABC)^T = C^T B^T A^T$

Identity Matrix:
	$I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$
	For any $m \times m$ matrix it is always 1s along the main diagonal. It must be square
	Any matrix or vector multiplied by the identity matrix equals itself ($AI = A$)
		In the same way 1 is the identity scalar (x * 1 = x)

Matrix Minor:
	The minor $M_{ij}$ of a $n \times n$ matrix A is the determinant of A with the i-th row and j-th column deleted

Matrix of Signs:
	$\begin{bmatrix} + & - & + \\ - & + & - \\ + & - & + \end{bmatrix}$
	Starting with the top left as $+$ form a checkerboard pattern
	Can be any sized matrix

Matrix of Cofactors:
	$\tilde{A} = \begin{bmatrix} M_{11} & -M_{12} & \dots \\ -M_{21} & M_{22} & \dots \\ \vdots & \vdots & \end{bmatrix}$
	Use the matrix of signs

Adjoint:
	$adj(A) = (\tilde{A})^T$
	$A \  adj(A) = det(A) I$

The Zero Vector:
	$\overline{0} = (0, 0, 0)$

#bonus
Transformations:
	A matrix can represent a transformation in space (Often 2D or 3D)
	For 3D we need a 4x4 matrix
	How transformations are represented within the matrix depends on whether its in a right-handed or left-handed coordinate system
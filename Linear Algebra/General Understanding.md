Matrix:
	$\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix}$
	An nxn grid of numbers used for representing the state of a graph or transformation in space

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

Transpose:
	$\begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} ^T = \begin{bmatrix} a_{11} & a_{21} \\ a_{12} & a_{22} \end{bmatrix}$

Identity Matrix:
	$I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$
	For any nxn matrix it is always 1s along the main diagonal
	Any matrix or vector multiplied by the identity matrix equals itself ($AI = A$)
		In the same way 1 is the identity scalar (x * 1 = x)

Transformations:
	A matrix can represent a transformation in space (Often 2D or 3D)
	For 3D we need a 4x4 matrix
	How transformations are represented within the matrix depends on whether its in a right-handed or left-handed coordinate system, and whether its row-major or column-major

Inverse:
	$A A^{-1} = I$
	For any matrix transformation the inverse is the opposite transformation
		For example a matrix representing a translation of (0, 5, 0), the inverse is a translation of (0, -5, 0). Multiply them together and they cancel out

Matrix of Cofactors:

Matrix of Signs:

Implicit vs Parametric Equations:

Parametric Sphere Equation:
	$(R cos(\theta) sin(\phi), R sin(\theta) sin(\phi), R cos(\phi))$

Row-Major vs Column-Major:

Adjoint:
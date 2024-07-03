$\overline v$ is a linear combination of $\overline v_1, \overline v_2, \dots, \overline v_n$ if there exists scalars $k_1, k_2, \dots, k_n$ such that:
	$\overline v = k_1 \overline v_1, k_2 \overline v_2, \dots k_n \overline v_n$

Express $\overline v$ as a linear combination of $\overline v_1, \overline v_2, \overline v_3$:
	$k_1 \begin{bmatrix} a_1 \\ a_2 \\ a_3 \end{bmatrix} + k_2 \begin{bmatrix} b_1 \\ b_2 \\ b_3 \end{bmatrix} + k_3 \begin{bmatrix} c_1 \\ c_2 \\ c_3 \end{bmatrix} = \begin{bmatrix} v_x \\ v_y \\ v_z \end{bmatrix}$
	Solve for $k_1, k_2, k_3$
	$A \overline k = \overline v$
	Apply Gaussian Elimination

Vectors $\overline v_1, \overline v_2, \dots, \overline v_n$ are linearly independent if none of them is a linear combination of the others

$k_1 \overline v_1 + k_2 \overline v_2 + \dots + k_n \overline v_n = \overline 0$ is only true when $k_1 = k_2 = \dots = k_n = 0$

Vectors are linearly independent if $A \overline k = \overline 0 \to \overline k = \overline 0$

The set of all linear combinations of a set of vectors is their span
	(They do not have to be linearly independent)

Assuming vectors are in $\mathbb{R}^m$, if these vectors span all of $\mathbb{R}^m$ they are a complete set

Colinear:
	Points on the same line

Coplanar:
	Points on the same plane

![[Pasted image 20240702150846.png]]
We'll use a right-handed coordinate system. Point the thumb in the z+ direction and curl fingers from x to y

Implicit Equations:
	2D: $f(x, y) = 0$
	3D: $f(x, y, z) = 0$
	For example:
		$y - mx - c = 0$
		$f(x, y) = y - mx - c$

Parametric Equations:
	2D: $x = f_1 (t)$, $y = f_2 (t)$
	3D: $x = f_1 (s, t)$, $y = f_2 (s,t)$, $z = f_3 (s,t)$
	For example:
		$x = cos(\theta)$, $y = sin(\theta)$

Parametric Sphere Equation:
	$x = R cos(\theta) sin(\phi)$
	$y = R sin(\theta) sin(\phi)$
	$z = R cos(\phi))$

An inclination or normal vector is a vector pointing perpendicular to a plane and represents the orientation of the plane

Finding the implicit equation of a plane given a point $P$ and a normal vector $\overline{n}$:
	Plane = $\forall X (\overrightarrow{PX} \perp \overline{n})$
	$\overrightarrow{PX} \perp \overline{n} \to \overrightarrow{PX} \cdot \overline{n} = 0$
	$\begin{bmatrix} X_x - P_x \\ X_y - P_y \\ X_z - P_z \end{bmatrix} \cdot \begin{bmatrix} n_x \\ n_y \\ n_z \end{bmatrix}= 0$
	$n_x (X_x - P_x) + n_y (X_y - P_y) + n_z (X_z - P_z) = 0$
$n_x (x - P_x) + n_y (y - P_y) + n_z (z - P_z) = 0$

Finding the implicit equation of a plane given a point $P$ and two vectors $\overline{u}, \overline{v}$:
	Cross the two vectors to find the normal vector $\overline{n}$, then solve as above

Finding the parametric equation of a plane given a point $P$ and two vectors $\overline{u}, \overline{v}$:
	$X = P + \overline{u} s + \overline{v} t$
		$x = P_x + u_{x} s + v_{x} t$
		$y = P_y + u_{y} s + v_{y} t$
		$z = P_z + u_{z} s + v_{z} t$

Finding the parametric equation of a plane given a point $P$ and a normal vector $\overline{n}$:
	Cross $\overline{n}$ with $-\overline{n}$ to find a random vector $\overline{u}$ along the plane
	Cross $\overline{n}$ with $\overline{u}$ to find another vector $\overline{v}$ along the plane
	Solve as above

Finding the implicit equation of a line given a point $P$ and a parallel vector $\overline{u}$:
	Plane = $\forall X (\overrightarrow{PX} \mid\mid \overline{u})$
	$\overrightarrow{PX} \mid\mid \overline{u} \to \overrightarrow{PX} \times \overline{u} = \overline{0}$
	$\begin{bmatrix} X_x - P_x \\ X_y - P_y \\ X_z - P_z \end{bmatrix} \times \begin{bmatrix} u_x \\ u_y \\ u_z \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$
	$(y - P_y) u_z - (z - P_z) u_y = 0$
	$(z - P_z) u_x - (x - P_x) u_z = 0$
	$(x - P_x) u_y - (y - P_y) u_x = 0$
	$\frac{x - P_x}{u_x} = \frac{y - P_y}{u_y} = \frac{z - P_z}{u_z}$

Finding the parametric equation of a line given a point $P$ and a parallel vector $\overline{u}$:
	$X = P + \overline{u} t$
	$x = P_x + u_x t$
	$y = P_y + u_y t$
	$z = P_z + u_z t$

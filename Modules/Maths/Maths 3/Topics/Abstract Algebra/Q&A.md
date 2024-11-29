
> [!question]- #schols [2023] ![[{06D2CE9A-EC53-49A5-B7F8-43A4AD0F217A}.png]]
  (i)
 To prove semigroup we need:
 Closure on BO,
  Associativity on BO
 $\dfrac{p}{2^n} \times (\dfrac{q}{2^m} \times \dfrac{k}{2^p}) = \dfrac{pqk}{2^n 2^m 2^p} = (\dfrac{p}{2^n} \times \dfrac{q}{2^m}) \times \dfrac{k}{2^p}$ 
 $\therefore$ There is associativity 
 .
 $\dfrac{p}{2^n} \times \dfrac{q}{2^m} = \dfrac{pq}{2^{n+m}}$ 
 $p,q \in \mathbb{N}, p,q \geq 1, p, q$ is odd $\to pq \in \mathbb{N}, pq \geq 1, pq$ is odd
 $n, m \in \mathbb{N} \to n + m \in \mathbb{N}$ 
 $\therefore$ There is closure
 (ii)
 $\dfrac{p}{2^n} + \dfrac{q}{2^m} = \dfrac{p(2^m) + q(2^n)}{2^{n+m}}$ 
 $p(2^m) + q(2^n) = 2(p(2^{m-1} + q(2^{n-1})))$
 $\therefore$ The numerator is not odd and thus there is not closure

> [!question]- #schols [2022] ![[{E6CD5337-38B6-47CA-B5EC-107D93A37A37}.png]]
 Proving Closure:
 $a \sqrt 2 + b(1 + i \sqrt 3) + c \sqrt 2 + d(1 + i \sqrt 3)$
 $(a + c) \sqrt 2 + (b + d)(1 + i \sqrt 3)$ 
 $a + c \in \mathbb{Z}$
 $b + d \in \mathbb{Z}$
 $\therefore$ There is closure
 Proving Associativity: 
 $p(a, b) = a \sqrt 2 + b (1 + i\sqrt 3)$
 $(p(a, b) + p(c, d)) + p(e, f) = (a + c + e) \sqrt 2 + (b + d + f) (1 + i \sqrt 3) = p(a, b) + (p(c, d) + p(e, f))$ 
 Proving Identity:
 $a \sqrt 2 + b(1 + i \sqrt 3) + 0 \sqrt 2 + 0(1 + i \sqrt 3) = a \sqrt 2 + b(1 + i \sqrt 3)$ 
 $0 \in \mathbb{Z}$ 
 $\therefore$ Identities exist for all elements of $A$ 
 Proving Inverses:
 $a \sqrt 2 + b(1 + i \sqrt 3) + (-a) \sqrt 2 + (-b)(1 + i \sqrt 3) = 0 \sqrt 2 + 0(1 + i \sqrt 3)$ 
 $-a, -b \in \mathbb{Z}$ 
 $\therefore$ Inverses exist for all elements of $A$ 

> [!question]- #schols [2021] ![[{0F00BD4E-EBA3-443B-9113-BCC1883BD9EF}.png]]
 Proving Closure:
 $3x_1 - y_1 + 2 z_1 = 0$
 $x_1 + 2y_1 + 3z_1 = 0$
 $3x_2 - y_2 + 2z_2 = 0$
 $x_2 + 2y_2 + 3z_2 = 0$ 
 .
 $3 x_1 + 3x_2 - y_1 - y_2 + 2z_1 + 2z_2 = 0$
 $3(x_1 + x_2) - (y_1 + y_2) + 2(z_1 + z_2) = 0$
 $x_1 + x_2 + 2y_1 + 2y_2 + 3z_1 + 3z_2 = 0$
 $(x_1 + x_2) + 2(y_1 + y_2) + 3(z_1 + z_2) = 0$
 $\therefore (x_1 + x_2, y_1 + y_2, z_1 + z_2) \in A$ 
 Proving Associativity:
 $((x_1, y_1, z_1) + (x_2, y_2, z_2)) + (x_3, y_3, z_3) = (x_1 + x_2 + x_3, y_1 + y_2 + y_3, z_1 + z_2 + z_3) = (x_1, y_1, z_1) + ((x_2, y_2, z_2) + (x_3, y_3, z_3))$ 
 Proving Identities:
 $(x_1, y_1, z_1) + (0, 0, 0) = (x_1 + 0, y_1 + 0, z_1 + 0) = (x_1, y_1, z_1)$ 
 $(0, 0,0) \in \mathbb{R}^3$ 
 $\therefore$ An identity exists for all elements of $A$ 
 Proving Inverses:
 $(x_1, y_1, z_1) + (-x_1, -y_1, -z_1) = (x_1 - x_1, y_1-y_1, z_1-z_1) = (0, 0, 0) = e$ 
 $(-x_1, -y_1, -z_1) \in \mathbb{R}^3$
$\therefore$ An inverse exists for all elements of $A$ 

> [!question]- #schols [2020] ![[{7269DDD1-0B7A-4E9B-82A8-B46035562110}.png]]
(i)
An operation that can be applied on every pair of two elements in a set that returns a value
(ii)
A set paired with a closed associative binary operation
(iii)
A semigroup where there exists an identity element in the set where for every element in the set: The binary operation applied on the element and identity returns the element
(iv)
A monoid where for every element in the set there exists an inverse element also in the set which when the binary operation is applied on them it returns the identity element
(v)
A set for which an identity element exists in the set where for every element in the set: The binary operation applied on the element and identity returns the element
(vi)
A set for which for every element in the set there exists an inverse element also in the set which when the binary operation is applied on them it returns the identity element

> [!question]- #schols [2020] ![[{BCDA5A41-68A0-481F-8151-C47A41CA8633}.png]]
 (i)
 Semigroup as the identity $0$ is not in $\mathbb{Z}^+$ 
 (ii)
 Monoid as the inverses are not in $\mathbb{Z} \backslash \mathbb{Z^+}$ 
 (iii)
 Group as all inverses are in $\mathbb{Z}$ 
 (iv)
 Group as all inverses are in $\mathbb{Z}$ 
 (v)
 $f_e = x \mapsto x$ 
 $f_a = x \mapsto f(x)$ 
 $f_{a^{-1}} = f(x) \mapsto x$ 
 The functions need to bijective for an inverse to exist which isn't specified 
 Thus it is a monoid 
 (vi)
 Now that the functions are invertible an inverse exists for all elements of the set
Thus it is now a group

> [!question]- #schols [2020] ![[{E9821831-D56C-49FC-ABF3-BF8C2AE5BC9C}.png]]
 $(A, *, e)$ is a monoid
 Not all elements are necessarily invertible otherwise it would be a group
 $a \in A, a * a' = e$ 
 $b \in A, b * b' = e$ 
 $(a*b) * (b'*a')$ 
 $a*(b * b') * a'$
 $a * e * a'$
 $a * a'$
 $e$ 

> [!question]- #schols [2020] ![[{44C5977C-BC9D-4DA0-B231-6D5DCB6BD22C}.png]]

$\forall s_1 \in R, s_2 \in S, s_1 \neq s_2$ 
	$s_2 \in [s_1]_{\sim} \to s_2 \notin R$ 
Let's call all $s \in R$ core elements of $S$ 
$S$ has $|R|$ core elements. All other elements of $S$ are related to exactly one other core element 
$u \sim v \leftrightarrow (w \circ u) \sim (w \circ v) \leftrightarrow (u \circ w) \sim (v \circ w)$ 
There is no identity for $(S, \circ)$ or $(R, *)$ 
.
As $*$ is specified as a binary operation it is closed by definition
.
Prove Associative:
Prove $a * (b * c) = (a * b) * c$ 
$\sim$ is an ER which means $\circ$ and $*$ can be swapped
$a \sim b \leftrightarrow a * c \sim b * c$ 



> [!question]- #schols [2018] ![[{4025F390-B0F0-4F30-AF71-90EA52931410}.png]]
 (a)
 Commutativity is when $a * b = b * a$ 
 $A \triangle B = (A - B) \cup (B - A) = (B - A) \cup (A - B) = B \triangle A$
 $A \triangle B = B \triangle A$ 
 (b)
 Yes
 $e = \emptyset$
 $A \triangle \emptyset = (A - \emptyset) \cup (\emptyset - A) = (A) \cup \emptyset = A$ 
 (c)
 $A \triangle A = (A - A) \cup (A - A)$ 
 Every element is its own inverse 
 (d)
Proof by contradiction
Assume $\nexists A, A = B \triangle C$ 
This would imply that $B \triangle C \notin P(\mathbb{N})$ 
Which implies there exists an element $x \in B \triangle C, x \notin \mathbb{N}$
But that is impossible as both $\cup$ and $-$ are closed for sets
Contradiction
$\therefore \exists A, A = B \triangle C$ 

> [!question]- #schols [2017] ![[{8DFEEF8E-0C9F-48DE-BB89-B4F7A86289F3}.png]]
 (a)
Prove forwards:
 $f$ being bijective implies there is a 1-1 correspondence between the inputs and the outputs
 Thus for all elements $x, x \mapsto f(x)$ there exists another function $f^{-1}$ which can map from the output to the input
 $f^{-1} : B \to A, f(x) \mapsto x$ 
 (b)
 Prove Closure:
 $\forall f_a, f_b \in \Upgamma$ 
 $f_a * f_b (x) = f_a(f_b(x))$ 
 $f_a, f_b : \mathbb{R} \to \mathbb{R}$ 
 $f_a (f_b(x)) : \mathbb{R} \to \mathbb{R} \to \mathbb{R} : \mathbb{R} \to \mathbb{R}$ 
 Composition on bijective functions also returns a bijective function as it's a 1-1-1 correspondence which is the same as a 1-1 correspondence 
 .
 Prove Associativity:
 $\forall f_a, f_b, f_c \in \Upgamma$ 
 $f_a * (f_b* f_c) = f_a(f_b(f_c(x)))) = (f_a * f_b) * f_c$ 
 (c)
 The identity element $f_e$ is the function that maps $x \mapsto x$ 
 $\forall f_a \in \Upgamma$ 
 $f_a * f_e = f_a(f_e(x))$ 
 $f_e(x) = x$
 $f_a(f_e(x)) = f_a(x)$ 
  Thus $(\Upgamma, *)$ is a monoid
  (d)
 All functions in $\Upgamma$ are bijective, thus they are invertible as proven in (a)
 Thus $\forall f \in \Upgamma, \exists f^{-1}$ s.t $f * f^{-1} = f_e$ 
 $f * f^{-1} (x) = f(f^{-1}(x))$
 $f * f^{-1} : x \mapsto f(x) \mapsto x$ 
 $\therefore f(f^{-1}(x)) = x$ 
 $\therefore$ There exists an inverse for all elements of $\Upgamma$ 
$\therefore (\Upgamma, *)$ is a group

> [!question]- #schols [2013] ![[{513EA847-BA07-4732-A8C3-ABCBD4A7886B}.png]]
![[{D692F2CB-40CD-44C1-82A8-474D931CDF8E}.png]]
 (a)
To prove transitivity: $xRy \land yRz \to xRz$
 Assume $a \sim b \land b \sim c$
 $s*a = b*s$
 $p*b = c * p$
 Prove $\exists k \in A, k * a = c * k$ 
 $p * b * s * a = c * p * b * s$
 $(p * b * s) * a = c * (p * b * s)$
 $k = p * b * s$
 $k * a = c * k$
 .
 (b)
 To prove reflexivity: $xRx = 1$ 
 $\forall x \in A, \exists s \in A, s * x = x * s$ 
 This is not commutativity as it is $\exists s$ not $\forall s$ 
 One value for $s$ where this is always true is $x$
 $x * x = x* x$
 $\therefore \ \sim$ is reflexive 
 .
 (c)
  To prove it is an ER it needs to be symmetric
 Prove $x \sim y \to y \sim x$ 
 Assume $(s * x = y * s)$
 Prove $(p * y = x * p)$ 
 We know every element in $A$ has an inverse
 $s^{-1} * s * x = s^{-1} * y * s$ 
 $x = s^{-1} * y *s$
 $x * s^{-1} = s^{-1} * y * s * s^{-1}$
$x * s^{-1} = s^{-1} * y$
 $p = s^{-1}$ 
 $\therefore \ \sim$ is symmetric
 $\therefore \ \sim$ is an ER
 .
 (d)
 Partial Order $\to$ Anti-Symmetric $\to$ ($x\sim y \land y \sim x \to x = y$)
 Prove $*$ is commutative ($x * y = y * x$)
 $(s * x = y * s) \land (s * y = x * s) \to x = y$ 
Start with the LHS and go to the RHS. See that commutativity is required to finish
 $s * x = y *s$
 $p * y = x * p$
 $x = s^{-1} * y * s$
 $p * y = s^{-1} * y * s * p$ 
 $y = p^{-1} * s^{-1} * y * s * p$
 This proves that $*$ is commutative as its the only way to make $y=y$ in the above equation 
 .
 (e)
 Prove $f(u) = g(u) = u \to \exists h \in A, h \circ f = g \circ h$ 
 $e = f_e : x \mapsto x$ 
 $f(u) = g(u) = u \to f = g = f_e$ 
 $h \circ f = h \circ f_e = h = f_e \circ h = g \circ h$ 
$h \circ f = g \circ h$ 
 
 > [!question]- ![[Pasted image 20241017121106.png]]
 (a)
 Yes as $3^p \times 3^q = 3^q \times 3^p$ thus the BO is associative 
 (b)
Yes as $3^p \times 3^0 = 3^p$ where $3^0 = e$ 
 (c)
 No as there are no numbers where $3^p \times 3^q = 3^0$ where $p, q \neq 0$ 
 $3^{pq} = 3^0$
 $pq = 0$
 Impossible

> [!question]- ![[Pasted image 20241017121708.png]]
> (a)
 Yes as $(x_1, y_1) + (x_2, y_2) = (x_2, y_2) + (x_1, y_1)$
 (b)
 Yes as $(x_1, y_1) + (0, 0) = (x_1, y_1)$ 
 (c)
$x_1 + 2y_2 = 0$
 Inverse $= (-x_1, -y_2)$
 $-x_1 - 2y_2 = 0 \leftrightarrow x_1 + 2y_2 = 0$
 Yes all elements have an inverse
 (d)
  A line
> [!question]- ![[{C8145A82-7824-4B6F-8639-366D92EF86A9}.png]]
 (a)
 This is a group as $+$ is both closed and associative
 $a + (b + c) = (a + b) + c = a + b + c$ 
 There exists an identity $0$ 
 $\forall a, a + 0 = a$ 
 And all elements have an inverse
 $\forall a, a + (-a) = 0$ 
 .
 (b)
 This is also a group as $+$ is closed an associative 
 $2p + (2q + 2k) = (2p + 2q) + 2k = 2p + 2q + 2k$ 
 There exists an identity 0
 $\forall a, a + 0 = a$ 
 All elements have an inverse 
 $\forall a, a + (-a) = 0$
 $-a \in E$ 
 .
 (c)
 Prove $f(a + b) = f(a) + f(b)$ 
 $f(a + b) = 2(a + b) = 2(a) + 2(b)$
 $f(a) + f(b) = 2(a) + 2(b)$ 
 $\therefore f$ is a homomorphism
 .
 (d)
 Prove $f(a) = f(b) \to a = b$ 
 $2a = 2b$
 $a = b$ 
 $\therefore f$ is injective
 .
 Every output is mapped
 $\forall a \in E, \exists n, f(n) = a$ 
 $n = 0.5a$ 
 $a = 2p, p \in \mathbb{Z}$ 
 $n = 0.5(2p) = p$ 
 $n \in \mathbb{Z}$ 
 $\therefore f$ is surjective
 $\therefore f$ is bijective
 $\therefore f$ is an isomorphism

> [!question]- ![[{C8145A82-7824-4B6F-8639-366D92EF86A9}.png]]
 (a)
 This is a group as $+$ is both closed and associative
 $a + (b + c) = (a + b) + c = a + b + c$ 
 There exists an identity $0$ 
 $\forall a, a + 0 = a$ 
 And all elements have an inverse
 $\forall a, a + (-a) = 0$ 
 .
 (b)
 This is also a group as $+$ is closed an associative 
 $2p + (2q + 2k) = (2p + 2q) + 2k = 2p + 2q + 2k$ 
 There exists an identity 0
 $\forall a, a + 0 = a$ 
 All elements have an inverse 
 $\forall a, a + (-a) = 0$
 $-a \in E$ 
 .
 (c)
 Prove $f(a + b) = f(a) + f(b)$ 
 $f(a + b) = 2(a + b) = 2(a) + 2(b)$
 $f(a) + f(b) = 2(a) + 2(b)$ 
 $\therefore f$ is a homomorphism
 .
 (d)
 Prove $f(a) = f(b) \to a = b$ 
 $2a = 2b$
 $a = b$ 
 $\therefore f$ is injective
 .
 Every output is mapped
 $\forall a \in E, \exists n, f(n) = a$ 
 $n = 0.5a$ 
 $a = 2p, p \in \mathbb{Z}$ 
 $n = 0.5(2p) = p$ 
 $n \in \mathbb{Z}$ 
 $\therefore f$ is surjective
 $\therefore f$ is bijective
 $\therefore f$ is an isomorphism

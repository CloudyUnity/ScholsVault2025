
> [!question]- #schols [2019] ![[{184BA602-E730-41CB-AAA6-2971CC371369}.png]]
 (a)
 $\varphi$ is bijective $\leftrightarrow \varphi^{-1}$ exists
 $\varphi_0$ is the identity element as it rotates by zero angles
 $\varphi_0 (z) = z$ 
 $\forall \theta \in \mathbb{R}, \varphi_{\theta} \circ \varphi_{-\theta} = \varphi_0$ 
 (b)
 Prove Closure:
 $\varphi_a \circ \varphi_b$ is a rotation of $a$ then $b$ angles
 This is equivalent to $\varphi_{a+b}$ 
 $a + b \in \mathbb{R}$ 
 $\therefore \varphi_{a+b} \in \Phi$
 $\therefore$ Closure
 Prove Associativity:
 $\varphi_a \circ (\varphi_b \circ \varphi_c) (z) = \varphi_a (\varphi_b (\varphi_c (z))) = (\varphi_a \circ \varphi_b) \circ \varphi_c (z)$ 
 Prove Identity:
 Done
 Prove Inverses:
 Done
 $\therefore \Phi$ is a group
 (c)
 Prove reflexivity:
 $\varphi_a (z) = \varphi_a (z)$ is true
 Prove transitivity:
 Assume $\varphi_a (z) = \varphi_b (z)$
 Assume $\varphi_b (z) = \varphi_c (z)$
Prove $\varphi_a (z) = \varphi_c (z)$
  $\varphi_a (z) = \varphi_b (z) = \varphi_c (z)$ by transitivity of $=$ 
Prove symmetry:
 Assume $\varphi_a (z) = \varphi_b (z)$ 
  $\varphi_b (z) = \varphi_a (z)$ by symmetry of $=$ 
 $\therefore \ \sim$ is an ER
 (d)
 Assuming $\theta$ is in radians
 $\Phi \backslash \sim \  = \{ \varphi_{\theta} | \ \theta \in \mathbb{R}, 0 < \theta < 2 \pi \}$ 

> [!question]- #schols [2018] ![[{0BAE4996-501F-4DF7-9993-2F4E03023290}.png]]
 $xRy \to yRx$ 
 $\lnot xRx$ 
 $xRy \land yRz \not\to xRz$ 
 .
 $xRy \leftrightarrow x \neq y$ 

> [!question]- #schols [2017] ![[{480FD349-3C9A-4768-A892-0297AE0F1550}.png]]
Equality
$x=y \to y = x$
$\therefore$ Reflexive
$x = y \land y = z \to x = z$
$\therefore$ Transitive 
$x = y \to y = x$
$\therefore$ Symmetric
$\therefore$ ER
$x = y \land y = x \to x = y$
$\therefore$ Antisymmetric 
$\therefore$ Partial Order

> [!question]- #schols [2014] ![[{3BDCFF66-36B3-450E-8C70-A3542811CA25}.png]]
 (a)
 $\lambda$ is the function to add $n$ to $i$ while modding by 8
 $\sigma$ is just a rotation shift as you swap the $ith$ bit with the $(i + n)th$ (mod 8) bit 
 .
 Prove reflexivity:
 $x = \sigma_0 (x)$ is true
 $\therefore xQx$ 
 .
 Prove transitivity:
 Assume $x = \sigma_n (y)$ 
 Assume $y = \sigma_m (z)$ 
 $x = \sigma_n (\sigma_m (z))$ 
 $\sigma_n \circ \sigma_m = \sigma_{n+m}$ 
 $n + m \in \mathbb{Z}$ 
 $x = \sigma_{n+m} (z)$ 
 $\therefore xQy \land yQz \to xQz$ 
 .
 Prove symmetry:
 Assume $y = \sigma_n (x)$ 
 $\sigma_n \circ \sigma_{-n} = \sigma_0$ 
 $\sigma_{-n} (y) = \sigma_{-n} (\sigma_n (x)) = x$
 $\therefore xQy \to yQx$ 
 $\therefore Q$ is an ER
 .
 Prove anti-symmetry:
 Assume $y = \sigma_n (x)$ 
 Assume $x = \sigma_m (y)$ 
 $x = \sigma_m \circ \sigma_n (x)$
 $\sigma_m \circ \sigma_n$ is not necessarily $\sigma_0$ 
 $\therefore Q$ is not anti-symmetric
 $\therefore Q$ is not a partial order
 .
 (b)
 $R_w = x \& w = y \& w$ 
 $x R_w x$ is true
 Prove transitivity:
 $x R_w y \land y R_w z$
 $x \& w = y \& w$
 $y \& w = z \& w$ 
 $x \& w = y \& w = z \& w$
 $x \& w = z \& w$ 
 Prove symmetry:
 Prove $x \& w = y \& w \to y \& w = x \& w$
 Proven true by symmetry of $=$ 
 $\therefore R_w$ is a ER for all values of $w$ 
 Prove anti-symmetry:
 Prove $(x \& w = y \& w) \land (y \& w = x \& w) \to x = y$ 
 Only true when $w = 0$ 

> [!question]- ![[{7A3E6924-CFA2-442C-85DD-009F8B9246F4}.png]]
> Yes as $x - x = 0 = (x - x)(x + 2x)$
> No as swapping x and y leads to a different equation
> $xQy \land yQz$
> $xQy := (x-y)(x + 2y) - (x-y) = 0$
> $xQy := (x- y)(x + 2y - 1) = 0$
> $xQy := x = y \lor x + 2y = 1$
> $y = 1 - 2z$
> $x + 2(1 - 2z) = 1$
> $x + 2 - 4z = 1$
> $x - 4z = -1$
> Assume $x = 3, z = 1, y = -1$
> $x + 2y = 3 + 2(-1) = 1$
> $y + 2z = -1 + 2 = 1$
> $x + 2z = 3 + 2 = 5 \neq 1$
> Not transitive by counter example
> Not an equivalence relation as not symmetric or transitive

> [!question]- ![[{2CF014D3-34CD-4B14-AF25-9F31FD546688}.png]]
> $cos(x) = cos(-x)$
> $cos(x) = cos(x + 2n \pi)$
> $[x]_R = \{x + 2n \pi | n \in \mathbb{Z}\} \cup \{-x + 2p \pi | p \in \mathbb{Z}\}$

> [!question]- ![[{C8C36D65-21CE-4EB7-A5AE-F6EC8EFC52AD}.png]]
> (i)
> $xQy := (x-y)(x + 2y) - (x-y) = 0$
> $xQy := (x- y)(x + 2y - 1) = 0$
> $xQy := x = y \lor x + 2y = 1$
> If $x \neq y$ then $xQy := x + 2y = 1$
> For $xQy$ we need $y + 2x = 1$ which only holds true with $x + 2y = 1$ when $x = y$
> Thus it is not symmetric
> (ii)
> $Q$ is reflexive as $xQx$ is true
> See above question for transitivity explanation
> Not a partial order



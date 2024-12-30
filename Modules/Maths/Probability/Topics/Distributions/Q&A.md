
> [!question]- #schols [2024] ![[Pasted image 20241027193209.png]]
 (i)
 $E(X^n) = \sum x^n P(X = x)$ 
 $E(X^n) = \sum x^n \dfrac{\lambda^x e^{-\lambda}}{x!}$
 $E(X^n) = \sum x x^{n-1} \dfrac{\lambda^x e^{-\lambda}}{x!}$
 $E(X^n) = \sum \dfrac{x}{x!} x^{n-1} \lambda^x e^{-\lambda}$
 $E(X^n) = \sum \dfrac{1}{(x-1)!} x^{n-1} \lambda^x e^{-\lambda}$
 $E(X^n) = \lambda \sum x^{n-1} \dfrac{\lambda^{x-1} e^{-\lambda}}{(x-1)!}$ 
 $E(X^n) = \lambda \sum x^{n-1} P(X = x-1)$
 $j = x-1$ 
 $E(X^n) = \lambda \sum (j+1)^{n-1} P(X = j)$ 
 $X$ has been shifted forward by +1 
 $E(X^n) = \lambda E((X+1)^{n-1})$ 
 (ii)
 $E(X^3) = \lambda E((X+1)^{2})$ 
 $\lambda \sum (x + 1)^2 P(X = x)$ 
 $\lambda \sum (x^2 + 2x + 1) P(X = x)$ 
 $\lambda (P(X=0) + (4)P(X=1))$
 $\lambda P(X=0) + 4\lambda P(X=1)$ 

> [!question]- #schols [2024] ![[Pasted image 20241027193224.png]]
 $X \sim Unif(0, 0.5)$
 $Y \sim Unif(0.5, 1)$
 .
 $f_X(x) = \dfrac{1}{0.5 - 0} = 2$ 
 $f_Y(y) = \dfrac{1}{1 - 0.5} = 2$ 
 .
 $P(X > 1/3) = \int^x _{1/3} 2 \ dx = 2x - 2/3$ 
 .
 $X$ and $Y$ are independent thus,
 $f_{X,Y} (x, y) = 2 \times 2 = 4$ 
 $P(Y - X > 1/3) = P(Y > X + 1/3)$ 
 $0 < X + 1/3 < Y < 1$ 
 $X + 1/3 < 0.5 \to X < 1/6$ 
 $P(Y - X > 1/3) = \int^{1/6} _0 \int^{1} _{x + 1/3} 4 \ dy\  dx$
 $\int ^{1/6} _0 4 - 4x - 4/3 \ dx$ 
 $4x - 2x^2 - \frac{4}{3} x |^{1/6} _0$ 
 $4(1/6) - 2(1/6)^2 - \frac{4}{3} (1/6) = \frac{7}{18}$ 

> [!question]- #schols  [2023] ![[{502FE453-F29D-441A-BE6D-F4B70AE26089}.png]]
 (i)
 $X \sim Pois(\mu_1)$ 
 $Y \sim Pois(\mu_2)$ 
 $P(X = x) = \dfrac{\lambda^x e^{-\lambda}}{x!}$
 $P(Y = y) = \dfrac{\lambda^y e^{-\lambda}}{y!}$
 $P(X = x, Y = y) = P(X = x) P(Y = y)$
 $P(X = x, Y = y) = \dfrac{\lambda^{x +y} e^{-2\lambda}}{x!y!}$ 
 (ii)
 Find $P(X + Y \leq 1)$ 
 Remember this is discrete
 The lower bound of $X$ and $Y$ are 0 as you can't have negative errors
 $(X + Y \leq 1) = \{(0, 0), (1, 0), (0, 1)\}$ 
 $P(X + Y \leq 1) = \sum P(X = x, Y = y)$
 $P(X + Y \leq 1) = \dfrac{\lambda^0 e^{-2\lambda}}{0!0!} + \dfrac{\lambda^1 e^{-2\lambda}}{1!0!} + \dfrac{\lambda^1 e^{-2\lambda}}{0!1!}$
 $P(X + Y \leq 1) = e^{-2\lambda} + 2\lambda e^{-2\lambda}$ 
 $P(X + Y \leq 1) = e^{-2\lambda}(1 + 2\lambda)$ 
 (iii)
 Find $P(X + Y = m)$
 $P(X = m - Y, Y = y) = \dfrac{\lambda^{m - y + y} e^{-2\lambda}}{(m-y)! y!}$ 
 $\dfrac{\lambda^m e^{-2\lambda}}{(m-y)!y!}$ 

> [!question]- #schols [2022] ![[{2120A254-1582-470F-87FC-5391B1EBA4BF}.png]]
 $f(x) = \lambda e^{-\lambda x}$ 
 $P(X < 1) = \int^1 _0 f(x) \ dx$
 $P(X < 1) = \lambda \int^1 _0 e^{-\lambda x} \ dx$
 $P(X < 1) = \lambda | \ \dfrac{e^{-\lambda x}}{-\lambda} |^1 _0 = \lambda (\dfrac{e^{-\lambda}}{-\lambda} - \dfrac{e^0}{-\lambda})$ 
 $P(X < 1) = -e^{-\lambda} + 1$ 
 $-e^{-\lambda} + 1 = 0.5$
 $e^{-\lambda} = 0.5$
 $-\lambda = ln(0.5)$ 
 $\lambda = 0.693147$ 
 .
 $P(X < 2) = \lambda \int^2 _0 e^{-\lambda x} \ dx$
 $P(X < 2) = \lambda (\dfrac{e^{-2 \lambda}}{-\lambda} - \dfrac{e^0}{-\lambda})$
 $P(X < 2) = -e^{-2\lambda} + 1$
 $P(X < 2) = -e^{-2 (0.693147)} + 1 \approx 0.75$ 

> [!question]- #schols #bonus [2021] ![[{28C5D56B-A191-4EEA-A1EF-A14D5F24CC49}.png]]
 $r = \lambda /t$
 $\lambda = rt$ 
 $X \sim Pois(rt)$ 
 $P(X = x) = \dfrac{(rt)^x e^{-rt}}{x!}$ 
 ...

#schols [2021]
![[{9C24DB56-6981-493C-AB21-852070A7DCD9}.png]]

> [!question]- ![[{9B3F366E-79B6-4144-BF33-A9722DD99E66}.png]]
 $E(X) = E(\sum X_i) = \sum E(X_i)$
 $E(X_i) = c(1) + 0 = c$ 
 $\sum E(X_i) = \sum c = nc$
 $E(X) = c$ 
 $E(X^2) = V(X) + E(X)^2$
 $V(X) = c - c = 0$ 

> [!question]- ![[{FA4A7902-E331-4AE5-98E1-432580A0533C}.png]]

(a)
$0 \leq y < 1, F_Y(y) = \int^y_0 y\ dy = \dfrac{y^2}{2}$ 
$F_Y(0.5) = 0.125$
$f(0.5) = 0.5$ 
$\therefore F_Y(0.5) < f(0.5)$ 
How can the CDF be less than the PDF? 

> [!question]- ![[{9D53680F-F95C-4F03-BF51-9BDD6C4A0844}.png]]
  (a)
 $F_V(v)$ 
 $P(V \leq v)$
 $1 - P(V > v)$
 $1 - P(min(Y_1, \dots, Y_n) > v)$
 $1 - P(Y_1 > v, \dots Y_n > v)$ 
 $1 - P(Y_1 > v) \dots P(Y_n > v)$ 
 $1 - (1 - P(Y_1 \leq v)) \dots (1 - P(Y_n \leq v))$ 
 $1 - (1 - F_Y(v))^n$ 
 .
 (b)
 $E(X) = 5$ 
 $\lambda = 0.2$ 
 $F(x) = 1 - exp(- \lambda x)$ 
 $F(x) = 1 - exp(-0.2x)$ 
 $F_V(v) = 1 - (1 - F(v))^{10}$
 $F_V (v) = 1 - (1 - (1 - exp(-0.2v)))^{10}$ 
 $F_V(v) = 1 - (e^{-0.2v})^{10}$ 
 $F_V(v) = 1 - e^{-2v}$ 
 $\lambda_V = 1/2$ 
 $V \sim Exp(1/2)$ 

> [!question]- ![[{ED9211AB-EAD9-420C-955B-144083EF62BD}.png]]
 (i)
 $P(X = x) = \dfrac{\lambda^x e^{-\lambda}}{x!}$ 
 $P(X = 2) = \dfrac{2^{2}e^{-2}}{2!} = 0.2707$
 $P(X=2)^5 = 0.2707^5 = 0.0015$ 
 .
 (ii)
 $P(X = 0) = 2^0 e^{-2} = 0.1354$ 
$5C2\ 0.1354^2 (1 - 0.1354)^3 = 0.119$ 

> [!question]- ![[{215938FD-8157-4124-A208-C1BA52716179}.png]]
 $P(X < 0) = 0$ 
 $P(X = 0) = \frac{1}{5}$
 $P(X = 1) = 0$
 $P(X=2) = \frac{1}{5}$ 
 $P(X = 3) = 0$
 $P(X = 4) = \frac{3}{5}$
 $P(X > 4) = 0$

> [!question]- ![[{4CED7DD6-0892-4B17-9581-03CA24B49D6D}.png]]
 (i)
 The total area of the function is equal to 1
 $\int^3_0 \int^3_0 cx^2 y(1 +y)\ dx\ dy = 1$ 
 $\frac{c}{3} \int^3_0  x^3 y(1 + y) \ dy\ |^3_0 = 1$
$\frac{c}{3} (27 - 0) \int^3_0 y + y^2 \ dy = 1$
 $9c (\dfrac{y^2}{2} + \dfrac{y^3}{3}) \ |^3_0 = 1$ 
 $9c((\frac{9}{2} + 9) - 0) = 1$
 $121.5c = 1$
 $c = 0.00823$ 
 .
 (ii)
 $c \int^2_1 x^2 \int^1_0 y + y^2 \ dy \ dx$ 
 $c \int^2_1 x^2 (0.5 + \frac{1}{3}) \ dx$
 $\frac{5}{6} c (\frac{1}{3}) (2^3 - 1)$
 $0.016$ 
 .
 (iii)
 $c \int^x_0 x^2 \int^y_0 y + y^2 \ dy \ dx$ 
 $c \int^x_0 x^2 (\dfrac{y^2}{2} + \dfrac{y^3}{3}) \ dx$ 
   $F(x, y) = c \dfrac{x^3}{3} (\dfrac{y^2}{2} + \dfrac{y^3}{3})$ 
 .
 (iv)
 $\int^3_0 cx^2 (y + y^2) \ dy$
 $cx^2 (\dfrac{3^2}{2} + \dfrac{3^3}{3})$ 
 $f(x) = 0.111105x^2$ 
 .
 (v)
 $\int^3_0 cx^2 (y + y^2) \ dx$ 
 $f(y) = 9c (y + y^2)$ 
 $f(x)f(y) = cx^2y (1 + y) = f(x, y)$ 
  $\therefore$ They are independent 

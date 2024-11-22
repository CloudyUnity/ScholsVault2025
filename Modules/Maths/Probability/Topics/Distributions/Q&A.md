
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


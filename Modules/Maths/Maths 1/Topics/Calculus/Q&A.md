
> [!question]- #schols ![[Pasted image 20240703144838.png]]
> (i)
> $u = -x^2$
> $du = -2x \ dx$
> $u \ du = 2x^3 \ dx$
> $0.5 u \ du = x^3 \ dx$
> $\int x^3 e^{-x^2} \ dx = \int 0.5 u e^u du$
> $\int u\ dv = uv - \int v \ du$
> $dv = e^u$
> $v = e^u$
> $\int u e^u \ du = u e^u - \int e^u \ du$
> $0.5(u e^u - e^u)$
> $0.5 e^u (u - 1)$
> $0.5 e^{-x^2} (-x^2 - 1)$
> $0.5 e^1 (-1 -1) - (0.5 e^0 (0 - 1))$
> $-e + 0.5$
> (ii)
> $-x^2 + 2x + 4$
>Complete the square, see [[Trinity/Schols/Modules/Maths/Misc/Completing the Square/Explanation|Explanation]]
>$-(x^2 - 2x + 1) + 1 + 4$
>$-(x-1)^2 + 5$
>$\int (-(x-1)^2 + 5)^{-0.5} \ dx$
>$u = x-1$
>$du = dx$
>$\int (-u^2 + 5)^{-0.5} \ dx$
>$\int \dfrac{1}{\sqrt{a^2 - x^2}} dx = sin^{-1} \dfrac{x}{a} + C$
>$sin^{-1} \dfrac{u}{\sqrt 5} + C$
>$sin^{-1} \dfrac{x-1}{\sqrt 5} + C$

>[!question]- #schols  ![[Pasted image 20240703145121.png]]
>(i)
>$u = ln \ x$
>$du = \frac{1}{x}\ dx$
>$x \ du = dx$
>$\int \frac{1}{x} x \dfrac{1}{\sqrt{1 - u^2}} \ du$
>$\int \dfrac{1}{\sqrt{a^2 - x^2}} = sin^{-1} (\dfrac{x}{a})$
>$sin^{-1} (\dfrac{u}{1}) = sin^{-1} (ln \ x)$
>$sin^{-1} (ln \ \sqrt{e}) - sin^{-1} (ln \ 1)$
>$\dfrac{\pi}{6}$
>(ii)
>$(1 - x^4) = (1 + x^2)(1-x^2)$
>$\dfrac{4x}{(1-x^2)(1+x^2)} = \dfrac{ax + b}{1+x^2} + \dfrac{cx + d}{1-x^2}$
>$\dfrac{4x}{(1-x^2)(1+x^2)} = \dfrac{(ax+b)(1-x^2) + (cx+d)(1+x^2)}{(1-x^2)(1+x^2)}$
>$b = d = 0$
>$4x = ax + cx$
>$a = c = 2$
>$\int \dfrac{2x}{1+x^2} \ dx + \int \dfrac{2x}{1-x^2} \ dx$
>$u = 1 + x^2$
>$du = 2x \ dx$
>$\int \dfrac{1}{u} \ du = ln |x^2 + 1|$
>$u = 1 - x^2$
>$du = -2x \ dx$
>$-\int \dfrac{1}{u} \ du = ln |-x^2 + 1|$
>$ln|x^2 + 1| - ln|-x^2 + 1| = ln|\dfrac{x^2 + 1}{-x^2 + 1}$
>$ln|\dfrac{0.5^2 + 1}{-0.5^2 + 1}| - ln|\dfrac{1}{1}|$
>$ln(\dfrac{5}{3})$
>To Verify Answer: #todo 
>(e) #bonus

> [!question]- #schols ![[Pasted image 20240703145449.png]]
> (i)
> $\dfrac{x}{(x+1)^2(x-2)} = \dfrac{ax + b}{(x+1)^2} + \dfrac{c}{x-2}$
> $x = (ax + b)(x-2) + c(x+1)^2$
> $1 = -2a + b + 2c$
> $a = b = c = 1$
> $\int \dfrac{1x+1}{(x+1)^2} \ dx = \int \dfrac{1}{x+1} \ dx = ln|x+1|$
> $\int \dfrac{1}{x-2} \ dx = ln|x-2|$
> $ln|x+1| - ln|x-2| + C$
> $ln|\dfrac{x+1}{x-2}| + C$
> ,
> (ii)
> $\dfrac{x^2}{x^2 - x - 2} = \dfrac{x^2 - x - 2 + x + 2}{x^2 - x - 2} = 1 + \dfrac{x+2}{x^2 - x - 2}$
> $x + 2 = a(x-2) + b(x+1)$
> $a + b = 1$
> $-2a + b = 2$
> $a = -\dfrac{1}{3}$
> $b = \dfrac{4}{3}$
> $\int - \dfrac{1}{3} \dfrac{1}{x+1} \ dx = - \dfrac{1}{3} ln|x+1|$
> $\int \dfrac{4}{3} \dfrac{1}{x-2} \ dx = \dfrac{4}{3} ln|x-2|$
> $\int 1 \ dx = x$
> $x + \dfrac{1}{3} (4ln|x-2| - ln|x+1|) + C$
> $x + \dfrac{1}{3} (ln|\dfrac{(x-2)^4}{x+1}|) + C$

> [!question]- #schols  ![[Pasted image 20240703150453.png]]
> $u = ln^3 \ x$
> $du = 3 (\dfrac{1}{x}) (ln^2 \ x)\ dx$
> $dv = dx$
> $v = x$
> $x ln^3 \ x - \int (x)3 (\dfrac{1}{x}) (ln^2 \ x)\ dx$
> $x ln^3 \ x - 3 \int ln^2 \ x \ dx$
> $u = ln^2 \ x$
> $du = 2 (\dfrac{1}{x}) (ln \ x) \ dx$
> $dv = dx$
> $v = x$
> $\dots + x ln^2 \ x - \int (x) 2 (\dfrac{1}{x}) (ln \ x) \ dx$
> $\dots + x ln^2 \ x - 2(x ln(x) - x)$
> $x ln^3 \ x - 3(x ln^2 \ x - 2x ln(x) - 2x)$
> $x ln^3 \ x - 3x ln^2 \ x - 6x ln(x) - 6x + C$

> [!question]- #schols [2024] ![[Pasted image 20241027191133.png]]


Slope/gradient of a line = $\dfrac{rise}{run}$

Slope: Measure of steepness of a line/surface
Gradient: Rate of change of a function

Tangent line slope of $f(x) = f'(x)$

Central Difference Curve (First Principles):
	$f'(x) = \lim_{h \to 0} \dfrac{f(x + h) - f(x)}{h}$

$(f(x) + g(x))' = f'(x) + g'(x)$
$(cf(x))' = c(f'(x))$

![[Pasted image 20240703135311.png]]

Product Rule:
	$y = u(x)v(x)$
	$\dfrac{dy}{dx} = v \dfrac{du}{dx} + u \dfrac{dv}{dx}$

Quotient Rule:
	$y = \dfrac{u(x)}{v(x)}$
	$\dfrac{dy}{dx} = \dfrac{1}{v^2} (v \dfrac{du}{dx} + u \dfrac{dv}{dx})$

Chain Rule:
	$y = v(u(x))$
	$\dfrac{dy}{dx} = \dfrac{dy}{du} \dfrac{du}{dx}$

$\dfrac{dist}{time} \to velocity \to acceleration \to jerk$

Integration = area under the curve

![[Pasted image 20240703140323.png]]

Indefinite Integral:
	$\int f(x) dx$
	Don't forget constant of integration!

Definite Integral:
	$\int_a ^b f(x) dx$

$\int f(x) + g(x) dx = \int f(x) dx + \int g(x) dx$
$\int cf(x) dx = c \int f(x) dx$

![[Pasted image 20240703140842.png]]

Integration by substitution:
	Idk man look it up

Integration by parts:
	$\int u \ dv = uv - \int v \ du$	
	For example:
		$\int x e^{2x}$
		$u = x, dv = e^{2x}$

Integrating partial fractions:
	$y = \dfrac{f(x)}{p(x)} = \dfrac{f(x)}{g_1(x)g_2(x) \dots g_n(x)}$
	You may need to factorise $p(x)$
	Number of partial fractions = number of roots in denominator
	$y = \dfrac{A(x)}{g_1(x)} + \dfrac{B(x)}{g_2(x)} + \dots + \dfrac{C(x)}{g_n(x)}$
	Degree of numerator = Degree of denominator - 1
		For example:
			$\dfrac{A}{x + 1} + \dfrac{Bx + C}{(x - 1)^2} + \dots$
	Combine partial fractions into a single fraction
		Must have the same denominator as the original
		$\dfrac{f(x)}{p(x)} = \dfrac{\dots}{p(x)}$
	Solve for $A, B, \dots$ and substitute into partial fractions
	Integrate the partial fractions

#bonus 
Graphing Rational Functions:
	[Link](https://learn-eu-central-1-prod-fleet01-xythos.content.blackboardcdn.com/62b985ffa0afc/3960187?X-Blackboard-S3-Bucket=learn-eu-central-1-prod-fleet01-xythos&X-Blackboard-Expiration=1720029600000&X-Blackboard-Signature=R4Z1sAjmsmw2RdFeN2oQDjW1XXxKuE%2B1%2Fd%2FmPwOEb8I%3D&X-Blackboard-Client-Id=300200&X-Blackboard-S3-Region=eu-central-1&response-cache-control=private%2C%20max-age%3D21600&response-content-disposition=inline%3B%20filename%2A%3DUTF-8%27%27CSU11001_Graphing_Rational_Functions.pdf&response-content-type=application%2Fpdf&X-Amz-Security-Token=IQoJb3JpZ2luX2VjENT%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaDGV1LWNlbnRyYWwtMSJHMEUCIGIloZvSrxDO%2BHxNMIBD8XYPC0rLnEN6Xg9Dou4sFB7XAiEA1itbucsEfXPsf0aAZziPfswTJUFQIl7i%2F9t8vtvPQ%2F0qxwUIjf%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARAEGgw2MzU1Njc5MjQxODMiDPOS8qPnzBTR%2B0NB8iqbBd8qXh65hsYszIrT0r5Nej5L6KAglYL1d3njcMKWIKujsEJMTTdSjczVwYNYnAY0oxThbgAW84VL2yXLXDwJDKM1pC1GQ8pSBLTDX15aGoC6z3UH8qnuDpxA%2BxVewTnpNfh4Yhshm0B%2F8JDeEY3lyREJwRIpRINtKJ69eOkkToUnn2RHHiLEyF61dc3Sf9CpUf8%2BFo6KVw5vKkIfkwSxmsjeOdJQfTDFk7xdB%2BLiiHSX1A6L0KNOMXtZy8VXE%2B3B9Hc3m%2Fbud9rqUFawb%2B%2BqGbIJhyBya6icwMDn%2BGYbNleGa7%2Fj39uRGQlsRD%2FGCWcJg%2Btcx8xGjyTknTOmecS3gX4MPiprYqW0RmWo%2ByGfkOocJxFtA6h1f%2BjlW4XjyHtI6%2BJVRTjD20%2FPHQBAZIt%2B%2BQRQEK8Y%2Bj8G07BjeGCiCBQtOwhiDYgokquwL2clN4K9lz4ASAT1ymFxvaSXztnwOZ0ZtJQTcVhwADZG%2BSrO%2FqczLezyx66IBfF%2Bw9Wf5lrvEtL0GeMFgCmuSZ%2FWIsZuQeQS6jkrPugOzGxm6LsuBcq0HwM1xxZ6ap5rYDAQRAoyP94G3HppR1KYwXKiTOKChMrVs1fmkmezctnCG032WPKWHbbk2PkDFpgsgOu6lhS%2F%2FOTjfdyf%2BRd4hq2k%2FoJb7Q06b%2Fys3rgggf7hexTN1bKNvIjb0EgJ2FDDoLOUTALSIc%2BRqy4D5vbRW8laRPmODseY%2FYgnc3cnYMA3jNwhsgcg4gMiWJZ%2FHfuSMCqaeLxxcUAXYhTIeju4xYHA6h07X3lqBx%2BUMNULmwV9%2FvJio4J1tuQL3GeOduQ31kYib33bi9sszT%2F70SzIj0Nym1KK0y%2FRUdP2yLMjSq3IWregkedVQgQ3L%2BZtMmyUA0Mws4SVtAY6sQGz%2FliIYPo8JxXLsht2EGpv2oqVByVTW5s4G9oYOV9so1rdw2FS7evHiUl46UsiaM4hbwycX92%2FYg2d%2FftfLLuR0mhUD9KRdBwdQBd%2B5O6s8GURbAJIDGNiBmj2CaZi3Qc9Zl51Ake0jove4eTbv1hBiBJcWu%2Fvu10%2BH3hBrk9aQ78dxen3c4gT%2BV%2F1iGJIrSzMA6QV5Z3%2FVBwvCx7DA8rNt371078K6%2FosOrycHBMHTew%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240703T120000Z&X-Amz-SignedHeaders=host&X-Amz-Expires=21600&X-Amz-Credential=ASIAZH6WM4PL7HF2ZX55%2F20240703%2Feu-central-1%2Fs3%2Faws4_request&X-Amz-Signature=0ecdd41086e816dc2937b5981fd90b66562dd68072f62a107b5f2cd17dc91afb)


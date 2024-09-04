Arithmetic Mean:
	For quantitative variables the arithmetic mean is:
		$\bar{x}_a = \dfrac{1}{n} \overset{n}{\underset{i = 1}{\sum}} x_i$
		$\bar{x}_a = \dfrac{1}{n} \overset{J}{\underset{j = 1}{\sum}} x_j f_j = \overset{J}{\underset{j = 1}{\sum}} x_j \tilde{f}_j$
	Weighted Arithmetic Mean:
		$\bar{x}_{\tilde a} = \dfrac{\sum x_i w_i}{\sum w_i}$
	$\sum x_i = n \bar{x}_a$
	$\sum (x_i - \bar{x}_a) = 0$
		$arg\  \underset{c}{min} [\sum (x_i - c)^2] = \sum (x_i - \bar{x}_a)^2$
			The sum of squared differences is minimised when $c = \bar{x}_a$
	Groups:
		Divide $n$ values into $L$ distinct groups of sizes $\{n_1, \dots, n_I, \dots, n_L\}$
		$\overset{L}{\underset{I=1}{\sum}} n_I = n$
		$\bar{x}_{a, I}$ is the mean for group $I$
		$\bar{x}_a = \dfrac{1}{n} \overset{L}{\underset{I=1}{\sum}} \bar{x}_{a, I} (n_I)$
	Linear Transformation:
		$\bar{y}_a = \dfrac{1}{n} \sum (\alpha + \beta x_i) = \alpha + \beta \bar{x}_a$

Geometric Mean:
	Used when the values are dependant or have large fluctuations
	$\bar{x}_g = \sqrt[n]{\prod x_i}$
	$\prod x_i = (\bar{x}_g) ^n$
	Discrete:
		$\bar{x}_g = \sqrt[n]{\prod x_i^{f_i}}$
	$log(\bar{x}_g) = \dfrac{1}{n} \sum log(x_i)$

Median:
	Means are sensitive to outliers but median is more robust
	Quantitative or Qualitative Ordinal 
	Value of the central index
	$n$ is odd $\to i = \dfrac{n + 1}{2}$
		$M_e = x_i$
	$n$ is even $\to i_1 = \dfrac{n}{2}, i_2 = \dfrac{n}{2} + 1$
		$M_e = 0.5 (x_{i_1} + x_{i_2})$
	 $arg \ \underset{c}{min} [\sum |x_i - c|] = \sum |x_i - M_e|$
	 Median Class:
		$M_e = m_{M_e} + \triangle_{M_e} \dfrac{\frac{n}{2} - fc_{M_e - 1}}{fc_{M_e} - fc_{M_e - 1}}$
			$m_{M_e}$ is the lower bound of the class containing the median
			$\triangle_{M_e}$ is the class width
			 $n$ is the number of observations
		The class containing the median will always be the first class to have its $f_c$ surpass 0.5

Mode:
	Largest frequency 
	If classes have different widths then divide $f_{i}$ by $\triangle_{i}$
	1 Mode = Unimodal
	2 Modes = Bimodal
	3+ Modes = Multimodal

Quantiles:
	Median splits the observations in two
	Quantiles splits the observations into $K$ equal parts
	Percentiles splits the observations into 100 parts
		The $k^{th}$ percentile:
			$q_k = m_{q_k} + \triangle_{q_k} \dfrac{k/100 - fc_{q_k - 1}}{fc_{q_k} - fc_{q_k - 1}}$

Summary Statistics:
	Given a dataset matrix $X$ with dimensions $n \times P$
	$n$ is the number of observations
	$P$ is the number of variables
	$X_p$ is the $p^{th}$ variable vector
	$X_i$ is the $i^{th}$ observation vector
	$x_{ip}$ is the $p^{th}$ variable for the $i^{th}$ unit
	A summary statistic is a statistic summarising information from given variable(s) or unit(s) 
	Different types of data allow for different types of summary statistics
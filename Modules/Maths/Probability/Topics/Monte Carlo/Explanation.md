Monte Carlo Simulation
	A simulation used to solve problems with random elements

Lottery Problem
	Every day of the year was randomly shuffled
	Leap year day included
	$H_0 :$ Lottery was fair
	Calculate the average draft number per month 
	Expected average draft $E_i$ per month is 183.5
	Sum of absolute deviations is given by
		$D = \overset{12}{\sum} | O_i - E_i |$
	We want to calculate the probability
		$P(\overset{12}{\sum} |O_i - E_i| \geq D)$
	Monte Carlo Sim
		Generate random permutation of the first 366 integers $a(1), a(2), \dots, a(366)$
		$a(i)$ is the $i$th day of the year
		Compute monthly averages $G_i$ for generated permutation
		Count experiment as success if
			$\overset{12}{\sum} |G_i - E_i| \geq D$
		$\tilde{f_n}(Success) = \dfrac{\# Success}{\# Experiments}$
		$P(\overset{12}{\sum} |O_i - E_i| \geq D) \approx \tilde{f_n}(Success)$
	Finding the Monthly Trend
		Rank months by average draft number
		Permutation of months is $a^* = \{a(1), a(2), \dots, a(12)\}$
		Assuming a uniform distribution how likely is $a^*$?
		$d(a) = \overset{12}{\sum} |a(i) - i|$
		We want to compute
			$D = d(a^*)$
			$P(d(a^*) \leq D)$
		Success = $d(a) \leq D$
		Run Monte Carlo sim
"**If you are taking Schol exams**: it is important to have a good understanding of the data structures and associated algorithms covered during this semester and to be able to select the best ones to solve new problems. Assignments, main and bonus ones, often have a critical thinking component which can be useful in preparing for exams. The more you practice your problem solving abilities the easier it becomes to solve new problems."

Algorithm
	Steps to correctly perform a general computational problem

Optimal Algorithm
	Where the lower bound $\ohm$ equals upper bound $O$ within a constant factor

Data Structure
	Ways to store information needed by algorithms

Time complexity can be calculated using either experiments or maths

Experiments
	Observe, Hypothesize, Predict, Verify and Validate
	Hypotheses must be falsifiable

Time $T(n)$
	The time taken by the algorithm with $n$ inputs

Doubling Hypothesis
	$O(N) = \dfrac{T(2N)}{T(N)} = \dfrac{a(2N)^b}{aN^b}$
	Double the input size, observe the increase in running time
	Fit a straight line to observations, use slope to determine time complexity
	$b$ is determined by the algorithm and input data
	$a$ is determined by those as well as hardware, software and system

In CS it's difficult to get precise measurements but very easy and cheap to run experiments

Tilde Notation
	$\sim g(n)$
		A quantity when divided by $f(n)$ approaches $1$ as $n$ grows
	$g(n) \sim f(n)$ 
		$g(n) / f(n)$ approaches 1 as $n$ grows
	$N+2 =\ \sim N$
	$k(N+a)(N+b) =\ \sim kN^2$



```java
int count = 0; 
for (int i = 0; i < N; i++) 
	if (a[i] == 0)
		 count++;
```
Time complexity is $O(N)$ in best case, $O(2N)$ in worst case (Loop + Array Access)
Total time complexity is $O(N)$

Assume nothing is compiled/optimized away

Cost Model
	All constants cost $1$
		String concatenation is not constant
			Depends on the size
			Use `StringBuilder` for speed
		Method calls are not constant
			Cost is equal to the cost of the function called
	Only highest order terms count
		$aN^3 + bN^2 + c = aN^3$
		When $N$ is large, lower terms are negligible 
		When $N$ is small, who gives a shit
	Use a basic operation as a proxy
		In the code above, base $O$ entirely off the array accesses 

$O(log_a \ N) = O(\dfrac{log_b \ N}{log_b \ a}) = O(c \ log_b \ N) = O(log \ N)$

#NeedsFactCheckingByTrueAmericanPatriots 
If the brute force algo is $\geq O(N \ log \ N)$ then sorting the array is free as it's a lower order term
	(This doesn't necessarily mean the sort algo will be faster)

$T(N)$ may have different orders of growth for different $N$
The asymptotic order of growth is when $N \to \infty$

For examples below assume $g(N) = N^2$

$\Theta (g(N))$ is the set of functions with asymptotic order of growth $g(N)$
	$c N^2$
	$aN^2 + bN + c$

$O(g(N))$ is the set of functions with asymptotic order of growth $\leq g(N)$
	$cN^2$
	$cN + d$

$\ohm (g(N))$ is the set of functions with asymptotic order of growth $\geq g(N)$
	$cN^2$
	$cN^5$
	$aN^3 + bN^2$

$\Theta(g_1(N)) \times \Theta(g_2 (N)) = \Theta (g_1(N) g_2(N))$

Memory costs
	Objects have 16 byte overhead
	Objects are 8-byte aligned (Padding)
	Any pointer is 8 bytes
	`T[]` = $sizeof(T) * N + 24$
	`T[][]` $\approx sizeof(T) * N * M$	
	For a recursive function $M$ call stack frames add to the memory cost

Shallow Memory Usage
	Don't include referenced objects

Deep Memory Usage
	Recursively count memory in pointers
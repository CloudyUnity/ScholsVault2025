Another type of symbol table
Try to use immutable keys

$x.equals(y) \to x.hashCode() == y.hashCode()$
Desirable:
	$!x.equals(y) \to x.hashCode \neq y.hashCode()$

Hashing a string
```java
int hash = 0;
for (int i = 0; i < str.length(); i++)
	hash = str.charAt(i) + (hash * 31);
```
Recommended to cache hash to avoid recalculation
Follow same rule for hashing objects, $y = x_i + 31y$

Hash(null) == 0

Fitting hash to array of size $M$
	Incorrect
		$Math.abs(hash)\  \% \  M$
		Breaks if hash == $-2^{31}$
	Correct
		$(hash \  \& \  0x7FFFFFFF) \  \% \  M$

Collisions (Separate-Chaining)
	Each slot of array is instead a linked list
	Need to search through full linked list when searching

$N$ is the number of key-value pairs

Number of keys is in a linked list is around $N/M$
List size is binomially distributed
Leads to too many probes
$M$ large $\to$ Lots of empty chains
$M$ small $\to$ Chains too long
Generally $M \sim N/4$

Resizing Separate-Chaining
	Try to make $N/M$ constant
	$N/M \geq 8 \to$ Double $M$
	$N/M \leq 2 \to$ Halve $M$
	Resizing needs all keys to be rehashed

Open Addressing
	On collision find next empty slot and insert
	$M > N$ must be true
	With $N=M/2$ mean displacement is $\sim 3/2$
	With $N=M$ mean displacement is $\sim \sqrt{\pi M/8}$
	Probe Count
		Given $N = aM$
		Search Hit = $\sim \dfrac{1}{2} (1 + \dfrac{1}{1-a})$
		Search Miss/Insert = $\sim \dfrac{1}{2} (1 + \dfrac{1}{(1-a)^2})$
		
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
Recommended to cache hash
Follow same rule for hashing objects with members, $y = x_i + 31y$

Hash(null) == 0

Fitting hash to array of size $M$
	Incorrect
		$Math.abs(hash)\  \% \  M$
		Breaks if hash is $-2^{31}$
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

Two probe hashing (Separate-Chaining Variant)
	Hash to two positions, insert into shorter chain
	Mean length becomes $log log N$

Open Addressing (Linear Probing)
	Less wasted space and better cache performance 
	More sensitive to poorly designed hash functions
	On collision find next empty slot and insert	
	$M > N$ must be true otherwise displacement could be infinite
	With $N=M/2$ mean displacement is $\sim 3/2$
	With $N=M$ mean displacement is $\sim \sqrt{\pi M/8}$
	Probe Count
		Given $N = aM$
		Search Hit = $\sim \dfrac{1}{2} (1 + \dfrac{1}{1-a})$
		Search Miss/Insert = $\sim \dfrac{1}{2} (1 + \dfrac{1}{(1-a)^2})$
		Typical: $a = N/M \sim 1/2$
			Double on $N/M \geq 1/2$
			Halve on $N/M \leq 1/8$
	Deletion requires reindexing all elements from deleted index to next empty index

One Way Hash
	Useful to avoid attacks from filling a single hashmap slot with a shitload of elements
	These are hash functions where it's hard to find a key that hashes to a desired value
	MD4, MD5, SHA0, SHA1 are insecure
	SHA2, WHIRLPOOL, RIPEMD-160 are secure

Double Hashing (Linear Probing Variant)
	Skip a variable amount instead of +1
	Eliminates cluttering, more difficult deletes

Cuckoo Hashing (Linear Probing Variant)
	Hash to two positions, if first one is occupied swap keys and place original into other position
	Constant worst-case time for search

Hash Tables vs BST
	Hash Tables:
		Simpler to code
		No effective alternative for unordered keys
		Faster for simple keys
		Better system support in java for strings (Cached Hash)
	BST:
		Stronger performance guarantee
		Support for ordered ST operations
		Easier to implement `compareTo()` than `equals()` and `hashCode()`
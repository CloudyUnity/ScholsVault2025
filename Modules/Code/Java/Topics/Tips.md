Be aware that sometimes it's better to start by sorting data although this often isn't the fastest solution

Use bit manip to tell if a number is even rather than modulo
```java
if (x & 1)
	return odd;
```

Don't forget to include null-checking, early returns, array/string length checks

For dynamic programming you might be able to use a hashmap to mark certain states as failure, avoiding recomputing work

For implementing a complex data structure
	For each meaningful state it may be in
		For each meaningful input 
			Create an example on paper
	Then write the code

If you need to determine any kind of union operation consider bitfields
For example the alphabet can be stored in a 26-bit number where each bit determines whether the letter has been seen

Assume no casts are implicit, write out c-style casts on everything explicitly 
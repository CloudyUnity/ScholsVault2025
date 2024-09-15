Accumulator (Tail Recursion)
```java
int func(int p){
	return funcRecursive(p, 1);
}
int funcRecursive(int p, int n){
	return isBoolean ? n : funcRecursive(k(p), m(n));
}
```
Recursively call functions while modifying some shared value for tracking
In functional languages this avoids growing call stacks due to link register being overridden. (No operations applied on recursive call result)
This also allows you to do some algos bottom-up leading to less redundant calculations (Fibonacci)
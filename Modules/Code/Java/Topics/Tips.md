Try to avoid preprocessing data such as sorting arrays, it's almost always better to find a 2-pass solution. Use as a last resort

Use bit manip to tell if a number is even rather than modulo
```java
if (x & 1)
	return odd;
```

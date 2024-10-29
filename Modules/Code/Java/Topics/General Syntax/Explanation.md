Sort an array
```java
// Ascending Order
import java.util.Arrays;
Arrays.sort(arr); // O(N log N)

// Descending Order, cannot use primitives array
import java.util.Collections;
Arrays.sort(arr, Collections.reverseOrder());
```

Logging
```java
System.out.println(str);
```

ArrayList to Array
```java
list.toArray(new T[list.size()]);
```

Math
```java
Math.min(a, b);
Math.max(a, b);
...
```

Null Checking
```java
if (ptr != null)
if (ptr) // Error
```

Lengths & Accessing
```java
str.length();
str.charAt(i);

arr.length;
arr[i];

list.size();
list.at(i);
```

Equals Override
```java
@Override
public boolean equals(Object y){
	if (y == this || y == null)
		return false;

	if (y.getClass() != this.getClass())
		return false;

	T t = (T) y;
	// Compare values
	return isEqual;
}
```

Substring
```java
str.substring(int startIndex);
str.substring(int startIndex, int endIndex); // Set endIndex to index AFTER the last char you want included
```

You cannot case from boolean to integer in any way!! (Dumb)
```java
int val = 255 * (x > 5); // Error
int val = 255 * (int)(x > 5); // Error
int val = x > 5 ? 255 : 0; // OK
```

Constants
```java
Integer.MAX_VALUE; // For int32
Integer.MIN_VALUE; // For int32
```
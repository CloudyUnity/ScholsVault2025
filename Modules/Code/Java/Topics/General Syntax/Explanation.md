Sort an array
```java
// Ascending Order
import java.util.Arrays;
Arrays.sort(arr);

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
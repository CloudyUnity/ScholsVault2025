```java
public interface java.util.List<T>
boolean Add(int, T);
T remove(int);
```
Implemented as LinkedList (doubly) or ArrayList

```java
??? stack<T>
??? queue<T>

T pop();
T dequeue();
void enqueue(T);
```

```java
public interface java.lang.Iterable<T>
Iterator<T> iterator();

public interface java.util.Iterator<T>
boolen hasNext();
T next();
void remove(); // Optional

for (T t : iterable)
	...
```

```java
public interface java.lang.Comparable<T>
int compareTo(T); // Returns member - arg
```
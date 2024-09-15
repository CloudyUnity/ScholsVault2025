
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
int compareTo(T); // Returns this - arg
boolean equals(T); // Returns this == arg
```

```java
public interface java.util.Collection<T>
boolean add(T);
boolean addAll(Collection<? extends T>);
boolean remove(T);
int size();
Object[] toArray();
T[] toArray(T[]);
void clear();
boolean contains(T);
boolean isEmpty();
Iterator<T> iterator();
```

Priority Queue
	Stores objects in stack ordered by some value

```java
	java.util.TreeMap
	java.util.TreeSet
```
#todo
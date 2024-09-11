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

Complete Tree
	Balanced tree except for bottom level
	Height with $N$ nodes is $log\ N$

Binary Heap
	Array representation of a heap-ordered complete tree
	Keys are assumed immutable
	Construction is $O(N \ log \ N)$
	![[Pasted image 20240911171741.png]]
	Root node is `a[1]`
	Parent of node $k$ is $k/2$
	Children of node $k$ is $2k, 2k+1$
	Insertion:
		Add node at the end, then swim it up
		$O(log \ N)$
	Remove Max:
		Exchange root with leaf node, then sink it down
		$O(log \ N)$
	Peter Principle
		If a child's key is larger than it's parent then swap them (Use larger child)

$d$-Way Binary Heaps
	Nodes have $d$ children
	Swim is $O(log_d N)$
	Sink is $O(d \ log_d N)$
	Optimal at $d=4$

Cache-Friendly Binary Heaps
	Cache-Aligned $d$-heap
	Funnel Heap
	B-Heap
	#todo 
		More info
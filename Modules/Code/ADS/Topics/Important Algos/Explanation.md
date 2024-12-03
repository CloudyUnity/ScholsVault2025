These are algorithms you are forced to memorize and be able to execute in any language

#todo 
	Include pros and cons of each algorithm compared to similar ones
	What problems are they a best fit for?
	Include the time and memory complexity

Quick Sort (Java)
```java
void quickSort(T[] arr, int lo, int hi) {
	if (lo >= hi) 
		return;
	int pi = partition(arr, lo, hi);
	quickSort(arr, lo, pi-1);
	quickSort(arr, pi+1, hi);
}

int partition(T[] arr, int lo, int hi) {
	T pivot = arr[hi];
	int i = lo - 1;
	for (int j = lo; j < hi; j++) {
		if (arr[j].compare(pivot) >= 0)
			continue;
		i++;
		T temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}
	T temp = arr[i+1];
	arr[i+1] = arr[hi];
	arr[hi] = temp;
	return i + 1;
}
```

Quick Sort (C)
```c
void quickSort(T* arr, int lo, int hi) {
	if (lo >= hi)
		return;
	int pi = partition(arr, lo, hi);
	quickSort(arr, lo, pi-1);
	quickSort(arr, pi+1, hi);
}

int partition(T* arr, int lo, int hi) {
	T pivot = arr[hi];
	int i = lo - 1;
	for (int j = lo; j < hi; j++) {
		if (compare(arr[j], pivot) >= 0)
			continue;
		i++;
		T temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}
	T temp = arr[i+1];
	arr[i+1] = arr[hi];
	arr[hi] = temp;
	return i + 1;
}
```

Insertion Sort (ARM)
```c
@ R0 - ArrayPtr
@ R1 - ArraySize
InsertionSort:
	PUSH {R4-R8, LR}
	MOV R4, #1 @ int i = 1;
.LInsertionSort_ForLoop:
	CMP R4, R1 @ if (i >= n) break;
	BGE .LInsertionSort_ForLoop_Break

	LDR R5, [R0, R4, LSL #2] @ int key = arr[i]
	SUB R6, R4, #1 @ int j = i - 1;

.LInsertionSort_ForLoop_WhileLoop:
	CMP R6, #0
	BGE .LInsertionSort_ForLoop_WhileLoop_Break

	LDR R7, [R0, R6, LSL #2] @ arr[j]
	CMP R7, R5 @ if (arr[j] > key) break;
	BGT .LInsertionSort_ForLoop_WhileLoop_Break

	ADD R8, R6, #1 @ j + 1
	STR R7, [R0, R8, LSL #2] @ arr[j+1] = arr[j];
	SUB R6, R6, #1 @ j--;
	
.LInsertionSort_ForLoop_WhileLoop_Break:

	ADD R8, R6, #1 @ j + 1
	STR R5, [R0, R8, LSL #2] @ arr[j+1] = key;

	ADD R4, R4, #1 @ i++;
	B .LInsertionSort_ForLoop @ continue;
.LInsertionSort_ForLoop_Break:
	POP {R4-R8, LR}
```

Merge Sort (Java)
	#todo 

Union-Find (Java)
	#todo 

Union-Find (C)
	#todo 

Dijkstra's (Java)
	#todo 

Dijkstra's (C)
	#todo 

Tree (Java)
	What is this?
	#todo

Binary Search (BinS) (Java)
$O(log\ N)$
```java
int binarySearch(int[] a, int key)
{
	int lo = 0;
	int hi = a.length - 1;
	while (lo <= hi)
	{
		int mid = lo + (hi - lo) / 2;
		if (key == a[mid])
			return mid;
		
		if (key < a[mid])
			hi = mid - 1;
		else if (key > a[mid])
			lo = mid + 1;
	}
	return -1;
}
```

Intro Sort (Java)
	$O(N \ log \ N)$
	Run quick sort
	If stack depth $> 2 log \ N$
		Heap sort
	If $N = 16$
		Insertion sort

Boids
	Avoidance
		Point away from $k$ nearest boids
	Centering
		Point towards center of mass of $k$ nearest boids
	Matching
		Update velocity to average of $k$ nearest boids
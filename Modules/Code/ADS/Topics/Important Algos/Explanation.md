These are algorithms you are forced to memorize and be able to execute in any language

#todo 
	Include pros and cons of each algorithm compared to similar ones
	What problems are they a best fit for?
	Include the time and memory complexity

Quick Sort (Java)
	#todo 

Quick Sort (C)
	#todo 

Insertion Sort (ARM)
	#todo 

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
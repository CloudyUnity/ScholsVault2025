![[Pasted image 20241027194308.png]]

Removing involves searching through all elements to find outdated ones and deleting them

Linked List:
	Record = O(N)
	Median = O(N)
	Remove = O(N)

List:
	Record = O(N)
	Median = O(1)
	Remove = O(N^2)

Dequeue:
	Sorted by timestamp
	Record = O(1)
	Median = O(N log N)
		Copy -> Sort -> Maths = N + NlogN + 1
	Remove = O(1)
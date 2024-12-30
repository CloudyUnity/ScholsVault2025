
![[Pasted image 20240716165055.png]]

(a)
This is like that GPU algorithm
Is it where you create a new array of size n
Then to sum n numbers where k < n
We'll assume n is a power of two
```c
for i..n/2
	arr[i] += arr[i + n/2];
for i..n/4
	arr[i] += arr[i + n/4];
...
```

```c
float compute_sum(float* input, int n) {
	float arr[n];
	for (int i = 0; i < n; i++) {
		arr[i] = input[i];
	}
	
	n /= 2;
	while (n > 1) {
		for (int i = 0; i < n; i++) {
			arr[i] += arr[i+n];
		}
		n /= 2;
	}
	return arr[0];
}
```

(b)
We can have $O(0.5N)$ memory by doing the first iteration manually to avoid needing to put everything into the new array
For logarithmic memory we need to make it so that doubling n only requires one extra memory slot
Speed doesn't matter here

For example with n=64 we need to solve it in 6 or so memory slots 
What if we make it more sequential?
Add 0 and 1 -> [0]
Add 2 and 3 -> [1]
Add [0] and [1] -> [0]
Add 4 and 5 -> [1]
Add 6 and 7 -> [2]
Add [1] and [2] -> [1]
And [0] and [1] -> [0]
This is it

This is like that fruit game lol
We can make two arrays of size logN 
The first one contains the sums
The second one contains the size of the sum slots
When two input numbers are added together they get put on the end of the sum array with size 1
When i >= 1 && sizeArr[i] == sizeArr[i-1]
	sumArr[i-1] += sumArr[i];
	sizeArr[i-1]++;
	i--;

```c
float compute_sum(float* input, int n) {
	int logN = log2(n); // Requires C99
	float sumArr[logN];
	int sizeArr[logN];

	int idx = 0;

	for (int i = 0; i < n/2; i++){
		sumArr[idx] = arr[i] + arr[i+n];
		sizeArr[idx] = 1;
		while (idx >= 1 && sizeArr[idx] == sizeArr[idx-1]) {
			sumArr[idx-1] += sizeArr[idx];
			sizeArr[idx-1]++;
			idx--;
		}
		idx++;
	}
	return sumArr[0];
}
```
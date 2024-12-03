
![[Pasted image 20240716172055.png]]

This is the 2D line intersection algorithm 
We have a bunch of horizontal lines and we need to find when the overlap vertically the most

The golden age will start when a specific creative person is born
The golden age will end when a specific creative person dies
Thus we can just check the start and end points of each line to find the max 
If you find the start of the golden age you just need to find the next person to die
You may need to check multiple starts as they could have the same number of creative people 

You can get the current time by doing `day + month * 50 + year * 1000` 

We could possibly do this quicker by doing 3 passes for each year, month and day

Ok looked up the algorithm, it's pretty simple
Create a struct DatePoint which contains a date and a deltaCount value (either +1 or -1) and a DatePoint* Next
Build a sorted linked list of DatePoints. Sort by date. Births get +1. Deaths get -1
Iterate through the linked list with a rolling counter incrementing by deltaCount
Keep track of a maxOverlapCount, maxOverlapTimeDiff, maxOverlapStart, maxOverlapEnd, maxOverlapStartTest
If counter > maxOverlapCount then maxOverlapCount = counter and set maxOverlapStartTest
If counter == maxOverlapCount then set maxOverlapStartTest
When counter goes down from maxOverlapCount then compare time against maxOverlapStartTest
	If time diff is greater than maxOverlapTimeDiff then set all time variables 

WAIT. Faster to use quicksort than build a linked list... BRB gotta memorize quick sort 

Ok new plan
DatePoint no longer has a ptr in it
We create a DatePoint array and fill it in with each creative person
Then create a DatePoint quicksorting function to sort the list. Prioritise deaths over births on equal dates 

```c
struct DatePoint {
	struct date Date;
	int DeltaCount;
};

// 1 - A first
// -1 - B first
int compare(struct DatePoint a, struct DatePoint b) {
	int timeA = a.Date.day + a.Date.month * 50 + a.Date.year * 1000;
	int timeB = b.Date.day + b.Date.month * 50 + b.Date.year * 1000;
	
	if (timeA == timeB) {
		if (a.DeltaCount == -1 && b.DeltaCount == 1)
			return 1;
		return -1;
	}
	
	if (timeA > timeB)
		return 1;
	return -1;
}

void quickSortDatePoint(struct DatePoint* arr, int lo, int hi) {
	if (lo >= hi)
		return;
	int pi = partitionDatePoint(arr, lo, hi);
	quickSortDatePoint(arr, lo, pi-1);
	quickSortDatePoint(arr, pi+1, hi);
}

int partitionDatePoint(struct DatePoint* arr, int lo, int hi) {
	struct DatePoint pivot = arr[hi]; // Unoptimized but whatever 
	int i = lo - 1;
	for (int j = lo; j < hi; j++) {
		if (compare(arr[j], pivot) == 1)
			continue;
		i++;
		struct DatePoint temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}
	struct DatePoint temp = arr[i+1];
	arr[i+1] = arr[hi];
	arr[hi] = temp;
	return i + 1;
}

void compute_golden_age(struct person* creative_people, int size) {
	struct DatePoint* dateArr = (struct DatePoint*)malloc(sizeof(struct DatePoint) * size * 2);
	for (int i = 0; i < size; i++) {
		dateArr[i*2].Date = creative_people[i].date_of_birth;
		dateArr[i*2].DeltaCount = 1;
		dateArr[i*2+1].Date = creative_people[i].date_of_death;
		dateArr[i*2+1].DeltaCount = -1;
	}
	
	quickSortDatePoint(dateArr, 0, size*2);

	int curOverlapCount = 0, maxOverlapCount = 0, maxOverlapDiff = 0;
	struct date start, end, startTest;
	for (int i = 0; i < size * 2; i++) {
		curOverlapCount += dateArr[i].DeltaCount;
		
		if (dateArr[i].DeltaCount == 1) {
			if (curOverlapCount >= maxOverlapCount) {
				maxOverlapCount = curOverlapCount;
				startTest = dateArr[i].Date;
			}
		}
		
		if (dateArr[i].DeltaCount == -1) {
			if (curOverlapCount + 1 == maxOverlapCount) {
				int timeStart = startTest.day + startTest.month * 50 + startTest.year * 1000;
				int timeEnd = dateArr[i].Date.day + dateArr[i].Date.month * 50 + dateArr[i].Date.year * 1000;
				if (timeEnd - timeStart <= maxOverlapDiff)
					continue;
				
				maxOverlapDiff = timeEnd - timeStart;
				start = startTest;
				end = dateArr[i].Date;
			}
		}		
	}

	fprintf("Creative Age started on %i/%i/%i and ended on %i/%i/%i.\n", start.day, start.month, start.year, end.day, end.month, end.year);
}
```

Overall time complexity is $O(N + N \ log \ N + 2N) \equiv O(N \ log \ N)$ 
Overall memory complexity is $O(N + log \ N) \equiv O(N)$ 

This algorithm works by assigning births a value of +1 and deaths a value of -1
Dates are placed into a sorted array with these delta values
Then you can simply iterate through the array and track when the maximum people were alive

Mistakes:
	Wrote `a.Date.DeltaCount` instead of `a.DeltaCount` 
	Forgot to write `struct` before `DatePoint` in one of the mallocs 
	Don't print to `stderr` if it's the output

![[Pasted image 20240716165423.png]]

This is kinda like a dynamic programming question
If I know B connects to C in 3 steps
And A connects to B 
Then A connects to C in 4 steps

So I need a way to store this kind of information easily 
Hashmaps are not available 
I'd need $N^2 - N$ unsigneds as I don't care about nodes that connect to themselves
Although it might be easier to leave them in
Given 10 nodes always multiply the smaller by 10 and add
0-5 = 0 + 5 = 5
3-8 = 30 + 8 = 38
8-3 = 30 + 8 = 38
8-9 = 89
0-1 = 1
Thus I need $N^2 - N = 100 - 10 = 90$ slots although the 0 slot will go unused 
Lets call these values pathVals 

Ok this is stupid there's no way it's a N^2 algorithm 

Ok it's an N^2 algorithm, unexpected
Here's my new approach:

For each node:
	Recursively check down every possible path. Use an int array to check whether a given node has been visited before
	Set the int array slots to the current node index so we don't need to clear the array on each iteration 
	Quit out if the separation goes above k (Probably easier to count down)

FUCK the known people uses ptrs not indices 
I think we can assume the input array contains all people in the world 

Ok fuck this question I'm out
#todo

```c
void check_down_path(struct person* people, int nodeIdx, int baseNodeIdx, unsigned kDown, int* dpArr) {
	dpArr[nodeIdx] = baseNodeIdx;
	kDown--;
	if (kDown <= 0)
		return;
	for (int i = 0; i < people[nodeIdx].number_of_known_people; i++) {
		check_down_path(people, people[nodeIdx].known_people[i])
	}
}

int within_k_degrees(struct person* people, int num_people, unsigned k) {

}
```
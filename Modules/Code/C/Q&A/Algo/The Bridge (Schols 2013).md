
![[Pasted image 20240716172812.png]]![[Pasted image 20240716173200.png]]

This is a dynamic programming question I think
Every turn dagobert has these options:
- Bubbles above front & Valid spot to move -> Move front leg forward N spaces
- Valid spot to move -> Move rear leg forward N spaces
- Rear leg not at back -> Move bubbles forward N spaces

Win state is when at all bubbles and legs are off the board

Starting State:
ooooo
LL
PPPGPPGPPGPGPPGPPG

Thankfully you can't move backwards so storing states we've already seen isn't as important
But how would you do it in case it's easy? 
The state is determined by the position of the legs, bubbles and steps. That's a lot to track
Actually this is only going to work if you can track the current best steps to reach every position otherwise the time will go crazy

Might be best to go backwards so start at the position
                     ooooo
                     LL
PPPGPPGPGGPPPPGPPPP

And try and reach the start state while tracking the best steps to reach every position along the way
Idk seems complicated

Try not backwards first

Assume you start at state S
You take k moves to reach state C
And it takes p moves to get to E using a path that contains C
Then through recursion you find a path to C that takes less steps
How can I update the total without redoing the rest of the sim? 
Do some sort of pointer stuff where E points to C points to S
E contains the moves to get from C to E
C contains the moves to get from S to C
If a new path B is found that also gets to E in less moves then make E point to B and update move count
If you reach a state that's already been found you can exit out
To calculate the final minimum start at the end and follow backwards while summing the move counts

Ok but how do I store this information? There's N+b states the legs and bubbles can be in
Thus we need a 3(N+b) sized State array
Make it so there's a separate WinState outside the array that gets used when the board is in a winning condition 

There's no reason to not always move bubbles as much as possible

```c
struct State {
	int PrevStateIdx = -1;
	int MovesToHere = -1;
}

// Gets the index into the tracking array for the state of the "board"
int getStateIndex(int rearPos, int frontPos, int bubblePos, int N, int b) {
	return rearPos + frontPos * (N + b) + bubblePos * 2 * (N + b);
}

// Finds the height of the tree to the state given
int movesToState(struct State* trackingArr, int stateIdx) {
	int counter = 0;
	int curState = stateIdx;
	while (counter != -1) {
		int prevState = trackingArr[curState].PrevStateIdx;
		if (prevState == curState)
			return counter; // General return
			
		counter++;
		curState = prevState;
	}
	return counter; // Edge cases
}

// Dynamic programming recursive search
void dynamic_search(int b, int N, char* planks, struct State* trackingArr, int rearLegPos, int frontLegPos, int bubblePos, struct State* winState, int curMoves, int prevStateIdx) {
	int stateIdx = getStateIndex(rearLegPos, frontLegPos, bubblePos, N, b);
	int existingPrev = trackingArr[stateIdx].PrevStateIdx;
	
	if (prevStateIdx = stateIdx) // Null move
		return;

	// Winning state writes into winState rather than trackingArr
	_Bool win = rearLegPos >= N && frontLegPos >= N && bubblePos - b >= N;
	if (win) {
		if (winState.PrevStateIdx == -1 || winState.MovesToHere > curMoves) {
			winState.PrevStateIdx = stateIdx;
			winState.MovesToHere = curMoves;
		}
		return;
	}

	// At a state that has already been seen before
	if (existingPrev != -1) {
		// If you got to this state faster then update the links
		if (movesToHere(trackingArr, stateIdx) > curMoves)  // O(?)
			trackingArr[stateIdx].PrevStateIdx = prevStateIdx;		
		return;
	}

	// Search every front leg move
	for (int i = frontLegpos+1; i < bubblePos; i++) {
		if (planks[i] == 'G')
			continue;
		dynamic_search(b, N, planks, trackingArr, rearLegPos, i, bubblePos, winState, curMoves+1, stateIdx); // O(b)
	}

	// Search every rear leg move
	for (int i = rearLegPos+1; i < frontLegPos; i++) {
		if (planks[i] == 'G')
			continue;
		dynamic_search(b, N, planks, trackingArr, i, frontLegPos, bubblePos, winState, curMoves+1, stateIdx); // O(b)
	}	

	// Search the maximum bubble move
	int bubbleMoveAmount = bubblePos - b - rearLegPos;
	if (bubbleMoveAmount > 0)
		dynamic_search(b, N, planks, trackingArr, rearLegPos, frontLegPos, bubblePos + bubbleMoveAmount, curMoves+1, stateIdx); // O(1)
}

int the_bridge(int b, int N, char* planks) {
	struct State trackingArr[3 * N + 3 * b]; // One state for every combination of rear leg, front leg and bubble position
	struct State winState;
	
	int startStateIdx = getStateIndex(0, 1, b-1, N, b);
	trackingArr[startStateIdx].PrevStateIdx = startStateIdx; // Points at itself to signify its terminal 
	
	dynamic_search(b, N, planks, trackingArr, 0, 1, b-1, &winState, 0, startStateIdx);

	return winState.MovesToHere;
}
```

For every possible N states of the bubbles theres $b^2$ states for the legs
Thus there are $Nb^2$ possible states
Thus the time complexity is $O(Nb^2 + b)$ 

I believe this determines the shortest possible moves as it checks every possible state the board can be in without redoing any work

Mistakes:
	FORGOT STRUCT SEMICOLON AGAIN
	Did `winState.` instead of `winState->` 
	Structs don't have default values. You need to set the values manually which changes time complexity slightly
	`trackingArr[3 * N + 3 * b]` is invalid. Needs to be comptime to do stack arrays. Just use malloc from now on for all arrays 
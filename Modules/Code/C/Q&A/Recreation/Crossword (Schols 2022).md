
![[Pasted image 20240716173536.png]]
![[Pasted image 20240716173544.png]]

So the idea here is that we need to find all words that share a character at the intersection points
I'm immediately thinking of making a 2 alphabet arrays for horizontal and vertical that contains the words for that letter 
The words can be represented by indices into the dictionary. But how do I store these indices? If this plan works it's O(N) I think? 
We can store the indices in 26 * 26 * N slots which is a lot of memory but setting can be avoided by making them -1 terminated 

Another idea which may be faster is going through each word and making two bitfields for horizontal and vertical 
Then we can AND the bitfields against each other to determine matches. This is N^2 so not great
Probably better for memory than time 

I'm going to assume all letters are capitals

```c
void completeCrosswordFragment(int vertical_word_length, int vertical_intersection_point, int horizontal_word_length, 
										 int horizontal_intersection_point, char** dictionary, int dictionary_length) {
	int* hAlphabetArr[26];
	int* vAlphabetArr[26];
	// Allocate alphabet arrays and set up index pointers
	for (int i = 0; i < 26; i++) { // O(1)
		hAlphabetArr[i] = malloc(sizeof(int) * (dictionary_length + 1));
		hAlphabetArr[i][0] = 1;
		vAlphabetArr[i] = malloc(sizeof(int) * (dictionary_length + 1));
		vAlphabetArr[i][0] = 1;
	}

	// Place all words into correct alphabet slots
	for (int i = 0; i < dictionary_length; i++) { // O(N)
		char* word = dictionary[i];
		
		if (strlen(word) <= horizontal_word_length) {
			char hLetter = word[horizontal_intersection_point];
			int frontIdx = hAlphabetArr[hLetter][0];
			hAlphabetArr[hLetter][frontIdx] = i;
			hAlphabetArr[hLetter][0]++;
		}
		
		if (strlen(word) <= vertical_word_length) {
			char vLetter = word[vertical_intersection_point];
			int frontIdx = vAlphabetArr[vLetter][0];
			vAlphabetArr[vLetter][frontIdx] = i;
			vAlphabetArr[vLetter][0]++;
		}
	}

	// Print all matching alphabet words
	for (int i = 0; i < 26; i++) { // O(N^2) worst case
		for (int j = 1; j < hAlphabet[i][0]; j++) {
			char* hWord = dictionary[hAlphabet[i][j]];
			for (int k = 1; k < vAlphabet[i][0]; k++) {
				char* vWord = dictionary[vAlphabet[i][k]];
				fprintf("Horizontal: %s, Vertical: %s", hWord, vWord);
			}
		}
	}

	// Free data
	for (int i = 0; i < 26; i++) {
		free(hAlphabetArr[i]);
		free(vAlphabetArr[i]);
	}
}
```

While yes printing is N^2 in the worst case, in practise/average case it would be incredibly fast as very few words will end up in each letter slot. All words are split between the 26 letter slots for each axis. 

Average case is O(N) due to main loop 
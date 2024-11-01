
![[Pasted image 20240801195332.png]]

(a)
This is a backtracking question
First function checks every letter to start from
Second function recursively checks adjacent letters to a certain position
Its easier to check the word backwards as it requires less params in the second func
To prevent a letters being reused we'll use a board state bitset 

We'll assume the word is stored in a char* where a char is a byte long
And we'll assume the board is stored in a 2D 4x4 matrix char** where a char is a byte long 

WordExists:
	for (y in col)
		for (x in row)		
			WordExistsFromChar(word, board, x, y);
WordExistsFromChar:
	if (wordIndex == 0)
		return true;
	if (word$[wordIndex]$ != board$[y][x]$)
		return false;	
	if (boardStateBits >> 4y + x == 1)
		return false;
	boardStateBits |= 1 << 4y + x;
	if (x < 3 && y < 3 && WordExistsFromChar(word, board, x+1, y+1, wordIndex-1))
		return true; 
	if (x < 3 && WordExistsFromChar(word, board, x+1, y, wordIndex-1))
		return true; 
	if (x < 3 && y > 0 && WordExistsFromChar(word, board, x+1, y-1, wordIndex-1))
		return true; 
	if (y < 3 && WordExistsFromChar(word, board, x, y+1, wordIndex-1))
		return true; 
	if (y > 0 && WordExistsFromChar(word, board, x, y-1, wordIndex-1))
		return true; 
	if (x > 0 && y < 3 && WordExistsFromChar(word, board, x-1, y+1, wordIndex-1))
		return true; 
	if (x > 0 && WordExistsFromChar(word, board, x-1, y, wordIndex-1))
		return true; 
	if (x > 0 && y > 0 && WordExistsFromChar(word, board, x-1, y-1, wordIndex-1))
		return true; 
	return false;
	
```arm
@ IN:
@ R0 - char* wordInput
@ R1 - char** boggleBoard
@ R2 - int wordSize
@ OUT:
@ R0 - bool result
WordExists:
	PUSH {LR, R6-R12}
	MOV R7, #0
	SUB R6, R2, #1	
.LWordExists_ForLoopY:
	CMP R7, #4
	BGE .LWordExists_ForLoopYBreak

	MOV R8, #0
.LWordExists_ForLoopX:
	CMP R8, #4
	BGE .LWordExists_ForLoopXBreak

	MOV R2, R8
	MOV R3, R7
	MOV R4, R6
	MOV R5, #0
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExists_ReturnTrue

	ADD R8, R8, #1
	B .LWordExists_ForLoopX
.LWordExists_ForLoopXBreak:

	ADD R7, R7, #1
	B .LWordExists_ForLoopY
.LWordExists_ForLoopYBreak:

	MOV R0, #0		
	POP {LR, R6-R12}

.LWordExists_ReturnTrue:
	MOV R0, #1		
	POP {LR, R6-R12}

@ IN:
@ R0 - char* wordInput
@ R1 - char** boggleBoard
@ R2 - int rowIndex
@ R3 - int colIndex
@ R4 - int wordIndex
@ R5 - int boardStateBits
@ OUT:
@ R2 - bool result
WordExistsFromChar:
	PUSH {LR, R6-R12}
	CMP R4, #0
	BEQ .LWordExistsFromChar_ReturnTrue

	LDRB R6, [R0, R4]
	MUL R7, R3, #4
	ADD R7, R7, R2
	LDRB R8, [R1, R7]	
	CMP R6, R8
	BNE .LWordExistsFromChar_ReturnFalse

	LSR R6, R5, R7
	AND R6, R6, #1
	CMP R6, #1
	BEQ .LWordExistsFromChar_ReturnFalse

	MOV R8, #1
	LSL R6, R8, R7
	ORR R5, R5, R6

	SUB R4, R4, #1
	MOV R10, R2
	MOV R11, R3

.LWordExistsFromChar_XP_YP:

	CMP R10, #3
	BGE .LWordExistsFromChar_YP
	CMP R11, #3
	BGE .LWordExistsFromChar_XP

	ADD R2, R10, #1
	ADD R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_XP:

	ADD R2, R10, #1
	MOV R3, R11
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_XP_YN:

	CMP R11, #0
	BLE .LWordExistsFromChar_YP

	ADD R2, R10, #1
	SUB R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_YP:

	CMP R11, #3
	BGE .LWordExistsFromChar_YN

	MOV R2, R10
	ADD R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_YN:

	CMP R11, #0
	BLE .LWordExistsFromChar_XN_YP

	MOV R2, R10
	SUB R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_XN_YP:

	CMP R10, #0
	BLE .LWordExistsFromChar_ReturnFalse
	CMP R11, #3
	BGE .LWordExistsFromChar_XN

	SUB R2, R10, #1
	ADD R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_XN:

	SUB R2, R10, #1
	MOV R3, R11
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_XN_YN:

	CMP R11, #0
	BLE .LWordExistsFromChar_ReturnFalse

	SUB R2, R10, #1
	SUB R3, R11, #1
	BL WordExistsFromChar
	CMP R2, #1
	BEQ .LWordExistsFromChar_ReturnTrue

.LWordExistsFromChar_ReturnFalse:
	MOV R2, #0
	POP {LR, R6-R12}

.LWordExistsFromChar_ReturnTrue:
	MOV R2, #1	
	POP {LR, R6-R12}
```

(b)
Take in a list of words (char**) and using a loop check over every single one to see if it exists
If so then counter++
Return counter

We'll store the words in an irregular dimensioned char** 
And the word lengths in an int array

```arm
@ IN:
@ R0 - char** wordList
@ R1 - char** boggleBoard
@ R2 - int* wordLengths
@ R3 - int wordsCount
@ OUT:
@ R0 - bool result
CalculateScore:
	PUSH {LR, R4-R12}

	MOV R7, #0
	
	MOV R6, R0
	MOV R8, R2
	MOV R9, R3

	MOV R5, #0
.LCalculateScore_Loop:

	CMP R5, R9
	BGE .LCalculateScore_LoopBreak

	LDR R0, [R6, R5, LSL #4]
	LDR R2, [R8, R5, LSL #4]	
	MOV R12, R2
	BL WordExists
	CMP R0, #0
	BL .LCalculateScore_LoopContinue

	ADD R7, R7, R12
	
.LCalculateScore_LoopContinue:
	ADD R5, R5, #1
	BL .LCalculateScore_Loop
.LCalculateScore_LoopBreak:
	MOV R0, R7
	POP {LR, R4-R12}
```

Mistakes Made:
	You cannot use immediate values in MUL
	For LDR I used LSL #4 instead of #2 
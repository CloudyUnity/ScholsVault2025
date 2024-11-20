
![[Pasted image 20240801194257.png]]

(a)
For decoding in assembly the easiest way is to follow the tree directly I think
We want to maximise cache coherency though so can we avoid an ACTUAL tree?
Lets try using a binary heap
Create a `char[]` of size $1 + 2 + 2^2 + \dots + 2^h$ where $h$ is the tree height
Start at index 1 for the root
The children of node $n$ are at index $2n$ and $2n+1$ 
If the char does not equal '\0' then you should return that as you've hit a leaf
This tree would be stored in the heap:
```c
char HuffmanHeap[N+1] = {'\0', // 0
						'\0' // Root
						'\0', '\0',
						' ', 'a', '\0', 'd', 
						'\0', '\0', '\0', '\0', '\0', 'e', '\0', '\0','\0',
						'\0', '\0', '\0', '\0', '\0', '\0', '\0', '\0', 'c', 'b', '\0', '\0', '\0', '\0', '\0', '\0', '\0', '\0'
						  };
```
While yes it looks large for this tree it is only 35 bytes so it's pretty efficient and fast for decoding
(b)
Go through each bit tracking the current heap index. If you hit a char then add it to the output stream and restart
Remember that the input will be stored in a word[] and the output is a char[]
.
```java
int heapIdx = 1;
int outIdx = 0;
	
for (w in words)
	for (b in 0..31)
		if (heap[heapIdx] != '\0') 
			output[outIdx] = heap[heapIdx];
			outIdx++;
			heapIdx = 1;
		int bit = w >> b & 1;
		heapIdx *= 2;
		if (bit == 1)
			heapIdx++;		
```
(c)
We can optimize out `outIdx` by just storing and incrementing the output address

```c
@ R0 - char* OutputAddr
@ R1 - int* InputAddr
@ R2 - char* HeapAddr
@ R3 - int InputSize
HuffmanDecode:
PUSH {R4-R12, LR}

MOV R6, #1 @ HeapIdx

MOV R4, #0 @ WordIdx
.LHuffmanDecode_WordLoop:
CMP R4, R3
BGE .LHuffmanDecode_WordLoopBreak

LDR R9, [R1, R4, LSL #2] @ word

MOV R5, #0 @ BitIdx
.LHuffmanDecode_BitLoop:
CMP R5, #31
BGE .LHuffmanDecode_BitLoopBreak

LDRB R8, [R2, R6]
CMP R8, #0
BEQ .LHuffmanDecode_BitLoop_CharNull

STRB R8, [R0]
ADD R0, R0, #1
MOV R6, #1

.LHuffmanDecode_BitLoop_CharNull:

LSR R8, R9, R5 @ bit
AND R8, R8, #1

MOV R10, #2
MUL R6, R6, R10 @ heapIdx *= 2

CMP R8, #1
BNE .LHuffmanDecode_BitLoop

ADD R6, R6, #1
B .LHuffmanDecode_BitLoop

ADD R5, R5, #1
B LHuffmanDecode_BitLoop
.LHuffmanDecode_BitLoopBreak:

ADD R4, R4, #1
B .LHuffmanDecode_WordLoop
.LHuffmanDecode_WordLoopBreak:

POP {R4-R12, LR}
```


First (wrong) thoughts:
	You don't need the tree once you've generated the codes
	Each code is a unique number so they can be stored directly as binary
	The codes don't extend past a byte
```c
struct codes { 
	char chars[MAX_ASCII];
	u8 codes[MAX_ASCII];
}
```
As MAX_ASCII will never grow that large, cache coherency is not much of an issue I think? 
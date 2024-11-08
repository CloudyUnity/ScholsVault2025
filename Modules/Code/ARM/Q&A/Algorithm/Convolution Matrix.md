
![[Pasted image 20240801195004.png]]

Calculate N
int N = 0;
for (rY < 2R + 1)
	for (rX < 2R + 1)
		N += conMat$[rY][rX]$;
for (y)
	for (x)
		int sum = 0;
		for (rY < 2R + 1)
			for (rX < 2R + 1)
				sum += conMat$[rY][rX] * pixels[y+rY-R][x+rX-R]$;
		sum /= N;
		K$[y][x]$ = sum;


```arm
@ IN:
@ R0 - char** DstImageR
@ R1 - char** SrcImageR
@ R2 - int** ConMatrix
@ R3 - int ImageWidth
@ R4 - int ImageHeight
@ R5 - ConMatrixR
@ OUT:
@ N/A
ConvolutionMatrix:
	PUSH {R6-R12, LR}

	MOV R12, #2
	MUL R12, R5, R12 @ 2R
	
	MOV R6, #0 @ N
	MOV R7, #0 @ rY
.LConvolutionMatrix_LoopN_Y:
	CMP R7, R12
	BGE .LConvolutionMatrix_LoopN_Y_Break

	MUL R9, R7, R12

	MOV R8, #0
.LConvolutionMatrix_LoopN_X:
	CMP R8, R12
	BGE .LConvolutionMatrix_LoopN_X_Break
	
	ADD R10, R9, R8
	LDR R10, [R2, R10, LSL #2]
	ADD R6, R6, R10

	ADD R8, R8, #1
	B .LConvolutionMatrix_LoopN_X
.LConvolutionMatrix_LoopN_X_Break:

	ADD R7, R7, #1
	B .LConvolutionMatrix_LoopN_Y
.LConvolutionMatrix_LoopN_Y_Break:


	MOV R7, #0 @ y
.LConvolutionMatrix_LoopMain_Y:
	CMP R7, R4
	BGE .LConvolutionMatrix_LoopMain_Y_Break

	MOV R8, #0 @ x
.LConvolutionMatrix_LoopMain_X:
	CMP R8, R3
	BGE .LConvolutionMatrix_LoopMain_X_Break

	PUSH {R0, R3, R4, R7, R8}
	SUB R7, R7, R5
	SUB R8, R8, R5

	MOV R9, #0 @ sum
	MOV R10, #0 @ rY
.LConvolutionMatrix_LoopMain_LoopConv_Y:
	CMP R10, R12
	BGE .LConvolutionMatrix_LoopMain_LoopConv_Y_Break

	MUL R3, R7, R12

	MOV R11, #0 @ rX
.LConvolutionMatrix_LoopMain_LoopConv_X:
	CMP R11, R12
	BGE .LConvolutionMatrix_LoopMain_LoopConv_X_Break

	ADD R0, R3, R11
	LDR R0, [R2, R0, LSL #2] @ conMat[rY][rX]

	ADD R7, R7, R10 @ y - R + rY
	ADD R8, R8, R11 @ x - R + rX
	ADD R7, R7, R8
	LDRB R7, [R1, R7]
	MUL R7, R7, R0
	ADD R9, R9, R7 @ sum += val;

	ADD R11, R11, #1
	B .LConvolutionMatrix_LoopMain_LoopConv_X
.LConvolutionMatrix_LoopMain_LoopConv_X_Break:

	ADD R10, R10, #1
	B .LConvolutionMatrix_LoopMain_LoopConv_Y
.LConvolutionMatrix_LoopMain_LoopConv_Y_Break:

	POP {R0, R3, R4, R7, R8}

	UDIV R9, R9, R6 @ sum /= N
	MUL R10, R7, R3 @ y * width
	ADD R10, R10, R8
	STRB R9, [R0, R10] @ K[y][x] = sum;

	ADD R8, R8, #1
	B .LConvolutionMatrix_LoopMain_X
.LConvolutionMatrix_LoopMain_X_Break:

	ADD R7, R7, #1
	B .LConvolutionMatrix_LoopMain_Y
.LConvolutionMatrix_LoopMain_Y_Break:

	POP {R6-R12, LR}
```

Mistakes made:
	Only minor syntax errors on labels 

![[Pasted image 20240801195116.png]]

(i)
I would store the cube in the format Pillar0(Row0 Row1 Row2 ... RowN) Pillar1(Row0 Row 1 Row2 ... RowN) ...

(ii)
```c
@ In:
@ R0 - int* MagicCubeAddress 
@ R1 - int x
@ R2 - int y
@ R3 - int z
@ R4 - int N
@ Out:
@ R0 - int Value
MagicCubeGet:
	PUSH {R5-R6}
	MUL R5, R3, R4
	MUL R5, R5, R4
	ADD R5, R5, R1
	MUL R6, R2, R4
	ADD R0, R5, R6
	POP {R5-R6}
	BX LR
```

(iii)
Diags:
	x == y == z
	n-x == y == z
	x == n-y == z
	x == y == n-z

int diagXYZSum = 0, diagNYZSum = 0, diagXNZSum = 0, diagXYNSum = 0;

for (int z = 0; z < n; z++)
	for (int y = 0; y < n; y++)
		int xSum = 0;
		for (int x = 0; x < n; x++)
			xSum += get(x, y, z);
			if (x == y == z)
				diagXYZSum += get(x, y, z);
			if (n-x == y == z)
				diagNYZSum += get(x, y, z);
			if (x == n-y == z)
				diagXNZSum += get(x, y, z);
			if (x == y == n-z)
				diagXYNSum += get(x, y, z);
		validate(xSum);
validate(diags); // x4

for (int z = 0; z < n; z++)
	for (int x = 0; x < n; x++)
		int ySum = 0;
		for (int y = 0; y < n; y++)
			ySum += get(x, y, z);
		validate(ySum);

for (int y = 0; y < n; y++)
	for (int x = 0; x < n; x++)
		int zSum = 0;
		for (int z = 0; z < n; z++)
			zSum += get(x, y, z);
		validate(zSum);

(iv)
Only the rows huh? Making life easy
```c
@ In:
@ R0 - int* MagicCubeAddress
@ R1 - int N
@ Out:
@ R0 - bool IsMagicCube
ValidateMagicCube:
	PUSH {R4-R10, LR}
	MOV R7, R0
	MOV R8, R1

	MUL R10, R8, R8 @ N^2
	MUL R10, R10, R8 @ N^3
	ADD R10, R10, #1 @ N^3 + 1
	MUL R10, R10, R8 @ N(N^3 + 1)
	MOV R4, #2
	UDIV R10, R10, R4 @ magicConstant = N(N^3 + 1)/2
	
	MOV R4, #0 @ z
.LValidateMagicCube_ZLoop:
	CMP R4, R8
	BGE .LValidateMagicCube_ZLoop_Break
	
	MOV R5, #0 @ y
.LValidateMagicCube_YLoop:
	CMP R5, R8
	BGE .LValidateMagicCube_YLoop_Break

	MOV R9, #0 @ xSum = 0;
	
	MOV R6, #0 @ x
.LValidateMagicCube_XLoop:
	CMP R6, R8
	BGE .LValidateMagicCube_XLoop_Break

	MOV R0, R7
	MOV R1, R6
	MOV R2, R5
	MOV R3, R4
	MOV R4, R8
	BL MagicCubeGet @ xSum += MagicCubeGet(cube, x, y, z, N);
	ADD R9, R9, R0

	ADD R6, R6, #1
	B .LValidateMagicCube_XLoop
.LValidateMagicCube_XLoop_Break:

	CMP R9, R10 @ Compare xSum with magic constant
	BNE .LValidateMagicCube_ReturnFalse

	ADD R5, R5, #1
	B .LValidateMagicCube_YLoop
.LValidateMagicCube_YLoop_Break:

	ADD R4, R4, #1
	B .LValidateMagicCube_ZLoop
.LValidateMagicCube_ZLoop_Break:
	MOV R0, #1
	POP {R4-R10, LR}

.LValidateMagicCube_ReturnFalse:
	MOV R0, #0
	POP {R4-R10, LR}
```

Mistakes:
	None :)
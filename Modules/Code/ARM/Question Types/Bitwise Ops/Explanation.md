Set bit n of Rn:
	ORR Rn, Rn, 0b1 LSL n

Reset bit n of Rn:
	AND Rn, Rn, 0b11111011111
	Where the 0 represents the specific bit to be reset

Reset bit n of Rn (Alt):
	BIC Rn, Rn, 0b1 LSL n

Toggle bit n of Rn:
	EOR Rn, Rn, 0b1 LSL n
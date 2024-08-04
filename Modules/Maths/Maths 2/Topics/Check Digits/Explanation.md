num = $a_1 a_2 a_3 a_4 a_{5} a_{6} a_{7} a_{8} a_{9} a_{10}$

Check digits are a number appended to the end of a sequence of numbers carefully chosen to detect errors in reading the sequence

ISBN-10 (Pre-2007):
	$a_{10}$ can be 'X' for a value of 10
	$a_{10} \equiv -10a_1 - 9a_2 - \  ...\  - 2a_9$ (mod 11)
	$10a_1 + 9a_2 +\  ...\  + 1a_{10} \equiv 0$ (mod 11)
	Can only detect errors when adjacent digits are swapped or single digit changed

ISBN-13 (Post-2007)
	978 is appended to start of all books
	num = 978$a_4 a_{5} a_{6} a_{7} a_{8} a_{9} a_{10} a_{11} a_{12} a_{13}$
	$1a_1 + 3a_2 + 1a_3 + 3a_4 + ... + 1a_{13} \equiv 0$ (mod 10)
	Does not detect all errors that ISBN-10 does	
		Fails adjacent digit swap error when difference between digits is $\pm 5$
	'X' is not used due to mod 10	
	Introduced to make books more compatible with other items

GTIN (EAN-13):
	Same check as ISBN-13 but without required 978

Dot Product Notation:
	$w$ = (1, 3, ... ,1)
		The weighting vector
	$w \cdot (a_1, a_2, ... ,a_k) \equiv 0$ (mod 10)	

#bonus 
EAN = European Article Numbers
UPC = Universal Product Code
ISBN = International Standard Book Number
GTIN = Global Trade Item Number
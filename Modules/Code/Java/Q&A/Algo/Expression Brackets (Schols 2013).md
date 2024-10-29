
![[Pasted image 20240716172212.png]]

3 + (4 + 5) -> 3 + 4 + 5
	+(+) -> Remove
(5 * 6) + 3 -> 5 * 6 + 3
	($*$)+ -> Remove
(1 * 2) / 4 -> 1 * 2 / 4
	($*$)/ -> Remove
3 * (1 + 4) -> 3 * (1 + 4)
	$*$(+) -> Keep
All brackets will be surrounded by other operators or nothing
To remove brackets it needs to be surrounded by less than or equal ops
The inner op of a bracket is the highest op in the non recursive bracket expression

Recursively fix brackets

```java
int GetOpScore(char c)
{
	if (c == '+' || c == '-')
		return 5;
	if (c == '*' || c == '/')
		return 15;
	if (c == '^')
		return 20;
	return -1;
}

boolean GEQPrecendence(char op, char opCompare)
{
	return GetOpScore(op) >= GetOpScore(opCompare);
}

boolean IsOp(char c)
{
	return c == '+' || c == '-' || c == '*' || c == '/' || c == '^';
}

int GetOpScoreOfExpr(String expr)
{
	int maxScore = -1;
	for (int i = 0; i < expr.length(); i++)
	{
		if (expr.charAt(i) == '(')
		{
			while (i < expr.length() && expr.charAt(i) != ')')
				i++;
			continue;
		}
		
		if (IsOp(expr.charAt(i)))
			maxScore = Math.max(maxScore, GetOpScore(expr.charAt(i)));
	}
	return maxScore;
}

String SolveEq(String input)
{
	String expr = "";
	for (int i = 0; i < input.length(); i++)
	{
		if (input.charAt(i) != '(')
		{
			expr += input.charAt(i);
			continue;
		}			

		int bracketScore = 1;
		int j = i+1;
		while (j < input.length())
		{
			if (input.charAt(j) == '(')
				bracketScore++;
			else if (input.charAt(j) == ')')
			{
				bracketScore--;
				if (bracketScore == 0)
					break;
			}
			j++;	
		}			

		String inner = input.substring(i+1, j);
		inner = SolveEq(inner);
		int opScore = GetOpScoreOfExpr(inner);
		if (opScore == 20)
		{
			expr += "(" + inner + ")";
			i = j+1;
			continue;
		}
		
		int leftOpScore = -1;
		int rightOpScore = -1;
		int leftI = i-1, rightI = j+1;
		
		while (leftI >= 0)
		{
			if (IsOp(input.charAt(leftI)))
			{
				leftOpScore = GetOpScore(input.charAt(leftI));
				break;
			}			
			leftI--;	
		}
		while (rightI < input.length())
		{
			if (IsOp(input.charAt(rightI)))
			{
				rightOpScore = GetOpScore(input.charAt(rightI));
				break;
			}			
			rightI++;
		}
		
		if (leftOpScore <= opScore && rightOpScore <= opScore)
			expr += inner;
		else
			expr += "(" + inner + ")";
		i = j+1;
	}
	return expr;
}
```

Mistakes made:
	Used `str.length` instead of `str.length()`
	Wrote `subString()` instead of `substring()`
	Didn't put bounds checking on search for right bracket
	Didn't account for recursive left brackets when searching for right bracket, see bracketScore
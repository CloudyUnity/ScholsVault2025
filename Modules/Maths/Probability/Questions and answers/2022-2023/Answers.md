# Q5
A basic, but wordy question regarding linear regression, computationally a very easy question but you need lots of background knowledge to approach it

(a) Scatter plot
(b) Use calculator to compute r, the result is r = 0.5683280943 or r = 0.568, The value suggests that there is a weak correlation between the two variables.
(c) the formula of r can be given by r = a + bx, where r is the correlation coefficient, a is the intercept and b is the slope of the line, most calculators will compute these values automatically.
  a = 1.35
  b = 1.70
  These values suggest that the values are correlated, as the slope is positive and that we predict the y value to be at 1.35 when x is at 0
  #questionable #manual_calculations_needed
- They are, the data points do seem to trend upwards in a logorithmic fashion, which explains the positive slope, i.e the value of b, since most data  points are near or above the 0 mark, a y intercept of 1.35 seems reasonable, these values are as such in line with what we would have expected
  #debatable 
- The formula for any point in a residual plot can be defined as $r_{i} = y_{i} - (a + bx_{i})$
  
  There are four assumptions for simple linear regression.
	- Linear relationship = There exists a *Linear* relationship between all the given variables, in this case 2
	- Independence = A previous data-point does not effect the next data-point, for example if we were gathering data on a die, and landing on 6 cause the dice to be 2 times more likely to land on 1 next roll, the collected data points would not be independent.
	- Homoscedasticity = The residuals (The difference between the actual data and what we expected) remains with constant variance throughout x.
	- The residuals of the model are normally distributed
	The given model fulfills are assumptions because #blahblahblah


# Q6
(a)
- 1 / 4
- For this question we can use [Hypergeometric distribution](https://en.wikipedia.org/wiki/Hypergeometric_distribution), this is a function that works similar to the normal distribution, but instead of showing us the probability of an event happening x times given y attemps at z probability, it does so assuming that we are sampling without distribution.
	We need this due to calculate the probability of the two of clubs appearing before the first ace, and the add that with the probability of picking it after the ace is drawn
	$$
{\displaystyle p_{X}(k)=\Pr(X=k)={\frac {{\binom {K}{k}}{\binom {N-K}{n-k}}}{\binom {N}{n}}}}
$$
- N is the population size,
- K  is the number of success states in the population,
- n  is the number of draws (i.e. quantity drawn in each trial),
- k  is the number of observed successes
The brackets that look like fractions but do not have the line on the equation represent:
$$
\binom{k}{n} = \frac{k!}{n!(k-n)!}
$$
which on your calculator is represented by the nCr above the division button most likely
	As such, there are 47 (52 - the 2 of club - 4 aces) cards to choose from for the first 19 draws, on which we must not draw the 2 of clubs, and afterwards we add the probability of  drawing a 2 of clubs
	$$
{{\frac {{\binom {1}{0}}{\binom {47-1}{19-0}}}{\binom {47}{19}}}*\left( \frac{1}{47-20} \right) = 5.311*10^{-15}}
$$
#debatable I am unsure if this is the correct answer as the answer is such a small number, might need double checking

***Note***: You could theoretically do this without the formula, but it would take too long, you do not get this formula at the back of the exam :(

#combinatronics

(b) 
- Given the problem:
$$
F: \text{coin is fair}
$$
$$
H: \text{heads}
$$
$$
T: \text{tails}
$$
$$
P(F|H) = \frac{P(H|F)\times P(F)}{P(H)}
$$
answer: $\frac{1}{3}$
- Given the problem:
$$
\frac{1}{3}^{2} = \frac{1}{9}
$$
	#### NAAAAAAAAAAA
- Did you fall for it? the answer is not $\frac{1}{9}$, soweee, you need to use Baye's theorem again ;(
- Given the problem:
$$
\text{F: coing is fair}
$$
$$
\text{HH: two heads in a row}
$$
Note that we are not changing the coin, meaning that to find $HH$ :
$$
P(HH) = P(HH∣F)P(F)+P(HH∣!F)P(!F) = \frac{5}{8}
$$
We then compute the answer using the same formula and get $\frac{1}{5}$ as the answer

- 100%, pretty obvious trick question

#bayesTheorem
#probability

(c)
- To solve this question we must first formalize the information given to use by the question
M1:
$$
P(M_{1}) = p^{2}+2p(1-p)
$$
$$
P(M_{2}) = p^{4} + \binom{4}{3}(1-p)p^{3} + \binom{4}{2}(1-p)^{2}p^{2}
$$
$$
\text{Note: } \binom{4}{3} = {}^4C_{3}
$$

from there we set the equations to be equal and solve to find the intesections, you should get the answer
$$
0\leq p \leq \frac{1}{3}
$$
I am not sure if there is a fuss about the $<$ vs $\leq$
#probability

(d)
- Given the problem:
remember:
$$
p(k)=\frac{λ^k}{k!}exp(−λ)
$$
The joint probability mass function is **a function that completely characterizes the distribution of a discrete random vector**
(i)
$$
p(X = x, Y= y) = P(X=x)P(Y=y) = \frac{(\mu_{1})^x}{x!}e^{-\mu_{1}} \cdot \frac{(\mu_{2})^y}{y!}e^{-\mu_{2}}
$$
(ii)
$$
\frac{(\mu_{1})^0}{0!}e^{-\mu_{1}}\cdot\frac{(\mu_{2})^0}{0!}e^{-\mu_{2}}
$$
$$
e^{-\mu_{1}}\cdot e^{-\mu_{2}} = 0 \text{ errors made}
$$
$$
\text{answer: } (1 - e^{-\mu_{1}} * e^{-\mu_{2}})
$$
(iii)
Remember, the sum of two different Poisson distributions i just the combination of their lambdas
$$
P(X + Y = m) = {\frac{(\mu_{1}+\mu_{2})^{m}{e^{-(\mu_{1}+\mu_{2})}}}{m!}}
$$
#Distributions #PoissonDistribution #debatable #hard
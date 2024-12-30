
> [!question]- #schols [2024] ![[Pasted image 20241027193145.png]]
 (i)
 $P(ABC) = P(A)P(B)P(C) = 0.6 \times 0.5 \times 0.4 = 0.12$
 (ii)
 Find probability not (exactly 0 rooms are not booked)
 not (every room is booked)
 not $(P(ABC)) = 1- 0.12 = 0.88$ 
 (iii)
 $P(A)P(B)'P(C)' + P(A)'P(B)P(C)' + P(A)'P(B)'P(C) = 0.6 (0.5) (0.6) + 0.4 (0.5) (0.6) + 0.4 (0.5) (0.4) = 0.38$ 

#NeedsFactCheckingByTrueAmericanPatriots 
> [!question]- #schols [2024] ![[Pasted image 20241027193153.png]]
 $4 = \{1, 3\}, \{3, 1\}, \{2, 2\}$
 $6 = \{1, 5\}, \{5, 1\}, \{4, 2\}, \{2, 4\}, \{3, 3\}$ 
 36 total
 $P(4) = 3/36 = 1/12$
 $P(6) = 5/36$
 $P(Neither) = 28/36$
 $P(4\  before\  6) = P(4) + P(Neither)P(4)$
 Situation restarts after 2 rolls
 $1/12 + 28/36 (1/12) = 4/27$ 

> [!question]- #schols [2023] ![[{7B3F3FA6-48F7-4E9F-BC90-E5B14EB0CD25}.png]]
 (i)
 P(20th Ace is not spades) = $\dfrac{3}{4}$
 $P(AceSpade_{21}) = \dfrac{1}{32}$ 
 $P = \dfrac{3}{4} \times \dfrac{1}{32} = 0.0234$ 
 (ii)
 $P(Club_{21} \ | \ Ace_{20}) = \dfrac{P(Club_{21} \cap Club_{20}' \cap Ace_{20})}{P(Ace_{20})}$  
 $P(Club_{20}' \cap Ace_{19}') = (47/52 \times 46/51 \times \dots \times 29/34) = \dfrac{47!}{28!} \div \dfrac{52!}{33!} = 0.0913$
 $0.0913 \times P(Ace_{20}) = 0.0913 \times 4/33 = 0.01107$
 $0.01107 \times P(Club_{21}) = 0.01107 \times 1/32 = 3.459E-4$ 
 $P(Club_{21} \cap Club_{20}' \cap Ace_{20}) = 3.459E-4$ 
 .
 $P(Ace_{19}') = (48/52 \times 47/51 \times \dots \times 30/34) = \dfrac{48!}{29!} \div \dfrac{52!}{33!} = 0.15114969$ 
 $P(Ace_{20}) = 0.15114969 \times 4/33 = 0.01832$ 
 $P(Club_{21} | Ace_{20}) = \dfrac{3.459E-4}{0.01832} = 0.018881$ 
 .
 (ii) ALTERNATIVE ANSWER:
 Take 4 aces out, avoid two of clubs for first 19
 47/48 x 46/47 x ... x 29/30 = $\dfrac{47!}{28!} \div \dfrac{48!}{29!} = 0.604$
 Ace 100%, 3 left 
 Get two of clubs out of remaining 29 + 3 = 32
 $0.604 \times 1/32 = 0.01888$ 

  > [!question]- #schols  [2023] ![[{1C0F733D-0597-4B4F-B12B-2FBC4F183228}.png]]
  (i)
  $P(F) = \dfrac{P(Select_F \cap H_F)}{P(H)}$ 
  $P(Select_F \cap H_F) = 0.5 \times 0.5 = 0.25$ 
  $P(H) = P(Select_F \cap H_F) + P(Select_2 \cap H_2)$ 
  $P(H) = 0.5 \times 0.5 + 0.5 \times 1 = 0.75$ 
  $P(F) = 0.25 \div 0.75 = \frac{1}{3}$ 
  (ii)
  $P(F) = \dfrac{P(Select_F \cap H_F \cap H_F)}{H \cap H}$ 
  $P(Select_F \cap H_F \cap H_F) = 0.5 \times 0.5 \times 0.5 = 0.125$
  $P(H \cap H) = P(Select_F \cap H_F \cap H_F) + P(Select_2 \cap H_2 \cap H_2)$
  $P(H \cap H) = 0.125 + 0.5 = 0.625$ 
  $P(F) = 0.125 \div 0.625 = \frac{1}{5}$ 
  (iii)
  100%???

> [!question]- #schols [2023] ![[{139E38E1-1B15-46F3-A7B3-213786C68109}.png]]
 M1(AA)
 M2(AAA, AAA)
 AA x2
 AAA x4
 .
 $P(M1) = pp' + p'p + pp = 2pp' + pp$ 
 To get $P(M2)$ we need to find when at least 2 of 4 work
 Same as not (exactly 0 or exactly 1) work
 $P(M2_0) = {{4}\choose{0}} p^0 (p')^4$ 
 $P(M2_1) = {{4}\choose{1}} p (p')^3$
 $P(M2) = 1 - ((p')^4 + 4p(p')^3)$
 .
 Find $p$ for which
 $P(M1) > P(M2)$ 
 $pp + 2pp' > 1 - ((p')^4 + 4p(p')^3)$ 
 $(p')^4 + 4p(p')^3 + pp + 2pp' > 1$ 
 $p' = 1 - p$
 $(1-p)^4 + 4p(1-p)^3 + p^2 + 2p(1-p) > 1$ 
 $(1 - 2p + p^2)^2 + 4p(1-p)(1 - 2p + p^2) + p^2 + 2p - 2p^2 > 1$
 $1 - 2p + p^2 - 2p + 4p^2 - 2p^3 + p^2 - 2p^2 + p^4 + 4p(1 - 2p + p^2 - p + 2p^2 - p^3) + 2p - p^2 > 1$
 $-4p + 4p^2 - 2p^3 + p^4 + 4p(1 - 3p + 3p^2 - p^3) + 2p - p^2 > 0$ 
 $p^4 - 2p^3 + 3p^2 - 2p + 4p - 12p^2 + 12p^3 - 4p^4 > 0$
 $-3p^4 + 10p^3 - 9p^2 + 2p > 0$ 
 $p > 0$ 
 $-3p^3 + 10p^2 - 9p + 2 > 0$ 
 $p = 1$
 Insert long division here
 $-3p^2 + 7p - 2 = 0$ 
 $p = 1/6$
 $p = (0, 1/6]$ 
  This is an answer but according to desmos the real answer is $(0, 2/3]$ so I must have made a maths mistake 

#NeedsFactCheckingByTrueAmericanPatriots 
> [!question]- #schols [2022] ![[{D019D6F1-0D0F-4F15-BB3C-F2D9CB541218}.png]]
 Chance of reset = $R$ 
 $R = pq + qp$ 
 $P = pp + Rpp + R^2 pp + ...$ 
 $P = pp [1 + R + R^2 + \dots + \infty]$
 $P = pp \dfrac{1}{1 - R}$
 $P = \dfrac{pp}{1 - R}$ 

> [!question]- #schols [2022] ![[{295AB61C-C114-4143-B2A6-411E634FEDF5}.png]]
 Uses Bayes Theorem 
 $T =$ Over 200 pounds
 $M =$ Is Man
 .
 $P(M) = 0.4$
 $P(M') = 0.6$ 
$P(T | M) = 0.04$
 $P(T | M') = 0.01$ 
 .
 Find $P(M' | T)$ 
 $P(M' | T) = \dfrac{P(M' \cap T)}{P(T)} = \dfrac{P(M' \cap T)}{P(M' \cap T) + P(M \cap T)}$ 
 	$P(A | B) = \dfrac{P(A \cap B)}{P(B)}$
 	$P(A \cap B) = P(B) P(A | B)$ 
 $P(M' \cap T) = P(M')P(T | M') = 0.6 \times 0.01 = \frac{3}{500}$
 $P(M \cap T) = P(M)P(T | M) = 0.4 \times 0.04 = 0.016$
 $P(M' | T) = \dfrac{\frac{3}{500}}{\frac{3}{500} + 0.016} = \dfrac{3}{11}$ 

> [!question]- #schols [2022] ![[{C3A9EEA2-BE7E-4C5D-9FFA-1D93C10A0C17}.png]]
 Range is inclusive 
 $A = \{1, 2, 3\}$
 $N = 1 \to B = \{1, 2, 3\} \to P(3) = \frac{1}{3}$
 $N = 2 \to B = \{2, 3\} \to P(3) = \frac{1}{2}$
 $N = 3 \to B = \{3\} \to P(3) = 1$ 
 $P(M_3) = \frac{1}{3} (\frac{1}{3} + \frac{1}{2} + 1)= \frac{11}{18}$ 

> [!question]- ![[{DB44A14E-D89C-4874-9B30-6555CBEEC2D2}.png]]
> $R_1$ = First ball is red
> $R_2$ = Second ball is red
> $P(R_1 | R_2) = P(R_1 \cap R_2) / P(R_2)$
> $P(R_1) = 6/9$
> $P(R_2) = 6/9 * 5/9 + 3/9 * 7/9 = 17/27$
> $P(R_1 \cap R_2) = 6/9 * 5/9 = 10/27$
> $P(R_1 | R_2) = 10/27 \ / \ 17/27 = 10/17$

> [!question]- ![[{B2E5EFF5-0A44-4556-8726-90122392032C}.png]]
> $E$ = Had education
> $A$ = Has an accident
> $P(E) = 0.6$
> $P(A \cap E') = 0.08$
> $P(A \cap E) = 0.05$
> Find $P(E | A')$
> $P(A' \cap E') = 0.92$
> $P(A' \cap E) = 0.95$
> $P(E | A') = \dfrac{P(E)P(A' \cap E)}{P(E)P(A \cap E) + P(E')P(A \cap E')}$
> $P(E | A') = \dfrac{0.6(0.95)}{0.6(0.95) + 0.4(0.08)} = 0.9468$

Boring Question:
> [!question]- ![[{3F2F9695-77A9-4567-A8EA-A6BF47AD567D}.png]]
> $P(A) = 0.4$
> $P(B) = 0.37$
> $P(A \cap B) = 0.1$
> $P(A \cup B) = 0.1 + 0.3 + 0.27 = 0.67$
> $P(A') = 0.6$
> $P(\overline{A \cup B}) = 0.33$
> $P(\overline{A \cap B}) = 0.9$
> $P(A | B) = 0.1/0.37 = 0.28$
> $P(B | A) = 0.1/0.4 = 0.25$

#NeedsFactCheckingByTrueAmericanPatriots 
> [!question]- ![[{D5C004A8-3681-4181-90A5-B5140041A2D1}.png]]
> $M$ = Sees magazine
> $T$ = Sees television
> $B$ = Buys 
> $P(M) = 1/50$
> $P(T) = 0.2$
> $P(M \cap T) = 0.01$
> $P(B | M \cup T) = 1/3$
> $P(B | \overline{M \cup T}) = 0.1$
> Find $P(B)$
> $P(B) = P(B | M \cup T) + P(B | \overline{M \cup T}) = 0.43$


> [!question]- ![[{FA75E8AF-F7D8-47E8-AFE3-ECBC8354E46E}.png]]
> $H$ = hardware problems
> $S$ = software problems
> $E$ = electronic problems
> $D$ = Shutdown
> $P(D | H) = 0.73$
> $P(D | S) = 0.12$
> $P(D | E) = 0.88$
> $P(H) = 0.2$
> $P(S) = 0.5$
> $P(E) = 0.3$
> Find $P(H | D), P(S |D), P(E|D)$
> #todo


> [!question]- ![[{DC4E51C8-D943-4E05-8F17-89A866862D58}.png]]
 $D =$ Detected as spam
 $S =$ Is spam
 Find $P(S' | D)$ 
 $P(S) = 0.5$
 $P(D | S) = 0.99$ 
 $P(D'|S) = 0.01$
 $P(D | S') = 0.05$
 $P(D'|S') = 0.95$ 
 . 
 $P(S'|D) = \dfrac{P(S' \cap D)}{P(S' \cap D) + P(S \cap D)}$ 
 $P(S' \cap D) = P(S')P(D|S') = 0.5 \times 0.05 = 0.025$ 
 $P(S \cap D) = P(S) P(D | S) = 0.5 \times 0.99 = 0.495$ 
$P(S' | D) = \dfrac{0.025}{0.025 + 0.495} = 0.048$ 

> [!question]- ![[{400A18B3-51D9-4640-93C1-9EF53B43B91B}.png]]
 Determine independence by $P(A|B) = P(A)$ 
 $A = \{THH, HTH, HHT\}$ 
 $P(A) = 3 / 8$ 
 $B = \{HHH, HHT, HTH, HTT\}$ 
 $A | B = \{HTH, HHT\}$
 $P(A|B) = 2/8$
 $P(A|B) \neq P(A) \to$ $A$ and $B$ are not independent 

> [!question]- ![[{0FDBC852-4838-4E73-8AC5-4083B4E6064F}.png]]
 (a)
 $P(Y_1 = 0, Y_2 = 0) = 1/9$ $(C, C)$ 
 $P(Y_1 = 0, Y_2 = 1) = 2/9$ $(C, B), (B, C)$
$P(Y_1 = 1, Y_2 = 0) = 2/9$ $(C, A), (A, C)$ 
 $P(Y_1 = 1, Y_2 = 1) = 2/9$ $(A, B), (B, A)$
 $P(Y_1 = 2, Y_2 = 0) = 1/9$ $(A, A)$
 $P(Y_1 = 0, Y_2 = 2) = 1/9$ $(B, B)$ 
 $P(Y_1 = 2, Y_2 = 1) = 0$ 
 $P(Y_1 =1, Y_2 =2) = 0$ 
 $P(Y_1 =2, Y_2 =2) = 0$ 
 .
 (b)
 $P(Y_1 = 0) = P(Y_2 = 0) = 4/9$
 $P(Y_1 = 1) = P(Y_2 = 1) = 4/9$ 
 $P(Y_1 = 2) = P(Y_2 = 2) = 1/9$ 
 .
 (c)
 Must be a typo. True for $n=2$ 
 $X \sim Bin(2, 1/3)$ 
$P(X = 0) = 2C0 \ (1/3)^0 (2/3)^2 = 4/9$
 $P(X = 1) = 2C1 \ (1/3)^1 (2/3)^1 = 4/9$ 
 $P(X = 2) = 2C2 \ (1/3)^2 (2/3)^0 = 1/9$ 
 .
 This is true as binomial can be viewed as "Exactly $x$ occurs out of $n$ events"
$P(Y_1 = 0)$ represents exactly $0$ $A$ occurring out of $2$ events
 $P(Y_1 = 1)$ represents exactly $1$ $A$ occurring out of $2$ events
 $P(Y_1 = 2)$ represents exactly $2$ $A$ occurring out of $2$ events
 $p = 1/3$ as for each contract there is a $1/3$ chance of $A$ being picked 
.
 (d)
 No as $Y_1$ having been given a value after the first contract directly affects the probabilities of certain events in $Y_2$ 
 For example if $Y_1 > 0$ then $P(Y_2 = 2) = 0$ 

> [!question]- ![[{7C570071-B981-4CFA-9722-9A620B9187A2}.png]]
 (i)
 $P(A \cap C) = \{(1, 2), (2, 1)\} = 2/36 = 1/18$
 $P(C) = \{(1, 1), (1, 2), (2, 1), (3, 1), (1, 3), (1, 4), (4, 1), (1, 5), (5, 1), (1, 6), (6, 1)\} = 11/36$ 
 $P(A|C) = 1/13 \div 11/36 = 2/11$
 .
 (ii)
 $P(B \cap C) = \{(1, 6), (6, 1)\} = 2/36 = 1/18$
 $P(B | C) = 2/11$ 
 .
 (iii)
 $P(A) = \{(1, 2), (2, 1)\} = 1/18$ 
 $P(A) \neq P(A | C) \to A$ and $C$ are not independent
 $P(B) = \{(1, 6), (6, 1), (3, 4), (4, 3), (2, 5), (5, 2)\}$
  $P(B) \neq P(B|C) \to B$ and $C$ are not independent

> [!question]- ![[{82DE30BC-6294-4E15-B573-F49CA9DBF5CF}.png]]
 (a)
 (i)
 $E(X) = 0.5P(x < 5) + 5P(x = 5) + 6P(x = 6) + 7P(x = 7) + 8P(x = 8) + 9P(x = 9) + 10P(x = 10)$
 $P(x < 5) = 4/10 = 2/5$ 
 $P(x = n) = 1/10$ 
 $E(X) = \$4.70$ 
 .
 (ii)
 $E(X^2) = V(X) + E(X)^2$
 $E(X^2) = 0.5^2 P(x < 5) + 5^2 P(x = 5) + 6^2 P(x = 6) + \dots$ 
 $E(X^2) = \$35.60$ 
 $E(X)^2 = \$22.09$ 
 $35.6 = V(X) + 22.09$
 $V(X) = \$13.51$ 
 $Sd(X) = \$3.67$ 
 .
 (b)
  (i)
  $X = \{1, 2, 4, 8, \dots\}$ 
 $P(X = 1) = 0.5$
 $P(X = 2) = 0.5^2$ 
 $P(X = 4) = 0.5^3$ 
 $P(X = x) = 0.5(x^{-1})$ 
 .
 (ii)
 $E(X) = \overset{\infty}{\sum} x P(X = x)$
 The sum is over infinity thus $E(X) = \infty$ 
 .
 (iii)
 It never says how much money you win from a successful bet 
 You could run out of money before you win (In a real world scenario)
  You should start betting way more money to speed up earning profits as half the time you only earn $\$1$ 

> [!question]- ![[{0135FABE-E07F-4420-967C-0F0E3CEE9640}.png]]
 (a)
 $X \sim Bin(n=12, p = 0.15)$ 
 $P(X = 1) = 12C1\ 0.15^1 0.85^{11} = 0.301$ 
 .
 (ii)
 $P(X < 3) = P(X = 0) + P(X=1) + P(X=2)$ 
 $P(X=0) = 12C0\ 0.15^0 0.85^{12} = 0.142$
 $P(X = 2) = 12C2\ 0.15^2 0.85^{10} = 0.292$
 $P(X < 3) = 0.142 + 0.301 + 0.292 = 0.735$ 
 .
 (iii)
 $P(X = 0) = 11C0\ 0.15^0 0.85^{11} = 0.167$
 $P(X = 1) = 11C1\ 0.15^1 0.85^{10} = 0.325$ 
  $P(X < 3) = 0.167 + 0.325 = 0.492$ 




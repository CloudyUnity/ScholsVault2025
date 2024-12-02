

> [!question]- #schols [2024] ![[{9A4CFF85-8E70-47E2-B74C-418C6BFB908F}.png]]

Not allowed:
	$ac^n e$ 
	$e c^n a$
	Where $n \geq 1$ 
.
In other words, you cannot have consonants between broads and slenders
You can have consonants between two broads or two slenders 
$ac^n ae$ is valid 
.
Regular Grammar:
	A context-free grammar where all production rules are of the form:
		$\langle T \rangle \to b \langle B \rangle$
		$\langle T \rangle \to b$
		$\langle T \rangle \to \epsilon$ 
	Irish-ish is a regular grammar as it has the production rules:
		$\langle S \rangle \to b \langle C_b \rangle$ 
		$\langle S \rangle \to e \langle C_e \rangle$ 
		$\langle S \rangle \to \epsilon$ 
		$\langle S \rangle \to c \langle S \rangle$ 
		$\langle C_b \rangle \to \langle C \rangle b$
		$\langle C_e \rangle \to \langle C \rangle e$ 
		$\langle C \rangle \to c$
.


> [!question]- #schols [2023] ![[{FC032DB6-E082-4FE5-A044-AEC1FFA53436}.png]]
 (a)
 If $L$ is a regular language then it can be formed by concat/union/kleene operations on the alphabet its formed from
 Thus $L^*$ can follow the same rules as $L$ but with a kleene star operation appended to the end 
 $\therefore L^*$ is regular
 .
 (b)
 The different states are:
 $P =$ Odd 0s. Even Length (Acceptor)
 $E =$ Even 0s, Even Length
 $O =$ Odd 0s, Odd Length
 $G =$ Even 0s, Odd Length
 $t(i, 0) = O$
 $t(i, 1) = G$
 $t(O, 0) = E$ 
 $t(O, 1) = P$ 
 $t(E, 0) = O$
 $t(E, 1) = G$ 
 $t(G, 0) = P$ 
 $t(G, 1) = E$
 $t(P, 0) = G$ 
 $t(P, 1) = O$ 
 .
 (c)
 $\langle S \rangle \to 0 \langle O \rangle$ 
 $\langle S \rangle \to 1 \langle G \rangle$ 
 $\langle O \rangle \to 0 \langle E \rangle$ 
 $\langle O \rangle \to 1 \langle P \rangle$
 $\langle E \rangle \to 0 \langle O \rangle$ 
 $\langle E \rangle \to 1 \langle G \rangle$ 
 $\langle G \rangle \to 0\langle P \rangle$
 $\langle G \rangle \to 1 \langle E \rangle$
 $\langle P \rangle \to 0 \langle G \rangle$
 $\langle P \rangle \to 1 \langle O \rangle$
 $\langle P \rangle \to \epsilon$ 
 .
 (d)
 $w = x u y$
 $x = \epsilon$
 $u = 1010$
 $y = 10$ 
 $xu^n y \in L$ as $u$ takes the FSA from the $P$ state back to the $P$ state
 $\langle P \rangle \to 1 \langle O \rangle \to 10 \langle E \rangle \to 101 \langle G \rangle \to 1010 \langle P \rangle$ 
 Thus it can be repeated $n$ times and the word remains in the language 

> [!question]- #schols [2022] ![[{7A61421D-EC9F-4B06-833A-D25B03F3FBE9}.png]]
 (a)
 I can't figure out how to do this with a regex no matter what I try so let's do it with a regular grammar
 $L$ is regular $\leftrightarrow$ A regular grammar describes it
 .
 $\langle S \rangle \to 0\langle O \rangle$
 $\langle S \rangle \to 2\langle O \rangle$
 $\langle S \rangle \to 1 \langle P \rangle$ 
 $\langle O \rangle \to 0 \langle E \rangle$ 
 $\langle O \rangle \to 2 \langle E \rangle$ 
 $\langle O \rangle \to 1 \langle G \rangle$
 $\langle E \rangle \to 0 \langle O \rangle$
 $\langle E \rangle \to 2 \langle O \rangle$ 
 $\langle E \rangle \to 1 \langle P \rangle$ 
 $\langle G \rangle \to 0 \langle P \rangle$
 $\langle G \rangle \to 2 \langle P \rangle$
 $\langle G \rangle \to 1 \langle O \rangle$
 $\langle P \rangle \to 0 \langle G \rangle$
 $\langle P \rangle \to 2 \langle G \rangle$
 $\langle P \rangle \to 1 \langle E \rangle$
 $\langle P \rangle \to \epsilon$ 
 .
 (b)
 States:
 $P =$ Even 02s + Odd len (Acceptor)
 $O =$ Odd 02s + Odd len
 $E =$ Even 02s + Even len
 $G =$ Odd 02s + Even len
 $i =$ Start State
 $t(i, 0/2) = O$
 $t(i, 1) = P$
 $t(O, 0/2) = E$ 
 $t(O, 1) = G$
 $t(E, 0/2) = O$
 $t(E, 1) = P$
 $t(G, 0/2) = P$
 $t(G, 1) = O$
 $t(P, 0/2) = G$
 $t(P, 1) = E$
 .
 (c)
 This is the myhill-nerode theorem which states that when two words are related in this way that they place the FSA in the same state
 As there are 5 states $(i, P, O, E, G)$ there are 5 equivalence classes 
 The only word in the $i$ class is $\epsilon$ 
 .
 (d)
 We will prove $M$ is irregular by using the pumping lemma 
 $w = xuy$
 $w = 01122$
 As all 0, 1, 2 need to be increased for $xu^ny$ to be an element of $M$, $u$ must contain all $0, 1, 2$ 
 $x = \epsilon$
 $u = 0112$
 $y = 2$ 
 $xu^2 y = 011201122 \notin M$ 
 This breaks the strict order of $0, 1, 2$ 
 There are no values for $x, u, y$ such that the pumping lemma is true
 $\therefore M$ is not a regular language
 
> [!question]- #schols [2021] ![[{EA49B183-4709-4311-B61D-D8BB8046F39F}.png]]
 (a)
 Forget about regexes, let's do regular grammar
 $P =$ Even len, contains substrings
 $O =$ Odd len, contains substrings
  $N_0 =$ Even len, does not contain substrings, Last input 0
$N_1 =$ Even len, does not contain substrings, Last input 1
 $N_2 =$ Even len, does not contain substrings, Last input 2
 $G_0 =$ Odd len, does not contain substrings, Last input 0
 $G_1 =$ Odd len, does not contain substrings, Last input 1
  $G_2 =$ Odd len, does not contain substrings, Last input 2
 .
 $\langle S \rangle \to 0 \langle G_0 \rangle$ 
 $\langle S \rangle \to 1 \langle G_1 \rangle$
 $\langle S \rangle \to 2 \langle G_2 \rangle$ 
 $\langle G_0 \rangle \to 0 \langle N_0 \rangle$
 $\langle G_0 \rangle \to 1 \langle N_1 \rangle$ 
 $\langle G_0 \rangle \to 2 \langle P \rangle$
 $\langle G_1 \rangle \to 0 \langle P \rangle$ 
 $\langle G_1 \rangle \to 1 \langle N_1 \rangle$ 
 $\langle G_1 \rangle \to 2\langle N_2 \rangle$
 $\langle G_2 \rangle \to 0 \langle N_0 \rangle$
 $\langle G_2 \rangle \to 1 \langle N_1 \rangle$
 $\langle G_2 \rangle \to 2 \langle N_2 \rangle$ 
 $\langle N_0 \rangle \to 0 \langle G_0 \rangle$
 $\langle N_0 \rangle \to 1 \langle G_1 \rangle$
 $\langle N_0 \rangle \to 2 \langle O \rangle$ 
 $\langle N_1 \rangle \to 0 \langle O \rangle$
 $\langle N_1 \rangle \to 1 \langle G_1 \rangle$
 $\langle N_1 \rangle \to 2 \langle G_2 \rangle$
 $\langle N_2 \rangle \to 0 \langle G_0 \rangle$
 $\langle N_2 \rangle \to 1 \langle G_1 \rangle$
 $\langle N_2 \rangle \to 2 \langle G_2 \rangle$ 
 $\langle P \rangle \to 0 \langle O \rangle$
 $\langle P \rangle \to 1 \langle O \rangle$
 $\langle P \rangle \to 2 \langle O \rangle$
 $\langle O \rangle \to 0 \langle P \rangle$
 $\langle O \rangle \to 1 \langle P \rangle$
 $\langle O \rangle \to 2 \langle P \rangle$
 $\langle P \rangle \to \epsilon$ 
 .
 (b)
 States:
 $i =$ Start State
 $P =$ Even len, contains substrings (Accepting)
 $O =$ Odd len, contains substrings
 $N_0 =$ Even len, does not contain substrings, Last input 0
 $N_1 =$ Even len, does not contain substrings, Last input 1
 $N_2 =$ Even len, does not contain substrings, Last input 2
 $G_0 =$ Odd len, does not contain substrings, Last input 0
 $G_1 =$ Odd len, does not contain substrings, Last input 1
 $G_2 =$ Odd len, does not contain substrings, Last input 2
 $t(i, 0) = G_0$
 $t(i, 1) = G_1$
 $t(i, 2) = G_2$
 $t(G_0, 0) = N_0$
 $t(G_0, 1) = N_1$
 $t(G_0, 2) = P$
 $t(G_1, 0) = P$
 $t(G_1, 1) = N_1$
 $t(G_1, 2) = N_2$
 $t(G_2, 0) = N_0$
 $t(G_2, 1) = N_1$
 $t(G_2, 2) = N_2$ 
 $t(N_0, 0) = G_0$
 $t(N_0, 1) = G_1$
 $t(N_0, 2) = O$ 
 $t(N_1, 0) = O$
 $t(N_1, 1) = G_1$
 $t(N_1, 2) = G_2$
 $t(N_2, 0)=G_0$
 $t(N_2,1)=G_1$
 $t(N_2,2)=G_2$
 $t(P, 0/1/2) = O$
 $t(O, 0/1/2) = P$ 
 .
 (c)
 By myhill-nerode theorem the classes split the language into words that place the FSA in the same state
 There are 9 states and thus 9 classes
. 
 (d)
 Pumping lemma
$w = xuy$
 $w = 011222$
 For $xu^n y$ to be in $M$ it needs to increase the total count of each $0, 1,2$
 Thus $u$ must contain at least 1 of each $0, 1,2$
 $u = 0112$
 $xu^2 y = 0112011222$
  This is not in $M$ as the strict order of $0$s then $1$s then $2$s is broken
$\therefore M$ is not a regular language 

> [!question]- #schols [2020] ![[{C80BD95A-7094-4FB0-9164-093E8CE8C3FD}.png]]
 (a)
 Finite
 Regular
 Recursively Enumerable
 Recursive 
 Context Sensitive
 Context Free
 .
 (b)
 $D_3$ is an acceptor state
 $ANY = \{A-Z, !, \#\, \$, \%, \&, ', (, ), -, @, \_, \{, \}, \sim\}$
 $t(i, ANY) = C_1$ 
 $t(C_1, ANY) = C_2$
 $t(C_2, ANY) = C_3$ 
 $\dots$
 $t(C_7, ANY) = C_8$ 
 $t(C_8, .) = D_1$ 
 $t(D_1, ANY) = D_2$
 $t(D_2, ANY) = D_3$ 
 .
 (c)
 To be context free there cannot be any production rules with multiple nonterminals 
 To be regular it can only use regular grammar style production rules
 $\langle S \rangle \to 0\langle S \rangle$ 
 $\langle S \rangle \to \epsilon$ 
 This the language $L = \{0^n | n \in \mathbb{N}\}$ 
 This is a regular grammar in normal form thus its a regular language
 It is also context free as there is only a single nonterminal on both the left and right side of each rule
 
#schols [2020]
![[{A7B34A7C-DD02-4B3D-B4C4-0FACEDF7A075}.png]]

#schols [2019]
![[{8726B1C2-910C-46F8-A5C1-B991D01DB04D}.png]]

#schols [2017]
![[{7A027DAD-2FCA-416C-909D-C704281AE739}.png]]
![[{D56D8187-8DC8-4B8C-807D-5C7316A041DB}.png]]

#schols [2016]
![[{9D310A25-DFF8-467D-9336-00B1AC5CF0F6}.png]]

#schols [2015]
![[{94CC7C05-231F-4B50-AAB6-EC972C8DED17}.png]]

#schols [2013]
![[{414ED171-FE49-4D46-8E0E-E56AD5E172F7}.png]]

> [!question]- ![[{C4AE9C3E-A680-438D-B1D1-8144161853CF}.png]]
 (a)
 $\circ$ is associative 
 It is closed as well
 There is an identity element
 There is however no inverse possible as you cannot concat anything to a word to reduce its length
 $\therefore$ It is a monoid
 .
(b)
  This object is also a monoid as there is no inverse
 $\nexists x, \forall a, a + x = 0$ 
 .
 (c)
We need to check $f(w \circ w') = f(w) + f(w')$ 
 $f(w \circ w') = | w \circ w'| = |w| + |w'|$ 
 $f(w) + f(w') = |w| + |w'|$ 
 $\therefore f$ is a homomorphism
 .
 (d)
We need to check bijectivity 
To check injectivity this must be true: $f(w) = f(w') \to w = w'$ 
Assume $f(w) = f(w')$ 
 $|w| = |w'|$ 
This does not prove the words are equal as they could be two separate words of the same length
$\therefore f$ is not injective
$\therefore f$ is not bijective
$\therefore f$ is not an isomorphism

> [!question]- ![[{6AA50076-3C11-4234-915A-A9D0BDD95CEC}.png]]
 (a)
 $L = \{ a^n b | n \in \mathbb{N}\} \cup \{a^n c | n \in \mathbb{N}\}$ 
 (b)
 $aaa \langle S \rangle, aab, aac$ 
 (c)
 $\{ aaaa^n \langle S \rangle | n \in \mathbb{N}\} \cup \{aaa^n b | n \in \mathbb{N}\} \cup \{aaa^n c | n \in \mathbb{N}\}$ 

> [!question]- ![[{196DE4DF-699C-4E62-BA09-6C5C8E0C0A5F}.png]]
(a)
This is a phase structure grammar as production rules have more than 1 nonterminal 
(b)
S -> A B C
A B -> 0 A D / 1 A E / e
C -> e
0 A D C / 1 A E C / e 
D C -> B 0 C 
E C -> B 1 C
.
0 A B 0 C / 1 A B 1 C / e
0 0 A D 0 C / 0 1 A E 0 C / 1 0 A D 1 C / 1 1 A E 1 C / e
0 0 A 0 D C / 0 1 A 0 E C / 1 0 A 1 D C / 1 1 A 1 E C / e
0 0 A 0 B 0 C / 0 1 A 0 B 1 C / 1 0 A 1 B 0 C / 1 1 A 1 B 1 C / e
0 0 A B 0 0 C / 0 1 A B 0 1 C / 1 0 A B 1 0 C / 1 1 A B 1 1 C / e
.
Possible words (Ignoring D/E):
n-bit (AB or e) (n-bit) (C or e) $n \geq 0$ 
When AB is used, the B can be put between any bits of the n bit number 
.
 $O = \{0, 1\}$ 
 $P = \{C, \epsilon\}$ 
 $P^1 = \{\{C\}, \{\epsilon \}\}$ 
 $L = \{ O^n \langle A \rangle O^k \langle B \rangle O^p P^1 | n, k, p \in \mathbb{N}, k + p = n\}$ 

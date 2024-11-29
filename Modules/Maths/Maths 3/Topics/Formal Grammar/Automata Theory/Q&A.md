
> [!question]- #schols [2018] ![[{01AD2794-B811-4FBD-84AA-78368EAF0B22}.png]] ![[{453FEBCA-7E03-4267-B6DD-FC899E84B66C}.png]]
 (a)
 $i \overset{0}{\to} A$
 $A \overset{1}{\to} B$
 $B \overset{1}{\to} C$ 
 $C \overset{0}{\to} A$ 
 $C$ is acceptor 
 .
 (b)
 $L = (\{0\} \circ \{1\} \circ \{1\}) \circ ((\{0\} \circ \{1\} \circ \{1\}) \cup \epsilon) \circ \dots \circ ((\{0\} \circ \{1\} \circ \{1\}) \cup \epsilon)$ 
 .
 (c)
 $w = xu^ny$
 $w = 010$ 
 Let $x = 0, u = 1, y = 0$ 
 $xu^2y = 0110 \notin M$
Let $x = 01, u = 0, y = \epsilon$ 
$x u^2 y = 0100 \notin M$
Let $x = \epsilon, u = 010, y = \epsilon$
$xu^2 y = 010010 \notin M$
$\therefore M$ is not a regular language

> [!question]- #schols [2013] ![[{F3864076-C465-490C-A6CD-EEF3C585B3B1}.png]] ![[{86425793-4796-4D64-B0A8-038A348BE23B}.png]]
 (b)
 Valid accepting states are when the last digit is 1 or 6
 All numbers can be modded by 5 so the only last digit is 1
 $i$ is the starting state
 $O$ is the 1 acceptor state
 $T$ is the 2 rejector state
 $H$ is the 3 rejector state
 $F$ is the 4 rejector state
 $i \overset{1}{\to} O$
 $O \overset{1}{\to} O$
 $T \overset{1}{\to} T$ 
 $H \overset{1}{\to} H$
 $F \overset{1}{\to} F$
 $i \overset{2}{\to} T$
 $O \overset{2}{\to} T$
 $T \overset{2}{\to} F$ 
 $H \overset{2}{\to} O$
 $F \overset{2}{\to} H$
 $i \overset{3}{\to} H$
 $O \overset{3}{\to} H$
 $T \overset{3}{\to} O$ 
 $H \overset{3}{\to} F$
 $F \overset{3}{\to} T$
 $i \overset{4}{\to} F$
 $O \overset{4}{\to} F$
 $T \overset{4}{\to} H$ 
 $H \overset{4}{\to} T$
 $F \overset{4}{\to} O$
 .
 Insert transition table
 .
 (c)
 $\langle S \rangle \to 1\langle O \rangle$ 
 $\langle S \rangle \to 2\langle T \rangle$
 $\langle S \rangle \to 3\langle H \rangle$ 
  $\langle S \rangle \to 4\langle F \rangle$ 
  $\langle O \rangle \to 1 \langle O \rangle$ 
 $\langle O \rangle \to 2 \langle T \rangle$ 
  $\langle O \rangle \to 3 \langle H \rangle$ 
  $\langle O \rangle \to 4 \langle F \rangle$ 
 $\langle T \rangle \to 1 \langle T \rangle$ 
 $\langle T \rangle \to 2 \langle F \rangle$ 
 $\langle T \rangle \to 3 \langle O \rangle$ 
 $\langle T \rangle \to 4 \langle H \rangle$ 
 $\langle H \rangle \to 1 \langle H \rangle$ 
 $\langle H \rangle \to 2 \langle O \rangle$ 
 $\langle H \rangle \to 3 \langle F \rangle$ 
 $\langle H \rangle \to 4 \langle T \rangle$ 
 $\langle F \rangle \to 1 \langle F \rangle$ 
 $\langle F \rangle \to 2 \langle H \rangle$ 
 $\langle F \rangle \to 3 \langle T \rangle$ 
 $\langle F \rangle \to 4 \langle O \rangle$ 
 $\langle O \rangle \to \epsilon$ 

> [!question]- ![[{0A2631AB-58FA-49B3-9FF8-4DCE56231578}.png]]
 (a)
 $L_0 = \{0\}$ 
 $L_1 = \{1\}$ 
 $L_2 = L_0 \circ L_0$ 
 $L_3 = L_0 \cup L_1$ 
 $L_4 = L_3^*$ 
 $L_5 = L_4 \circ L_2$ 
 $L_6 = L_5 \circ L_4$ 
 $L = L_6$ 
 (b)
 Rejector: $S, A$ 
 Acceptor: $B$ 
 $S \overset{1}{\to} S$ 
 $S \overset{0}{\to} A$
 $A \overset{1}{\to} S$
 $A \overset{0}{\to} B$ 
 $B \overset{0, 1}{\to} B$ 
 (c)
 $t(i, 1) = i$
 $t(i, 0) = A$ 
 $t(A, 0) = B$
 $t(A, 1) = i$
 $t(B, 0) = B$ 
 $t(B, 1) = B$ 
 (d)
 There is only one equivalence class as there is only one acceptor state $B$ 
 $x \equiv_L y \leftrightarrow (\forall w \in A^*,  xw \in L \leftrightarrow yw \in L)$ 
 As $x, y \in L$ they always reach the acceptor state


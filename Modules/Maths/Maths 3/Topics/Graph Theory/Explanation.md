
$V$ = Finite set of vertices
$E$ = Finite set of edges

$V \neq \emptyset$ 

$V_n = \{ A \in P(V) | \ \ \#A = n\}$ 
Set of all subsets of $V$ containing $n$ vertices 

$\{v_1, v_2\} = v_1v_2$ 

Trivial Graph
	A graph with 1 vertex and 0 edges

Incidence
	$v, v' \in V$ 
	$e = vv'$
	$e \in E \to v$ and $e$ are incident to each other 

Incidence Table
	$V \times E$ matrix
	Values are 0 or 1 depending on whether they are incident 

Adjacency
	$v, w \in V, v \neq w$ 
	$\exists vw \in E \to v$ and $w$ are adjacent 

Adjacency Matrix
	$V \times V$ matrix
	Values are 0 or 1 depending on whether they are adjacent 

Complete Graph ($K_n$)
	A graph where 
		$\forall v, v' \in V$
		$v \neq v'$ 
		$vv' \in E$ 
	Has the highest number of edges possible given the vertices. Every vertex is connected 
	$K_n$ is a complete graph with $n$ vertices 
	Adjacency matrix is all 1s except for diagonal 

Bipartite Graph
	A graph where
		$\exists V_1, V_2 \subset V$ 
		$V_1 \cup V_2 = V$
		$V_1 \cap V_2 = \emptyset$
		$\forall vw \in E$
			$v \in V_1, w \in V_2$ 
	A complete bipartite graph is where
		$\forall v \in V_1, w \in V_2$
		$\exists vw \in E$ 
		Denoted by $K_{p, q}$ where $|V_1| = p, |V_2| = q$ 

Graph Isomorphism
	Given two graphs $(V, E), (V', E')$ 
	An isomorphism between them is a bijective function $\varphi : V \mapsto V'$ satisfying
		$\forall a, b \in V$
		$a \neq b$
		$ab \in E \leftrightarrow \varphi(a) \varphi(b) \in E'$ 
	$\varphi$ is bijective IFF $\exists \varphi^{-1} : V' \mapsto V$ 
	Bijection sets up
		A 1-1 correspondence from vertices of $V$ to $V'$ 
		A 1-1 correspondence from edges of $E$ to $E'$ 
	$\exists \varphi \to$ The graphs are isomorphic 

Subgraph
	$(V', E') \subseteq (V, E)$ IFF
		$V' \subseteq V \land E' \subseteq E$ 

Vertex Degrees
	The degree of a vertex $v$ is the number of incident edges to $v$ in $E$ 
	$deg \ v = 0 \to v$ is isolated
	$deg \ v = 1 \to v$ is pendant
	$\sum deg \ v = 2 |E|$ 
		Proof:
		$\sum deg \ v$ is the sum of all entries in the adjacency matrix
		Every edge $vv' \in E$ contributes twice to the sum for both vertices
		Thus the sum is $2 \times |E|$ 
			(Also must be even)

Number of vertices with odd degrees must be even
	Proof:
	Assume it isn't
	$\sum deg \ v$ must be an odd integer as odd + even = odd
	Contradiction

K-Regular Graphs
	A graph is K-Regular if every vertex has a degree of K

Regular Graphs
	$\exists K \in \mathbb{N}$ s.t. graph is K-Regular 
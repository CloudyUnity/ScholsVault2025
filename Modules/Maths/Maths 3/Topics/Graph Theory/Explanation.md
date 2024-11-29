
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

A complete graph with $n$ vertices is $(n-1)$-Regular because every vertex is adjacent to all other vertices 
$\therefore$ A complete bipartite graph $K_{p, q}$ is regular $\leftrightarrow p = q$
Proof:
	$V = V_1 \cup V_2$
	$V_1 \cap V_2 = \emptyset$ 
	$|V_1| = p$
	$|V_2| = q$ 
	Prove Backwards:
		Assume $p=q$ 
		The graph is complete $\to$ 
		$\forall v \in V_1, \ deg\  v = p = q$
		$\forall v \in V_2, \ deg \ v = p = q$ 
		$\therefore K_{p, q}$ is $p$-regular
	Prove Forwards:
		Assume $K_{p, q}$ is regular
		$\forall v \in V_1, v' \in V_2, \ deg \ v = \ deg \ v'$
		$K_{p, q}$ is complete $\to$ $v$ is adjacent to all vertices in $V_2$ 
		$deg \ v = |V_2|$
		$deg \ v' = |V_1|$ 
		$\therefore |V_1| = |V_2|$ 

Walk $v_0 v_1 \dots v_n$ 
	Finite sequence of vertices of the graph 
	Traverses edges, passes through vertices 

Trail $v_0 v_1 \dots v_n$ 
	A walk where every edge traversed is distinct 

Path $v_0 v_1 \dots v_n$ 
	A trail where every vertex passes through is distinct 

Trivial Walk/Trail/Path
	A walk/trail/path of length zero with 1 vertex

Connected Graph
	A graph where there exists a path between every two vertices

Components of  a graph
	Define a relation $\sim$
	$v \sim v' \leftrightarrow \exists$ walk from $v$ to $v'$ 
	$\sim$ is an ER
	Proof:
		Prove reflexivity:
			$v \sim v$ as its a trivial walk
		Prove symmetry:
			$a \sim b \to \exists$ walk $a v_1 v_2 \dots b$ 
			$\therefore \exists$ walk $b \dots v_2 v_1 a$
			$\therefore b \sim a$ 
		Prove transitivity:
			$a \sim b \land b \sim c$ 
			$\exists$ walk $a v_1 v_2 \dots v_{n-1} b$ 
			$\exists$ walk $b w_1 w_2 \dots w_{n-1} c$
			$\therefore \exists$ walk $a v_1 v_2 \dots b w_1 w_2 \dots c$ 
			$\therefore a \sim c$ 
	$\sim$ partitions $V$ into disjoint subsets $V_1, V_2, \dots, V_p$
		 $V_1 \cup V_2 \cup \dots \cup V_p = V$
		$V_i \cap V_j = \emptyset, i \neq j$ 
		$a, b \in V_i \leftrightarrow a \sim b$
	$E_i = \{ab \in E | a, b \in V_i\}$ 
	$(V_1, E_1), (V_2, E_2), \dots, (V_p, E_p)$ are subgraphs of $(V, E)$ 
	These subgraphs are the components of the graph

The vertices and edges of any walk in an undirected graph are all within a single component 

All components are connected graphs by definition 
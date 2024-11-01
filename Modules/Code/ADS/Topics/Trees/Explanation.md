Complete Tree
	Balanced tree except for bottom level
	Height with $N$ nodes is $log\ N$

Binary Heap
	Array representation of a heap-ordered complete tree
	Keys are assumed immutable
	Construction is $O(N \ log \ N)$
	![[Pasted image 20240911171741.png]]
	Root node is `a[1]`
	Parent of node $k$ is $k/2$
	Children of node $k$ is $2k, 2k+1$
	Insertion:
		Add node at the end, then swim it up
		$O(log \ N)$
	Remove Max:
		Exchange root with leaf node, then sink it down
		$O(log \ N)$
	Peter Principle
		If a child's key is larger than it's parent then swap them (Use larger child)

$d$-Way Binary Heaps
	Nodes have $d$ children
	Swim is $O(log_d N)$
	Sink is $O(d \ log_d N)$
	Optimal at $d=4$

Cache-Friendly Binary Heaps
	Cache-Aligned $d$-heap
	Funnel Heap
	B-Heap
	#todo 
		More info

Tree Height
	Max links from root to leaf
Tree Levels
	Max nodes from root to leaf
Tree Size 
	Number of nodes
Tree Depth of Node $k$
	Links from root to $k$
Rank($k$)
	Number of keys less than $k$
Select($n$)
	Key where Rank($k$) = $n$

Binary Search Tree (BST)
	Binary Tree in symmetric order
	Node $k$ is larger than its left child and smaller than its right
	Search
		If less go left, if greater go right, else hit
	Floor($k$)
		Largest key less than $k$
		Search for Floor($k$) in  node $n$
			$n = k \to f(k) = n$
			$n \geq k \to f(k) \in n_L$
			Otherwise recursively search the right subtree for a $n \leq k$ else $f(k) = n$
	Ceiling($k$)
		Smallest key greater than $k$
	Rank() and Select() can be optimized by storing subtree counts in each node
	Traversals
		Inorder
			Traverse left, process node, traverse right
		Preorder
			Process node, traverse left, traverse right
		Postorder
			Traverse right, traverse left, process node

BST Deletion
	Lazy Tombstone
		Replace node with tombstone
	Delete Min
		Go left until you can't, replace left link with right link
	Hibbard Deletion
		$p$ is the parent of $k$ to be deleted
		$\lnot k_L \land \lnot k_R \to p_k = null$
		$\lnot k_L \land k_R \to p_R = k_R$ 
		$k_L \land \lnot k_R \to p_L = k_L$ 
		Otherwise
			$x =$ Min($k_R$)
			$x_L = k_L$
			$x_R =$ DeleteMin($k_R$)
			$p_k = x$
			Update counts in $x$ recursively

2-3 Tree
	Nodes can have 2 or 3 children 
	Leads to complete balanced binary trees at the cost of maintaining multiple node types and lots of code branches
	3 Children
		Two keys $k_1, k_2$
		$k_M \to k_{1} < M < k_{2}$
	Insert
		Add key to leaf 2-node to make 3-node
		Add key to leaf 3-node to make 4-node
	Local transformations to remove 4-nodes
		![[Pasted image 20240912153944.png]]

Red-Black Trees (Left-Leaning)
	2-3 Trees have their 3-nodes converted to 2-nodes with red glue links
		Larger key becomes parent, red glue links the two nodes to the left
		Color of parent link is stored in node class
	No node should have two glue links connected
	Every path from root to leaf has the same number of black links
	Leads to better balance without the cost of 2-3 trees
	Rotate Left
		When a red link leans right
			$p_k = p_R$
		Set $k$ to parent
		$p_R = k_L$
		$k_L = p$ (Red)		
	Color Flip
		When $p$ has two red child links to $k$ and $m$
		Set parent of $p$ as red link
	Insertion
		Do standard BST insert, color link red
		If it is a right link, rotate left
		If two red lefts in a row then rotate right
		If two red child then color flip

Variants
	B+ Tree
	B* Tree
	B# Tree

File System
	Page
		Continuous block of data
	Probe
		First access to a page 
	Time for a probe is larger than access within a page, less is better
	Cost Model
		Number of probes

B-Tree
	2-3 Trees that allow up to $M-1$ links per node
	$L \geq 2$ in root
	$\frac{M}{2} \leq L \leq M-1$ links in other nodes
	External nodes contain client keys
	Internal nodes contain key copies to guide search
	Search
		From root find interval for search key and take link
		Terminate in external node
	Insert
		Search for new key
		Insert at bottom
		If node has $M$ links then split it up the tree
	Search/Insert takes between $log_{M-1} \ N$ and $log_{M/2} \ N$ probes
	In practise number of probes is at most 4
	Keeps root page in memory
	#todo 
		Huh?

1D Range Search
	Given an ordered priority queue
	Range Search
		$O(R + log \ N)$
		Find all keys between $k_1$ and $k_2$ 
	Range Count
		$O(log \ N)$
		Number of keys between $k_1$ and $k_2$
	$k_1$ and $k_2$ don't have to be elements in the $PQ$
	$R$ is the number of matching keys
	BST Implementation		
		Range Count
			$O(log \ N)$
			Contains($k_2$)
				Rank($k_2$) - Rank($k_1$) + 1
			!Contains($k_2$)
				TreeSize() - Rank($k_1$)
		Range Search
			$O(R + log \ N)$
			Recursively check all keys in $k_L$ if in range
			Check $k$
			Recursively check all keys in $k_R$ if in range

Line Segments Intersection Test
	$O(N \ log \ N + R)$
	Assume all coordinates are distinct
	Determines horizontal-vertical intersections only
	$h$-Segment is a horizontal segment
	$v$-Segment is a vertical segment
	Sweep vertical line left to right
	x coords define events
	At $h$-Segment Left Endpoint insert y coord into BST
	At $h$-Segment Right Endpoint remove y coord from BST
	At $v$-Segment do a 1D Range Search between endpoint interval
	This algo reduces a 2D problem into a 1D $\times$ 1D problem

2D Range Search
	Assume keys are 2D
	Find keys in an AABB ($h$-$v$ rectangle) 
	Grid Implementation
		Divide space into $M \times M$ grid
		Put points into their respective square
		Only examine squares the AABB covers
		Space: $O(M^2 + N)$
		Time: $O(1 + N/M^2)$ per square examined
		Rule of Thumb: $M = \sqrt N$
		Can lead to a clustering problem

Partitioning data structures that alleviates clustering problem
	2D Tree
		Recursively divide space into halfplanes (Like BVH) 
	QuadTree
		Recursively divide space into 4 quadrants (Like sparse voxel octree)
	BSP Tree
		Recursively divide space into two non-AABB regions

2D Tree
	Average of $O(R + log \ N)$
	Worst case of $O(R + \sqrt N)$
	BST but alternating using x and y coord as key
	![[Pasted image 20240915210139.png]]
	Nearest Neighbour Search
		$O(log \ N)$
		Worst Case: $O(N)$
		Check distance from $p$ to $k$
		Recursively check $k_{LB}$ if it could contain a closer point
		Recursively check $k_{RT}$ if it could contain a closer point

KD Tree
	Recursively partition $K$-dimensional space into 2 halfspaces
	Called a Bounding Volume Hierarchy in 3D
	Like a 2D Tree but you cycle through all dimensions

N-Body Simulation
	Simulate the motion of $N$ particles mutually affected by eachothers gravity
	Treat clusters of particles as single aggregate particle
	Compute force between particle and center of mass of aggregate
	Appel's Algo
		$O(N log \ N)$
		Build 3D Tree
		Store center of mass of subtree in each node
		To compute total force on a particle, traverse tree until distance from particle is sufficiently large

1D Interval Search
	Data structure for holding set of overlapping intervals
	Given an interval (lo, hi) find all intersecting intervals
	Create BST of intervals
		Red-Black BST is fastest
	Store max right endpoint of subtree in node
	Insert
		Use lo as the key
		Update max in each node on search path
	Intersect (Any)
		$O(log \ N)$
		If node intersects, return it
		Else if $!k_L$ : check right
		Else if $max(k_L) < lo$ : check right
		Else check left
	Intersect (All)
		$O(R \ log \ N)$

AABBs Intersection Test
	$O(N\ log\ N + R\ log \ N)$
	Sweep vertical line from left to right
	Intersections create a 1D Interval 
	Left Endpoint
		1D Interval Search
		Insert y-Interval
	Right Endpoint
		Remove y-Interval
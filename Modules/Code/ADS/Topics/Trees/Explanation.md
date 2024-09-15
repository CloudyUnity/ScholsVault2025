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
		$k_L \oplus k_R \to p_k = k_{LR}$
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

Left-Leaning Red-Black Trees from 2-3 Trees
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
	
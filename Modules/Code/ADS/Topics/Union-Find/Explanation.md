For determining when two objects are connected
Similar to pathfinding 

Be aware you can get faster performance in specific problems by using bitfields

$p=>q$ 
	$p$ is connected to $q$

Reflexive
	$p=>p$

Symmetric
	$p=>q \to q=>p$

Transitive
	$p=>q \land q=>r \to p=>r$

Connected Component ($CC$
	Maximal set of objects mutually connected
	Often represented by an index 

Find($p$)
	Returns $CC$ that contains $p$

Union($p, q$)
	Combine all $CC$s that contain $p$ or $q$

Connected($p, q$)
	Returns Find($p$) = Find($q$)

Quick-Find
	int id$[N]$;
	id$[p]$ stores the $CC$ index containing $p$
	Union
		Change all entries whose id is id$[p]$ to id$[q]$
		Very expensive

Quick-Union
	int id$[N]$;
	id$[p]$ is the parent of $p$
	Root/$CC$ is when id$[r_p]$ = $r_p$
	Union
		Set id$[r_p]$ to $r_q$
		Trees can get very tall

Weighted quick-union
	Given a large tree and small tree, always points the small tree at root of the large tree
	Leads to more balanced trees as the biggest root will continue to grow lateral branches
	Needs a separate array to keep track of tree sizes

Path Compression
	Whenever computing the root $r_p$ of $p$, set all nodes along to way to also point at $r_p$
	One-Pass
		In Find($p$) loop set all nodes to point to their grandparent
		`id[i] = id[id[i]];`
	Keeps trees almost completely flat assuming re-use

Weighted Quick-Union Path Compression ($WQUPC$)
	$M$ union-find ops on $N$ objects leads to $O(N + M \ lg^* N)$ array accesses
	In theory not linear but linear in practise 
	#todo 
		What's $lg^* \ N$?

Percolation
	Given a $N\times N$ grid of random boolean squares
	Square vacancy is determined by probability $p$
	The system percolates iff a path from top to bottom exists
	![[Pasted image 20240915200802.png]]
	There exists a threshold $p^*$ where grids sharply go from mostly never percolating to mostly percolating
	This is a "Dynamic Connectivity" problem, perfect for $WQUPC$ 
	Clever trick
		Introduce two new nodes for top and bottom which have forced connections. Percolates iff id$[t]$ = id$[b]$
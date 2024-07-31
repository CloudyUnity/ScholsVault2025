CPUs run on Fetch-Decode-Execute cycles
To do this they need to know what instructions are incoming so they can begin fetching and decoding them before they're executed
Branch instructions fuck this up as the CPU doesn't know what is incoming causing wasted cycles
Modern CPUs have branch predictors to help this problem but not in Cortex-M3 no sir

#bonus 
Cache Locality:
	This is for modern processors only but it's cool so shut up
	Every processor has caches so that it can store certain memory closer for faster access
	Each CPU core has an individual L1 cache and all cores share a L2 and L3 cache
	When a core wants memory that is not in a close cache that's called a cache miss and takes FUCKING FOREVER
	Otherwise its a cache hit
	When a core does grab memory from RAM it doesn't just grab 1 address it grabs a massive chunk of memory to fit into a cacheline
	Following this we can see that it is way faster to read lots of memory when its close together rather than spread out across the heap
	So if you have a lot of data to iterate through try to avoid pointers on each object, and if you are constantly creating new data then try to allocate a large chunk of memory and fill into it rather than constantly allocating new memory for each object
	Now how does memory avoid getting corrupted when every cores has its own L1 cache which could represent the same memory? Good question
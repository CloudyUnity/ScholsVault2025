
![[Pasted image 20240716173425.png]]
![[Pasted image 20240716173434.png]]

Obviously the way to make this simple is to make a function for grabbing the state of a position

```c
int get_state(struct grid64x64* grid, int x, int y) {
	if (x < 0 || y < 0 || x >= 64 || y >= 64)
		return 0;
	
	uint64_t row = grid->cells[y];
	return (row >> x) & 1;
}

void set_state(struct grid64x64* grid, int x, int y, int state) {
	if (x < 0 || y < 0 || x >= 64 || y >= 64)
		return 0;
	
	if (state) {
		grid->cells[y] |= (1 << x); // OR
		return;
	}

	grid->cells[y] &= ~(1 << x); // NAND
}

struct grid64x64* grid64x64_next_state(struct grid64x64* grid) {
	struct grid64x64* newGrid = malloc(sizeof(struct grid64x64));
	
	for (int y = 0; y < 64; y++) {
		uint64_t row = grid->cells[y];
		for (int x = 0; x < 64; x++) {
			// Get neighbour count
			int neighbourCount = 0;
			neighbourCount += get_state(grid, x-1, y-1);
			neighbourCount += get_state(grid, x, y-1);
			neighbourCount += get_state(grid, x+1, y-1);
			neighbourCount += get_state(grid, x-1, y);
			neighbourCount += get_state(grid, x+1, y);
			neighbourCount += get_state(grid, x-1, y+1);
			neighbourCount += get_state(grid, x+1, y+1);

			// Live Cells
			if (get_state(grid, x, y)) {
				// Too few or many neighbours kills a cell
				if (neighbourCount < 2 || neighbourCount > 3) {
					setState(newGrid, x, y, 0);
					continue;
				}
				
				// Otherwise stay alive
				setState(newGrid, x, y, 1);
				continue;
			}

			// Dead Cells
			// Exactly 3 neighbours turns them alive
			if (neighbourCount == 3) {
				setState(newGrid, x, y, 1);
				continue;
			}				
			
			// Otherwise stay dead
			setState(newGrid, x, y, 0);
		}
	}
}
```

Damn easy question fr fr

Mistakes:
	None :)
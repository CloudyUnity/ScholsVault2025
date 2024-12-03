
![[Pasted image 20240716173650.png]]
![[Pasted image 20240716173657.png]]

Adding a value:
	Loop through list looking for first node where the first array item is larger than the value
		Or node is null (go to tail)
	Go back to prev node 
	Loop through array until you find the first item to be larger than the value
	Place item into slot and shuffle everything up. Go until num_items+1
	Increment num_items
	If num_items was K then move the top shuffled item to
		If the next node has < K items then place in there
		Else add a new node in between and assign it to `[0]` 

Deleting a value:
	Loop through and find the node (optimally)
	If num_items == 1 then delete node
	else
		If (nodeCount + nextCount >= K + 1)
			Copy all elements from node into next starting from num_items to K
				Ignore value
			Quicksort next
			Delete node
		else
			Delete value and shuffle down

```c
struct sorted_list* list_new() {
	return malloc(sizeof(struct sorted_list));
}

struct list_node* node_new() {
	return malloc(sizeof(struct list_node));
}

float node_add(struct list_node* this, float val) {
	_Bool isShuffling = 0;
	float curShuffle = -1;
	for (int i = 0; i < curNode->num_items + 1; i++) {
		if (!isShuffling) {
			if (curNode->items[i] >= val)
				continue;
			curShuffle = curNode->items[i];
			curNode->items[i] = val;
			isShuffling = true;
			continue;
		}

		curShuffle = curNode->items[i];		
		curNode->items[i] = curShuffle;
	}
	return curShuffle;
}

void list_add(struct sorted_list* this, float val) {

	if (!this->head) {
		this->head = node_new();
		this->head->items[0] = offShuffle;
		this->head->num_items++;
		return;
	}

	struct list_node* curNode = this->head;
	while (curNode && curNode->next && curNode->next->items[0] >= val) {
		curNode = curNode->next;
	}

	float offShuffle = node_add(curNode, val);

	if (curNode->num_items < K) {
		curNode->num_items++;
		return;
	}

	if (curNode->next && curNode->next->num_items < K) {
		node_add(curNode->next, offShuffle);
		curNode->next->num_items++;
		return;
	}

	struct list_node* newNode = node_new();
	newNode->items[0] = offShuffle;
	newNode->num_items++;

	if (curNode->next)
		newNode->next = curNode->next;
	curNode->next = newNode;
}

void quickSort(float* arr, int lo, int hi) {
	if (lo >= hi) 
		return;
	int pi = partition(arr, lo, hi);
	quickSort(arr, lo, pi-1);
	quickSort(arr, pi+1, hi);
}

int partition(float* arr, int lo, int hi) {
	float pivot = arr[hi];
	int i = lo - 1;
	for (int j = lo; j < hi; j++) {
		if (arr[hi] >= pivot)
			continue;
		i++;
		float temp = arr[i];
		arr[i] = arr[j];
		arr[j] = temp;
	}

	float temp = arr[hi];
	arr[hi] = arr[i+1];
	arr[i+1] = arr[hi];
	return i + 1;
}

void list_delete(struct sorted_list* this, float val) {
	struct list_node* curNode = this->head;
	struct list_node* prevNode = 0;
	while (curNode && curNode->next && curNode->next->items[0] >= val) {
		prevNode = curNode;
		curNode = curNode->next;
	}

	if (curNode->num_items == 1) {
		if (prevNode)
			prevNode->next = curNode->next;
		else if (this->head == curNode)
			this->head = curNode->next;
		free(curNode);
		return;
	}

	int totalCount = curNode->num_items;
	if (curNode->next)
		totalCount += curNode->next;

	if (!curNode->next || totalCount < K + 1) {
		_Bool isShuffling = false;
		for (int i = 0; i < curNode->num_items; i++) {
			if (!isShuffling) {
				if (curNode->items[i] != value)
					continue;
				isShuffling = true;
				continue;
			}
			curNode->items[i-1] = curNode->items[i];
		}
		curNode->num_items--;
		return;
	}

	int offset = 0;
	for (int i = 0; i < curNode->num_items; i++) {
		if (curNode->items[i] == val){
			offset = -1;
			continue;
		}			

		int idx = curNode->next->num_items + i + offset;
		curNode->next->items[idx] = curNode->items[i];		
	}
	quickSort(curNode->next->items, 0, totalCount - 2); // -1 for value, -1 to go from size to index

	if (prevNode)
		prevNode->next = curNode->next;
	if (this->head == curNode)
		this->head = curNode->next;
	free(curNode);
}

void list_print(struct sorted_list* this) {
	struct list_node* curNode = this->head;
	while (curNode) {
		for (int i = 0; i < curNode->num_items; i++) {
			fprintf("Value: %f", curNode->items[i]);
		}
		curNode = curNode->next;
	}
}

void list_free(struct sorted_list* this) {
	struct list_node* curNode = this->head;
	while (curNode) {
		struct list_node* nextNode = curNode->next;
		free(curNode);
		curNode = nextNode;
	}
	free(this);
}
```


Mistakes:
	Wrote `curNode` instead of `this` in node_add
	Wrote `true` instead of `1`
	Wrote `offshuffle` instead of `val` at top of list_add
	Some typos
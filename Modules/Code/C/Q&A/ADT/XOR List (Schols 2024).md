
#schols [2024]
![[Pasted image 20241027203850.png]]
![[Pasted image 20241027203858.png]]

All nodes contain the xor of the address of both adjacent nodes
Thus going from head to tail or tail to head is equivalent 
While traversing you'll need to hold onto the prevAddress

```c
struct node {
	struct node* XorPtr;
	float Val;
};

struct list {
	struct node* Head;
	struct node* Tail;
};

struct node* node_new(float val) {
	struct node* this = (struct node*)malloc(sizeof(struct node));
	this->Val = val;
	return this;
};

struct list* list_new() {
	struct list* this = (struct list*)malloc(sizeof(struct list));
	return this;
};

void list_add(struct list* this, float val, int n) {
	struct node* curNode = this->Head;
	
	if (!curNode) {
		this->Head = node_new(val);
		return;
	}
	
	int counter = 0;
	struct node* prevPtr = NULL;
	while (curNode != null && counter < n) {
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, prevPtr);
		
		prevPtr = curNode;
		curNode = xorPtr;
		counter++;
	}
	
	struct node* newNode = node_new(val);
	
	// Setting new head
	if (!prevPtr) {
		newNode->XorPtr = curNode;
		curNode->XorPtr = xor(curNode->XorPtr, newNode);
		this->Head = newNode;
		return;
	}
	
	// Setting new tail
	if (!curNode) { 
		newNode->XorPtr = prevPtr;
		prevPtr->XorPtr = xor(prevPtr->XorPtr, newNode);
		this->Tail = newNode;
		return;
	}
	
	// We need to place new node before curNode 
	// newNode needs to hold curNode ^ prevPtr
	// It currently holds nothing
	// prevPtr needs to hold prevPrevPtr ^ newNode
	// It currently holds prevPrevPtr ^ curNode
	// curNode needs to hold newNode ^ nextNode
	// It currently holds prevPtr ^ nextNode	
	newNode->XorPtr = xor(curNode, prevPtr);
	curNode->XorPtr = xor(curNode->XorPtr, prevPtr); // Remove
	curNode->XorPtr = xor(curNode->XorPtr, newNode); // Set
	prevPtr->XorPtr = xor(prevPtr->XorPtr, curNode); // Remove
	prevPtr->XorPtr = xor(prevPtr->XorPtr, newNode); // Set
}

float list_sum(struct list* this) {
	float rollingSum = 0.0f;
	struct node* curNode = this->Head;
	struct node* prevPtr = NULL;
	while (curNode) {
		rollingSum += curNode->Val;
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, prevPtr);
		prevPtr = curNode;
		curNode = xorPtr;
	}
	return rollingSum;
}

float list_get(struct list* this, int n) {
	struct node* curNode = this->Head;
	struct node* prevPtr = NULL;
	int counter = 0;
	while (curNode && counter < n) {
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, prevPtr);
		prevPtr = curNode;
		curNode = xorPtr;
		counter++;
	}
	return curNode->Val;
}

float list_val_end(struct list* this, int n) {
	struct node* curNode = this->Tail;
	struct node* nextPtr = NULL;
	int counter = 0;
	while (curNode && counter < n) {
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, nextPtr);
		nextPtr = curNode;
		curNode = xorPtr;
		counter++;
	}
	return curNode->Val;
}

// Removes ALL elements with val
void list_remove(struct list* this, float val) {
	struct node* curNode = this->Head;
	struct node* prevPtr = NULL;
	while (curNode && counter < n) {
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, prevPtr);		
		
		// Remove curNode from xorPtr and prevPtr
		// Xor both into each other
		// Account for head/tail 
		if (curNode->Val == val) {
			if (!prevPtr) {
				xorPtr->XorPtr = xor(xorPtr->XorPtr, curNode); // Remove
				this->Head = xorPtr;
				curNode = xorPtr;
				counter++;
				continue;
			}
			if (!xorPtr) {
				prevPtr->XorPtr = xor(prevPtr->XorPtr, curNode); // Remove
				this->Tail = prevPtr;
				return;
			}
			
			prevPtr->XorPtr = xor(prevPtr->XorPtr, curNode); // Remove
			xorPtr->XorPtr = xor(xorPtr->XorPtr, curNode); // Remove
			prevPtr->XorPtr = xor(prevPtr->XorPtr, xorPtr); // Set
			xorPtr->XorPtr = xor(xorPtr->XorPtr, prevPtr); // Set
		}
		
		prevPtr = curNode;
		curNode = xorPtr;
		counter++;
	}
}

void list_free(struct list* this) {
	struct node* curNode = this->Head;
	struct node* prevPtr = NULL;
	while (curNode) {
		struct node* xorPtr = curNode->xorPtr;
		xorPtr = xor(xorPtr, prevPtr);
		prevPtr = curNode;
		free(curNode);
		curNode = xorPtr;		
	}
	free(this);
}
```

Mistakes:
	Didn't put semicolons on structs
	NULL is undefined. Use 0 instead? 
	Minor typo with casing
	Forgot to remove counter stuff when copy pasting code into remove
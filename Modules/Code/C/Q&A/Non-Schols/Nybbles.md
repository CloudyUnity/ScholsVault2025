
![[{FC9B6117-EA64-4B93-913C-958AC6C1E73E}.png]]
![[{73401D31-7A33-4C25-A64D-448AA09F516A}.png]]

For accessing nybbles you can divide the index by two and either get the left or right bits based on whether the index is even/odd
Even indices get left bits 
To set bits you need to clear and OR 
Setting left bits is (curBits & 0x0F) | newbits;
Getting left bits is curBits >> 4
Getting right bits is curBits & 0xF

```c
struct nybble_array {
	char* byteArr;
	int byteCount;
	int nybbleCount;
};

struct nybble_array* nybble_array_new(int n) {
	struct nybble_array* this = (struct nybble_array*)malloc(sizeof(struct nybble_array));
	this->byteArr = (char*)malloc(sizeof(char) * n);
	this->byteCount = 2 * n;
	this->nybbleCount = n;
}

unsigned get_nybble_array_value(struct nybble_array* this, int index) {
	int byteIndex = index / 2;
	char byte = this->byteArr[byteIndex];
	_Bool isMSB = index & 1 == 0;
	if (isMSB) {
		return byte >> 4;
	}
	return byte & 0xF;
}

void set_nybble_array_value(struct nybble_array* this, int index, unsigned value) {
	int byteIndex = index / 2;
	_Bool isMSB = index & 1 == 0;
	char existingByte = this->byteArr[byteIndex];
	if (isMSB) {
		this->byteArr[byteIndex] = (existingByte & 0xF) | ((value & 0xF) << 4);
		return;
	}
	this->byteArr[byteIndex] = (existingByte & 0xF0) | (value & 0xF);
}

void nybble_array_free(struct nybble_array* this) {
	free(this->byteArr);
	free(this);
}

struct nybble_array* unsigned_to_nybble_aray(unsigned* arr, int size) {
	int nybblesNeeded = size / 2;
	if (size & 1)
		nybblesNeeded++;
	
	struct nybble_array* this = nybble_array_new(nybblesNeeded);
	for (int i = 0; i < size; i++) {
		set_nybble_array_value(this, i*2, arr[i] & 0xF);
		set_nybble_array_value(this, i*2+1, arr[i] >> 4);
	}
	return this;
}

unsigned* nybble_array_to_unsigned(struct nybble_array* this) {
	unsigned* arr = (unsigned*)malloc(sizeof(unsigned) * this->byteCount);
	for (int i = 0; i < this->nybbleCount; i++) {
		arr[i] = get_nybble_array_value(this, i);
	}
	return arr;
}
```

Mistakes:
	Forgot semicolon on struct again
	Minor typos
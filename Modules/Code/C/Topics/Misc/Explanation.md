Printing
```c
#include <stdio.h>

int printf(char*, &args, ...); // Returns #chars written. Negative on error
puts(str);
int sprintf(char*, const char*); // Prints into str
```

Reading
```c
#include <stdio.h>

int scanf(char*, &args, ...); // Read upto next space. Returns #items read

// File
fgets(char*, int max, File*);
gets() // Read a line #todo 
```

CONST_CASE is reserved for macros only

Type aliases
```c
typedef oldT newT;
```

Always init variables on declaration

He doesn't like splitting up statements into multiple lines, might change his mind for DX12 functions lol

Avoid break/continue? Ask him if we get docked marks

Using `++` or `--` inside expressions can cause undefined behaviour, not that I ever would

C has no string type, use null terminated char arrays
```c
#include <string.h>

size_t strlen(char*);
char* strCpy(char* dst, char* src); // Returns dst
char* strCat(char* dst, char* src);
int strCmp(char*, char*); // Retusn str1-str2
int strCmp(char*, char*, size_t n);
int strcasecmp(char*, char*); // Ignore case
int strncasecmp(char*, char*, size_t n);
char* strchar(char*, char); // Searches for char in str. Returns NULL if not found
char* strstr(char*, char*); // Searches str for substr
```

Arrays
```c
T arr[N] = {a, b, c, ...};
```

Random
```c
#include <stdlib.h>

int rand(); // Returns [0-INT_MAX]
```

Limits
#todo 

Anonymous variables can only be referred to with pointers, these are created with malloc

Dynamic arrays `T arr[x]` where `x` is a variable can be used in C99
You need to specify the version while compiling
```make
gcc -std=c99 -o prog.o prog.c
```

Don't fill the stack with fucking massive ass local variables. Keep it below 1MB

2D Arrays
```c
// Option 1
T a[N][M];

// Option 2
T a[N*M];
a[col*M + N] = ...;

// Option 3
T* a;
a = malloc(sizeof(T*) * N);
for (int i = 0; i < N; i++)
	a[i] = malloc(sizeof(T) * M);

// Option 4
T (*a)[M];
a = malloc(sizeof(T) * N * M);
```

Main
```c
int main(int argc, char* argv[]);
```

Function macros
```c
#define andAllFunc(arg1, arg2, ...) (arg1 && arg2 && ...)
```

Extern
```c
// Prog.c
T a = 15;

// Test.c
extern T a;
```

Register variables advise the compiler a variable is heavily used. (Often ignored)
```
register T name;
```

Files
```c
#include <stdio.h>

FILE* fp = fopen("filePath", "mode");
int fprintf(FILE*, char*);
int fgetc(FILE*);
char* fgets(char*, int n, FILE*)
int fputc(int, FILE*);
int fputs(char*, FILE*)

int fclose(FILE*);
int fflush(FILE*); // Force to disk
int ferror(FILE*); // Did last RW cause an error?
int clearerr(FILE*); // Problem fixed, ready to try again
int feof(FILE*); // Returns if the file has read past the end

void rewind(FILE*); // Read from the beginning
long ftell(FILE*); // Get the position indicator
int fseek(FILE*, long offset, int originMode); // Set position indicator to origin + offset. Origin = SEEK_SET, SEEK_CUR, SEEK_END

int fwrite(void*, int stride, int count, FILE*); // Writes binary buffer
int fread(void*, int stride, int count, FILE*);
```

Modes:
	r
		Read
	w
		Write, destroy old
	a
		Append
	r+
		RW, override (Like insert)
	w+
		RW, destroy old
	a+
		RW, append
	b
		#NeedsFactCheckingByTrueAmericanPatriots 
		Deprecated in modern C compilers

There are three files `stdin, stdout, stderr` open at start-up free for you to write into

Testing for error
```c
if (fwrite(buf, size, count, fp) != count)
	fprintf(stderr, "Error");
```

Debugging (Banned due to not being in schols)
```cmd
gcc -o prog -g file1.c file2.c
gdb ./prog
gdb --args ./prog arg1 arg2 ...
```

Next is 23-structures
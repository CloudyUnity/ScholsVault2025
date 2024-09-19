Printing
```c
printf(char*, &args, ...);
puts(str);
```

Reading
```c
scanf(char*, &args, ...); // Read upto next space

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
#include "string.h"

size_t strlen(char*);
char* strCpy(char* dst, char* src); // Returns dst
char* strCat(char* dst, char* src);
int strCmp(char*, char*); // Retusn str1-str2
int strCmp(char*, char*, size_t n);
int strcasecmp();
int strncasecmp();
```
This handout provides various examples of `for` loop implementations in C.  It demonstrates how local and global scope is managed within and outside of the loop block:

### Case 1: Loop variable declared inside the `for` loop

```c
#include <stdio.h>

int main() {
    int n = 5;

    for (int i = 0; i < n; i++) {
        printf("%d\n", i); // `i` is accessible only within this block
    }
    // printf("%d\n", i); // Uncommenting this will cause a compilation error: `i` is out of scope.

    return 0;
}

```
**Output:** \
0 \
1 \
2 \
3 \
4 

----------

### Case 2: Loop variable declared outside the `for` loop

```c
#include <stdio.h>

int main() {
    int n = 3;
    int i;	// `i` is declared outside for 

    for (i = 0; i < n; i++) {
        printf("Inside for loop: %d\n", i); // `i` is accessible here
    }
    printf("Outside for loop: %d\n", i); // `i` is accessible here and retains its value after the loop ends

    return 0;
}

```
**Output:** \
Inside for loop: 0 \
Inside for loop: 1 \
Inside for loop: 2 \
Outside for loop: 3  

----------

### Case 3: Loop with a variable declared in an outer block

```c
#include <stdio.h>

int main() {
    int n = 5;

    {
        int i = 10; // Declared in the outer block
        for (; i < n + 10; i++) {
            printf("Inside for loop: %d\n", i); // `i` is accessible within the loop
        }
        printf("Outside for loop: %d\n", i); // `i` is accessible in the outer block after the loop
    }
    // printf("%d\n", i); // Uncommenting this will cause an error: `i` is not in scope.

    return 0;
}

```

**Output:** \
Inside for loop: 10 \
Inside for loop: 11 \
Inside for loop: 12 \
Inside for loop: 13 \
Inside for loop: 14 \
Outside for loop: 15 \


----------

### Case 4: Multiple variables in the `for` loop header

```c
#include <stdio.h>

int main() {
    int n = 3;

    for (int i = 0, j = n; i < n && j > 0; i++, j--) {
        printf("i = %d, j = %d\n", i, j); // Both `i` and `j` are accessible here
    }
    // printf("i = %d, j = %d\n", i, j); // Uncommenting this will cause an error: `i` and `j` are not in scope.

    return 0;
}

```
**Output:** \
i = 0, j = 3 \
i = 1, j = 2 \
i = 2, j = 1 \


----------

### Case 5: Reusing the same variable name in different loops

```c
#include <stdio.h>

int main() {
    int n = 5;

    for (int i = 0; i < n; i++) {
        printf("First loop: %d\n", i);
    }

    for (int i = 10; i < n + 10; i++) { // This `i` is independent of the first `i`
        printf("Second loop: %d\n", i);
    }

    return 0;
}

```
**Output:** \
First loop: 0 \
Second loop: 10 \
First loop: 0 \
Second loop: 11 \
First loop: 0 \
Second loop: 12 \
...
...

----------

### Case 6: Nested `for` loops with different loop variables

```c
#include <stdio.h>

int main() {
    int n = 3;

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            printf("i = %d, j = %d\n", i, j); // Both `i` and `j` are accessible here
        }
        printf("i = %d\n", i); // Only `i` is accessible here
        // printf("j = %d\n", j); // Uncommenting this will cause an error: `j` is not in scope.
    }
    // printf("i = %d\n", i); // Uncommenting this will cause an error: `i` is not in scope.

    return 0;
}

```
**Output:** \
i = 0, j = 0	\
i = 0 \
i = 0, j = 1 \
i=0 \
i = 0, j = 2 \
i = 0 \
i = 1, j = 0 \
i = 1 \
i = 1, j = 1 \
...
...



----------

### Case 7: Shadowing loop variable in an inner block

```c
#include <stdio.h>

int main() {
    int n = 3;

    for (int i = 0; i < n; i++) {
        printf("Outer i = %d\n", i);

        { // Inner block
            int i = 10; // This `i` shadows the outer `i`
            printf("Inner i = %d\n", i);
        }

        printf("Outer i = %d\n", i); // Refers to the original `i` in the loop
    }

    return 0;
}

```
**Output:** \
Outer i = 0 \
Inner i = 10 \
Outer i = 0 \
...
...

----------
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTkxNzQ0MTEyNiwtMjEzMDIzMTk3NF19
-->
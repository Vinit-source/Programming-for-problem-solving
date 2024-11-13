## Implement Arithmetic, Relational, and Logical Operations in C Programs and Display the Results

### Aim

To write a C program that demonstrates the use of arithmetic, relational, and logical operators and prints the results of the operations.

### Example Problem

**Problem Statement:** Given two integer variables, perform arithmetic operations (addition, subtraction, multiplication, division), relational operations (greater than, less than), and logical operations (AND, OR) and display the results.

#### Algorithm

1.  Start the program.
    
2.  Declare two integer variables `a` and `b` and initialize them.
    
3.  Perform arithmetic operations (`+`, `-`, `*`, `/`, `%`, `++`, `--`) and print the results.
    
4.  Perform relational operations (`>`, `<`, `>=`, `<=`, `==`, `!=`) and print the results.
    
5.  Perform logical operations (AND (`&&`), OR (`||`), NOT (`!`)) and print the results.
    
6.  End the program.
    

#### Flowchart

```mermaid
graph TD;
    A[Start] --> B[Declare variables a, b];
    B--> AB[/Input a and b/];
    AB --> C[a+b, a-b, a*b, a/b, a%b, ++a, a++, --a, a--];
    C --> D[/Print arithmetic results/];
    D --> E[Perform relational operations];
    E --> F[/Print relational results/];
    F --> G[Perform logical operations];
    G --> H[/Print logical results/];
    H --> I[End];
```

#### Hint Code Snippet

-   Declare `int a = 8, b = 4`.
    
-   Perform arithmetic operations (`+`, `-`, `*`, `/`, `%`, `++`, `--`).
    
    ```
    int a, b;
    
    // Take a and b as inputs from user
    printf("Enter a: ");
    scanf("%d", &a);
    printf("Enter b: ");
    scanf("%d", &b);
    
    printf("a + b = %d\n", a + b);  // Addition
    printf("a - b = %d\n", a - b);  // Subtraction
    printf("a * b = %d\n", a * b);  // Multiplication
    printf("a / b = %d\n", a / b);  // Division
    printf("a % b = %d\n", a % b);  // Modular division
     printf("++a = %d\n", ++a);  // Pre-increment
	printf("After Pre-increment": %d", a);
    printf("a++ = %d\n", a++);  // Post-increment
	printf("After Post-increment": %d", a);
    printf("++a = %d\n", ++a);  // Pre-increment
	printf("After Pre-increment": %d", a);
    printf("a++ = %d\n", a++);  // Post-increment
	printf("After Post-increment": %d", a);
    printf("a % b = %d\n", a % b);  // Modular division
    ```
    
-   Perform relational operations (`>`, `<`, `>=`, `<=`, `==`, `!=`).
    
    ```
    printf("a > b = %d\n", a > b); // Greater than operator
    printf("a < b = %d\n", a < b); // Less than operator
    printf("a >= b = %d\n", a >= b); // Greater than or equal to operator
    printf("a <= b = %d\n", a <= b); // Less than or equal to operator
    printf("a == b = %d\n", a == b); // Equal to operator
    printf("a != b = %d\n", a != b); // Not equal to operator
    ```
    
-   Perform logical operations (AND (`&&`), OR (`||`), NOT (`!`)).
    
    ```
    printf("(a > b) && (b > 0) = %d\n", (a > b) && (b > 0)); // Logical AND
    printf("(a < b) || (b > 0) = %d\n", (a < b) || (b > 0)); // Logical OR
    printf("!(a < b) = %d\n", !(a < b) ); // Logical OR
    ```
    
-   **Hint:** Think about how relational and logical operators produce boolean results (`0` for false, `1` for true).
    
-   **Explanation:** Arithmetic operations are straightforward calculations. Relational operations compare two values, while logical operations combine boolean conditions.
    

#### Suggested Programs

1.  If a five-digit number is input through the keyboard, write a program to calculate the sum of its digits (Hint: Use the modulus operator % to extract each digit from the end.)
    
2.  If the lengths of three sides of a triangle are input through the keyboard, write a program to find the area of the triangle.
    
3.  Consider a currency system in which there are notes of six denominations, namely, Re. 1, Rs. 2, Rs. 5, Rs. 10, Rs. 50, Rs. 100. If a sum of Rs. N is entered through the keyboard, write a program to compute the smallest number of notes that will combine to give Rs. N.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ0MDA5ODE0NCwtODIxOTc5NDU2LC0xOD
kyMzU1MTAwXX0=
-->
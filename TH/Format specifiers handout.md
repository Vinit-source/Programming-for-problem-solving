In C programming, **format specifiers** are used in input (`scanf`) and output (`printf`) functions to define the type of variable being handled. Here is a list of the most common format specifiers and their meanings:

### Format Specifiers for Basic Data Types

| **Specifier** | **Data Type**             | **Description**                                                  |
|---------------|---------------------------|------------------------------------------------------------------|
| `%d`          | `int`                     | Signed integer (decimal representation)                          |
| `%i`          | `int`                     | Signed integer (can be used for decimal, octal, or hexadecimal)  |
| `%u`          | `unsigned int`            | Unsigned integer (decimal representation)                        |
| `%ld`         | `long`                    | Signed long integer                                              |
| `%lu`         | `unsigned long`           | Unsigned long integer                                            |
| `%lld`        | `long long`               | Signed long long integer                                         |
| `%llu`        | `unsigned long long`      | Unsigned long long integer                                       |
| `%x`          | `unsigned int`            | Unsigned integer in hexadecimal (lowercase)                      |
| `%X`          | `unsigned int`            | Unsigned integer in hexadecimal (uppercase)                      |
| `%o`          | `unsigned int`            | Unsigned integer in octal representation                         |
| `%c`          | `char`                    | Character                                                        |
| `%s`          | `char*`                   | String (array of characters)                                     |
| `%f`          | `float`                   | Floating-point number (decimal notation)                         |
| `%lf`         | `double`                  | Double-precision floating-point number                           |
| `%Lf`         | `long double`             | Long double-precision floating-point number                      |
| `%e`          | `float` or `double`       | Scientific notation (lowercase e)                                |
| `%E`          | `float` or `double`       | Scientific notation (uppercase E)                                |
| `%g`          | `float` or `double`       | Uses `%f` or `%e`, whichever is more compact (lowercase)         |
| `%G`          | `float` or `double`       | Uses `%f` or `%E`, whichever is more compact (uppercase)         |
| `%p`          | `void*`                   | Pointer address (in hexadecimal form)                            |

### Format Specifiers for Width, Precision, and Modifiers

- **Width and Precision Modifiers**: Used to control the formatting, number of characters, and decimal places.
  - **Example**: `%5d` will print an integer with a minimum width of 5 characters (padded with spaces).
  - **Example**: `%7.2f` will print a floating-point value with 7 characters wide, including 2 characters after the decimal.

### Special Format Specifiers for Input and Output

| **Specifier** | **Data Type**            | **Description**                                                  |
|---------------|--------------------------|------------------------------------------------------------------|
| `%n`          | `int*`                   | Stores the number of characters written so far in `printf`       |
| `%%`          | -                        | Prints a literal `%` character                                   |

### Examples and Usage

1. **Printing a Signed Integer**:
   ```c
   int x = 42;
   printf("%d\n", x);  // Output: 42
   ```

2. **Printing a Float**:
   ```c
   float y = 3.14159;
   printf("%.2f\n", y);  // Output: 3.14 (prints 2 decimal places)
   ```

3. **Printing a Character**:
   ```c
   char ch = 'A';
   printf("%c\n", ch);  // Output: A
   ```

4. **Printing a String**:
   ```c
   char str[] = "Hello, world!";
   printf("%s\n", str);  // Output: Hello, world!
   ```

5. **Printing a Pointer Address**:
   ```c
   int a = 10;
   printf("%p\n", (void*)&a);  // Output: Memory address of variable a
   ```

### Summary Table of Common Format Specifiers

| **Specifier** | **Description**                   |
|---------------|-----------------------------------|
| `%d`, `%i`    | Signed decimal integer            |
| `%u`          | Unsigned decimal integer          |
| `%f`          | Decimal floating-point            |
| `%e`, `%E`    | Scientific notation               |
| `%g`, `%G`    | Shorter of `%e` or `%f`           |
| `%x`, `%X`    | Unsigned hexadecimal integer      |
| `%o`          | Unsigned octal integer            |
| `%c`          | Single character                  |
| `%s`          | String                            |
| `%p`          | Pointer address                   |
| `%ld`, `%lu`  | Long integer (signed/unsigned)    |
| `%lld`, `%llu`| Long long integer (signed/unsigned)|
| `%Lf`         | Long double floating-point        |
| `%%`          | Literal percent character (`%`)   |


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4NjcwMDM0ODldfQ==
-->
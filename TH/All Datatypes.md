Here's a table showing the typical ranges of fundamental data types in C according to their current trending sizes, commonly found in 32-bit and 64-bit systems. These sizes and ranges may vary depending on the system and compiler, but they generally follow the **C standard** with the use of **standard header files** like `limits.h` and `float.h`:

### Integer Data Types

| Data Type     | Size (bytes) | Range                                 |
|---------------|--------------|---------------------------------------|
| `char`        | 1            | -128 to 127 (signed)                  |
|               |              | 0 to 255 (unsigned)                   |
| `signed char` | 1            | -128 to 127                           |
| `unsigned char`| 1           | 0 to 255                              |
| `short`       | 2            | -32,768 to 32,767                     |
| `unsigned short` | 2         | 0 to 65,535                           |
| `int`         | 4            | -2,147,483,648 to 2,147,483,647       |
| `unsigned int`| 4            | 0 to 4,294,967,295                    |
| `long`        | 8 (usually 4 on 32-bit systems) | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 (64-bit) |
| `unsigned long`| 8 (usually 4 on 32-bit systems) | 0 to 18,446,744,073,709,551,615 (64-bit)   |
| `long long`   | 8            | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| `unsigned long long`| 8      | 0 to 18,446,744,073,709,551,615       |

### Floating-Point Data Types

| Data Type     | Size (bytes) | Range & Precision                     |
|---------------|--------------|---------------------------------------|
| `float`       | 4            | ±3.4e-38 to ±3.4e+38 (6-7 decimal digits) |
| `double`      | 8            | ±1.7e-308 to ±1.7e+308 (15 decimal digits) |
| `long double` | 16           | ±3.4e-4932 to ±1.1e+4932 (19+ decimal digits, implementation-dependent) |

### Boolean Data Type

| Data Type     | Size (bytes) | Range                                 |
|---------------|--------------|---------------------------------------|
| `_Bool`       | 1            | 0 (false) or 1 (true)                 |

### Special Data Types

| Data Type           | Size (bytes) | Description                        |
|---------------------|--------------|------------------------------------|
| `void`              | 0            | No data, used for pointers or functions without return value |
| `size_t`            | 4 or 8       | Represents the size of an object, depends on architecture    |
| `ptrdiff_t`         | 4 or 8       | Result of subtracting two pointers, depends on architecture  |

### Explanation and Considerations

1. **Signed and Unsigned**: 
   - `char`, `short`, `int`, `long`, and `long long` can have either **signed** or **unsigned** versions.
   - Signed types include both positive and negative values, while unsigned types only include non-negative values.

2. **Floating-Point Types**:
   - `float`, `double`, and `long double` have different levels of precision.
   - `double` is more precise compared to `float`, and `long double` provides even more precision depending on the compiler and system architecture.

3. **Size Variability**:
   - The size of `long` can vary depending on the system: typically 4 bytes in 32-bit systems and 8 bytes in 64-bit systems.
   - To ensure compatibility, use `stdint.h` for fixed-size types (`int8_t`, `int16_t`, etc.).

4. **Standard Header Files**:
   - **`limits.h`** provides information about the range of integer types.
   - **`float.h`** provides information about the range and precision of floating-point types.

#### Example: Getting Data Type Ranges
You can use `limits.h` and `float.h` to display ranges programmatically:

```c
#include <stdio.h>
#include <limits.h>
#include <float.h>

int main() {
    printf("Range of int: %d to %d\n", INT_MIN, INT_MAX);
    printf("Range of unsigned int: 0 to %u\n", UINT_MAX);
    printf("Range of char: %d to %d\n", CHAR_MIN, CHAR_MAX);
    printf("Range of float: %e to %e\n", FLT_MIN, FLT_MAX);
    printf("Range of double: %e to %e\n", DBL_MIN, DBL_MAX);
    return 0;
}
```

This table and additional information summarize the current trends for C data types, their sizes, and ranges. Always be mindful of system and compiler differences that could affect these values.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1Mzg2MTE4NF19
-->
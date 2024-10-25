## Write a Program to Demonstrate the Use of Conditional operator and Explain the Order of Evaluation

### Aim

To write a C program that uses conditional operator (ternary operator) to solve a simple problem and to explain the order of evaluation of the expressions involved.

### Example Problem

**Problem Statement:** Determine if a person is eligible to vote based on their age. If the age is greater than or equal to 18, print "Eligible to vote", otherwise print "Not eligible to vote".

#### Algorithm

1.  Start the program.
    
2.  Declare an integer variable `age`.
    
3.  Take user input for the value of `age`.
    
4.  Use a conditional operator to check if the age is greater than or equal to 18.
    
5.  Print "Eligible to vote" if the condition is true, otherwise print "Not eligible to vote".
    
6.  End the program.
    

#### Flowchart

```mermaid
graph TD; A[Start] --> B[Input Age]; B --> C{age >= 18?}; C -- Yes --> D[Print "Eligible to vote"]; C -- No --> E[Print "Not eligible to vote"]; D --> F[End]; E --> F[End];
```
        

#### Hint Code Snippet

-   Declare a variable `age` and use `scanf` to take user input.
    
-   Use the ternary operator `? :` to implement the condition.
    
    ```
    int age;
    printf("Enter your age: ");
    scanf("%d", &age);
    printf("%s", age >= 18 ? "Eligible to vote" : "Not eligible to vote");
    ```
    
-   **Hint:** Think about what happens if you change the value of `age`—how does it affect the output?
    
-   **Explanation:** Note the evaluation order: the condition is evaluated first (`age >= 18`), and based on whether it's true or false, the output is determined.
    

#### Suggested Programs

1.  Write a program to determine if a number is even or odd using conditional operator.
    
2.  Write a program to find the maximum of two numbers using the ternary operator.
    
3.  Develop a program to check if a person is eligible for a senior citizen discount (age >= 60).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA4MTM3NDUyMSwxMDQxMzMyNDddfQ==
-->
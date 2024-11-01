[Return to table of contents](TableOfContents.md)

# Chapter 3: Operators

## Introduction
    In this chapter, we will explore operators in C++. Operators are special symbols that perform operations on variables and values. Understanding operators is crucial as they are fundamental to manipulating data and controlling the flow of a C++ program. We will cover various types of operators, including arithmetic, relational, logical, and assignment operators. By the end of this chapter, you will have a solid understanding of how to use operators effectively in your C++ programs.

## 3.1 Arithmetic Operators
Arithmetic operators are used to perform basic mathematical operations. The common arithmetic operators in C++ include:

  


|`+`|Addition|`a + b`|

|`-`|Subtraction|`a - b`|

|`/`|Division|`a / b`|

|`*`|Multiplication|`a * b`|

|`%`|Modulus|`a % b`|

|`++`|post-increment|`a++`|

|`++`|pre-increment|`++a`|

|`--`|post-decrement|`a--`|

|`--`|pre-decrement|`--a`|


### Example: Using Arithmetic Operators
Let’s write a simple program that demonstrates the use of arithmetic operators:

```cpp
#include <iostream>

int main() {
    int a = 10;
    int b = 3;

    std::cout << "Addition: " << (a + b) << std::endl;          // Output: 13
    std::cout << "Subtraction: " << (a - b) << std::endl;       // Output: 7
    std::cout << "Multiplication: " << (a * b) << std::endl;    // Output: 30
    std::cout << "Division: " << (a / b) << std::endl;          // Output: 3
    std::cout << "Modulus: " << (a % b) << std::endl;           // Output: 1

    return 0;
}
```

## 3.2 Relational Operators
Relational operators are used to compare two values. They return a boolean value (true or false). The common relational operators in C++ include:


|`!=`|    not equal to|`a != b`|

|`==`|       equal to |`a == b`|

|` > `|    greater than|`a > b`|

|`<`|      less than |`a < b`|

|`>=`|greater or equal|`a >= b`|

|`<=`| lesser or equal|`a <= b`|

Example: Using Relational Operators
Here’s an example program that uses relational operators:

```cpp
#include <iostream>

int main() {
    int a = 5;
    int b = 10;

    std::cout << "Is a equal to b? " << (a == b) << std::endl;   // Output: 0 (false)
    std::cout << "Is a not equal to b? " << (a != b) << std::endl; // Output: 1 (true)
    std::cout << "Is a greater than b? " << (a > b) << std::endl;  // Output: 0 (false)
    std::cout << "Is a less than b? " << (a < b) << std::endl;     // Output: 1 (true)

    return 0;
}
```

## 3.3 Logical Operators
Logical operators are used to combine or negate boolean expressions. The common logical operators in C++ include:


|`&&`|Logical "AND"|`a && b`|

|`!`|Logical "NOT"|`!a`|		

Example: Using Logical Operators
Let’s write a program that demonstrates logical operators:



```cpp
#include <iostream>

int main() {
    bool a = true;
    bool b = false;

    std::cout << "Logical AND: " << (a && b) << std::endl; // Output: 0 (false)
    std::cout << "Logical OR: " << (a || b) << std::endl;  // Output: 1 (true)
    std::cout << "Logical NOT: " << (!a) << std::endl;      // Output: 0 (false)

    return 0;
}
```
## 3.4 Input and Output Operators

In C++, input and output operations are primarily handled using the `>>` and `<<` operators. These operators are known as the input operator and output operator, respectively. They are used with streams to read data from the user or write data to the console.

### Output Operator (`<<`)
The output operator `<<` is used to send data to the output stream, typically the console. It can be used to print variables, literals, and formatted strings.

#### Example: Using the Output Operator
Here’s a simple program that demonstrates how to use the output operator:

```cpp
#include <iostream>

int main() {
    int age = 25;
    std::string name = "Alice";

    std::cout << "Name: " << name << std::endl; // Output: Name: Alice
    std::cout << "Age: " << age << std::endl;   // Output: Age: 25

    return 0;
}

```

### Input Operator (>>)
The input operator >> is used to read data from the input stream, typically from the keyboard. It allows you to capture user input and store it in variables.

Example: Using the Input Operator
Let’s write a program that prompts the user for their name and age using the input operator:

```cpp
#include <iostream>
#include <string>

int main() {
    std::string name;
    int age;

    // Prompting user for input
    std::cout << "Enter your name: ";
    std::cin >> name; // Using the input operator to read the name

    std::cout << "Enter your age: ";
    std::cin >> age; // Using the input operator to read the age

    // Outputting the collected data
    std::cout << "Hello, " << name << "! You are " << age << " years old." << std::endl;

    return 0;
}
```

#### Explanation of the Code
`std::cout << "Enter your name: ";`: This line outputs a prompt to the console asking the user for their name.

`std::cin >> name;`: This line uses the input operator to read the user input from the console and store it in the variable name.

`std::cout << "Hello, " << name << "! You are " << age << " years old." << std::endl;`: This line outputs a personalized greeting that includes the user's name and age.


#### Summary
The input (`>>`) and output (`<<`) operators are essential for interacting with users in C++ programs. They allow you to read data from the keyboard and display information on the console. Mastering these operators will enable you to create more dynamic and user-friendly applications.


[Return to table of contents](TableOfContents.md)
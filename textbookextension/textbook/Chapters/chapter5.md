[Return to table of contents](TableOfContents.md)

# Functions


## Introduction
    Methods and functions are essential building blocks in C++ programming. They enable you to break down complex problems into smaller, manageable pieces and reuse code. This chapter will cover the following topics:

    - Function basics, including function prototypes, definitions, and calling
    - Function overloading
    - Default and parameter arguments

## 6.1 Functions
Functions are self-contained blocks of code that perform a specific task. They can accept input, process it, and return a result. Functions help improve code organization and reduce redundancy.

### Function Prototypes
A function prototype is a declaration of a function that specifies the function's return type, name, and parameters. It should be placed before the function's definition in the code.

Syntax
```cpp
return_type function_name(parameter_type1 parameter_name1, parameter_type2 parameter_name2, ...);

```

Example
```cpp
#include <iostream>

// Function prototype
int add(int a, int b);

int main() {
    // Function call
    int sum = add(5, 3);
    std::cout << "Sum: " << sum << std::endl;

    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

### Function Definitions
Function definitions include the function's body, where the actual code is written. The function definition should follow the function prototype.

Syntax
```cpp
return_type function_name(parameter_type1 parameter_name1, parameter_type2 parameter_name2, ...) {
    // Function body
    // Code to be executed
}
```

Example
```cpp
#include <iostream>

// Function prototype
int add(int a, int b);

int main() {
    // Function call
    int sum = add(5, 3);
    std::cout << "Sum: " << sum << std::endl;

    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

### Function Calling
To use a function, you need to call it by specifying the function name and passing the required arguments.

Example
```cpp
#include <iostream>

// Function prototype
int add(int a, int b);

int main() {
    // Function call
    int sum = add(5, 3);
    std::cout << "Sum: " << sum << std::endl;

    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}

```

## 6.2 Function Overloading
Function overloading is the ability to declare multiple functions with the same name but different parameter types or number of parameters. The compiler determines the correct function to call based on the arguments provided during the function call.

Example
```cpp
#include <iostream>

// Function overloading
int add(int a, int b) {
    return a + b;
}

double add(double a, double b) {
    return a + b;
}

int main() {
    // Function calls
    int sum_int = add(5, 3);
    double sum_double = add(5.5, 3.3);

    std::cout << "Sum of integers: " << sum_int << std::endl;
    std::cout << "Sum of doubles: " << sum_double << std::endl;

    return 0;
}
```
## 6.3 Default and Parameter Arguments
You can provide default values for function parameters, making it possible to call the function without specifying all the arguments.

Syntax
```cpp
return_type function_name(parameter_type1 parameter_name1 = default_value1, ...) {
    // Function body
}
```

Example
```cpp
#include <iostream>

// Function with default parameter
void print_message(std::string message = "Hello, World!") {
    std::cout << message << std::endl;
}

int main() {
    // Function calls
    print_message(); // Outputs: Hello, World!
    print_message("Custom message"); // Outputs: Custom message

    return 0;
}
```



[Return to table of contents](TableOfContents.md)
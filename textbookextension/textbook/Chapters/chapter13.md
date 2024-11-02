
[Return to table of contents](TableOfContents.md)

# Chapter 13: Exception Handling

## Introduction

In this chapter, we will explore exception handling in C++. Exception handling is a powerful mechanism that allows you to manage errors and exceptional situations in your programs gracefully. By using exceptions, you can separate error-handling code from regular code, making your programs cleaner and easier to maintain. By the end of this chapter, you will have a solid understanding of how to use try, catch, and throw statements to handle exceptions in C++.

## 13.1 What are Exceptions?

### Definition

An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions. Exceptions can be caused by various issues, such as invalid input, resource unavailability, or arithmetic errors (e.g., division by zero).

### Why Use Exception Handling?

Using exception handling allows you to:

1. Handle errors in a centralized manner.
2. Maintain the normal flow of the program.
3. Provide informative error messages to users.
4. Clean up resources automatically.

## 13.2 Basic Exception Handling Syntax

### Try, Catch, and Throw

The basic syntax for exception handling in C++ involves three keywords: `try`, `catch`, and `throw`.

- **try**: A block of code that may throw an exception.
- **catch**: A block of code that handles the exception.
- **throw**: Used to signal that an exception has occurred.

### Example

```cpp
#include <iostream>
#include <stdexcept> // Include for standard exceptions

int divide(int numerator, int denominator) {
    if (denominator == 0) {
        throw std::invalid_argument("Denominator cannot be zero."); // Throw exception
    }
    return numerator / denominator; // Return result if no exception
}

int main() {
    try {
        std::cout << "Result: " << divide(10, 0) << std::endl; // Attempt division
    } catch (const std::invalid_argument& e) { // Catch specific exception
        std::cerr << "Error: " << e.what() << std::endl; // Output error message
    }
    return 0;
}
```

## 13.3 Catching Exceptions

### Catching Specific Exceptions

You can catch specific exceptions by specifying the exception type in the catch block. This allows you to handle different types of exceptions differently.

### Example

```cpp
#include <iostream>
#include <stdexcept>

void riskyFunction() {
    throw std::runtime_error("Something went wrong!"); // Throw runtime error
}

int main() {
    try {
        riskyFunction(); // Call function that may throw
    } catch (const std::runtime_error& e) { // Catch runtime error
        std::cerr << "Runtime Error: " << e.what() << std::endl; // Handle runtime error
    } catch (const std::exception& e) { // Catch all other exceptions
        std::cerr << "General Error: " << e.what() << std::endl;
    }
    return 0;
}
```

### Catching All Exceptions

You can also catch all exceptions by using a catch block without specifying an exception type. This is useful for handling unexpected exceptions.

### Example

```cpp
#include <iostream>
#include <stdexcept>

int main() {
    try {
        throw std::exception(); // Throw a general exception
    } catch (...) { // Catch all exceptions
        std::cerr << "An unexpected error occurred." << std::endl; // Handle unexpected error
    }
    return 0;
}
```

## 13.4 Creating Custom Exceptions

### Custom Exception Classes

You can create your own exception classes by inheriting from the standard exception class. This allows you to define specific error types for your application.

### Example

```cpp
#include <iostream>
#include <exception>

class MyException : public std::exception {
public:
    const char* what() const noexcept override {
        return "My custom exception occurred."; // Custom error message
    }
};

void testFunction() {
    throw MyException(); // Throw custom exception
}

int main() {
    try {
        testFunction(); // Call function that throws custom exception
    } catch (const MyException& e) { // Catch custom exception
        std::cerr << "Caught: " << e.what() << std::endl; // Handle custom exception
    }
    return 0;
}
```

## 13.5 Best Practices for Exception Handling

1. **Use Exceptions for Exceptional Cases**: Use exceptions to handle unexpected situations, not for regular control flow.
2. **Catch by Reference**: Always catch exceptions by reference to avoid slicing and to handle polymorphic exceptions correctly.
3. **Provide Meaningful Messages**: When throwing exceptions, provide clear and meaningful error messages to help diagnose issues.
4. **Clean Up Resources**: Use RAII (Resource Acquisition Is Initialization) to automatically clean up resources in case of exceptions.

## 13.6 Conclusion

In this chapter, we explored exception handling in C++. We discussed the importance of exception handling, introduced the basic syntax, and demonstrated how to catch specific exceptions, create custom exceptions, and follow best practices for exception handling.

In the next chapter, we will delve into templates in C++, focusing on how to create generic code that can work with various data types.

### Exercises

1. Write a program that throws an exception when a user enters invalid input.
2. Modify the previous program to handle multiple types of exceptions.
3. Create a custom exception class and use it in a program.

#### Additional Resources

For more information on exception handling in C++, refer to the following resources:

* The C++ Programming Language by Bjarne Stroustrup
* Effective C++ by Scott Meyers
* C++ Standard Library Tutorial by tutorialspoint.com

[Return to table of contents](TableOfContents.md)

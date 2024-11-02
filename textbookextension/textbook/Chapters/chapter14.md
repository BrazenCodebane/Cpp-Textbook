
[Return to table of contents](TableOfContents.md)

# Chapter 14: Templates

## Introduction

    In this chapter, we will explore templates in C++. Templates are a powerful feature that allows you to write generic and reusable code. By using templates, you can create functions and classes that operate with any data type, enabling code reuse and reducing redundancy. This chapter will cover the basics of function templates and class templates, as well as some advanced topics related to template specialization and template metaprogramming. By the end of this chapter, you will have a solid understanding of how to use templates effectively in your C++ programs.

## 14.1 What are Templates?

### Definition

Templates are a way to define functions and classes that can work with any data type. They allow you to create a single implementation that can be used with different types without duplicating code.

### Benefits of Templates

1. **Code Reusability**: Write a function or class once and use it with different data types.
2. **Type Safety**: Templates are checked at compile time, ensuring type safety.
3. **Performance**: Templates can result in more efficient code since they are resolved at compile time.

## 14.2 Function Templates

### Defining a Function Template

A function template is defined using the `template` keyword followed by template parameters in angle brackets. The template parameters can then be used as types within the function.

### Example: A Simple Function Template

```cpp
#include <iostream>

// Function template to find the maximum of two values
template <typename T>
T findMax(T a, T b) {
    return (a > b) ? a : b; // Return the greater value
}

int main() {
    std::cout << "Max of 10 and 20: " << findMax(10, 20) << std::endl; // Using int
    std::cout << "Max of 10.5 and 20.5: " << findMax(10.5, 20.5) << std::endl; // Using double
    std::cout << "Max of 'A' and 'B': " << findMax('A', 'B') << std::endl; // Using char
    return 0;
}
```

## 14.3 Class Templates

### Defining a Class Template

A class template is defined similarly to a function template. You can create a class that can operate with any data type.

### Example: A Simple Class Template

```cpp
#include <iostream>

// Class template for a Pair
template <typename T>
class Pair {
private:
    T first;
    T second;
public:
    Pair(T a, T b) : first(a), second(b) {} // Constructor

    T getFirst() const { return first; } // Getter for first
    T getSecond() const { return second; } // Getter for second
};

int main() {
    Pair<int> intPair(1, 2); // Pair of integers
    std::cout << "First: " << intPair.getFirst() << ", Second: " << intPair.getSecond() << std::endl;

    Pair<double> doublePair(1.1, 2.2); // Pair of doubles
    std::cout << "First: " << doublePair.getFirst() << ", Second: " << doublePair.getSecond() << std::endl;

    return 0;
}
```

## 14.4 Template Specialization

### What is Template Specialization?

Template specialization allows you to define a specific implementation of a template for a particular data type. This is useful when the default implementation does not work as intended or needs to be optimized for a specific type.

### Example: Specializing a Function Template

```cpp
#include <iostream>

// Primary template
template <typename T>
void printValue(T value) {
    std::cout << "Value: " << value << std::endl;
}

// Specialized template for char*
template <>
void printValue<char*>(char* value) {
    std::cout << "String: " << value << std::endl;
}

int main() {
    printValue(42); // Calls primary template
    printValue("Hello, World!"); // Calls specialized template
    return 0;
}
```

### Example: Specializing a Class Template

```cpp
#include <iostream>

// Primary class template
template <typename T>
class Storage {
private:
    T value;
public:
    Storage(T v) : value(v) {}
    void display() { std::cout << "Value: " << value << std::endl; }
};

// Specialized class template for const char*
template <>
class Storage<const char*> {
private:
    const char* value;
public:
    Storage(const char* v) : value(v) {}
    void display() { std::cout << "String: " << value << std::endl; }
};

int main() {
    Storage<int> intStorage(42); // Uses primary template
    intStorage.display();

    Storage<const char*> strStorage("Hello, World!"); // Uses specialized template
    strStorage.display();

    return 0;
}
```

## 14.5 Template Metaprogramming

### What is Template Metaprogramming?

Template metaprogramming is a technique that allows you to perform computations at compile time using templates. This can be used to optimize code, generate code, or even implement complex algorithms.

### Example: Calculating Factorials at Compile Time

```cpp
#include <iostream>

// Template to calculate factorial at compile time
template <unsigned int n>
struct Factorial {
    enum { value = n * Factorial<n - 1>::value };
};

// Specialization for base case (n = 0)
template <>
struct Factorial<0> {
    enum { value = 1 };
};

int main() {
    std::cout << "Factorial of 5: " << Factorial<5>::value << std::endl;
    return 0;
}
```

## 14.6 Conclusion

In this chapter, we explored templates in C++. We discussed the basics of function templates and class templates, as well as advanced topics like template specialization and template metaprogramming. By using templates effectively, you can write more efficient, reusable, and flexible code.

In the next chapter, we will delve into the world of C++ Standard Library, focusing on containers, algorithms, and iterators.

### Exercises

1. Write a function template to swap two values of any type.
2. Implement a class template for a Stack that can store elements of any type.
3. Use template metaprogramming to calculate the sum of the first n natural numbers at compile time.

#### Additional Resources

For more information on templates in C++, refer to the following resources:

* The C++ Programming Language by Bjarne Stroustrup
* Effective C++ by Scott Meyers
* C++ Templates: The Complete Guide by David Vandevoorde and Nicolai M. Josuttis
* C++ Standard Library Tutorial by tutorialspoint.com

[Return to table of contents](TableOfContents.md)
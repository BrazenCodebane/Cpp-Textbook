
[Return to table of contents](TableOfContents.md)

# Chapter 7: Strings and String Manipulation

## Introduction

    In this chapter, we will explore one of the most fundamental data types in C++: strings. Strings are used to represent text and are essential for any program that deals with user input, output, or text processing. We will learn how to create, manipulate, and perform various operations on strings. By the end of this chapter, you will have a solid understanding of string handling in C++ and the tools available for string manipulation.

## 3.1 Understanding Strings in C++

### What is a String?

In C++, a string is a sequence of characters. The C++ Standard Library provides the `std::string` class, which offers a convenient way to work with strings, allowing for dynamic memory management and various built-in functions to manipulate text.

### Declaring and Initializing Strings

To use strings in C++, you must include the `<string>` header file. Here’s how to declare and initialize a string:

```cpp
#include <iostream>
#include <string>

int main() {
    std::string greeting = "Hello, World!"; // Declare and initialize a string
    std::cout << greeting << std::endl; // Output the string
    return 0;
}
```

## 3.2 Basic String Operations

### Concatenation

Concatenation is the process of joining two or more strings together. In C++, you can use the `+` operator to concatenate strings.

#### Example of Concatenation

```cpp
#include <iostream>
#include <string>

int main() {
    std::string firstName = "John";
    std::string lastName = "Doe";
    std::string fullName = firstName + " " + lastName; // Concatenate strings
    std::cout << "Full Name: " << fullName << std::endl; // Output the full name
    return 0;
}
```

### Length of a String

You can find the length of a string using the `.length()` or `.size()` method.

#### Example of Finding Length

```cpp
#include <iostream>
#include <string>

int main() {
    std::string text = "Hello, World!";
    std::cout << "Length of text: " << text.length() << std::endl; // Output the length
    return 0;
}
```

### Accessing Characters

You can access individual characters in a string using the subscript operator `[]`.

#### Example of Accessing Characters

```cpp
#include <iostream>
#include <string>

int main() {
    std::string message = "Hello";
    std::cout << "First character: " << message[0] << std::endl; // Output the first character
    return 0;
}
```

## 3.3 String Manipulation Functions

### Finding Substrings

You can find the position of a substring within a string using the `.find()` method.

#### Example of Finding a Substring

```cpp
#include <iostream>
#include <string>

int main() {
    std::string phrase = "Hello, World!";
    size_t position = phrase.find("World");
    if (position != std::string::npos) {
        std::cout << "'World' found at position: " << position << std::endl; // Output position
    } else {
        std::cout << "'World' not found." << std::endl;
    }
    return 0;
}
```

### Replacing Substrings

You can replace a substring within a string using the `.replace()` method.

#### Example of Replacing a Substring

```cpp
#include <iostream>
#include <string>

int main() {
    std::string text = "Hello, John!";
    text.replace(7, 4, "Doe"); // Replace "John" with "Doe"
    std::cout << text << std::endl; // Output the modified string
    return 0;
}
```

### String Comparison

You can compare strings using relational operators like `==`, `!=`, `<`, `>`, etc.

#### Example of String Comparison

```cpp
#include <iostream>
#include <string>

int main() {
    std::string str1 = "apple";
    std::string str2 = "banana";
    if (str1 < str2) {
        std::cout << str1 << " is less than " << str2 << std::endl; // Output comparison result
    }
    return 0;
}
```

## 3.4 User Input and Strings

### Getting User Input

You can read strings from the user using `std::cin`. Be cautious when reading strings with spaces, as `std::cin` will only read until the first space.

#### Example of Getting User Input

```cpp
#include <iostream>
#include <string>

int main() {
    std::string name;
    std::cout << "Enter your name: ";
    std::getline(std::cin, name); // Read entire line with spaces
    std::cout << "Hello, " << name << "!" << std::endl; // Output greeting
    return 0;
}
```

## 3.5 Conclusion

In this chapter, we explored the world of strings in C++. We learned how to declare, initialize, and manipulate strings using various built-in functions and operators. Understanding strings is crucial for any C++ programmer, as they are used extensively in real-world applications. With this knowledge, you can now create more sophisticated programs that interact with users and process text data.

In the next chapter, we will delve into control structures, including loops and conditional statements, which are essential for controlling the flow of your programs.

Exercises

1. Write a program that takes a string as input and outputs the string in uppercase.
2. Create a program that concatenates two strings and outputs the result.
3. Write a program that finds and outputs the position of a substring within a string.

Additional Resources

For more information on C++ strings, refer to the official C++ documentation or online resources like cppreference.com.
Practice writing C++ programs using online platforms like LeetCode, HackerRank, or CodeWars.

[Return to table of contents](TableOfContents.md)
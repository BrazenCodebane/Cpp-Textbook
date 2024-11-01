[Return to table of contents](TableOfContents.md)

# Chapter 2: Data Types
## Introduction
    In the previous chapter, we wrote our first C++ program and learned about variables. In this chapter, we will delve deeper into the types of data that can be stored in variables and the operators that can be used to manipulate this data. Understanding data types and operators is crucial for effective programming, as they form the building blocks for creating complex expressions and algorithms.

## 2.1 Data Types in C++
C++ supports several built-in data types, which can be broadly categorized into three groups: 
- fundamental types, 
- derived types, 
- user-defined types.

## 2.1.1 Fundamental Data Types
Fundamental data types are the basic types provided by C++. They include:

Integer Types: Used to store whole numbers.

int: Typically 4 bytes, can hold values from -2,147,483,648 to 2,147,483,647.
```cpp 
int variableName;
```

short: Typically 2 bytes, can hold smaller integer values.
```cpp 
short variableName;
```

long: Typically 4 or 8 bytes, can hold larger integer values.
```cpp 
long variableName;
```
long long: At least 8 bytes, for very large integers.
```cpp 
long long variableName;
```
Floating-Point Types: Used to store decimal numbers.
```cpp 
float long variableName;
```

double: Typically 8 bytes, double precision.
```cpp 
double variableName;
```
long double: Extended precision, size varies by implementation.
```cpp 
long double variableName;
```
Character Type: Used to store single characters.

character: Typically 1 byte, can hold a single character (e.g., 'A', 'b', '3').
```cpp 
char variableName;
```

Boolean Type: Used to store truth values. Can hold either true or false.

```cpp 
bool variableName;
```







Here’s an example that demonstrates various data types:




```cpp
#include <iostream>

int main() {
    int age = 25;                  // Integer
    float height = 5.9;           // Floating-point
    char initial = 'J';            // Character
    bool isStudent = true;         // Boolean

    std::cout << "Age: " << age << std::endl;
    std::cout << "Height: " << height << std::endl;
    std::cout << "Initial: " << initial << std::endl;
    std::cout << "Is Student: " << std::boolalpha << isStudent << std::endl;

    return 0;

}
```


[Return to table of contents](TableOfContents.md)
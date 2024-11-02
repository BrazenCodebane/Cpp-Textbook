
[Return to table of contents](TableOfContents.md)

# Chapter 8: Arrays and Vectors

## Introduction

In this chapter, we will explore two fundamental data structures in C++: arrays and vectors. Both are used to store collections of elements, but they have distinct characteristics and use cases. Understanding how to use arrays and vectors effectively is crucial for managing collections of data in your programs. By the end of this chapter, you will be able to declare, initialize, and manipulate both arrays and vectors.

## 8.1 Understanding Arrays

### What is an Array?

An array is a collection of elements of the same data type, stored in contiguous memory locations. Arrays provide a way to group related data together, making it easier to manage and manipulate.

### Declaring and Initializing Arrays

To declare an array in C++, you specify the data type, followed by the array name and its size in square brackets. Here’s how to declare and initialize an array:

```cpp
#include <iostream>

int main() {
    int numbers[5]; // Declare an array of integers with size 5
    // Initialize the array
    numbers[0] = 10;
    numbers[1] = 20;
    numbers[2] = 30;
    numbers[3] = 40;
    numbers[4] = 50;

    // Output the array elements
    for (int i = 0; i < 5; i++) {
        std::cout << "Element " << i << ": " << numbers[i] << std::endl;
    }
    return 0;
}
```

### Accessing Array Elements

You can access elements in an array using the subscript operator `[]`, where the index starts at 0.

#### Example of Accessing Array Elements

```cpp
#include <iostream>

int main() {
    int arr[3] = {1, 2, 3}; // Declare and initialize an array
    std::cout << "First element: " << arr[0] << std::endl; // Accessing the first element
    std::cout << "Second element: " << arr[1] << std::endl; // Accessing the second element
    return 0;
}
```

## 8.2 Multidimensional Arrays

C++ also supports multidimensional arrays, which are arrays of arrays. The most common type is the two-dimensional array, often used to represent matrices or grids.

### Declaring and Initializing a Two-Dimensional Array

To declare a two-dimensional array, specify the number of rows and columns.

#### Example of a Two-Dimensional Array

```cpp
#include <iostream>

int main() {
    int matrix[2][3] = { {1, 2, 3}, {4, 5, 6} }; // Declare and initialize a 2x3 matrix

    // Output the matrix elements
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            std::cout << "Element [" << i << "][" << j << "]: " << matrix[i][j] << std::endl;
        }
    }
    return 0;
}
```

## 8.3 Understanding Vectors

### What is a Vector?

A vector is a dynamic array provided by the C++ Standard Library. Unlike regular arrays, vectors can grow or shrink in size, making them more flexible for managing collections of data.

### Declaring and Initializing Vectors

To use vectors, you must include the `<vector>` header file. Here’s how to declare and initialize a vector:

```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> numbers; // Declare an empty vector of integers

    // Adding elements to the vector
    numbers.push_back(10);
    numbers.push_back(20);
    numbers.push_back(30);

    // Output the vector elements
    for (size_t i = 0; i < numbers.size(); i++) {
        std::cout << "Element " << i << ": " << numbers[i] << std::endl;
    }
    return 0;
}
```

### Accessing Vector Elements

You can access elements in a vector using the subscript operator `[]`, just like with arrays.

#### Example of Accessing Vector Elements

```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5}; // Declare and initialize a vector

    std::cout << "First element: " << vec[0] << std::endl; // Accessing the first element
    std::cout << "Second element: " << vec[1] << std::endl; // Accessing the second element
    return 0;
}
```

 ## 8.4 Vector Operations

### Resizing Vectors

You can resize a vector using the `.resize()` method.

#### Example of Resizing a Vector

```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> numbers = {1, 2, 3}; // Declare and initialize a vector
    numbers.resize(5); // Resize the vector to 5 elements

    // Output the vector elements
    for (size_t i = 0; i < numbers.size(); i++) {
        std::cout << "Element " << i << ": " << numbers[i] << std::endl;
    }
    return 0;
}
```

### Inserting and Erasing Elements

You can insert or erase elements in a vector using the `.insert()` and `.erase()` methods.

#### Example of Inserting and Erasing Elements

```cpp
#include <iostream>
#include <vector>

int main() {
    std::vector<int> numbers = {1, 2, 3, 4, 5}; // Declare and initialize a vector

    numbers.insert(numbers.begin() + 2, 10); // Insert an element at the 2nd position
    numbers.erase(numbers.begin() + 3); // Erase an element at the 3rd position

    // Output the vector elements
    for (size_t i = 0; i < numbers.size(); i++) {
        std::cout << "Element " << i << ": " << numbers[i] << std::endl;
    }
    return 0;
}
```

## 8.5 Conclusion

In this chapter, we explored the world of arrays and vectors in C++. We learned how to declare, initialize, and manipulate both arrays and vectors, as well as their differences and use cases. Understanding arrays and vectors is crucial for managing collections of data in your programs. With this knowledge, you can now create more sophisticated programs that effectively handle data.

In the next chapter, we will delve into control structures, including loops and conditional statements, which are essential for controlling the flow of your programs.

Exercises

1. Write a program that takes an array of integers as input and outputs the sum of its elements.
2. Create a program that initializes a two-dimensional array and outputs its elements.
3. Write a program that takes a vector of strings as input and outputs the concatenated string.

Additional Resources

For more information on C++ arrays and vectors, refer to the official C++ documentation or online resources like cppreference.com.
Practice writing C++ programs using online platforms like LeetCode, HackerRank, or CodeWars.

[Return to table of contents](TableOfContents.md)


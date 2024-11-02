
[Return to table of contents](TableOfContents.md)

# Chapter 12: File Input and Output

## Introduction

In this chapter, we will explore file input and output (I/O) in C++. File I/O is a critical aspect of programming that allows you to read from and write to files on the disk. This capability is essential for data persistence, allowing programs to save information between executions. By the end of this chapter, you will have a solid understanding of how to work with files in C++, including opening, reading, writing, and closing files.

## 12.1 File Streams

### What are File Streams?

In C++, file I/O is handled through the use of **streams**. A stream is an abstraction that represents a flow of data. There are two primary types of file streams:

1. **Input Stream**: Used for reading data from a file.
2. **Output Stream**: Used for writing data to a file.

To work with files, you will typically use the `fstream`, `ifstream`, and `ofstream` classes from the `<fstream>` header.

### Example

```cpp
#include <fstream> // Include fstream for file I/O
#include <iostream>

int main() {
    std::ifstream inputFile("input.txt"); // Create an input file stream
    std::ofstream outputFile("output.txt"); // Create an output file stream

    // Check if the input file is open
    if (!inputFile.is_open()) {
        std::cerr << "Error opening input file!" << std::endl;
        return 1;
    }

    // Check if the output file is open
    if (!outputFile.is_open()) {
        std::cerr << "Error opening output file!" << std::endl;
        return 1;
    }

    // File operations will go here

    inputFile.close(); // Close the input file
    outputFile.close(); // Close the output file
    return 0;
}
```

## 12.2 Reading from Files

### Using `ifstream`

To read data from a file, you will use the `ifstream` class. You can read data line by line or word by word, depending on your needs.

### Example: Reading Line by Line

```cpp
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ifstream inputFile("input.txt");
    std::string line;

    if (!inputFile.is_open()) {
        std::cerr << "Error opening input file!" << std::endl;
        return 1;
    }

    while (std::getline(inputFile, line)) { // Read line by line
        std::cout << line << std::endl; // Output the line to the console
    }

    inputFile.close();
    return 0;
}
```

### Example: Reading Word by Word

```cpp
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ifstream inputFile("input.txt");
    std::string word;

    if (!inputFile.is_open()) {
        std::cerr << "Error opening input file!" << std::endl;
        return 1;
    }

    while (inputFile >> word) { // Read word by word
        std::cout << word << std::endl; // Output the word to the console
    }

    inputFile.close();
    return 0;
}
```

## 12.3 Writing to Files

### Using `ofstream`

To write data to a file, you will use the `ofstream` class. You can write data in various formats, including plain text and formatted output.

### Example: Writing to a File

```cpp
#include <fstream>
#include <iostream>

int main() {
    std::ofstream outputFile("output.txt");

    if (!outputFile.is_open()) {
        std::cerr << "Error opening output file!" << std::endl;
        return 1;
    }

    outputFile << "Hello, World!" << std::endl; // Write a line to the file
    outputFile << "This is a sample output file." << std::endl; // Write another line

    outputFile.close();
    return 0;
}
```

### Example: Writing Formatted Output

```cpp
#include <fstream>
#include <iostream>
#include <iomanip>

int main() {
    std::ofstream outputFile("output.txt");

    if (!outputFile.is_open()) {
        std::cerr << "Error opening output file!" << std::endl;
        return 1;
    }

    outputFile << std::fixed << std::setprecision(2); // Set fixed format and precision
    outputFile << "Value: " << 123.456789 << std::endl; // Write formatted output

    outputFile.close();
    return 0;
}
```

## 12.4 Error Handling

### Checking File Operations

It is crucial to handle potential errors when working with files. You can check the state of the file stream using the `is_open()` method.

### Example: Error Handling

```cpp
#include <fstream>
#include <iostream>

int main() {
    std::ifstream inputFile("input.txt");

    if (!inputFile.is_open()) {
        std::cerr << "Error opening input file!" << std::endl;
        return 1;
    }

    // File operations will go here

    inputFile.close();
    return 0;
}
```

## 12.5 Conclusion

In this chapter, we explored file input and output in C++. We discussed the importance of file I/O, introduced file streams, and demonstrated how to read from and write to files using `ifstream` and `ofstream`. Additionally, we covered error handling techniques to ensure robust file operations.

In the next chapter, we will delve into exception handling in C++, focusing on how to handle runtime errors and exceptions.

### Exercises

1. Write a program that reads from a file and writes the contents to another file.
2. Modify the previous program to handle errors when reading from or writing to the files.
3. Create a program that reads from a file, processes the data, and writes the results to another file.

#### Additional Resources

For more information on file I/O and error handling in C++, refer to the following resources:

* The C++ Programming Language by Bjarne Stroustrup
* Effective C++ by Scott Meyers
* C++ Standard Library Tutorial by tutorialspoint.com

[Return to table of contents](TableOfContents.md)
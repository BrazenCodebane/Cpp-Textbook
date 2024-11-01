[Return to table of contents](TableOfContents.md)

# Loops

## Introduction
    Loops are fundamental constructs in programming that allow you to execute a block of code multiple times, based on a specified condition. In C++, there are three primary types of loops: for, while, and do while. Each type serves different purposes and is suitable for various scenarios. This chapter will explore each of these loops, their syntax, and practical examples.

## 5.1 The for Loop
The for loop is typically used when the number of iterations is known beforehand. It consists of three parts: initialization, condition, and increment/decrement.

Syntax
```cpp
for (initialization; condition; increment/decrement) {
    // Code to be executed in each iteration
}
```

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    // Print numbers from 1 to 5
    for (int i = 1; i <= 5; i++) {
        cout << "Number: " << i << endl;
    }

    return 0;
}

```

In this example, the loop initializes the variable i to 1, checks if i is less than or equal to 5, and increments i by 1 after each iteration. The loop will print the numbers from 1 to 5.

## 5.1.1 Nested for Loops
You can also nest for loops within each other. This is commonly used for working with multi-dimensional arrays or performing complex iterations.

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 3; i++) {
        for (int j = 1; j <= 2; j++) {
            cout << "i: " << i << ", j: " << j << endl;
        }
    }

    return 0;
}
```

This code will produce a combination of i and j values, demonstrating how nested loops work.

## 5.2 The while Loop
The while loop is used when the number of iterations is not known ahead of time and depends on a condition. The loop continues as long as the specified condition is true.

Syntax
```cpp
while (condition) {
    // Code to be executed as long as the condition is true
}
```

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    int count = 1;

    // Print numbers from 1 to 5 using a while loop
    while (count <= 5) {
        cout << "Count: " << count << endl;
        count++; // Increment the count
    }

    return 0;
}
```

In this example, the loop continues to execute as long as count is less than or equal to 5. The value of count is incremented in each iteration.

## 5.2.1 Infinite Loops
Be cautious with while loops, as they can lead to infinite loops if the condition never becomes false. Always ensure that the loop will eventually terminate.

Example of an Infinite Loop

```cpp
#include <iostream>
using namespace std;

int main() {
    int count = 1;

    // This will create an infinite loop
    while (count <= 5) {
        cout << "Count: " << count << endl;
        // Missing count++ will cause an infinite loop
    }

    return 0;
}
```

## 5.3 The do while Loop
The do while loop is similar to the while loop but guarantees that the code block will execute at least once, as the condition is checked after the execution of the loop body.

Syntax
```cpp
do {
    // Code to be executed
} while (condition);
```

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    int count = 1;

    // Print numbers from 1 to 5 using a do while loop
    do {
        cout << "Count: " << count << endl;
        count++; // Increment the count
    } while (count <= 5);

    return 0;
}
```

In this example, the loop will execute and print the value of count before checking the condition. Even if the initial value of count were greater than 5, the loop would still execute once.

## 5.4 Loop Control Statements
C++ provides several control statements that can alter the flow of loops:

### 5.4.1 break
The break statement is used to exit a loop prematurely.

Example
```cpp

#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        if ( i == 5) {
            break; // Exit the loop when i reaches 5
        }
        cout << "Number: " << i << endl;
    }

    return 0;
}
```

In this example, the loop will stop when i reaches 5.

### 5.4.2 continue
The continue statement skips the current iteration and moves to the next one.

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        if (i == 5) {
            continue; // Skip the current iteration when i is 5
        }
        cout << "Number: " << i << endl;
    }

    return 0;
}
```

In this example, the loop will skip printing the number 5.

### 5.4.3 return
The return statement can be used to exit a function and terminate the loop.

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        if (i == 5) {
            return 0; // Exit the function and terminate the loop
        }
        cout << "Number: " << i << endl;
    }

    return 0;
}
```
In this example, the function will exit and the loop will terminate when i reaches 5.


## Conclussion

By mastering these loop constructs and control statements, you'll be able to write more efficient and effective C++ programs.








[Return to table of contents](TableOfContents.md)
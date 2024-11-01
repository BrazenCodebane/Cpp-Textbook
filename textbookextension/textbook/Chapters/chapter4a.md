
[Return to table of contents](TableOfContents.md)

# If/else if/else  || switch

## Introduction
    In programming, making decisions is a fundamental aspect of controlling the flow of execution. C++ provides several mechanisms for making decisions, the most common being the if, else if, else statements and the switch statement. This chapter will explore these constructs in detail, including their syntax, use cases, and best practices.

## 4.1 The if Statement
The if statement is the simplest form of decision-making in C++. It allows you to execute a block of code only if a specified condition evaluates to true.

##Syntax
```cpp
if (condition) {
    // Code to be executed if the condition is true
}
```

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Enter a number: ";
    cin >> number;

    if (number > 0) {
        cout << "The number is positive." << endl;
    }

    return 0;
}

```

In this example, the message "The number is positive." will only be displayed if the user inputs a positive number.

## 4.2 The else Statement
The else statement can be used in conjunction with the if statement to provide an alternative block of code that executes when the condition is false.

Syntax
```cpp
if (condition) {
    // Code to be executed if the condition is true
} else {
    // Code to be executed if the condition is false
}

```
Example

```cpp
#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Enter a number: ";
    cin >> number;

    if (number > 0) {
        cout << "The number is positive." << endl;
    } else {
        cout << "The number is not positive." << endl;
    }

    return 0;
}
```

In this case, if the number is not positive, the program will output "The number is not positive."

## 4.3 The else if Statement
When you have multiple conditions to evaluate, you can use else if to check additional conditions if the previous ones are false.

Syntax
```cpp
if (condition1) {
    // Code to be executed if condition1 is true
} else if (condition2) {
    // Code to be executed if condition2 is true
} else {
    // Code to be executed if none of the conditions are true
}

```

Example

```cpp

#include <iostream>
using namespace std;

int main() {
    int number;
    cout << "Enter a number: ";
    cin >> number;

    if (number > 0) {
        cout << "The number is positive." << endl;
    } else if (number < 0) {
        cout << "The number is negative." << endl;
    } else {
        cout << "The number is zero." << endl;
    }

    return 0;
}

```
Here, the program checks if the number is positive, negative, or zero, providing an appropriate message for each case.

## 4.4 The switch Statement
The switch statement is another control structure that allows you to execute one block of code among many based on the value of a variable or expression. It is particularly useful when you have multiple discrete values to check against.

Syntax
```cpp
switch (expression) {
    case value1:
        // Code to be executed if expression == value1
        break;
    case value2:
        // Code to be executed if expression == value2
        break;
    // You can have any number of case statements.
    default:
        // Code to be executed if expression doesn't match any case
}
```

Example
```cpp
#include <iostream>
using namespace std;

int main() {
    int day;
    cout << "Enter a day number (1-7): ";
    cin >> day;

    switch (day) {
        case 1:
            cout << "Monday" << endl;
            break;
        case 2:
            cout << "Tuesday" << endl;
            break;
        case 3:
            cout << "Wednesday" << endl;
            break;
        case 4:
            cout << "Thursday" << endl;
            break;
        case 5:
            cout << "Friday" << endl;
            break;
        case 6:
            cout << "Saturday" << endl;
            break;
        case 7:
            cout << "Sunday" << endl;
            break;
        default:
            cout << "Invalid day number." << endl;
    }

    return 0;
}
```

In this example, the program outputs the name of the day corresponding to the number entered by the user. If the input is not between 1 and 7, the program displays "Invalid day number."

[Return to table of contents](TableOfContents.md)
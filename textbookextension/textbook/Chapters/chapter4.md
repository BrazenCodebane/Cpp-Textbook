[Return to table of contents](TableOfContents.md)

# Chapter 4: Control Flow Statements
## Introduction
    In this chapter, we will discuss control flow statements in C++. Control flow statements are essential tools that help determine the order in which different parts of a program are executed. They allow you to make decisions, repeat actions, and manage how your program behaves based on certain conditions. Understanding control flow is crucial for writing effective and functional programs. We will cover three main types of control flow statements: conditional statements, loops, and branching statements.

## 4.1 Conditional Statements
Conditional statements allow a program to execute specific sections of code based on whether a condition is true or false. The most common types of conditional statements are:

### `If` Statement:
 This statement checks a condition and executes a block of code if the condition is true. For example, if a user enters a number, the program can check if that number is positive and respond accordingly.

### `Else` Statement: 
This statement follows an if statement and executes a block of code if the condition in the if statement is false. For instance, if the number is not positive, the program can indicate that the number is either negative or zero.

### `Else If` Statement:
 This statement allows you to check multiple conditions in sequence. You can use it to evaluate several possibilities. For example, if the number is greater than zero, the program can say it is positive; if it is less than zero, it can say it is negative; and if it is zero, it can indicate that as well.

## 4.2 Loops
Loops are control flow statements that allow a program to execute a block of code multiple times based on a condition. There are several types of loops:

### `For` Loop:
 This type of loop is used when you know in advance how many times you want to repeat a block of code. For example, if you want to print numbers from 1 to 5, you can set up a loop that runs exactly five times.

### `While` Loop:
 This loop continues to execute as long as a specified condition is true. For instance, you can use a while loop to keep asking a user for input until they provide a valid response.

### `Do While` Loop:
 This loop is similar to the while loop, but it guarantees that the code will run at least once before checking the condition. For example, you might want to display a menu to the user and ensure they see it before asking for their choice.

## 4.3 Branching Statements
Branching statements allow you to change the flow of control in a program. The most common branching statements are:

### `Break` Statement:
 This statement is used to exit a loop or switch statement prematurely. For example, if you are searching for a specific item in a list and find it, you can use a break statement to stop searching further.

### `Continue` Statement:
 This statement skips the current iteration of a loop and moves to the next iteration. For instance, if you are processing a list of numbers and want to skip any negative numbers, you can use a continue statement to move on to the next number without processing the negative one.

### `Return` Statement:
 This statement is used to exit a function and can also return a value to the part of the program that called the function. For example, if a function calculates the sum of two numbers, it can use a return statement to send that sum back to the main part of the program.

## Conclusion
Control flow statements are fundamental to programming in C++. They allow you to make decisions, repeat actions, and manage how your program behaves based on different conditions. By mastering these statements, you will be able to write more complex and functional programs that can respond dynamically to user input and other conditions. In the next chapter, we will explore functions, which are essential for organizing and reusing code in your programs.

[Return to table of contents](TableOfContents.md)
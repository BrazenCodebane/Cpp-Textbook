
[Return to table of contents](TableOfContents.md)

# Chapter 10: OOP Concepts

## Introduction

    In this chapter, we will explore the fundamental concepts of Object-Oriented Programming (OOP) in C++. OOP is a programming paradigm that uses "objects" to represent data and methods to manipulate that data. The four main principles of OOP are encapsulation, inheritance, polymorphism, and abstraction. By the end of this chapter, you will have a solid understanding of these concepts and how they can be applied in C++ programming.

## 10.1 Encapsulation

### What is Encapsulation?

Encapsulation is the bundling of data and methods that operate on that data within a single unit, typically a class. This helps restrict direct access to some of the object's components, which can prevent unintended interference and misuse.

### Example of Encapsulation

```cpp
#include <iostream>

class BankAccount {
private:
    double balance; // Private member variable

public:
    BankAccount(double initialBalance) : balance(initialBalance) {} // Constructor

    void deposit(double amount) {
        balance += amount; // Method to deposit money
    }

    void withdraw(double amount) {
        if (amount <= balance) {
            balance -= amount; // Method to withdraw money
        } else {
            std::cout << "Insufficient funds!" << std::endl;
        }
    }

    double getBalance() const { // Method to get the current balance
        return balance;
    }
};

int main() {
    BankAccount account(100.0); // Create a BankAccount object
    account.deposit(50.0); // Deposit money
    account.withdraw(30.0); // Withdraw money
    std::cout << "Current balance: $" << account.getBalance() << std::endl; // Output balance
    return 0;
}
```

## 10.2 Inheritance

### What is Inheritance?

Inheritance allows a class (derived class) to inherit properties and methods from another class (base class). This promotes code reusability and establishes a hierarchical relationship between classes.

### Example of Inheritance

```cpp
#include <iostream>

class Animal {
public:
    void speak() {
        std::cout << "Animal speaks!" << std::endl;
    }
};

class Dog : public Animal { // Dog inherits from Animal
public:
    void bark() {
        std::cout << "Dog barks!" << std::endl;
    }
};

int main() {
    Dog dog;
    dog.speak(); // Call inherited method
    dog.bark();  // Call Dog's method
    return 0;
}
```

## 10.3 Polymorphism

### What is Polymorphism?

Polymorphism allows methods to do different things based on the object that it is acting upon. This can be achieved through function overloading and method overriding.

### Example of Polymorphism

```cpp
#include <iostream>

class Shape {
public:
    virtual void draw() { // Virtual function
        std::cout << "Drawing a shape!" << std::endl;
    }
};

class Circle : public Shape {
public:
    void draw() override { // Override base class method
        std::cout << "Drawing a circle!" << std::endl;
    }
};

int main() {
    Shape* shape = new Circle(); // Create a Circle object
    shape->draw(); // Calls Circle's draw method
    delete shape; // Clean up
    return 0;
}
```

## 10.4 Abstraction

### What is Abstraction?

Abstraction is the concept of hiding the complex implementation details of a system and exposing only the necessary parts. This can be achieved through abstract classes and interfaces.

### Example of Abstraction

```cpp
#include <iostream>

class AbstractShape {
public:
    virtual void draw() = 0; // Pure virtual function
};

class Rectangle : public AbstractShape {
public:
    void draw() override {
        std::cout << "Drawing a rectangle!" << std::endl;
    }
};

int main() {
    AbstractShape* shape = new Rectangle(); // Create a Rectangle object
    shape->draw(); // Calls Rectangle's draw method
    delete shape; // Clean up
    return 0;
}
```

## 10.5 Conclusion

In this chapter, we introduced the fundamental concepts of Object-Oriented Programming in C++. Understanding OOP principles such as encapsulation, inheritance, polymorphism, and abstraction is essential for writing maintainable and reusable code. With this knowledge, you can now create more complex and organized programs.

In the next chapter, we will delve deeper into classes, focusing on their structure, functionality, and best practices.

### Exercises

1. Create a class that represents a simple geometric shape and implement methods for calculating its area and perimeter.
2. Write a program that demonstrates inheritance by creating a base class and derived classes for different types of vehicles.
3. Implement a simple calculator using polymorphism to handle different mathematical operations.

Additional Resources

For more information on C++ OOP concepts, refer to the official C++ documentation or online resources like cppreference.com.
Practice writing C++ programs using online platforms like LeetCode, HackerRank, or CodeWars.

[Return to table of contents](TableOfContents.md)



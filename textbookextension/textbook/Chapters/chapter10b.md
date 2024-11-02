
[Return to table of contents](TableOfContents.md)

# Chapter 10b: Class Member Access Specifiers

## Introduction

    In this chapter, we will explore class member access specifiers in C++. Access specifiers are essential for controlling the visibility and accessibility of class members (both variables and functions) from outside the class. Understanding how to use access specifiers effectively is crucial for implementing encapsulation, which is one of the core principles of Object-Oriented Programming (OOP). By the end of this chapter, you will have a clear understanding of the three main access specifiers: public, private, and protected, along with their usage and implications.

## 10b.1 Public Access Specifier

### What is Public Access?

Members declared under the `public` access specifier are accessible from anywhere in the program where the object of the class is visible. This means that other functions and classes can access these members directly.

### Example of Public Access

```cpp
#include <iostream>

class MyClass {
public:
    int publicVar; // Public member variable

    void publicMethod() { // Public member function
        std::cout << "Public Method Called!" << std::endl;
    }
};

int main() {
    MyClass obj; // Create an object of MyClass
    obj.publicVar = 5; // Access public member variable
    std::cout << "Public Variable: " << obj.publicVar << std::endl; // Output: 5
    obj.publicMethod(); // Call public member function
    return 0;
}
```

## 10b.2 Private Access Specifier

### What is Private Access?

Members declared under the `private` access specifier are not accessible from outside the class. They can only be accessed by member functions of the same class or by friends of the class (if any are declared). This promotes encapsulation by hiding the internal state and implementation details from outside interference.

### Example of Private Access

```cpp
#include <iostream>

class MyClass {
private:
    int privateVar; // Private member variable

public:
    MyClass(int value) : privateVar(value) {} // Constructor

    void display() { // Public member function to access private member
        std::cout << "Private Variable: " << privateVar << std::endl;
    }
};

int main() {
    MyClass obj(10); // Create an object of MyClass
    // obj.privateVar = 20; // Error: privateVar is not accessible
    obj.display(); // Call public method to display private variable
    return 0;
}
```

## 10b.3 Protected Access Specifier

### What is Protected Access?

Members declared under the `protected` access specifier are accessible within the class itself and by derived classes (subclasses), but not from outside the class. This is useful in inheritance scenarios where you want to allow derived classes to access certain members of the base class while still keeping them hidden from the rest of the program.

### Example of Protected Access

```cpp
#include <iostream>

class Base {
protected:
    int protectedVar; // Protected member variable

public:
    Base(int value) : protectedVar(value) {} // Constructor
};

class Derived : public Base {
public:
    void display() { // Public method in derived class
        std::cout << "Protected Variable: " << protectedVar << std::endl; // Access protected member
    }
};

int main() {
    Derived obj(20); // Create an object of Derived class
    obj.display(); // Call method to display protected variable
    // std::cout << obj.protectedVar; // Error: protectedVar is not accessible outside the class
    return 0;
}
```

## 10b.4 Summary of Access Specifiers

| Access Specifier | Accessibility                                 |
|-------------------|----------------------------------------------|
| `public`          | Accessible from anywhere in the program     |
| `private`         | Accessible only within the class             |
| `protected`       | Accessible within the class and derived classes |

## 10b.5 Conclusion

In this chapter, we examined the three main access specifiers in C++: public, private, and protected. Understanding how to use these access specifiers effectively is crucial for implementing encapsulation and ensuring that your classes maintain a clear and controlled interface. By using access specifiers, you can protect the internal state of your objects and control how they interact with other parts of your program.

In the next chapter, we will explore operator overloading, which allows us to redefine the behavior of operators when working with user-defined data types.

### Exercises

1. Create a class with a mix of public, private, and protected members. Implement methods to demonstrate their accessibility.
2. Write a program that uses inheritance to show how protected members can be accessed in derived classes.
3. Implement a class with private members and provide public methods to manipulate those members.

#### Additional Resources

For more information on access specifiers and encapsulation, refer to the following resources:

* The C++ Programming Language by Bjarne Stroustrup
* C++ Tutorial by tutorialspoint.com
* C++ Documentation by cppreference.com


[Return to table of contents](TableOfContents.md)
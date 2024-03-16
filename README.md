# C++ Lab HW1

## 1. What is the meaning of object-oriented programming (OOP)? Write only the name of four
key concepts of (OOP). 
Four key concepts of OOP are:
1. Encapsulation
2. Inheritance
3. Polymorphism
4. Readability and maintainability

## 2. What are the preprocessor and namespace?
- **Preprocessor**: Processes code before compilation, handling directives like `#include` and `#define`.
- **Namespace**: Groups entities under a name to avoid conflicts, allowing for same-named functions in different contexts.

## 3. Explain the concept of inheritance in OOP.
Inheritance in OOP allows a class to inherit attributes and methods from another class, enabling code reuse and creating a hierarchical organization of classes. The class that inherits is called the child or subclass, while the class being inherited from is the parent or superclass.

## 4. Write a program to calculate the factorial of 10 using recursion.
```cpp
#include <iostream>

int calculate(int result, int i){
    if (i == 11){
        return result;
    }
    result = result * i;
    return calculate(result, i+1);
}


int main() {
    int result = 1;
    int i = 1;
    std::cout << calculate(result, i);

    return 0;
}
```

## 5. Explain the 5 main Control Statements in C++.
1. **If Statement**: Allows conditional execution of a block of code. If the condition is true, the code block is executed; otherwise, it is skipped.

2. **Switch Statement**: Used for multi-way branching. Based on the value of an expression, the control is transferred to a matching case label. If no case matches, an optional default case may be executed.

3. **For Loop**: Allows repetitive execution of a block of code a specific number of times. It initializes a loop control variable, checks a condition, and modifies the loop control variable in each iteration.

4. **While Loop**: Executes a block of code repeatedly as long as a given condition is true. The condition is checked before the execution of the loop’s body.

5. **Do-While Loop**: Similar to the while loop, but the condition is checked after the execution of the loop’s body. This ensures that the loop’s body is executed at least once.

## 6. Explain the three main Logic operators in C++.
1. **Logical AND (`&&`)**: Returns `true` if both operands are true; otherwise, returns `false`.

2. **Logical OR (`||`)**: Returns `true` if at least one of the operands is true; otherwise, returns `false`.

3. **Logical NOT (`!`)**: Returns `true` if the operand is false; otherwise, returns `false`.

## 7. What are nested loops? Write a program to print the series: (1, 1) (1, 2) (1, 3), (2, 1) (2, 2) (2,
3), and (3, 1) (3, 2) (3, 3).
Nested loops are loops within loops. They allow you to perform complex iterations where each loop may depend on the counters of the outer loops.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i=1; i<4; i++){
        for (int j=1; j<4; j++){
            cout << "(" << i << ", " << j << ")" <<endl;
        }
    }

    return 0;
}
```

## 8. What class in C++. What are the two primary components of a class?
1. Attributes or Properties

2. Methods or Functions

## 9. What is object? Also explain Access specifiers:
An **object** is an instance of a class, containing data and methods to manipulate that data.

**Access Specifiers** control access to class members:

- **Public**: Accessible from anywhere.
- **Protected**: Accessible in the class and by derived classes.
- **Private**: Accessible only within the class.

## 10. What are Instance and static variables?
- **Instance variables**: Unique to each object instance.
- **Static variables**: Shared across all instances of a class.

## 11. What is a function, and why is it used in programming? Write a program to call a function for adding two numbers.
```cpp
#include <iostream>

// Function declaration
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(5, 3); // Function call
    std::cout << "The sum is: " << result << std::endl;
    return 0;
}
```

## 12. What are the Constructors and Destructors? As program to call the constructor and destructor.
**Constructors** initialize objects when created. **Destructors** clean up resources when objects are destroyed.

```cpp
#include <iostream>
using namespace std;

class Demo {
public:
    Demo() { // Constructor
        cout << "Constructor called." << endl;
    }
    ~Demo() { // Destructor
        cout << "Destructor called." << endl;
    }
};

int main() {
    Demo obj;
    return 0;
}
```

## 13
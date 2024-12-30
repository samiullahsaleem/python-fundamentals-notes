# Python Notes

Welcome to the **Python Fundamentals Notes** repository! This repository contains comprehensive notes covering the basics of Python programming, intended for beginners and intermediate learners. The notes include explanations, examples, and exercises to solidify your understanding.

## Table of Contents

1. [Introduction to Python](https://github.com/samiullahsaleem/python-notes?tab=readme-ov-file#introduction-to-python)
2. [Data Types and Variables](https://github.com/samiullahsaleem/python-notes?tab=readme-ov-file#2-data-types-and-variables)
3. [Control Flow Statements](https://github.com/samiullahsaleem/python-notes?tab=readme-ov-file#control-flow-statements)
4. [Functions](#4-functions)
5. [Object-Oriented Programming (OOP)](#5-object-oriented-programming-oop)
6. [Modules and Libraries](#6-modules-and-libraries)
7. [File Handling](#7-file-handling)
8. [Error and Exception Handling](#8-error-and-exception-handling)
9. [Python Best Practices](#9-python-best-practices)
10. [Additional Resources](#10-additional-resources)

## 1. Introduction to Python

### What is Python?
Python is a versatile, high-level, and interpreted programming language that emphasizes code readability and simplicity. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming. Python is widely used in web development, data analysis, artificial intelligence, scientific computing, and more.

### Why Choose Python?
- **Ease of Learning**: Python has a simple syntax similar to English, making it beginner-friendly.
- **Versatility**: From web development to machine learning, Python can handle a variety of tasks.
- **Extensive Libraries**: Python boasts a rich ecosystem of libraries and frameworks, such as NumPy, Pandas, Django, and Flask.

### Writing Your First Python Program
```python
# This is a simple Python program
print("Hello, World!")
```
- Use the `print()` function to display output in the console.

---

## 2. Data Types and Variables

### What are Variables?
Variables are containers used to store data values. In Python, variables are dynamically typed, meaning you don’t need to specify the type of variable explicitly—it is inferred based on the value assigned.

### Characteristics of Variables in Python
1. **Dynamic Typing**: You can assign different types of values to the same variable.
2. **Case Sensitivity**: Variable names are case-sensitive (e.g., `name` and `Name` are different).
3. **No Declaration Required**: Python does not require variable declaration before usage.

### Variable Naming Rules
- Must start with a letter or an underscore (_).
- Cannot start with a number.
- Can contain alphanumeric characters and underscores.
- Cannot use reserved keywords (e.g., `if`, `else`, `while`).

### Declaring Variables
```python
x = 10       # Integer
name = "Alice"  # String
pi = 3.14    # Float
is_valid = True  # Boolean
```

### Built-in Data Types in Python
Python offers several built-in data types, categorized as follows:

#### 1. Numeric Types
- **int**: Integer values (e.g., 10, -5)
- **float**: Decimal values (e.g., 3.14, -0.001)
- **complex**: Complex numbers with a real and imaginary part (e.g., 1+2j)

```python
integer_value = 42       # int
float_value = 3.1415     # float
complex_value = 2 + 3j   # complex
```

#### 2. Text Type
- **str**: Sequence of characters (e.g., "Hello, World!")

```python
text = "Python is powerful"
```

#### 3. Boolean Type
- **bool**: Represents True or False values

```python
is_active = True
is_closed = False
```

#### 4. Sequence Types
- **list**: Ordered, mutable collection of items (e.g., [1, 2, 3])
- **tuple**: Ordered, immutable collection of items (e.g., (1, 2, 3))
- **range**: Sequence of numbers generated using `range()`

```python
list_example = [1, 2, 3, 4]
tuple_example = (1, 2, 3, 4)
range_example = range(5)  # 0, 1, 2, 3, 4
```

#### 5. Set Types
- **set**: Unordered collection of unique items (e.g., {1, 2, 3})
- **frozenset**: Immutable version of a set

```python
set_example = {1, 2, 3, 4}
frozenset_example = frozenset([1, 2, 3, 4])
```

#### 6. Mapping Type
- **dict**: Key-value pairs (e.g., {"key": "value"})

```python
dict_example = {"name": "Alice", "age": 25}
```

### Type Checking
You can check the type of a variable using the `type()` function.
```python
x = 10
print(type(x))  # Output: <class 'int'>
```

### Type Conversion
Python allows explicit conversion between data types using functions like `int()`, `float()`, `str()`, etc.

#### Examples:
```python
# Convert int to float
x = 10
x_float = float(x)  # 10.0

# Convert float to int
y = 3.14
y_int = int(y)  # 3

# Convert int to string
z = 42
z_str = str(z)  # "42"

# Convert list to tuple
list_example = [1, 2, 3]
tuple_example = tuple(list_example)  # (1, 2, 3)
```

### Mutable vs Immutable Data Types
- **Mutable**: Can be changed after creation (e.g., `list`, `dict`, `set`).
- **Immutable**: Cannot be changed after creation (e.g., `int`, `float`, `tuple`, `str`).

```python
# Mutable example
my_list = [1, 2, 3]
my_list.append(4)  # Now my_list is [1, 2, 3, 4]

# Immutable example
my_tuple = (1, 2, 3)
# my_tuple[0] = 4  # This will raise an error
```

### Special Data Types
- **NoneType**: Represents the absence of a value, denoted by `None`.

```python
x = None
print(type(x))  # Output: <class 'NoneType'>
```

### Advanced Data Structures
Python also offers advanced structures like `collections` and `dataclasses` for specialized use cases.

---

## 3. Control Flow Statements
Conditional statements are used to execute a block of code only when a specific condition is met. The main keywords are `if`, `elif`, and `else`.

### Syntax
```python
if condition:
    # Code block executed if the condition is True
elif another_condition:
    # Code block executed if the previous condition is False and this condition is True
else:
    # Code block executed if all previous conditions are False
```

### Example
```python
x = 10
if x > 0:
    print("Positive number")
elif x == 0:
    print("Zero")
else:
    print("Negative number")
```

### Nested Conditions
You can nest conditions within one another to handle complex scenarios.
```python
x = 10
y = 5
if x > 0:
    if y > 0:
        print("Both x and y are positive")
    else:
        print("x is positive but y is not")
```

---

## Loops

Loops are used to repeat a block of code multiple times. Python provides two main types of loops: `for` and `while`.

### a. For Loop
The `for` loop iterates over a sequence (like a list, tuple, or range).

#### Syntax
```python
for variable in sequence:
    # Code block executed for each item in the sequence
```

#### Example
```python
for i in range(5):
    print(i)  # Prints numbers from 0 to 4
```

#### Iterating Over a List
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### b. While Loop
The `while` loop repeats as long as the given condition is `True`.

#### Syntax
```python
while condition:
    # Code block executed as long as the condition is True
```

#### Example
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

---

## Loop Control Statements

Loop control statements alter the execution flow within a loop. Python supports the following:

### a. Break Statement
The `break` statement exits the loop immediately.
```python
for i in range(10):
    if i == 5:
        break  # Exits the loop when i is 5
    print(i)
```

### b. Continue Statement
The `continue` statement skips the current iteration and moves to the next one.
```python
for i in range(10):
    if i % 2 == 0:
        continue  # Skips even numbers
    print(i)
```

### c. Pass Statement
The `pass` statement acts as a placeholder and does nothing.
```python
for i in range(5):
    if i == 3:
        pass  # Placeholder for future code
    print(i)
```

---

## Control Flow with Exception Handling
Exception handling influences the program’s control flow by directing it to specific blocks (`except`, `else`, `finally`) depending on whether an error occurs.

### Key Concepts:
1. **`try` block**: Contains code that may raise exceptions.
2. **`except` block**: Executes when a specific exception is raised.
3. **`else` block**: Executes only if no exceptions occur.
4. **`finally` block**: Always executes, regardless of whether an exception occurred.

### Multiple Exceptions
You can handle different exceptions using multiple `except` blocks.
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("Invalid input! Please enter a valid number.")
except ZeroDivisionError:
    print("Division by zero is not allowed.")
else:
    print(f"Result: {result}")
finally:
    print("Operation completed.")
```

### Catch-All Exceptions
To catch any exception, use a generic `except` block.
```python
try:
    # Risky operation
except Exception as e:
    print(f"An error occurred: {e}")
```

## Raising Exceptions
You can raise exceptions explicitly using the `raise` keyword.
```python
x = -5
if x < 0:
    raise ValueError("Negative value not allowed!")
```

## Nested `try-except` Blocks
Handle exceptions separately for different segments of code using nested blocks.
```python
try:
    x = int(input("Enter numerator: "))
    try:
        y = int(input("Enter denominator: "))
        print(x / y)
    except ZeroDivisionError:
        print("Cannot divide by zero!")
except ValueError:
    print("Invalid input! Please enter numeric values.")
```

## Exception Hierarchy
Exceptions in Python follow a hierarchical structure:
- BaseException
  - Exception
    - ArithmeticError
      - ZeroDivisionError
      - OverflowError
    - ValueError
    - KeyError
    - IndexError

### Example:
```python
try:
    my_list = [1, 2, 3]
    print(my_list[5])
except IndexError:
    print("Index out of range!")
```

## Custom Exceptions
Define your own exceptions by creating a class that inherits from `Exception`.
```python
class NegativeValueError(Exception):
    pass

try:
    num = int(input("Enter a positive number: "))
    if num < 0:
        raise NegativeValueError("Negative numbers are not allowed!")
except NegativeValueError as e:
    print(e)
```

## Exception Handling in Loops
Use exception handling to manage errors within loops.
```python
for i in range(5):
    try:
        num = int(input(f"Enter a number for iteration {i+1}: "))
        print(f"Square: {num ** 2}")
    except ValueError:
        print("Invalid input, skipping this iteration.")
```

## Practical Examples
### File Handling with Exceptions
```python
try:
    with open("nonexistent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("File not found! Please check the filename.")
finally:
    print("File operation attempt completed.")
```

### Database Connection
```python
try:
    connection = connect_to_database()
    if not connection:
        raise ConnectionError("Failed to connect to the database!")
except ConnectionError as e:
    print(e)
finally:
    print("Database operation completed.")
```

## Best Practices
1. Be specific with exceptions to avoid masking errors.
2. Use `finally` for cleanup actions like closing files or database connections.
3. Avoid bare `except` blocks; always specify the exception.
4. Log exceptions for debugging purposes.
5. Use custom exceptions for domain-specific error handling.

---

## Comprehensions with Control Flow

List comprehensions, dictionary comprehensions, and set comprehensions allow concise expressions with control flow.

### List Comprehension with Conditional Logic
```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = [x for x in numbers if x % 2 == 0]
print(even_numbers)  # Output: [2, 4, 6]
```

### Dictionary Comprehension with Conditional Logic
```python
squares = {x: x**2 for x in range(5) if x % 2 == 0}
print(squares)  # Output: {0: 0, 2: 4, 4: 16}
```

---

## Advanced Control Flow Features

### Else with Loops
Python supports an optional `else` block with `for` and `while` loops, which executes only if the loop completes normally (i.e., without a `break`).
```python
for i in range(5):
    if i == 3:
        break
    print(i)
else:
    print("Loop completed without a break")
```

### Infinite Loops
Use infinite loops with caution. They run indefinitely unless explicitly terminated.
```python
while True:
    print("This is an infinite loop")
    break  # Safeguard to prevent actual infinite looping
```

---

## 4. Functions

### Why Use Functions?
Functions help in organizing code into reusable blocks, improving readability and reducing redundancy.

### Syntax
```python
def function_name(parameters):
    # Block of code
    return result
```

### Example
```python
def add_numbers(a, b):
    return a + b

print(add_numbers(5, 3))  # Output: 8
```

### Lambda Functions
Lambda functions are anonymous functions defined using the `lambda` keyword.
```python
square = lambda x: x ** 2
print(square(4))  # Output: 16
```

### Scope of Variables
- **Local Scope**: Variables defined within a function.
- **Global Scope**: Variables defined outside any function.
```python
global_var = "I am global"
def my_function():
    local_var = "I am local"
    print(global_var)
my_function()
```

---

## 5. Object-Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes to structure software. Python fully supports OOP, providing features like inheritance, encapsulation, polymorphism, and abstraction.

## Key Concepts of OOP

1. **Classes and Objects**
   - A **class** is a blueprint for creating objects. It defines attributes (variables) and methods (functions) that the objects created from the class will have.
   - An **object** is an instance of a class.

### Example:
```python
class Dog:
    # Class attributes
    species = "Canis familiaris"

    # Constructor
    def __init__(self, name, age):
        self.name = name  # Instance attribute
        self.age = age    # Instance attribute

    # Method
    def bark(self):
        return f"{self.name} says Woof!"

# Creating an object
my_dog = Dog("Buddy", 5)

print(my_dog.name)  # Output: Buddy
print(my_dog.bark())  # Output: Buddy says Woof!
```

---

2. **Encapsulation**
   - Encapsulation is the bundling of data and methods that operate on that data into a single unit, usually a class.
   - It also involves restricting direct access to some of an object's components (using private attributes).

### Example:
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def withdraw(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
            return amount
        else:
            return "Insufficient funds"

    def get_balance(self):
        return self.__balance

# Creating an object
account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # Output: 1500
```

---

3. **Inheritance**
   - Inheritance allows a class (child class) to inherit attributes and methods from another class (parent class).

### Example:
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass  # Abstract method

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

# Creating objects
dog = Dog("Buddy")
cat = Cat("Kitty")

print(dog.speak())  # Output: Buddy says Woof!
print(cat.speak())  # Output: Kitty says Meow!
```

---

4. **Polymorphism**
   - Polymorphism allows objects of different classes to be treated as objects of a common superclass. It is achieved through method overriding and interfaces.

### Example:
```python
class Bird:
    def fly(self):
        return "Flying high!"

class Penguin(Bird):
    def fly(self):
        return "Penguins can't fly."

# Polymorphism in action
animals = [Bird(), Penguin()]
for animal in animals:
    print(animal.fly())
```

---

5. **Abstraction**
   - Abstraction is the process of hiding implementation details and showing only the functionality.
   - In Python, abstraction can be achieved using abstract base classes (ABCs) from the `abc` module.

### Example:
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

# Creating an object
rect = Rectangle(5, 10)
print(rect.area())  # Output: 50
print(rect.perimeter())  # Output: 30
```

---

6. **Method Overriding**
   - A child class can provide a specific implementation of a method already defined in its parent class.

### Example:
```python
class Parent:
    def greet(self):
        return "Hello from Parent"

class Child(Parent):
    def greet(self):
        return "Hello from Child"

# Creating objects
parent = Parent()
child = Child()

print(parent.greet())  # Output: Hello from Parent
print(child.greet())   # Output: Hello from Child
```

---

7. **Special (Magic/Dunder) Methods**
   - Special methods in Python begin and end with double underscores (`__`). They allow you to define behavior for built-in operations.

### Example:
```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Point(self.x + other.x, self.y + other.y)

    def __repr__(self):
        return f"Point({self.x}, {self.y})"

p1 = Point(1, 2)
p2 = Point(3, 4)

print(p1 + p2)  # Output: Point(4, 6)
```

---

8. **Composition**
   - Composition is a way to combine objects to build complex systems. Instead of inheritance, classes can use other classes to achieve functionality.

### Example:
```python
class Engine:
    def start(self):
        return "Engine started"

class Car:
    def __init__(self):
        self.engine = Engine()

    def drive(self):
        return self.engine.start() + " and car is moving"

# Creating an object
car = Car()
print(car.drive())  # Output: Engine started and car is moving
```

---

## Best Practices for OOP

1. **Follow the Single Responsibility Principle**: Each class should have one responsibility.
2. **Use meaningful class and method names**.
3. **Keep methods short and focused**.
4. **Leverage inheritance and composition wisely**.
5. **Avoid overusing inheritance**; prefer composition when appropriate.

---

## 6. Modules and Libraries

### What are Modules?
Modules are files containing Python code that can define functions, classes, and variables.
```python
# Importing a module
import math
print(math.sqrt(16))  # Output: 4.0
```

### Third-party Libraries
Install libraries using `pip`, Python's package manager.
```bash
pip install requests
```

Example:
```python
import requests
response = requests.get("https://api.github.com")
print(response.status_code)
```

---

## 7. File Handling

### Why File Handling?
File handling allows reading and writing data to files, enabling persistent data storage.

### Example
```python
# Writing to a file
with open("example.txt", "w") as file:
    file.write("Hello, World!")

# Reading from a file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

## 8. Error and Exception Handling

### Why Handle Exceptions?
To prevent program crashes due to unexpected errors.

### Syntax
```python
try:
    # Block of code
except ExceptionType as e:
    # Handle exception
finally:
    # Execute regardless of exception
```

### Example
```python
try:
    result = 10 / 0
except ZeroDivisionError as e:
    print("Error:", e)
finally:
    print("Execution completed.")
```

---

## 9. Python Best Practices

### Tips
- Write readable and modular code.
- Use meaningful variable and function names.
- Follow PEP 8 standards.

---

## 10. Additional Resources
- [Official Python Documentation](https://docs.python.org/3/)
- [Python Community on Reddit](https://www.reddit.com/r/Python/)
- [Interactive Python Tutorials](https://www.learnpython.org/)

Feel free to explore, contribute, and enhance these notes!

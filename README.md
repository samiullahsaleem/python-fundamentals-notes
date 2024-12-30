# Python Fundamentals Notes

Welcome to the **Python Fundamentals Notes** repository! This repository contains comprehensive notes covering the basics of Python programming, intended for beginners and intermediate learners. The notes include explanations, examples, and exercises to solidify your understanding.

## Table of Contents

1. [Introduction to Python](#introduction-to-python)
2. [Data Types and Variables](#data-types-and-variables)
3. [Control Flow Statements](#control-flow-statements)
4. [Functions](#functions)
5. [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)
6. [Modules and Libraries](#modules-and-libraries)
7. [File Handling](#file-handling)
8. [Error and Exception Handling](#error-and-exception-handling)
9. [Python Best Practices](#python-best-practices)
10. [Additional Resources](#additional-resources)

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

### What is Control Flow?
Control flow determines the order in which statements are executed in a program.

### Conditional Statements
Conditional statements execute blocks of code based on conditions.
```python
x = 10
if x > 0:
    print("Positive number")
elif x == 0:
    print("Zero")
else:
    print("Negative number")
```

### Loops
Loops are used to repeat a block of code multiple times.

#### For Loop
```python
for i in range(5):
    print(i)  # Prints numbers from 0 to 4
```

#### While Loop
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Loop Control Statements
- **break**: Exits the loop.
- **continue**: Skips the current iteration.
- **pass**: Placeholder statement.
```python
for i in range(10):
    if i == 5:
        break
    if i % 2 == 0:
        continue
    print(i)
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

### Core Concepts
- **Class**: Blueprint for creating objects.
- **Object**: Instance of a class.
- **Inheritance**: Mechanism to create a new class using an existing class.
- **Encapsulation**: Hiding implementation details.
- **Polymorphism**: Methods with the same name behaving differently in different contexts.

### Example
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        return f"Hi, I am {self.name} and I am {self.age} years old."

person = Person("Alice", 25)
print(person.introduce())
```

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

# Introduction to Python
Python is a high-level, general-purpose programming language. Its design philosophy emphasizes code readability with the use of significant indentation. Python is dynamically-typed and garbage-collected. It supports multiple programming paradigms, including structured, object-oriented and functional programming.

# Syntax and Semantics

### Syntax
The syntax of a programming language refers to the order in which different elements are combined to form valid expressions. It is also the set of rules that defines how a Python code will be written and interpreted.

An example of a syntax rule for programming is the assignment statement:
>The print() is a reserved keyword and we have to pass the variable inside it to print the value.
```python
print(expression)
 ```
 
 ### Semantics
Python uses emphasizes the meaning of a program, which uses dynamic semantics means that its variable is dynamic object and we don’t have to specify its data type while initializing the variable.

For example:
>The general form of a WHILE loop in python. For the semantics, it keeps on running inside the statement until the Boolean expression is False.

```python
while(<boolean expression>):
  <statement>
 ```
 **Note:** It is mainly used if we don’t know how many times we should run this or until it has not met the Boolean expression.
 

# Variables and Types

### Assigning Values To The Variables

Variables hold values. In Python, variables do not require forward declaration; you only need to provide a variable name and assign it some value.

```python
p = 1.1
q = 2
r = 1/2
z = 'James'
```

### Data Types

There are different data types available in python such as
> - Text Type - **str**
> - Numeric Types - **int, float, complex**
> - Sequence Types - **list, tuple**
> - Mapping Type - **dict**
> - Set Types - **set**
> - Boolean Type - **bool**

```python
# 1. Text Type
>>> x = 'h1'
>>> print(type(x))
<class 'str'>

# 2. Numeric Types
>>> x = 42
>>> print(type(x))
<class 'int'>
>>> x = 3.14
>>> print(type(x))
<class 'float'>

# 3. Sequence Types
```python
>>> x = [1,2,3,4]
>>> print(type(x))
<class 'list'>
>>> x = (1,2,3,4)
>>> print(type(x))
<class 'tuple'>

# 4. Mapping Types
>>> x = {'name':'James','age':24}
>>> print(type(x))
<class 'dict'>

# 5. Sets Types
>>> x = set(('James','Opel','James','Troy'))
>>> print(type(x))
<class 'set'>

# 6. Boolean Types
>>> x = False
>>> print(type(x))
<class 'bool'>
```

# Python import module
Python modules are .py files that contain Python code. Any python file can be a module. Modules are used to group together related code in a project so you can use the same code in a different file without writing the entire code.

Modules, sometimes called **packages**, allow referencing of pre-written code that can perform common tasks that can be helpful to solve programs.

The syntax for the import statement is:
```python
import [module]
```

For example:
> Using the math module we can use many functions like 
> - ceil
> - floor
> - pow
> - sqrt
> - abs
> - random

```python
import math

# ceil function
>> x = math.ceil(1.431)
>> print(x)
2

# floor function
>> x = math.floor(1.431)
>> print(x)
1
```

# Unit Testing

### About
Unit testing is a method for testing software that looks at the smallest testable pieces of code, called units, which are tested for correct operation. By doing unit testing, we can verify that each part of the code, including helper functions that may not be exposed to the user, works correctly and as intended.

### Importing Modules
To start building test functions, first, we must import a library called **unittest** to use PyUnit.
```python
import unitest
```

### Python AssertEqual Method
The **assertEqual()** is indeed a “unittest” utility method in Python that has been cast off to verify the equivalence of two possible values during unit testing. It helps to find out whether the function works properly or not. If the two input variables, strings, or values are equivalent, assertEqual() returns **true**; otherwise, it returns **false**.

#### Example 1:
This test case will call the function which casts the string to int and by using assertEquals() it checks the value returned by the function as well as the provided correct value when it matched both returned value and the final value it will return saying that
>Ran 1 test in 0.001s <br/> OK

```python
import unittest

def castString(string):
    return int(string)

class TestStringMethods(unittest.TestCase):
    def test_split(self):
        self.assertEqual(castString('1'),1,'Incorrect Casting')
if __name__ == '__main__':
    unittest.main()
```



# File I/O Handling
To handle different types of files, it has different sets of rules and syntax. This file handling helps to read, write, and append to the files.<br/>
<br/>There are two types of data files such as:
- **Text files** - A text file consists of human readable characters, which can be opened by any text editor. 
-  **Binary files** - They are made up of non-human readable characters and symbols, which require specific programs to access its contents.

Hence, in Python, a file operation takes place in the following order

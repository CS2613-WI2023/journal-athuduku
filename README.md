# Introduction to Python
Python is a high-level, general-purpose programming language. Its design philosophy emphasizes code readability with the use of significant indentation. Python is dynamically-typed and garbage-collected. It supports multiple programming paradigms, including structured, object-oriented and functional programming.

# Syntax and Symantics

### Syntax
The syntax of a programming language refers to the order to which different elements are combined to from valid expressions. It also the set of rules that defines how a Python code will be written and interpreted.

An example of a syntax rule for programming is the assignment statement:
>The print() is a reserved keyword and we have to pass the variable inside it to print the value.
```python
print(expression)
 ```
 
 ### Symantics
Python uses emphasizes the meaning of a program, which uses dynamic semantics means that its variable are dynamic objects which we dont have to specify its data type while initializing the variable.

For example:
>The general form of a WHILE loop in python. For the symantics, it keep on running inside statement until the boolean expression is False.

```python
while(<boolean expression>):
  <statement>
 ```
 **Note:** It is mainly used if we dont know how many times we should run this or util it not met the boolean expression.
 

# Vairables and Types

### Assigning Values To The Variables

Variables hold values. In Python, variables do not require forward declaration - all you need to do is provide a variable name and assign it some value.

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
Python modules are .py files that contain Python code. Any python file can be module. Modules are used to group together related code in a project so you can use the same code in different file without writing the etire code.

Modules, sometimes called **packges**, allow to reference pre-written code that can perform common tasks that can be helpful to solve programs.

The syntax for the import statement is:
```python
import [module]
```

For example:
> Using math module we can use many function like 
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
To get started building test functions, first we must need to import a library called **unittest** to use PyUnit.
```python
import unitest
```

### Python AssertEqual Method
The **assertEqual()** is indeed a “unittest” utility method in Python that has been castoff to verify the equivalence of two possible values during unit testing. It helps to find out whether the function works properly or not. If the two input variables, strings, or values are equivalent, assertEqual() returns **true**; otherwise, it returns **false**.

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


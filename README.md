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
 
 >The general form of a For loop in python. For the semantics, it keeps on running inside the statement until the Boolean expression is False.

```python
for i in range(1,10):
  <statement>
 ```
 **Note:** It is mainly used if we know how many times we should run this.
 

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

# Functions
A function is a block of code which only runs when it is called.
You can pass data, known as parameters, into a function.
A function can return data as a result.

### Creating a Function
In python a function is defined by the keyword **def**.
Its also similar to the method in other programming languages.
```python
def first_function():
  print('Hello this function is called')
first_function() # calling function
```

# Classes and Objects
Python is an object-oriented programming language.
Almost everything in Python is an object, with its properties and methods.
A Class is like an object constructor or a "blueprint" for creating objects.

### Creating a Class
In python, the class is defined by the keyword **class**.
```python
class Math:
 
 # constructor
 def __init__(self,x,y):
   self.x = x
   self.y = y
   
 # methods or functions
 def sum(self):
   return self.x + self.y
   
 def subtract(self):
   return self.x - self.y
   
 def divide(self):
   return self.x / self.y
   
 def multiply(self):
   return self.x * self.y
   
# creating the object for the class
objectClass = Class(1,2)
objectClass.add() # returns 3
objectClass.multiply() # returns 2
```

The __init__() is a built-in function it is always called whenever we create an object instance for the class.
So this class has a constructor which can set values inside the class and can be accessed easily by the functions. The **self** keyword is used to represent an instance of the given class which means that only the attributes and methods present inside the class can be accessible.

### Inheriting a Class
Inheritance allows us to define a class that inherits all the methods and properties from another class.
<br/>
<br/>
**Parent class** is the class being inherited from, also called base class.
<br/>
**Child class** is the class that inherits from another class, also called derived class.

#### Parent Class
Any class can be a parent class, so the syntax is the same as creating any other class:
```python
class Animal:
 def __init__(self,name):
   self.name = name
```
#### Child Class
To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:
```python
class Dog(Animal):
 def __init__(self,name):
   super().__init__(name)
   self.speak = 'Bow Bow'
```
**Note:** The **child's __init__()** function **overrides** the inheritance of the **parent's __init__() function** so if we create an object of child class it first calls the __init__() function in child class.

By using the **super()** function, you do not have to use the name of parent element to call the methods, constructor,and variables, it will be automatically inherited from parent class. And also we dont need to pass the self on calling the __init__() of parent class.

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
- Opening the file
- Read or write (file operations)
- Close the file

There are different modes to open a file in Python<br/>
- **r** - Open a file for reading. (default if not specified)
- **w** - Open a file for writing. Creates a new file if it does not exist or overrides if the file exists 
- **x**	- Open a file for exclusive creation. If the file already exists, the operation fails.
- **a**	- Open a file for appending at the end of the file without truncating it. Creates a new file if it does not exist.
- **t**	- Open in text mode. (default)
- **b**	- Open in binary mode.
- **+**	- Open a file for updating (reading and writing)

### Opening Files in Python
In python, we use the **open()** method to open files.<br/>
To demonstrate how we open files in Python, let's suppose we have a file named 'data.txt' with the following content.
But in a CSV file, we have to **import csv** first and then we need to call **reader()** or **writer()** method.

### In Text File
```python
1 This file contains some data
2 It's separated by lines
```
Now let's try to open this file to access the data inside the file using open() function.
```python
# for reading the file
fileRead = open('data.txt','r') 

# for writing into the file
fileWrite = open('data.txt','w')

# for appending the data without losing the existing data
fileAppend = open('data.txt','a')
```

### In CSV File
```python
1 Name,Salary,Age
2 James,60000,24
3 Trish,67000,30![1](https://user-images.githubusercontent.com/122243218/214736535-a7eb0b0c-4b9c-46f6-bf9a-128e02a234ea.jpg)

```
Now let's try to open this file to access the data inside the file using open() function.
```python
# for reading the csv file
import csv

# for reading the data
with open('data.txt','r') as fileRead:
      reader = csv.reader(fileRead,delimiter=' ')
      
# for writing the data
with open('data.txt','w') as fileWrite:
      writer = csv.writer(fileWriter,delimiter=' ')
```

### Closing File
When we are done performing operations on the file, we need to properly close the file.
<br/>
Closing a file will free up the resources that were tied to the file. It is done using the **close()** method in Python. For example,
```python
# open a file
file1 = open("data.txt", "r")

# read the file
read_content = file1.read()
print(read_content)

# close the file
file1.close()
```

# Conclusion


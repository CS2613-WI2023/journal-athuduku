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
> 1. Text Type - **str**
> 2. Numeric Types - **int, float, complex**
> 3. Sequence Types - **list, tuple**
> 4. Mapping Type - **dict**
> 5. Set Types - **set**
> 6. Boolean Type - **bool**

##### 1. Text Type
```python
>>> x = 'h1'
>>> print(type(x))
<class 'str'>
```

##### 2. Numeric Types
```python
>>> x = 42
>>> print(type(x))
<class 'int'>
>>> x = 3.14
>>> print(type(x))
<class 'float'>
```
##### 3. Sequence Types
```python
>>> x = [1,2,3,4]
>>> print(type(x))
<class 'list'>
>>> x = (1,2,3,4)
>>> print(type(x))
<class 'tuple'>
```

##### 4. Mapping Types
```python
>>> x = {'name':'James','age':24}
>>> print(type(x))
<class 'dict'>
```

##### 5. Sets Types
```python
>>> x = set(('James','Opel','James','Troy'))
>>> print(type(x))
<class 'set'>
```

##### 6. Boolean Types
```python
>>> x = False
>>> print(type(x))
<class 'bool'>
```







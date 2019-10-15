
# Python Fundamentals
(prepared by - Shivam Shukla)

## 1 - Python Identifiers

Identifiers are just the names assigned to variables, classes, methods etc to uniquely identify them.



```python
#Rule 1- Allowed symbols - a-z, A-Z, _ , 0-9.
#Rule 2- Start with alphbets( a-z, A-Z) OR _.
#Rule 3- Can't be keywords.

variable = 78
random123 = 212
_shivam = 101

# BUT if variable or method name start with '_' , it has some specific meaning

_var1 = 1    # this is a protected variable
__var2 = 2   # the variable starting with 2 '_', is PRIVATE variable
__var3__ = 3 # var3 is a MAGIC variable.


# 34random = 78
# if = 78

# Identifiers are also case sensititve
total = 10
Total = 100
TOTAL = 1000

T_O_T_A_L =10000

print(total,Total,TOTAL,T_O_T_A_L)

# No variable name length limit.

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx = 10

print(xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx)
```

    10 100 1000 10000
    10
    

## 2- Reserved Words

-> Python has total 33 reserved words while Java has 53 reserved words.

-> Reserved words represents some specific meaning or functionality.

True, False, None   ( only these 3 are starting with uppercase letter,  else are in lowercase)

-> In python, no switch or do-while concept is there.
-> int, float... are also not reserved words.



```python
# we can also check for keywords as follows 

import keyword
keyword.kwlist
```




    ['False',
     'None',
     'True',
     'and',
     'as',
     'assert',
     'break',
     'class',
     'continue',
     'def',
     'del',
     'elif',
     'else',
     'except',
     'finally',
     'for',
     'from',
     'global',
     'if',
     'import',
     'in',
     'is',
     'lambda',
     'nonlocal',
     'not',
     'or',
     'pass',
     'raise',
     'return',
     'try',
     'while',
     'with',
     'yield']



## 3- Data Types

Data types defines the type of the value stored in variable such as INTEGER, FLOAT, STRING, CHARACTER etc.
Python is DYNAMICALLY TYPED language, so the type of variable is automatically defined for the variable based on the value assigned to it.

Python 3 has generally 14 built-in datatypes

1)  int

2)  float

3)  complex ( to represent complex numbers )

4)  bool 

5)  str

6)  list

7)  tuple

8)  set

9)  frozenSet

10) dict

11) byte

12) bytearray

13) range

14) None



```python
# we can know the type of variable using type method.

x =10
y ='Shivam'

print("Type of x : ",type(x))
print("Type of y : ",type(y))
```

    Type of x :  <class 'int'>
    Type of y :  <class 'str'>
    

## 4- Everything in Python is an OBJECT

In python everything is represented as OBJECT.


```python
# We can get the address of a object using id() method.

x = 100

print(id(x))
print(type(x))
print(x)
```

    1736142080
    <class 'int'>
    100
    

## 5- int type

In python, long type is applicable but only til version 2.
In Py 3, the long integer can also be stored in int type.



```python

x = 1234567890123456789012345678901234567890123456789
type(x)    # int

# we can represent Integral values in 4 ways

# 1) Decimal form(base 10)

deciaml_x = 1111
print("Value of decimal_x      : ",deciaml_x)


# 2) Binary form(base 2)

# we must prefix the number with 0b or 0B.
binary_x = 0b1111

# The OUTPUT value will alsways be DECIMAL as we are just representing a decimal number in other base.
print("Value of binary_x       : ",binary_x)

# 3) Octal form(base 8)

# we must prefix the number with 0o or 0O.
octal_x = 0o123

# 0o123 = 1x8^2 + 2x8^1 + 3x8^0 = 64+ 16+ 3 = 83 
print("Value of octal_x        : ",octal_x)



# 4) Hexadecimal form(base 16)

# we must prefix the number with 0x or 0X.
# allowed symbols - 0-9, A-Z OR a-z
hexadecimal_x = 0x0A0b0C0d0e0F
print("Value of hexadecimal_x  : ",hexadecimal_x )
```

    Value of decimal_x      :  1111
    Value of binary_x       :  15
    Value of octal_x        :  83
    Value of hexadecimal_x  :  11042563100175
    

## 6- Base conversion functions

Python has in built base conversion functions to convert number from binary to decimal, decimal to binary, octal to dec, and so on.

The 3 built in functions are ->

#### bin() -> Used to convert number of any base to binary.

#### oct() -> Used to convert number of any base to octal.

#### hex() -> Used to convert number of any base to hexadecimal.

Examples are illustrated below



```python
# bin() ->

x = bin(15)

print(x)
print(bin(0o17))
print(bin(0Xf))

# oct() ->

print(oct(15))
print(oct(0b1111))
print(oct(0Xf))

# hex() ->

print(hex(15))
print(hex(0b1111))
print(hex(0O123))
```

    0b1111
    0b1111
    0b1111
    0o17
    0o17
    0o17
    0xf
    0xf
    0x53
    

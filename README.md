
# Python Fundamentals
(prepared by - Shivam Shukla)

## 1 - Python Identifiers

Identifiers are just the names assigned to variables, classes, methods etc to uniquely identify them.



```python
#Rule 1- Allowed symbols - a-z, A-Z, _ , 0-9.
#Rule 2- Start with alphabets( a-z, A-Z) OR _.
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

# Identifiers are also case sensitive
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

It has 5 fundamental data types -> int , float, bool, str, complex.

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

# The OUTPUT value will always be DECIMAL as we are just representing a decimal number in other base.
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
    

## 7- float type

A number with decimal point is called floating point number and to represent this number, we have to use float data type.

Eg. area= 25.25

#### We can represent floating point number only in the decimal form OR Exponential/ Scientific form ( not in OCTAL, BINARY, HEX ).

See following examples.


```python
# floating point number in decimal form ->
principal = 9189982.50

print(type(principal))


# following are syntax error ->

# f1 = 0B11.011
# f2 = 0o34.214
# f3 = 0xAb4.54


# Exponential form OR Scientific form ->

v = 3.0e8  # OR 3E8
print(v)


random = 3.4e-2
print(random)
```

    <class 'float'>
    300000000.0
    0.034
    

## 8- Complex data type

It is a python specific special data types and used to represent complex numbers.

##### General syntax of complex number = a + bj
Here, a - real part

b- imaginary part and  j^2 = -1

It is used to develop some scientific applications.
(we can't use i or any other symbol instead of j OR J)

Note->

#### 1.) We can use int or float type values to represent real or imaginary part.

#### 2.) We MUST represent the imaginary part in DECIMAL form( not in OCTAL,BIN,HEX), however we can represent the real part in any of 4 integral representation.


```python
# complex type example ->

comp_num = 10 + 20j
print(comp_num)

comp_num = 10.0 + 20.10j
print(comp_num)

comp_num = 0b1111 + 20.10j
print(comp_num)

# Extracting the real and imaginary part
print(comp_num.real)
print(comp_num.imag)


# We can also perform arithmetic operations on complex type->

x = 10 +20.55j
y = 30 -2.45j

print(x-y)
print(x+y)
print(x*y)
print(x/y)
```

    (10+20j)
    (10+20.1j)
    (15+20.1j)
    15.0
    20.1
    (-20+23j)
    (40+18.1j)
    (350.3475+592j)
    (0.2755538754032136+0.7075035664912624j)
    

## 9- bool data type

To represent logical values( True/False ) we go for bool data type.

Internally True is represented as 1 and False is represented as 0.

So we can perform arithmetic operation on boolean values.


```python
# bool type

flag = True
print(type(flag))

# Performing arithmetic operation ->

print("True + True = ",True + True)
print("True - Flase = ",True - False)
print("True * False = ",True * False)
print("False / True = ",False / True)

```

    <class 'bool'>
    True + True =  2
    True - Flase =  1
    True * False =  0
    False / True =  0.0
    

## 10- str data type

string type is used to represent a sequence of characters.

We can use single quotes(' ') , double quotes (" ") or even triple quotes (""" """ OR ''' ''') to represent the String.



```python
# str type

name = 'shivam'
print(name,type(name))

name = "Shivam"
print(name,type(name))

name = "'shivam'"
print(name,type(name))

# triple quotes 

# triple quotes are basically used for MULTILINE STRING LITERAL or to include single or double quotes in the string.

var1 = '''shivam
shukla'''
print(var1)



pattern = """   *
  ***
 *****
*******"""

print(pattern)

''' Triple quotes are also 
used defining DOC STRING!'''

str1 = '''"this" is tricky!'''
print(str1)



```

    shivam <class 'str'>
    Shivam <class 'str'>
    'shivam' <class 'str'>
    shivam
    shukla
       *
      ***
     *****
    *******
    "this" is tricky!
    

## 11- str type - index( positive and negative )

string type is a sequence of characters and the characters can be accessed using the INDEX.

Python has both positive and negative index(for reverse traversing).


```python
# str index 

name = 'Shivam'

''' INDEX   0    1    2    3    4    5  
    NAME    S    h    i    v    a    m
    INDEX  -6   -5   -4   -3   -2   -1 '''

print(name[0])
print(name[-1])

# name[100]    -> IndexError!
```

    S
    m
    

## 12- str type - slice operator

It breaks the string into substrings.

##### SYNTAX - string[ begin : end ]

##### SYNTAX - string[ begin : end : step ]

It returns the substring from 'begin' index to 'end -1' index of string.

If we do not specify the begin index, then it will start from 0 and if end index is not specified, it will give the string upto end.

Slice operator never rise INDEX ERROR even though the index is out of bound.


```python
# slice operator

name = "Shivam"

print(name[ 0 : 4 ])
print(name[   : 4 ])
print(name[ 4 :   ])
print(name[ 4 : 4 ])

print(name[ 2 : 100])

print(name[   :   ])

print(name[ -1 :    ])

print(name[ -6 :    ])

print(name[ 0 : 4 : 2 ])

# it reverses a string
print(name[ -1 : -7 : -1 ])
#OR
print(name[ -1 :    : -1 ])
#OR
print(name[    :    : -1 ])
#OR
print(name[  6 :    : -1 ])


# Application of slice 
name = "shivam"
print(name)

# To capitalize
name = name[0].upper() + name[ 1 : ]

print(name)


```

    Shiv
    Shiv
    am
    
    ivam
    Shivam
    m
    Shivam
    Si
    mavihS
    mavihS
    mavihS
    mavihS
    shivam
    Shivam
    

## 13- str type -> + and * operator

+ ' + ' -> is string concatenation operator
* ' * ' -> is string repetition operator


```python
# + and * operator
x = "ten"

y = x + "10"

print(y)

z = x * 10
print(z)

z1 = 10 * x       # 10 * x and x * 10 both are valid
print(z1)

# for *, one operand must be STRING and other must be INT.
print('*'*20)
print("shivam")
print('*'*20)
```

    ten10
    tentententententententententen
    tentententententententententen
    ********************
    shivam
    ********************
    

## 14- Type Conversion using int()

The process of changing the variable type from one to another is called type conversion.

int() is used to convert other data type values to int.



```python
# int()

# we can use int() to cast the input value to int

x = input("Enter a string : ")
print("You entered : ",x,type(x))

x = int(input("Enter a integer : "))
print("You entered : ",x,type(x))


# float to int -> VALID
print(int(78.90))

# complex to int -> NOT VALID

# bool to int -> VALID
print(int(True))

# str to int -> VALID only when string contains only INTEGRAL VALUE and in BASE -10.
print(int("78"))

# print(int("SeventyEight"))   not valid as it doesn't contain integral value
# print(int("ob1111"))         not valid as number represented in binary(base 2)

```

    Enter a string : 78
    You entered :  78 <class 'str'>
    Enter a integer : 78
    You entered :  78 <class 'int'>
    78
    1
    78
    

## 15- Type Conversion using float()

To convert values to float type.


```python
# float()

# int to float -> VALID

print(float(15))
print(float(0b1111))   # any of 4 bases integral value can be passed.

# complex to float -> NOT VALID  and gives TypeError

# bool to float -> VALID
print(float(True))

# str to float -> VALID only when string containing integral OR float value in base 10.

print(float("78.0"))
print(float("78"))
#print(float("78a78"))  ValueError
```

    15.0
    15.0
    1.0
    78.0
    78.0
    

## 16- Type Conversion using complex()

complex() has 2 forms as it has both real and imaginary part ->

* Form-1 -> complex(real part)

We pass only real part and imaginary part will be implicitly 0.So the output will be = real + 0j

* Form-2 -> complex(real, imag)

We can pass both real and imag value.So the output will be = real + imagj


```python
# complex()

# we can pass int, float, str and bool value to complex()

print(complex(10))
print(complex(10.0))
print(complex(0b1010))
print(complex("10.00"))
print(complex(True*10))

# form-2 has several restrictions

print(complex(10,20))
print(complex(10.0,20.50))

# Restriction 1) If the 1st argument is string then we can't pass 2nd argument.

# print(complex("10",20))

# Restriction 2) 2nd argument can't be string in complex()

# print(complex(20,"10"))


```

    (10+0j)
    (10+0j)
    (10+0j)
    (10+0j)
    (10+0j)
    (10+20j)
    (10+20.5j)
    

## 17- Type Conversion using bool()


For non zero argument, bool value will be True and for 0 as a argument, bool value will be False.


```python
# bool()

# int to bool -> VALID
print(bool(10))
print(bool(-10))
print(bool(-0))    # 0 can't be negavie or positive, it's just ZERO, so value is False.
print(bool(0))

# float to bool -> VALID
print(bool(10.0))
print(bool(0.0000001))
print(bool(0.0000000))

# complex to bool -> VALID

# If both real and imag part are 0 then only the value will be False else True.
print(bool(10+20j))
print(bool(10.5+2.0j))
print(bool(0+0j))


# str to bool -> VALID

# Any non empty string will be True and empty string will be false.
print(bool("shivam"))
print(bool("False"))
print(bool("True"))
print(bool("yes"))
print(bool("no"))
print(bool(" "))
print(bool(""))

```

    True
    True
    False
    False
    True
    True
    False
    True
    True
    False
    True
    True
    True
    True
    True
    True
    False
    

## 18- Type Conversion using str()

We can easily convert the other types to str without any major restrictions.



```python
# str()

# int to str -> VALID any base int can be onverted to string repressentation of that integer in base-10.
print(str(10))
print(str(0b1010))    # 10

# float to str -> VALID
print(str(10.0))

# complex to str -> VALID
print(str(10+20j))

# bool to str -> VALID
print(str(True))
print(str(False))

```

    10
    10
    10.0
    (10+20j)
    True
    False
    

## 19- Type Casting Summary Table


|  | int argument  | float argument  | complex argument  | bool argument  | str argument 
|---|---|---|---|---|---|
| int()  | yes  | yes  | NO  | yes  | yes( only int with base-10)  |   
| float()  | yes  | yes  | NO  | yes  | yes  |   
| complex() (2 Forms)  | yes  | yes  | yes  | yes  | yes(some restrictions)  |   
| bool()  | yes  | yes  | yes  | yes  | yes  |  
| str()  | yes  | yes  | yes  | yes  | yes  |   

## 20- IMMUTABILTY

##### * MUTABLE -> it means the object is changebale i.e. we can make changes to existing objects.

##### * IMMUTABLE -> it means that we CAN'T MAKE CHANGES TO EXISTING OBJECT, if we try to do so, a NEW OBJECT will be creaated with those changes.

###### All the FUNDAMENTAL DATA TYPES (int, float, complex, bool, str ) are IMMUTABLE.

As we have discussed ablove that everything in python is an object and we can see the address of that object using id(),  so we can show that fundamental types in py are immutable ->



```python
# immutablity

x = 10             # int object with value 10
print(id(x))       # printing address of object x     1987076544
y=x

# we can also check whether the 2 reference variables are pointing to same variable or not using IS operator.
print(x is y)      # True means address of x and y are same.


# Now if we try to make any changes to x, a new object will be created as per the definition of immutabilty, so now let's see->

x = x + 1
print(id(x))       # printing address of object x     1987076576
print(x is y)      # Falsw 

# as we can see that address of x and after modifying the value of x are diiferent. So fundamental data types are immutable.
# the old reference with address 1987076544 will be available for Garbage Collection


##############################################################################################################################
# Python uses object reusability i.e it will first check whecther the object alsredy exist or not, if it exists, the it will
# simply assign the reference variable to existing object else create a new object.

# BUT this concept is applicabe for int , float, bool and str nut NOT FOR COMPLEX.
# Example

a = 10
b = 10
print(a is b)     # True

a = 10 + 10j
b = 10 + 10j
print(a is b)     # False
##############################################################################################################################


# Example of Mutability -> list
l = [10,20,30,40,50]
print(id(l))       # 2366418934280

l[0]=100
print(id(l))       # 2366418934280

# after making change the to list object a new object is not created, so we can ake changes to exisiting 
object hence list is mutable.

```

    1987076544
    True
    1987076576
    False
    True
    False
    2366418934280
    2366418934280
    

## 21- list 

To represent group of values( may be of different types ) as a single entity, we use list.

It has following properties->

* oder is preserved
* duplicates are allowed
* represented as  [ ..... ]
* indexing and slicing concept is applicable.
* growable in nature
* MUTABLE in nature


```python
# list->

# we can create list object in 2 ways ->
l = list([10,20,'Shivam'])

# OR

l = [10,20,'Shivam']

print(type(l))
print(l)

```

    <class 'list'>
    [10, 20, 'Shivam']
    

* index start from 0 (for starting element) OR -1 (for last element).
* slicing can be done by using list[start : end +1]


```python
l = [10,20,'Shivam']

print(l[1:3])
print(l[-1])
print(l[-3])
```

    [20, 'Shivam']
    Shivam
    10
    

* to add element to list use 'append' and to remove, use 'remove'


```python
l.append('Shukla')
l.append(50)
l.remove(20)

l
```




    [10, 'Shivam', 'Shukla', 50]



* To copy a list use [ : ] instead of just assigning thr reference of other list.


```python
l=[10,20,30,40,50,60]
l1=l

print(l1)

l[0]=1000
print(l1)
# Here we made changes to 'l' but changes are reflected in l1 also!!!!!!!!!!!!

# To overcome this we have to create a deep copy not a shallow copy.

# deep copy
l2=l[ : ]

print(l2)
l[3]=5000

print(l1)
print(l2)

```

    [10, 20, 30, 40, 50, 60]
    [1000, 20, 30, 40, 50, 60]
    [1000, 20, 30, 40, 50, 60]
    [1000, 20, 30, 5000, 50, 60]
    [1000, 20, 30, 40, 50, 60]
    

* REVERSE a list



```python
l[ : : -1]
```




    [60, 50, 5000, 30, 20, 1000]



## 22. Tuple

Exactly same as LIST but only one difference that it is IMMUTABLE 

* Read only version of List.
* Represented by (......)
* Hetrogeneous Elements are allowed as in the list.


```python
t=(10,20,30,40)

print(type(t))
print(t[0])
print(t[-1])

# If we try to modify element of a tuple, we'll get Type Error.

#t[0]=40

#TypeError                                 Traceback (most recent call last)
# <ipython-input-12-2371b0c12f2f> in <module>()
#       5 print(t[-1])
#       6 
# ----> 7 t[0]=40

# TypeError: 'tuple' object does not support item assignment
```

    <class 'tuple'>
    10
    40
    

#### We can't add OR remove element from a Tuple.

So append OR remove methods are not applicable.

### Ambiguity between int and Tuble with 1 element.


```python
# Emplty Tuple
t=()
print(type(t))

# tuple with 1 element( , is must after element).
t1=( 10 ,)
print(type(t1))


# int type( without ,)
t2=(10)
print(type(t2))
```

    <class 'tuple'>
    <class 'tuple'>
    <class 'int'>
    

## 23. SET

* Order is not preserved.
* DUPLICATES are NOT Allowed.
* Can be used to remove the duplicate elemnts from the list.
* Indexing and Slicing are NOT applicable as Set is not Scriptable.


```python
s={10,20,30,40,50}

print(type(s))
print(s)

listt = [ 10,10,10,30,20,30,20]

# removing duplicate from list.
sett = set(listt)

print(sett)
```

    <class 'set'>
    {40, 10, 50, 20, 30}
    {10, 20, 30}
    

##### Elements can be added or removed from the set using 'add' and 'remove' methods.


```python
sett.add(90)
sett.remove(20)
sett.add(8000)

print(sett)
```

    {8000, 1000, 50, 90, 60, 30}
    

### Ambiguity between EMPTY SET and DICTIONARY



```python
s = { }  # By default it is EMPTY DICTIONARY

s1 = set() # Empty set can be created using set().

print(type(s))
print(type(s1))
```

    <class 'dict'>
    <class 'set'>
    

## 24. Frozen Set

Exactly same as SET except that frozen set is IMMUTABLE.

* We can't add or remove any element.



```python
fr = frozenset({10,20,30,40})

#OR

s = { 1,2,3,4,5}
fr = frozenset(s)

print(fr)
```

    frozenset({1, 2, 3, 4, 5})
    

## 24. DICT

Used to represent KEY-VALUE PAIR.

* Internally, data is stored based on the HASH code of KEYS. So order is not preserved.
* DUPLICATE KEYS are NOT allowed!
* Duplicate valus are allowed.
* MUTABLE.
* Indexing ans Slicing NOT applicable.


```python
#Empty Dict
d={}

d={100:'Shivam',101:'Tim',102:'Steve'}

print(type(d))
print(d)

print(d[100])

# We can change the value associated with the Key.
d[102]='Colt'

print(d)
```

    <class 'dict'>
    {100: 'Shivam', 101: 'Tim', 102: 'Steve'}
    Shivam
    {100: 'Shivam', 101: 'Tim', 102: 'Colt'}
    

## 25. Range Data Type

Used to represent a sequence of numbers.
* IMMUTABLE
* Orde is preserved
* Indexing and slicing is applicable.


```python
r = range( 10 ) # r= 0,1,.....,9.

print(type(r))

# we can use range for iteration.
for x in r:
    print(x)
    
```

    <class 'range'>
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    

* Form 1 - range(n) : 0 to n-1

* Form 2 - range(begin, end) : begin to end -10

* Form 3 - range(begin, end, increment) : begin to end - 1 with increment.

* Form 4 - range(begin, end, decrement) : begin to end + 1 with decrement.


```python
for x in range(5,10):
    print(x)

print("***********")

for x in range(2,10,2):
    print(x)
    
print("***********")

for x in range(10,2,-2):
    print(x)
```

    5
    6
    7
    8
    9
    ***********
    2
    4
    6
    8
    ***********
    10
    8
    6
    4
    

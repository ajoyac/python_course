# Python course

This tutorial is designed for anybody to get the bases for use learn python programming lenguage from scratch.
It may help to have to have basic undestandig of Computer information.
## Python topics
 * [Overview](#overview)
   - What is it
   - History
   - pep
 * [Setting up](#setting-up)
   - Getting Python
   - Installing Python
   - Enviroment 
   - pip
   - mongoose and Basilisk
 * [Basic Syntax](#basic-syntax)
   - Interactive mode Programing
   - Reserverd Words
   - Lines and Indentation
   - Comments in python
 * [Variables types](#variable-types)
   - Assign Values to Variables
   - Standard Data Types
 * [Basic Operators](#basic-operators)
   - Types of Operator
   - how to use it.
   - decison making
   - loops
 

## Overview
### What is it 

Python is a high-level, interpreted, interactive and object-oriented scripting language. Python is designed to be highly readable. It uses English keywords frequently where as other languages use punctuation, and it has fewer syntactical constructions than other languages.

Python is Interpreted − Python is processed at runtime by the interpreter. You do not need to compile your program before executing it. This is similar to PERL and PHP.

Python is Interactive − You can actually sit at a Python prompt and interact with the interpreter directly to write your programs.

Python is Object-Oriented − Python supports Object-Oriented style or technique of programming that encapsulates code within objects.

Python is a Beginner's Language − Python is a great language for the beginner-level programmers and supports the development of a wide range of applications from simple text processing to WWW browsers to games.

### History
Python was conceived in the late 1980s, and its implementation began in December 1989 by Guido van Rossum ![Guido van Rossum](https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Guido_van_Rossum_OSCON_2006.jpg/400px-Guido_van_Rossum_OSCON_2006.jpg)

Python 2.0 was released on 16 October 2000 and had many major new features, including a cycle-detecting garbage collector and support for Unicode. With this release, the development process became more transparent and community-backed. and it has an end of life [2020](https://pythonclock.org/)

Python 3.0 was released on 3 December 2008 after a long testing period. It is a major revision of the language that is not completely backward-compatible with previous versions. However, many of its major features have been backported to the Python 2.6.x and 2.7.x version series, and releases of Python 3 include the 2to3 utility, which automates the translation of Python 2 code to Python 3.

### PEP
 [PEP](https://www.python.org/dev/peps/) contains the index of all Python Enhancement Proposals, known as PEPs. PEP numbers are assigned by the PEP editors, and once assigned are never changed 
 
#### PEP to read
Some of the peps to check are:
 - [pep 8](https://www.python.org/dev/peps/pep-0008/) talk about the style of the code
 - [pep 20](https://www.python.org/dev/peps/pep-0020/) talk about the Zen of python

## Setting up
Python is multi platform. it can be found: multiple unix/linux OS

### Windows
 if you don't have it already go to: [https://www.python.org/](https://www.python.org/)
 for windows there is a msi version 
### linux 
 for linux you might already have it or check your pkg manager it might be something like this(or even you already have it)
 
 `sudo apt install python3`
 
 `sudo apt-get install python3`
 
 `yum install python3`
 
 `pacman install python3`
 ### Mac
 for macos check home brew
 `brew install python`
 
 the full steps can be fount at [here](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-macos)
 But if you are like me TL;DR;
 open terminal 
 ```
 xcode-select -p
 xcode-select --install
 /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
 echo "export PATH=/usr/local/bin:$PATH"  >> ~/.bash_profile
 source ~/.bash_profile
 brew doctor	
 brew install python3
 ```
 
 for ios: there is an [app](http://omz-software.com/pythonista/) for that 
 
 ### Setting up PATH
Programs and other executable files can be in many directories, so operating systems provide a search path that lists the directories that the OS searches for executables.

The path is stored in an environment variable, which is a named string maintained by the operating system. This variable contains information available to the command shell and other programs.

### pip
pip is a package management system used to install and manage software packages written in Python. Many packages can be found in the default source for packages and their dependencies

to install a package `pip install <package name>`

to delete the package `pip uninstall <package name>`

### basilisk and mongoose
[Basilisk](https://github.com/ajoyac/basilisk) is a restapi server that will provide challenge and verify your answer,
It can manages what have been already completed (its written in python)

[mongoose](https://github.com/ajoyac/mongoose) sdk to perform the exercises prepared in basilisk

how to install it? using pip! of course!

```pip install --extra-index-url https://test.pypi.org/simple/ --upgrade mongoose```

## Basic Syntax

The first we talk about how the code have to look, but there is something to check.


### Interactive Mode Programming
to open the interactive mode of python
open a terminal, and just write `python`
```python
python3
Python 3.6.4 (default, Jan  7 2018, 15:53:53)
[GCC 6.4.0] on cygwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

#### Hello world n19848
write in the python terminal
```python
print ("Hello, Python!")
```
and it will  print 
```
Hello, Python!
```
now lets create a file with the same information and run it as
```bash
python <filename>
```


#### RESERVERD WORDS
there are word you cant use, I always recomend read the documentation

![ reserverd words](https://cdn-images-1.medium.com/max/1200/1*TjYrRbTtdGArQwBywBJHgg.png)
It can be found at here(https://docs.python.org/3/library/functions.html#built-in-funcs)
indentation lines
``` python
#!/usr/bin/python3

import sys

try:
   # open file stream
   file = open(file_name, "w")

except IOError:
   print ("There was an error writing to", file_name)
   sys.exit()
print ("Enter '", file_finish,)
print "' When finished"

while file_text != file_finish:
   file_text = raw_input("Enter text: ")
   
   if file_text == file_finish:
      # close the file
	  file.close
      break
   file.write(file_text)
   file.write("\n")
file.close()
file_name = input("Enter filename: ")

if len(file_name) == 0:
   print ("Next time please enter something")
   sys.exit()

try:
   file = open(file_name, "r")

except IOError:
   print ("There was an error reading file")
   sys.exit()
file_text = file.read()
file.close()
print (file_text)
```
#### comments!

You can let comments on your code. this will permit to left some notes or documentation on the code you wrote
 you might want to explain somehtin  sinces it will happend something 
 
 a) left unseen a code along time
 b) some one else required to read your code
 
``` python

#!/usr/bin/python3
# First comment

print ("Hello, Python!") # second comment
This produces the following result −
```
```
Hello, Python!
```
You can type a comment on the same line after a statement or expression −
```python
name = "Madisetti" # This is again comment
```
Python does not have multiple-line commenting feature. You have to comment each line individually as follows −
```python
# This is a comment.
# This is a comment, too.
# This is a comment, too.
# I said that already.
```
one line multiple statements
```
import sys; x = 'foo'; sys.stdout.write(x + '\n')
```

# Variables types
## Assigning Values to Variables
Python variables do not need explicit declaration to reserve memory space. The declaration happens automatically when you assign a value to a variable. The equal sign (=) is used to assign values to variables.

``` python 
counter = 100          # An integer assignment
miles   = 1000.0       # A floating point
name    = "John"       # A string

print (counter)
print (miles)
print (name)
```

Here, 100, 1000.0 and "John" are the values assigned to counter, miles, and name variables, respectively. This produces the following result −
```
100
1000.0
John
```
### Multiple Assigment

Python allows you to assign a single value to several variables simultaneously.

``` python
a, b, c = 1, 2, "john"
```
Here, two integer objects with values 1 and 2 are assigned to the variables a and b respectively, and one string object with the value "john" is assigned to the variable c.

## Standard Data Types
 - Numbers
 - String
 - List
 - Tuple
 - Dictionary
### Python Numbers
Number data types store numeric values, supports:
 - int (signed integers)
 - float (floating point real values)
 - complex (complex numbers)
 
### Strings 
Strings in Python are identified as a contiguous set of characters represented in the quotation marks. Python allows either pair of single or double quotes. Subsets of strings can be taken using the slice operator ([ ] and [:] ) with indexes starting at 0 in the beginning of the string and working their way from -1 to the end.

The plus (+) sign is the string concatenation operator and the asterisk (*) is the repetition operator. For example −
``` python
tr = 'Hello World!'

print (str)          # Prints complete string
print (str[0])       # Prints first character of the string
print (str[2:5])     # Prints characters starting from 3rd to 5th
print (str[2:])      # Prints string starting from 3rd character
print (str * 2)      # Prints string two times
print (str + "TEST") # Prints concatenated string
```

This will oputput:

```
Hello World!
H
llo
llo World!
Hello World!Hello World!
Hello World!TEST
```

### Lists
Lists are the most versatile of Python's compound data types. A list contains items separated by commas and enclosed within square brackets ([]). To some extent, lists are similar to arrays in C. One of the differences between them is that all the items belonging to a list can be of different data type.

The values stored in a list can be accessed using the slice operator ([ ] and [:]) with indexes starting at 0 in the beginning of the list and working their way to end -1. The plus (+) sign is the list concatenation operator, and the asterisk (*) is the repetition operator.
``` python
list1 = [ 'abcd', 786 , 2.23, 'john', 70.2 ]
tinylist = [123, 'john']

print (list1)          # Prints complete list
print (list1[0])       # Prints first element of the list
print (list1[1:3])     # Prints elements starting from 2nd till 3rd 
print (list1[2:])      # Prints elements starting from 3rd element
print (tinylist * 2)  # Prints list two times
print (list1 + tinylist) # Prints concatenated lists
```
It produces:

```
['abcd', 786, 2.23, 'john', 70.200000000000003]
abcd
[786, 2.23]
[2.23, 'john', 70.200000000000003]
[123, 'john', 123, 'john']
['abcd', 786, 2.23, 'john', 70.200000000000003, 123, 'john']
```

### tuple 
It like a  a list but it is only read only so in the case:

```python
tuple = ( 'abcd', 786 , 2.23, 'john', 70.2  )
list = [ 'abcd', 786 , 2.23, 'john', 70.2  ]
tuple[2] = 1000    # Invalid syntax with tuple
list[2] = 1000     # Valid syntax with list
```
it wil generate an error

### Python Dictionary
Python's dictionaries are kind of hash-table type it work as consist of key-value pairs,
A dictionary key can be almost any Python type, but are usually numbers or strings. Values, on the other hand, can be any arbitrary Python object.(It requires to be a something hasshable**)

Dictionaries are enclosed by curly braces ({ }) and values can be assigned and accessed using square braces ([]).

```python 
dict = {}
dict['one'] = "This is one"
dict[2]     = "This is two"

tinydict = {'name': 'john','code':6734, 'dept': 'sales'}

print (dict['one'])       # Prints value for 'one' key
print (dict[2])           # Prints value for 2 key
print (tinydict)          # Prints complete dictionary
print (tinydict.keys())   # Prints all the keys
print (tinydict.values()) # Prints all the values
```

result:

```
This is one
This is two
{'name': 'john', 'dept': 'sales', 'code': 6734}
dict_keys(['name', 'dept', 'code'])
dict_values(['john', 'sales', 6734])
```

### Data type conversions

Sometimes, you may need to perform conversions between the built-in types. To convert between types, you simply use the type-names as a function.

There are several built-in functions to perform conversion from one data type to another. These functions return a new object representing the converted value. 
(look the built-in functions above for review)

some examples:

``` python

a = int("101010',2)
a = int("1A',16)
a = int("123'10)
a = int(99.99)
a = set([1,2,3,4])
b = tuple(a)
at = chr(64)
another_a = ord("a")
binstr = bin("10")  
```

## Basic Operators

### number operations 

```python
a = 21
b = 10
c = 0

c = a + b
print ("Line 1 - Value of c is ", c)

c = a - b
print ("Line 2 - Value of c is ", c )

c = a * b
print ("Line 3 - Value of c is ", c)

c = a / b
print ("Line 4 - Value of c is ", c )

c = a % b
print ("Line 5 - Value of c is ", c)

a = 2
b = 3
c = a**b 
print ("Line 6 - Value of c is ", c)

a = 10
b = 5
c = a//b 
print ("Line 7 - Value of c is ", c)
```

### comparations operations.
``` python
a = 21
b = 10

if ( a == b ):
   print ("Line 1 - a is equal to b")
else:
   print ("Line 1 - a is not equal to b")

if ( a != b ):
   print ("Line 2 - a is not equal to b")
else:
   print ("Line 2 - a is equal to b")

if ( a < b ):
   print ("Line 3 - a is less than b" )
else:
   print ("Line 3 - a is not less than b")

if ( a > b ):
   print ("Line 4 - a is greater than b")
else:
   print ("Line 4 - a is not greater than b")

a,b = b,a #values of a and b swapped. a becomes 10, b becomes 21

if ( a <= b ):
   print ("Line 5 - a is either less than or equal to  b")
else:
   print ("Line 5 - a is neither less than nor equal to  b")

if ( b >= a ):
   print ("Line 6 - b is either greater than  or equal to b")
else:
   print ("Line 6 - b is neither greater than  nor equal to b")
```

### Assigment operations

```
!/usr/bin/python3

a = 21
b = 10
c = 0

c = a + b
print ("Line 1 - Value of c is ", c)

c += a
print ("Line 2 - Value of c is ", c )

c *= a
print ("Line 3 - Value of c is ", c )

c /= a 
print ("Line 4 - Value of c is ", c )

c  = 2
c %= a
print ("Line 5 - Value of c is ", c)

c **= a
print ("Line 6 - Value of c is ", c)

c //= a
print ("Line 7 - Value of c is ", c)

```

### Decision Making
Decision-making is the anticipation of conditions occurring during the execution of a program and specified actions taken according to the conditions.

Decision structures evaluate multiple expressions, which produce TRUE or FALSE as the outcome. You need to determine which action to take and which statements to execute if the outcome is TRUE or FALSE otherwise.

Following is the general form of a typical decision making structure found in most of the programming languages −

example IF Statement
``` python
var1 = 100
if var1:
   print ("1 - Got a true expression value")
   print (var1)

var2 = 0
if var2:
   print ("2 - Got a true expression value")
   print (var2)
print ("Good bye!")
```
example if else statement

```python

amount = int(input("Enter amount: "))

if amount<1000:
   discount = amount*0.05
   print ("Discount",discount)
else:
   discount = amount*0.10
   print ("Discount",discount)
    
print ("Net payable:",amount-discount)

```

Example elif statement: 

```
#!/usr/bin/python3

amount = int(input("Enter amount: "))

if amount<1000:
   discount = amount*0.05
   print ("Discount",discount)
elif amount<5000:
   discount = amount*0.10
   print ("Discount",discount)
else:
   discount = amount*0.15
   print ("Discount",discount)
    
print ("Net payable:",amount-discount)
```

## Loops

### While loops 

While example
```
count = 0
while (count < 9):
   print ('The count is:', count)
   count = count + 1

print ("Good bye!")
```

### while infinite
``` python
var = 1
while var == 1 :  # This constructs an infinite loop
   num = int(input("Enter a number  :"))
   print ("You entered: ", num)

print ("Good bye!")
```

### For loops
for using numbers:
``` python
for var in range(5):
   print (var)
```
For using lists or strings

```python
for letter in 'Python':     # traversal of a string sequence
   print ('Current Letter :', letter)
print()
fruits = ['banana', 'apple',  'mango']

for fruit in fruits:        # traversal of List sequence
   print ('Current fruit :', fruit)

print ("Good bye!")
```

or using index (but why???)

``` python
#!/usr/bin/python3

fruits = ['banana', 'apple',  'mango']
for index in range(len(fruits)):
   print ('Current fruit :', fruits[index])

print ("Good bye!")
```

### Controls inside a loop

BREAK statemeant:
``` python
no = int(input('any number: '))
numbers = [11,33,55,39,55,75,37,21,23,41,13]

for num in numbers:
   if num == no:
      print ('number found in list')
      break
else:
   print ('number not found in list')
```

Continue statment:
```
for letter in 'Python':     # First Example
   if letter == 'h':
      continue
   print ('Current Letter :', letter)
```















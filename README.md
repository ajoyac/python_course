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
 * [Basic Syntax](#basic-Syntax)
   - Interactive mode Programing
   - Reserverd Words
   - Lines and Indentation
   - Comments in python
 * Variables types
  -  Assign Values to Variables
  -  Standard Data Types
 * Basic Operators 
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

 if you don't have it already go to: [https://www.python.org/](https://www.python.org/)
 for windows there is a msi version 
 
 for linux you might already have it or check your pkg manager it might be something like this(or even you already have it)
 
 `sudo apt install python3`
 
 `sudo apt-get install python3`
 
 `yum install python3`
 
 `pacman install python3`
 
 for macos check home brew
 `brew install python`
 
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
there are word you cant use

![ reserverd words](https://cdn-images-1.medium.com/max/1200/1*TjYrRbTtdGArQwBywBJHgg.png)

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

#!/usr/bin/python3

# First comment
```python
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

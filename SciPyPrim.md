# Introduction to Python

# Introduction

This was written as an introduction to programming for students with a background in STEM, but no experience with learning the basics of programming. Many college level courses include programming in the curriculum, but fail to give students a thorough understanding of the foundation of programming with a particular language. In this guide, I attempt to remedy that, walking the reader through the most basic points of programming to help the new user become more acclimated with Python.

## Variables

Variables in programming are not quite the same as what they are for mathematics, but they are not that different. A variable for a computer is a way of storing information that will be recalled later. The way this works is that when a variable is defined, the computer sets aside a block of memory for this information to occupy. That is a simple enough process, but how big is the piece of reserved space in memory? That is defined by the type of the variable. A *** variable type *** is a piece of information that is included in every majorly used program that encodes how large the reserved memory block needs to be, and exactly what type of information it will be holding. It should be noted that programming languages and computers are very particular about information type agreeing with variable type.

Here are the main types of variables:

- Character
- String
- Integer
- Float
    - half
    - single
    - double
    - quadruple
    - octuple
- Boolean

**Character** type variables are individual letters. These are not used often for the purpose of mathematics.

To define a character,
```python
my_char = 'a'
```

**String** type variables are used in print statements and consist of a grouping of character variables.

To define a string,
```python
my_string = 'string'
```

**Integer** type variables are defined as the same as mathematical integers, that is to say that they are whole numbers, including zero, that are positive or negative.

To define an integer,
```python
my_int = 1
```

**Float** type variables are decimal numbers. The precision of these can vary by programming language: the common types are single, double, and quadruple precision, but double precision is the default for python. Note that there are multiple subcategories (half, single, double, quadruple, and octuple). These refer to the precision of the variable, which encodes how many decimal places it can store. Double is the typical standard for most modern programs, however in scientific computing, both the less precise and the more precise options have uses.

To define a float,
```python
my_float = 2.
```

**Boolean** type variables contain one of two values: True or False. These are often used to create infinitely running loops or to break out of loops

To define a boolean,
```python
my_bool = True
```
These can be further classified into two major types:
- alphanumeric variables
    - char
    - string
- numeric variables
    - boolean
    - integer
    - float

These lists have both been ordered in a specific order: from least to greatest with respect to precision. What does this mean? To explain this, it is important to now define the term precision.

*** Precision ***, in variables, refers to the amount of detail stored in one variable. For numeric values, this is easy to see. A boolean has only two possible values that it can hold: 0 and 1, which makes it the least precise numeric variable. Beyond that, an integer can hold any integer value within the bounds of a particular computer.



### Variable Naming Conventions
Some common and popular naming conventions for python variables, according to the PEP 8 style guide:
- Never use the characters 'l' (lower case L), 'O' (capital o), or 'I' (capital letter i) as single character variable names

    - If these options are tempting, use the opposite case instead, as it is significantly more distinguishable
    
    
- Variable names should be lowercase, with words separated by underscores as necessary to improve readability. mixedCase is allowed only in contexts where that's already the prevailing style.

## Arrays

Arrays are a way of grouping together variables, and they exist in one form or another in just about every programming language. The uses for arrays are expansive, as having a way of systematically organizing and indexing variables that should be grouped together is invaluable for efficient programming. 

Arrays can be created for most variable types, such as integer, float, and string. Additionally, in some programming languages, including python, strings are classified as an array of characters, and include similar functionality

Arrays are denoted by square brackets around the values, eg. [1,2,3] or ['a','b','c']. 

These assigned values are accessed by referencing with an index value. eg. a[1] These index values start numbering at 0 and go to N-1 in an array of length N.

In many programming languages, the size of an array must be defined when the array is created and it is not flexible. However, in Python, this is not the case. Python allows for arrays to be dynamically resized as needed and will automatically accomodate elements being added or removed so long as the computer has available memory space.

Some situations where arrays are required in python:
- for loop iterations (covered later on)
- plotting/data visualization

Some common uses for these arrays are:
- discretized points in space
- discrete time steps 
- commonly used ordered values.

Ex. Defining an empty array
```python
my_array = []
```

Within the array, you can use any type of variable (or array of variables) as each item, separating them with commas.

Arrays in python also have built in functions, some of the most useful ones for scientific programming are append, remove, and insert.

These are accessed after creating an array by putting a '.' after the array and typing the function name with the parameter(s) in parentheses.

Ex. Accessing Array Functions
```python
a = []
a.append(3)
a.append(4)
a.remove(3)
a.insert(0,1)
```

## Conditionals

Conditionals in python are a way to for run only in a specified condition. This is done through *** logical expressions *** (also called boolean expressions). These logical expressions always evaluate to being either true or false, therefore the following forms of python conditionals work based on the logical expression being true or false.

- if
- if...else
- if...else if...else

*** if *** used to :

Ex. 
```python
if a == 1:
    print(a)
```

*** if...else *** is used in order to allow something to happen if the condition is not true.

Ex.
```python
if a==1:
    print(a)
else:
    print("a is not 1")
```

*** if...else if...else *** is a way of combining multiple if statements in order for code to look cleaner. These are not built into every language, however most programming languages have some form of this type of statement.

Ex.
```python
if a==1:
    print("a is {}".format(1))
else if a==2:
    print("a is {}".format(2))
else:
    print("a is not 1 or 2")
    
```

## Loops

There are 2 different classes of loop in python (3 in many other languages). These are ***For*** and ***While*** loops. Generally, a for loop is a loop that iterates from a start point to an end point that are defined when the loop is initialized, and a while loop defines only the end condition, which follows the same rules as conditionals. 

In python, they are defined slightly different:

*** For Loop***: iterates over a list.

```python
for a in range(10):
    print(a)
```

*** While loop***: iterates until the end case is reached.

```python
b = 0
while b<10:
    print(b)
    b+=1
```

## Math in Python

Basic operations like addition, subtraction, multiplication, and division are done by using their symbols, +, -, *, / respectively. Typically, these are assigned to a variable or done by modifying an existing variable. In code, this looks as follows:

Addition:
```python
a = 1 + 2
```

Subtraction
```python
s = 4 - 1
```

Multiplication
```python
m = 3 * 3
```
One important note with math is that if there are two integers, an integer operation will be done. If either or both inputs are floats, then a float operation is conducted, and the distinction between the two is significant, but mainly for division. Float division uses decimals, however integer division truncates.

Division
```python
d = 1. / 2.
```

Integer division
```python
D = 1 // 2
```


## Packages

importing a package in python is done as follow:

```python
import package_name
```

additionally, you can optionally add an alternative name to reference the package within the program,

```python
import package_name as pack
```
This is usually done to give the package a more convenient and accessible name, or a less confusing name if there are similar packages.

Additionally, packages can be imported by a selected part too,

```python
from package_name import function
```
or the same thing with an alternate syntax,
```python
import package_name.function
```

Some frequently used packages for scientific programming in python are:
1. math
1. cmath
1. numpy
1. scipy
1. matplotlib
1. vpython
Each of these packages has a documentation page that can be found on google by searching for "PackageName documentation". The documentation will contain information such as the names, parameters, and uses of many or all available functions in the current version of the package. 

## Object Oriented Principles

Normally in an introduction to scientific programming, object oriented aspects of python will be ignored because scientific computation has been gravitating towards functional programming since the 1980s. However, with python, understanding some key concepts involved with object oriented programming can significantly improve understanding of packages in python.

*** Object-oriented programming *** is a type of programming language structure designed around the idea that there should be a base "object" that has attributes known as "properties, and functions, known as "properties". These attributes and properties belong to the object, and any objects based off of the original object. This concept of passing traits is known as *** inheritance ***. 

When an object has a method, it is accessed in the following way:

```
class_name.method_name(parameters)
```

More specifically, for packages in python, it utilizes the following form:

```python
package_name.function(parameters)
```

Ex. A more specific example using Numpy
```python
numpy.linspace(0,10,101)
```

## File Input and Output (I/O)

File input in python as done by reading in a file 
This process uses the following steps:
1. open a file
1. read the file
1. close the file

Ex. 1
```python
f = open('groceries.txt','r')
print(f.read())
f.close()
```

Ex. 2
```python
f = open('groceries.txt','r')
for line in f.readlines():
    print(line)
f.close()
```
Ex. 3, The pythonic way
```python
with open('groceries.txt') as f:
    print(f.read())
```
https://docs.python.org/3/tutorial/inputoutput.html

# Thinking Like a Programmer


## Reading Code

No matter whether you're a novice or an expert with programming, being able to read and understand a program is incredibly important. While some sections of code may be well commented, up to the modern standards for formatting the language, and in a language you understand, not every program will be. Since there is such a wide variety to the programs that students and professsionals have to deal with and utilize, it is critically important to be able to read code in ways that give insight and understanding.

1. Look for comments

2. Look for well defined blocks
    - **imports**    
        Import blocks contain segments of code that contain lines like "import numpy" or "from scipy import linalg" or 
        other similarly formatted lines that are importing some external package into the program.
        
    - **initialization**    
        Initialization blocks are typically found early in the program
        
    - **functions**    
        These vary in appearance, but the important qualities to look for are the parameters, what the function 
        reads in, and the return statement, which tells you what is returned when the function is called.
        
    - **main loop**    
        The main loop of the function is whatever the primary section of code is. This can be identified by 
        noting that it is the driving portion of code that calls other functions or organizes the primary
        objective of the program.
        
    - **conditionals**    
        Conditional blocks contain any type of if statement or other logical statement, these are easily 
        identifiable by keywords like "if", "else", and "elseif"
        
    - **other familiar looking sections**    
        These are any other sections of code that look like something you may have seen before! Your previous 
        programming experiences, regardless of the language used, can be relevant here.    
        
3. Try to walk through the program as you read through

## Comments

It cannot be stressed enough just how important comments are. While writing the program, the code will almost always make sense to the author or authors of the code, but if anyone aside from the authors attempt to read it, it may as well be a foreign language. 

### What Makes a Good Comment?

A good comment follows PEP 8 standards. The section from the PEP 8 page reads:
> Comments that contradict the code are worse than no comments. Always make a priority of keeping the comments up-to-date when the code changes!

>Comments should be complete sentences. The first word should be capitalized, unless it is an identifier that begins with a lower case letter (never alter the case of identifiers!).

>Block comments generally consist of one or more paragraphs built out of complete sentences, with each sentence ending in a period.

>You should use two spaces after a sentence-ending period in multi- sentence comments, except after the final sentence.

>When writing English, follow Strunk and White.

>Python coders from non-English speaking countries: please write your comments in English, unless you are 120% sure that the code will never be read by people who don't speak your language.



## Solving real problems

Solving more realistic problems is the most important part of scientific computing. The goal is to create a complete model of a situation as best as possible, with all the components of the code working together to simulate some version of reality.

### Breaking the process into pieces: Discretization

In programming, the first step in solving it is to discretize the system. A continuous system, while more often able to be analytically analyzed, is not capable of being identically translated into a program because of the discretized nature of computing. However, the problem of dealing with continuous systems is entirely avoided by breaking up continuous systems into small pieces.

### Dealing with Space

Space discretization is most often achieved by making an array in space. In C based languages, this can be done by defining an array manually. In python, there are tools in numpy that make this significantly easier such as **arange** and **linspace**.
```python
import numpy as np

#np.linspace(START,END,Number of Steps)
print(np.linspace(0,1,11))

print("\n\n")

#np.linspace(START(inclusive),END(exclusive),STEP SIZE)
print(np.arange(0,1.01,.1))
```
### Dealing with Time

While space can be conveniently broken up into an array that represents each point in space, breaking a sytem up to represent different times has different approaches. In space discretization, where each point is to be located is usually specified with the creation of the system.The analogous of that for time is picking the time step while time is moving forward. 

The new concept that time deals with that space does not is the updating process. The points in space are fixed, they do not shift where they are located. However the reason for time entering a function is for systems that are dynamic. Since the system is not fixed, it requires a variable, like position or temperature, being updated with each step forward in time.

### Utilizing functions

The general rule of thumb is that any time a task needs to be done multiple times the exact same way, or with repetitive varying parameters, the repetitive portion of code should be replaced with a function. Even if something is typed out twice, it could be made more efficient by instead creating a function that can be called in one simple line.

## Debugging code

### Popular Debugging Methods

1. Print Debugging
    >This is done by inserting print statements throughout your code, wherever you deem necessary, in order to find out which values are not coming out correctly so that the location and type of error can be pinpointed.
1. Rubber Duck Debugging
    >This is a process where a rubber duck, friend, or other placeholder to talk at is set up. You then talk through what the code is supposed to be doing in each step of the process. 
   
*note: on a UNIX system, when a program is run from a terminal (using bash or another similar shell), it is possible put the output of the program into a new file or concatenate it onto the end of an existing file by using
- python FILE.py > outputfile.dat (for new file/overwrite)
- python FILE.py >> outputfile.dat (for existing file/concatenate)
[comment]: <> (Maybe more to be added?)

### Common Errors

2. Array Out of Bounds
    >This is an error that shows up when the index you are trying to access in an array is greater than the total number of indeces.
2. Unexpected EOF (End of File)
    >This is an error that occurs when one or more parentheses are missing (often in a print statement towards the end, but this can occur anywhere)
2. Missing Parentheses
    >This error follows the namesake, and occurs when parentheses are missing (i.e. print "dog" instead of print("dog")
2. Missing Arguments
    >This error occurs when the number of arguments given to a function do not line up with the number of required arguments.


## Utilizing External Resources

Advanced programmers may like to think that they know the answers to whatever arises, but someone that claims to have all the solutions to every problem that may arise is clearly a liar! Most programmers either dabble a little in many languages obtaining a passable proficiency without delving too far into one particular language, or become an expert on one specific language or type of task. 

For average users, students, professionals, and anybody that isn't an expert in the specific question they're asking, or even an expert that just wants a second opinion, external resources are the key to everything. Programming is a puzzle, and there are many different pathways by which the answer can come about. Since there are so many ways to approach the puzzle, answers, hints, and collaborators are everywhere! 

Searching for problems through google is undoubtedly the most useful skill programmers know. It allows you to avoid reinventing the wheel or getting stumped by a portion of the code by having access to the thousands of people before you that have been stumped by that issue. 

### Reading Documentation
For many packages in python, and other existing programs have existing documentation online. These documentation pages often include a list of functions included in the package and the arguments each function takes. By searching the name of a particular package on google, one of the first links is usually to the documentation page. Knowing how to use a function and what inputs it takes and outputs it returns are extremely useful for utilizing new packages.

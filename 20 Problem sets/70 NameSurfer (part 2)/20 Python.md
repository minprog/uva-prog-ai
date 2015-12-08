# Python!

For the second part of the assignment you'll write some programs in the 
programming language Python. This is to show you how much difference there can 
be with the right language for the job and how easy it can be to pick up a new 
language with a couple of languages under your belt. Python is a flexible 
language with a clean syntax, making it a popular choice for many programmers.

For this assignment you have to process the data in the `names-data.txt` file 
and write out some statistics, something that is definitely easier in Python 
than it would be in Java. For this reason, a lot of AI students end up learning 
Python later on in their bachelors anyway, but we thought we'd give you a head 
start.

### Python version

We will be working with Python `3.4`, which already comes installed on your VM. 
Note if you type `python` in the terminal, you will run the old `2.7` version.
In order to run the correct version, **you should use the` python3 `command**. If 
you find this confusing and want to make sure you always run the right version, 
you can simply rename the command `python`. In the terminal, type:
    
    alias python=python3

Now, whenever you run Python, you will run version `3.4`. The reason the default 
version is `2.7`, is because the newer `3.x` versions were not compatible with 
the older versions of Python. As a result all the libraries and tools written for 
Python also needed to be updated to Python 3 be useable. Adoption has been slow 
(Python 3 was released in 2010), but most tools currently support Python 3. 
There are still some tools you can't use though and as a result most operating 
systems still come with version `2.7` by default. However, we won't be needing these 
specific tools and Python 3 is the only version that is actively developed, so 
we will use that.

### Settting up

You can write Python in `gedit` or any other text editor of your prefences. Make 
sure to save your file with a `.py` extension. You can then run the file in the 
terminal using

    python3 my_file.py

### Grading

Learning a new language in a week can be tall order. Given that we have not 
taught you anything about Pythonic design or style, you will not be graded in 
these categories for this part of the assigment. The problems are stated as
open ended as possible, to allow you to come up with your own solutions. As 
that can be difficult in a completely new langauge, we will not also
grade the correctness of your solutions.

So, all that remains is the scope of assignment, which will count towards your 
grade for this week. **This means your solution does not have to be perfect 
or elegantly designed for a good grade.** All we want you to do is to really try 
and solve the problems and learn as much of the language as you can in the 
process. It will come in very handy at some point in your bachelor, for sure.


## Python vs Java

Python supports many of the same imperative constructs you learned in Java, like 
the `if` statement, `for` and `while` loops and functions using `returns`. So, 
learning Python should feel a lot more familiar than when you transitioned from
Prolog to Java. However, there are some big difference to keep in mind:

### Whitespace

In Java you started a block of code with `{` and marked the end with `}`. You 
used whitespace (tabs or spaces) to make the code more readible, but that did 
not affect the actual code. Python does not use brackets to delimit a block of 
code, but actually counts where the whitespace starts and ends. The start of a 
block is still marked with `:`, but the end is computed based on the whitespace.
*Make sure not to mix your tabs and spaces in Python, it will make for some hard 
to find errors.*

Also, in Python there is no need for the `;` at the end of the line. Python simply
assumes the line stops where you placed the enter. Below is some sample code to 
show the difference

`Java`
    
    if (x > 100) {
        x += 10;
    }
    System.out.println(x);   

`Python`
    
    if x > 100:
        x += 10
    print(x)

### Variable types

In Python there is no need to declare the type of the variable. If you assign a
value to a variable, Python will just create a variable of the most logical type.
The types in Python are very similar to the types in Java

| Python | Java    |
| ------ | ------- |
| int    | int     |
| float  | double  |
| bool   | boolean |
| string | String  |

Below is a sample from the interpreter, an interactive version of Python. You 
can try it yourself by typing `python3` in the terminal, allowing you to quickly 
test things. Quit the interpreter by typing `quit()`

    >>> x = 3
    >>> type(x)
    <class 'int'>
    >>> x = 5.0
    >>> type(x)
    <class 'float'>
    >>> quit()

It can be very convenient to not have to explicitly state the type of each 
variable. As you can see, you can even just change the type of a variable 
with a new assignment. However, this means you can just overwrite one variable with
another without a problem, which can lead to some hard to track down bugs if you 
are not careful with your variable names.

### Interpreted language

Python code is not compiled beforehand like Java is. It is simply read into 
Python line by line until the code has completed or an error is produced. This 
can be a very nice feature, but it does mean that you will not know if your code 
contains any errors until you actually run it.

This also means you don't need to write a main or run function, but you can just 
start writing code at the top of the file. A *Hello world* in Python thus becomes 
extremely simple. This is all the code you would need in `hello-world.py`
    
    print("Hello World!")
 
One result of running code this way that may seem strange at first, is that the 
order in which you define functions can actually matter, i.e. you cannot call 
functions that have not been defined yet (even though they might be defined 
later in the file). The most common way around this, is to write all you 
functions first in the file, including a simple `main()` function and then 
calling it at the bottom of the file. This ensures that all functions will be
read into memory before you start executing the code.

    def main():
        print("Hello World!")

    if __name__ == "__main__":
        main()

## The assignments

Below are the assignments. **You only need to attempt 2 of them for full credit 
on the assignment**

### Top 10 names

Read in the `names-data.txt` or `dutch-names.txt` file and determine the top 10
names for each of the 11 decades. Print the results in the terminal, in order 
of the ranking for each decade.

    The top 10 names for the 1900's were:
    Mary, William, Margaret, George, Ruth, Elisabeth, Robert, Marie, Mildred, Henry
    ....
    ....

Save the file as `top-10-names.py`

### First letter popularity

Read in the `names-data.txt` or `dutch-names.txt` file and determine in which 
decade a letter was most popular as the first letter of a name. You may use 
whatever definition of *most popular* makes sense to you based on the data files
you have. Print the results for each letter in the alphabet to the terminal.

    Names starting with the letter A were most popular in the 1950's
    Names starting with the letter B were most popular in the 1940's
    Names starting with the letter C were most popular in the 2000's
    ....
    ....

Save the file as `first-letters.py`

### Create `dutch-names.txt`

When we requested the statistics for the Dutch names for the last 11 decades, 
the file we got was not in exactly the same format as `names-data.txt` (as almost 
always the case for any data you get). So we wrote a Python script to convert 
it to the same format. Here are the files we got:

* [Male names](Namen_man_per_10_jaar.csv)
* [Female names](Namen_vrouw_per_10_jaar.csv)

Try and create a file `dutch-names.txt` that contains the combined data from 
both files using popularity rankings (instead of the actual counts) for each 
decade. Your file should end up looking like this: [link](dutch-names.txt)

Save the file as `dutch-names.py`


## Extra reading on Python

The structures below might be useful for the assignments. The first link provided 
is to the book [Think Python](http://www.greenteapress.com/thinkpython2/html/index.html), 
which walks through the topics using short examples. The second link is to the 
[Python docs](https://docs.python.org/3/tutorial/index.html), which provides a 
readable tutorial and complete reference for the language.

There is no need to read all of these for the assignment. You might prefer the 
one source over the other, or just to Google it for yourself. It is just provided 
here as an easy point of reference for the elements you could want to use.

### Loops

Loops in Python are easy. Usually you just loop over the elements in the list 
directly. This is the most common `for` loop in Python

    >>> letters = ['a', 'b', 'c']
    >>> for let in letters:
    >>>     print(let)
    a
    b
    c

If you want to use the index directly, you can use range to compute the indices.

    >>> for i in range(3):
    >>>     print(i)
    0
    1
    2

You can then use the indices to access the elements, just like you would in Java.

    >>> letters = ['a', 'b', 'c']
    >>> for i in range(len(letters)):
    >>>     print(i, letters[i])
    0 a
    1 b
    2 c

* [Think Python](http://www.greenteapress.com/thinkpython2/html/thinkpython2008.html)
* [Python docs](https://docs.python.org/3/tutorial/controlflow.html#for-statements)

### Lists

Lists are used to store multiple values together. They are most like `ArrayLists`
in Java, as they have no fixed size and just can just add and remove elements 
from it. In Python, the elements don't even have to be the same type!

    >>> x = []
    >>> x.append(8)
    >>> x.append('A')
    >>> print(x)
    [8, 'A']

You can use the same square bracket notation `[i]` as in Java to retrieve or update 
elements. You can even create a subset of the list using the `:`, look up the
section on slices (10.5) below.

* [Think Python](http://www.greenteapress.com/thinkpython2/html/thinkpython2011.html)
* [Python docs](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)

### Strings

Strings in Python work a lot like Strings in Java. In addition, string in Python 
can be indexed and sliced using square brackes in exactly the same way as lists 
can.

    >>> x = "Hello World"
    >>> x[2:9]
    'llo Wor'

* [Think Python](http://www.greenteapress.com/thinkpython2/html/thinkpython2009.html)
* [Python docs](https://docs.python.org/3/library/stdtypes.html#string-methods)

### Dictionaries

Dictionaries work like `HashMaps` in Java; hey map a key to a value. A dictionary 
can be created with curly brackets `{}`. Values can be added or retrieved using 
the familiar square brackets.

    >>> d = {}
    >>> d['Mary'] = 1
    >>> d['William'] = 2
    >>> print(d)
    {'William': 2, 'Mary': 1}

* [Think Python](http://www.greenteapress.com/thinkpython2/html/thinkpython2012.html) 
* [Python docs](https://docs.python.org/3/library/stdtypes.html#mapping-types-dict)

### Files

Reading files in Python is very simple. Just use the `open()` function. The first
argument is the filename and the second is `'r'`, indicating you want to read
file. 
    
    >>> f = open('test.txt', 'r')
    >>> f.readlines()
    ['This is a test\n', 'file.\n']

* [Think Python](http://www.greenteapress.com/thinkpython2/html/thinkpython2015.html)
* [Python docs](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files)


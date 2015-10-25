# Console Programs

Your job in this assignment is to write programs to solve each of these problems.

## Getting starting

For these programs we will also be using the files that were provided with 
`pset2.zip` from the Graphics Program assignment. 

## Problem 5: `FindRange.java`

Write a `ConsoleProgram` that reads in a list of integers, one per line, until a
sentinel value of 0 (which you should be able to change easily to some other
value). When the sentinel is read, your program should display the smallest and
largest values in the list, as illustrated in this sample run:

    This program finds the smallest and largest integers
    in a list. Enter values, one per line, using a 0
    to signal the end of the list.
    ? 17
    ? 42
    ? 11
    ? 19
    ? 35
    ? 0
    The smallest value is 11
    The largest value is 42

Your program should handle the following special cases:

* If the user enters only one value before the sentinel, the program should
  report that value as both the largest and smallest.
* If the user enters the sentinel on the very first input line, then no values
  have been entered, and your program should display a message to that effect.

## Problem 6: `Hailstone.java`

Douglas Hofstadter’s Pulitzer-prize-winning book *Gödel, Escher,
Bach*. Hofstadter’s book contains many interesting mathematical puzzles, many of
which can be expressed in the form of computer programs. Of these, most require
programming skills well beyond the second week of this course. However, in
Chapter XII, Hofstadter mentions a wonderful problem that is well within the
scope of the covered control statements. The problem can be expressed as
follows:

1. Pick some positive integer and call it *n*.  
2. If *n* is even, divide it by two.  
3. If *n* is odd, multiply it by three and add one.  
4. Continue this process until *n* is equal to one.  

On page 401 of the Vintage edition, Hofstadter illustrates this process with the
following example, starting with the number 15:

    15 is odd, so I make 3n + 1: 46
    46 is even, so I take half: 23
    23 is odd, so I make 3n + 1: 70
    70 is even, so I take half: 35
    35 is odd, so I make 3n + 1: 106
    106 is even, so I take half: 53
    53 is odd, so I make 3n + 1: 160
    160 is even, so I take half: 80
    80 is even, so I take half: 40
    40 is even, so I take half: 20
    20 is even, so I take half: 10
    10 is even, so I take half: 5
    5 is odd, so I make 3n + 1: 16
    16 is even, so I take half: 8
    8 is even, so I take half: 4
    4 is even, so I take half: 2
    2 is even, so I take half: 1
    
As you can see from this example, the numbers go up and down, but eventually—at
least for all numbers that have ever been tried—comes down to end in 1. In some
respects, this process is reminiscent of the formation of hailstones, which get
carried upward by the winds over and over again before they finally descend to
the ground. Because of this analogy, this sequence of numbers is usually called
the **Hailstone sequence**, although it goes by many other names as well.

Write a `ConsoleProgram` that reads in a number from the user and then displays
the Hailstone sequence for that number, just as in Hofstadter’s book, followed
by a line showing the number of steps taken to reach 1. For example, your
program should be able to produce a sample run that looks like this:

    This program computes Hailstone sequences.
    Enter a number: 17
    17 is odd, so I make 3n+1 = 52
    52 is even, so I take half = 26
    26 is even, so I take half = 13
    13 is odd, so I make 3n+1 = 40
    40 is even, so I take half = 20
    20 is even, so I take half = 10
    10 is even, so I take half = 5
    5 is odd, so I make 3n+1 = 16
    16 is even, so I take half = 8
    8 is even, so I take half = 4
    4 is even, so I take half = 2
    2 is even, so I take half = 1
    The process took 12 steps to reach 1.

The fascinating thing about this problem is that no one has yet been able to
prove that it always stops. The number of steps in the process can certainly get
very large. How many steps, for example, does your program take when *n* is 27?


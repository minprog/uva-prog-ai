# Homework Week 1

The homework for this week covers the chapters 1, 2, and 3 from
[Think Java]. You should read these chapters before you start on the exercises.

Please take note that the exercises are based on the exercises in *Think Java*,
but are not identical.

Submit your answers on the submit tab when you are finished.

[Think Java]: http://www.greenteapress.com/thinkapjava/

## Chapter 1

### Exercise 1
Computer scientists have the annoying habit of using common English words to
mean something other than their common English meaning. For example, in English,
statements and comments are the same thing, but in programs they are different.

The glossary at the end of each chapter is intended to highlight words and
phrases that have special meanings in computer science. When you see familiar
words, don't assume that you know what they mean!

1. In computer jargon, what's the difference between a statement and a comment?
2. What does it mean to say that a program is portable?
3. What is an executable?

### Exercise 2
Before you do anything else, find out how to compile and run a Java program in
your environment. Some environments provide sample programs similar to the
example in Section 1.5.

1. Type in the "Hello, world" program (see Section 1.5), then compile and run
   it.
2. Add a print statement that prints a second message after the "Hello,
   world!". Something witty like, "How are you?". Compile and run the program
   again.
3. Add a comment to the program (anywhere), recompile, and run it again. The new
   comment should not affect the result.

This exercise may seem trivial, but it is the starting place for many of the
programs we will work with. To debug with confidence, you have to have
confidence in your programming environment. In some environments, it is easy to
lose track of which program is executing, and you might find yourself trying to
debug one program while you are accidentally running another. Adding (and
changing) print statements is a simple way to be sure that the program you are
looking at is the program you are running.

### Exercise 3
It is a good idea to commit as many errors as you can think of, so that you
see what error messages the compiler produces. Sometimes the compiler tells
you exactly what is wrong, and all you have to do is fix it. But sometimes
the error messages are misleading. You will develop a sense for when you can
trust the compiler and when you have to figure things out yourself.

1. Remove one of the open squiggly-braces.
2. Remove one of the close squiggly-braces.
3. Instead of `main`, write `mian`.
4. Remove the word `static`.
5. Remove the word `public`.
6. Remove the word `System`.
7. Replace `println` with `Println`.
8. Replace `println` with `print`. This one is tricky because it is a logic
   error, not a syntax error. The statement `System.out.print` is legal, but it
   may or may not do what you expect.
9. Delete one of the parentheses. Add an extra one.

## Chapter 2

### Exercise 1
1. Create a new program named `Date.java`. Copy or type in something like the
   "Hello, World" program and make sure you can compile and run it.
2. Following the example in Section 2.4, write a program that creates variables
   named `day`, `date`, `month` and `year`. `day` will contain the day of the
   week and `date` will contain the day of the month. What type is each
   variable? Assign values to those variables that represent today's date.
3. Print the value of each variable on a line by itself. This is an intermediate
   step that is useful for checking that everything is working so far.
4. Modify the program so that it prints the date in standard European form:
   `Saturday, 16 July, 2011`.
5. Modify the program again so that the total output is:

    European format:
    Saturday 16 July, 2011
    American format:
    Saturday, July 16, 2011

The point of this exercise is to use string concatenation to display values with
different types (`int` and `String`), and to practice developing programs
gradually by adding a few statements at a time.

### Exercise 2
1. Create a new program called `Time.java`. From now on, I won't remind you to
   start with a small, working program, but you should.
2. Following the example in Section 2.6, create variables named `hour`, `minute`
   and `second`, and assign them values that are roughly the current time. Use a
   24-hour clock, so that at 2pm the value of hour is 14.
3. Make the program calculate and print the number of seconds since midnight.
4. Make the program calculate and print the number of seconds remaining in the
   day.
5. Make the program calculate and print the percentage of the day that has
   passed.
6. Change the values of `hour`, `minute` and `second` to reflect the current
   time (I assume that some time has elapsed), and check to make sure that the
   program works correctly with different values.

The point of this exercise is to use some of the arithmetic operations, and to
start thinking about compound entities like the time of day that that are
represented with multiple values. Also, you might run into problems computing
percentages with `ints`, which is the motivation for floating point numbers in
the next chapter.

HINT: you may want to use additional variables to hold values temporarily during
the computation. Variables like this, that are used in a computation but never
printed, are sometimes called intermediate or temporary variables.

## Chapter 3

### Exercise 1
Draw a stack frame that shows the state of the program below when `main` invokes
`printTime` with the arguments `11` and `59`.

    public static void printTime(int hour, int minute) {
       System.out.print(hour);
       System.out.print(":");
       System.out.println(minute);
    }

### Exercise 2
The point of this exercise is to practice reading code and to make sure that you
understand the flow of execution through a program with multiple methods.

1. What is the output of the following program? Be precise about where there are
   spaces and where there are newlines.
   
   HINT: Start by describing in words what `ping` and `baffle` do when they are
   invoked.
2. Draw a stack diagram that shows the state of the program the first time
   `ping` is invoked.

    public static void zoop()
    {
       baffle();
       System.out.print("You wugga ");
       baffle();
    }
    
    public static void main(String[] args)
    {
       System.out.print("No, I ");
       zoop();
       System.out.print("I ");
       baffle();
    }
    
    public static void baffle()
    {
       System.out.print("wug");
       ping();
    }
    
    public static void ping()
    {
       System.out.println(".");
    }

### Exercise 3
The point of this exercise is to make sure you understand how to write and
invoke methods that take parameters.

1. Write the first line of a method named `zool` that takes three parameters: an
   `int` and two `Strings`.

2. Write a line of code that invokes `zool`, passing as arguments the value
   `11`, the name of your first pet, and the name of the street you grew up on.
   
### Exercise 4
The purpose of this exercise is to take code from a previous exercise and
encapsulate it in a method that takes parameters. You should start with a
working solution to Exercise 2.1.

1. Write a method called `printEuropean` that takes the day, date, month, and
   year as parameters and that prints them in European format.
2. Test your method by invoking it from `main` and passing appropriate
   arguments. The output should look something like this (except that the date
   might be different): `Saturday, 16 July, 2011`
3. Once you have debugged `printEuropean`, write another method called
   `printAmerican` that prints the date in American format.

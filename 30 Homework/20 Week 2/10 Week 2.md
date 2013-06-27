# Homework Week 2

The homework for this week covers the chapters 4, 6, and 7 from
[Think Java]. You should read these chapters before you start on the exercises.

Please take note that the exercises are based on the exercises in *Think Java*,
but are not identical.

Submit your answers on the submit tab when you are finished.

[Think Java]: http://www.greenteapress.com/thinkapjava/

## Chapter 4

### Exercise 1
This exercise reviews the flow of execution through a program with multiple
methods. Read the following code and answer the questions below.

    public class Buzz
    {
       public static void baffle(String blimp)
       {
          System.out.println(blimp);
          zippo("ping", -5);
       }
    
       public static void zippo(String quince, int flag)
       {
          if (flag < 0)
          {
             System.out.println(quince + " zoop");
          }
          else
          {
             System.out.println("ik");
             baffle(quince);
             System.out.println("boo-wa-ha-ha");
          }
       }
    
       public static void main(String[] args)
       {
          zippo("rattle", 13);
       }
    }

1. Add the comment `1` next to the first statement of this program that will be
   executed. Be careful to distinguish things that are statements from things
   that are not.
2. Add the comment `2` next to the second statement, and so on until the end of
   the program. If a statement is executed more than once, it might end up with
   more than one number next to it, separate numbers with a comma.
3. What is the value of the parameter `blimp` when `baffle` gets invoked?
4. What is the output of this program?

### Exercise 2
The first verse of the song "99 Bottles of Beer" is:

99 bottles of beer on the wall, 99 bottles of beer, ya' take one down, ya' pass
it around, 98 bottles of beer on the wall.

Subsequent verses are identical except that the number of bottles gets smaller
by one in each verse, until the last verse:

No bottles of beer on the wall, no bottles of beer, ya' can't take one down, ya'
can't pass it around, 'cause there are no more bottles of beer on the wall!

And then the song(finally) ends.

Write a program that prints the entire lyrics of "99 Bottles of Beer." You might
want to write additional methods to separate the major functions of the program.

As you develop your code, test it with a small number of verses, like "3 Bottles
of Beer."

The purpose of this exercise is to take a problem and break it into smaller
problems, and to solve the smaller problems by writing simple methods.

### Exercise 3
What is the output of the following program?

    public class Narf
    {
       public static void zoop(String fred, int bob)
       {
          System.out.println(fred);
          if (bob == 5)
          {
             ping("not ");
          }
          else
          {
             System.out.println("!");
          }
       }
    
       public static void main(String[] args)
       {
          int bizz = 5;
          int buzz = 2;
          zoop("just for", bizz);
          clink(2 * buzz);
       }
    
       public static void clink(int fork)
       {
          System.out.print("It's ");
          zoop("breakfast ", fork) ;
       }
    
       public static void ping(String strangStrung)
       {
          System.out.println("any " + strangStrung + "more ");
       }
    }

## Chapter 6

### Exercise 1
Write a method name `isDivisible` that takes two integers, `n` and `m` and that
returns `true` if `n` is divisible by `m` and `false` otherwise.

### Exercise 2
If you are given three sticks, you may or may not be able to arrange them in a
triangle. For example, if one of the sticks is 12 decimeters long and the others
are 1 decimeter long you will not be be able to get the short sticks to meet in
the middle. For any three lengths, there is a simple test to see if it is
possible to form a triangle:

"If any of the three lengths is greater than the sum of the other two, then you
cannot form a triangle. Otherwise you can."

Write a method named `isTriangle` that takes three integers as arguments and
that returns either `true` or `false`, depending on whether you can or cannot
form a triangle from sticks with the given lengths.

The point of this exercise is to use conditional statements to write a value
method.

### Exercise 3
What is the output of the following program? The purpose of this exercise is to
make sure you understand logical operators and the flow of execution through
value methods.

    public static void main(String[] args)
    {
       boolean flag1 = isHoopy(202);
       boolean flag2 = isFrabjuous(202);
       System.out.println(flag1);
       System.out.println(flag2);
       if (flag1 && flag2)
       {
          System.out.println("ping!");
       }
       if (flag1 || flag2)
       {
          System.out.println("pong!");
       }
    }
    
    public static boolean isHoopy(int x)
    {
       boolean hoopyFlag;
       if (x % 2 == 0)
       {
          hoopyFlag = true;
       }
       else 
       {
          hoopyFlag = false;
       }
       return hoopyFlag;
    }
    
    public static boolean isFrabjuous(int x)
    {
       boolean frabjuousFlag;
       if (x > 0)
       {
          frabjuousFlag = true;
       }
       else
       {
          frabjuousFlag = false;
       }
       return frabjuousFlag;
    }

### Exercise 4
The distance between two points $$(x_1, y_1)$$ and $$(x_2, y_2)$$ is

$$ "Distance" = sqrt((x_2 - x_1)^2 + (y_2 - y_1)^2)$$

Write a method named `distance` that takes four doubles as parameters -- `x1`,
`y1`, `x2`, and `y2` -- and that prints the distance between the points.

You should assume that there is a method named `sumSquares` that calculates and
returns the sum of the squares of its arguments. For example:

    double x = sumSquares(3.0, 4.0);

would assign the value `25.0` to `x`.

The point of this exercise is to write a new method that uses an existing
one. You should write only one method: `distance`. You should not write
`sumSquares` or `main` and you should not invoke `distance`.

## Chapter 7

### Exercise 1
Consider the following code:

    public static void main(String[] args) {
       loop(10);
    }
    
    public static void loop(int n) {
       int i = n;
       while (i > 0) {
          System.out.println(i);
          if (i % 2 == 0) {
             i = i / 2;
          } else {
             i = i + 1;
          }
       }
    }

1. Draw a table that shows the value of the variables `i` and `n` during the
   execution of `loop`. The table should contain one column for each variable
   and one line for each iteration.
2. What is the output of this program?

### Exercise 2
Write an iterative method called `power` that takes a double `x` and an integer
`n` and that returns $$x^n$$.

### Exercise 3
The mathematical function **factorial** is defined as follows:

$$0! = 1$$  
$$n! = n * (n - 1)$$

(Factorial is usually denoted with the symbol !, which is not to be confused
with the logical operator `!` which means NOT.) This definition says that the
factorial of 0 is 1, and the factorial of any other value, $$n$$, is $$n$$
multiplied by the factorial of $$n−1$$. So 3! is 3 times 2!, which is 2 times
1!, which is 1 times 0!. Putting it all together, we get 3! equal to 3 times 2
times 1 times 1, which is 6.

Write an iterative Java method that computes factorial.

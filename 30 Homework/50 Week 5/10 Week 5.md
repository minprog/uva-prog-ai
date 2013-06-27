# Homework Week 5

The homework for this week covers the chapters 11, 12, 15 from [Think Java]. You
should read these chapters before you start on the exercises.

Please take note that the exercises are based on the exercises in *Think Java*,
but are not identical.

Submit your answers on the submit tab when you are finished.

[Think Java]: http://www.greenteapress.com/thinkapjava/

## Chapter 11

### Exercise 1
A rational number is a number that can be represented as the ratio of two
integers. For example, 2/3 is a rational number, and you can think of 7 as a
rational number with an implicit 1 in the denominator. For this assignment, you
are going to write a class definition for rational numbers.

 1. Create a new program called `Rational.java` that defines a class named
    `Rational`. A `Rational` object should have two integer instance variables
    to store the numerator and denominator.
 2. Write a constructor that takes no arguments and that sets the numerator to 0
    and denominator to 1.
 3. Write a method called `printRational` that takes a Rational object as an
    argument and prints it in some reasonable format.
 4. Write a `main` method that creates a new object with type Rational, sets its
    instance variables to some values, and prints the object.
 5. At this stage, you have a minimal testable program. Test it and, if
    necessary, debug it.
 6. Write a second constructor for your class that takes two arguments and that
    uses them to initalize the instance variables.
 7. Write a method called `negate` that reverses the sign of a rational
    number. This method should be a modifier, so it should return `void`. Add
    lines to `main` to test the new method.
 8. Write a method called `invert` that inverts the number by swapping the
    numerator and denominator. Add lines to `main` to test the new method.
 9. Write a method called `toDouble` that converts the rational number to a
    double (floating-point number) and returns the result. This method is a pure
    function; it does not modify the object. As always, test the new method.
10. Write a modifier named `reduce` that reduces a rational number to its lowest
    terms by finding the greatest common divisor (GCD) of the numerator and
    denominator and dividing through. This method should be a pure function; it
    should not modify the instance variables of the object on which it is
    invoked. To find the GCD, see Exercise 10 in Chapter 6).
11. Write a method called `add` that takes two Rational numbers as arguments and
    returns a new Rational object. The return object should contain the sum of
    the arguments.

    There are several ways to add fractions. You can use any one you want, but
    you should make sure that the result of the operation is reduced so that the
    numerator and denominator have no common divisor (other than 1).

The purpose of this exercise is to write a class definition that includes a
variety of methods, including constructors, modifiers and pure functions.

## Chapter 12

### Exercise 1
Write a method called `cloneArray` that takes an array of integers as a
parameter, creates a new array that is the same size, copies the elements from
the first array into the new one, and then returns a reference to the new array.

### Exercise 2
Write a method called `randomDouble` that takes two doubles, `low` and `high`,
and that returns a random double $$x$$ so that $$low <= x < high$$.

### Exercise 3
Write a method called `randomInt` that takes two arguments, `low` and `high`,
and that returns a random integer between `low` and `high` including `high`.

### Exercise 4
Encapsulate the following code from Section 12.10 in a method called `makeHist`
that takes an array of scores and returns a histogram of the values in the
array.

    int[] counts = new int[100];
    
    for (int i = 0; i < scores.length; i++) {
       int index = scores[i];
       counts[index]++;
    }

### Exercise 5
Write a method named `areFactors` that takes an integer `n` and an array of
integers, and that returns `true` if the numbers in the array are all factors f
`n` (which is to say that `n` is divisible by all of them). HINT: See Exercise 1
of Chapter 6.

### Exercise 6
Some programmers disagree with the general rule that variables and methods
should be given meaningful names. Instead they think variables and methods
should be named after fruit.

For each of the following methods, write one sentence that describes abstractly
what the method does. For each variable, identify the role it plays. Finally,
give each method and variable a new meaningful name.

    public static int banana(int[] a) {
       int grape = 0;
       int i = 0;
       while (i < a.length) {
          grape = grape + a[i];
          i++;
       }
       return grape;
    }
    
    public static int apple(int[] a, int p) {
       int i = 0;
       int pear = 0;
       while (i < a.length) {
          if (a[i] == p)
             pear++;
          i++;
       }
       return pear;
    }
    
    public static int grapefruit(int[] a, int p) {
       for (int i = 0; i < a.length; i++) {
          if (a[i] == p)
             return i;
       }
       return -1;
    }

The purpose of this exercise is to practice reading code and recognizing the
computation patterns we have seen.

### Exercise 7
1. What is the output of the following program?
2. Draw a stack diagram that shows the state of the program just before `mus`
   returns.
3. Describe in a few words what `mus` does.

        public static int[] make(int n)
        {
           int[] a = new int[n];
        
           for (int i = 0; i < n; i++)
           {
              a[i] = i+1;
           }
           return a;
        }
        public static void dub(int[] jub)
        {
           for (int i = 0; i < jub.length; i++)
           {
              jub[i] *= 2;
           }
        }
        public static int mus(int[] zoo)
        {
           int fus = 0;
           for (int i = 0; i < zoo.length; i++)
           {
              fus = fus + zoo[i];
           }
           return fus;
        }
        public static void main(String[] args)
        {
           int[] bob = make(5);
           dub(bob);
        
           System.out.println(mus(bob));
        }

### Exercise 8
One not-very-efficient way to sort the elements of an array is to find the
largest element and swap it with the first element, then find the second-largest
element and swap it with the second, and so on. This method is called
a **selection sort** (see http://en.wikipedia.org/wiki/Selection_sort).

1. Write a method called `indexOfMaxInRange` that takes an array of integers,
   finds the largest element in the given range and returns its index.
2. Write a method called `swapElement` that takes an array of integers and two
   indices, and that swaps the elements at the given indices.
3. Write a method called `selectionSort` that takes an array of integers and
   that uses `indexOfMaxInRange` and `swapElement` to sort the array from
   largest to smallest.

### Exercise 9
Write a method called `letterHist` that takes a String as a parameter and that
returns a histogram of the letters in the String. The zeroeth element of the
histogram should contain the number of *a*'s in the String (upper and lower
case); the 25th element should contain the number of *z*'s. Your solution should
only traverse the String once.

### Exercise 10
A word is said to be a "doubloon" if every letter that appears in the word
appears exactly twice. For example, the following are all the doubloons I found
in my dictionary.

> Abba, Anna, appall, appearer, appeases, arraigning, beriberi, bilabial, boob,
> Caucasus, coco, Dada, deed, Emmett, Hannah, horseshoer, intestines, Isis,
> mama, Mimi, murmur, noon, Otto, papa, peep, reappear, redder, sees,
> Shanghaiings, Toto

Write a method called `isDoubloon` that returns `true` if the given word is a
doubloon and `false` otherwise.

### Exercise 11
Two words are anagrams if they contain the same letters (and the same number of
each letter). For example, "stop" is an anagram of "pots" and "allen downey" is
an anagram of "well annoyed."

Write a method that takes two Strings and returns `true` if the Strings are
anagrams of each other.

Optional challenge: read the letters of the Strings only once.

### Exercise 12
In Scrabble each player has a set of tiles with letters on them, and the object
of the game is to use those letters to spell words. The scoring system is
complicated, but longer words are usually worth more than shorter words.

Imagine you are given your set of tiles as a String, like `"quijibo"` and you
are given another String to test, like `"jib"`. Write a method called `canSpell`
that takes two Strings and returns `true` if the set of tiles can be used to
spell the word. You might have more than one tile with the same letter, but you
can only use each tile once.

Optional challenge: read the letters of the Strings only once.

### Exercise 13
In real Scrabble, there are some blank tiles that can be used as wild cards;
that is, a blank tile can be used to represent any letter.

Think of an algorithm for `canSpell` that deals with wild cards. Don't get
bogged down in details of implementation like how to represent wild cards. Just
describe the algorithm, using English, pseudocode, and/or Java.

## Chapter 15

### Exercise 1
This exercise is a continuation of Exercise 1 from Chapter 11. The purpose is to
practice the syntax of object methods and get familiar with the relevant error
messages.

1. Transform the methods in the `Rational` class from class methods to object
   methods, and make the necessary changes in `main`.
2. Make a few mistakes. Try invoking class methods as if they were object
   methods and vice-versa. Try to get a sense for what is legal and what is not,
   and for the error messages that you get when you mess up.
3. Think about the pros and cons of class and object methods. Which is more
   concise (usually)? Which is a more natural way to express computation (or,
   maybe more fairly, what kind of computations can be expressed most naturally
   using each style)?

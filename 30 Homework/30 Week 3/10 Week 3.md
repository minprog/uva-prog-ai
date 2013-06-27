# Homework Week 3

The homework for this week covers the chapters 8, 9, 11, and 15 from
[Think Java]. You should read these chapters before you start on the exercises.

Please take note that the exercises are based on the exercises in *Think Java*,
but are not identical.

Submit your answers on the submit tab when you are finished.

[Think Java]: http://www.greenteapress.com/thinkapjava/

## Chapter 8

### Exercise 1
Write a method that takes a `String` as an argument and that prints the letters
backwards all on one line.

### Exercise 2
Read the stack trace in Section 8.4 and answer these questions:

- What kind of Exception occurred, and what package is it defined in?
- What is the value of the index that caused the exception?
- What method threw the exception, and where is that method defined?
- What method invoked `charAt`?
- In `BadString.java`, what is the line number where `charAt` was invoked?

### Exercise 3
The purpose of this exercise is to review encapsulation and generalization.

1. Encapsulate the following code fragment, transforming it into a method that
   takes a String as an argument and that returns the final value of `count`.
2. In a sentence or two, describe what the resulting method does (without
   getting into the details of how).
3. Rewrite the function to use a for-loop instead of a while-loop.
4. Now that you have generalized the code so that it works on any String, what
   could you do to generalize it more?

    String s = "((3 + 7) * 2)";
    int len = s.length();
    
    int i = 0;
    int count = 0;
    
    while (i < len) {
       char c = s.charAt(i);
    
       if (c == '(') {
          count = count + 1;
       } else if (c == ')') {
          count = count - 1;
       }
       i = i + 1;
    }
    
    System.out.println(count);
       
### Exercise 4
The point of this exercise is to explore Java types and fill in some of the
details that aren't covered in the chapter.

1. Create a new program named `Test.java` and write a `main` method that
   contains expressions that combine various types using the `+` operator. For
   example, what happens when you "add" a `String` and a `char`? Does it perform
   addition or concatenation? What is the type of the result? (How can you
   determine the type of the result?)
2. Make a bigger copy of the following table and fill it in. At the intersection
   of each pair of types, you should indicate whether it is legal to use the `+`
   operator with these types, what operation is performed (addition or
   concatenation), and what the type of the result is.
   
   |---------+---------+------+-----+--------|
   |         | boolean | char | int | String |
   |---------|---------|------|-----|--------|
   | boolean |         |      |     |        |
   | char    |         |      |     |        |
   | int     |         |      |     |        |
   | String  |         |      |     |        |
   
3. Think about some of the choices the designers of Java made when they filled
   in this table. How many of the entries seem unavoidable, as if there were no
   other choice? How many seem like arbitrary choices from several equally
   reasonable possibilities? How many seem problematic?
4. Here's a puzzler: normally, the statement `x++` is exactly equivalent to `x =
   x + 1`. But if `x` is a char, it's not! In that case, `x++` is legal, but `x
   = x + 1` causes an error. Try it out and see what the error message is, then
   see if you can figure out what is going on.

### Exercise 5
What is the output of this program? Describe in a sentence what mystery does
(not how it works).

    public class Mystery 
    {
    	public static String mystery(String s) 
    	{
    		int i = s.length() - 1;
    		String total = "";
    		while (i >= 0) 
    		{
    			char ch = s.charAt(i);
    			System.out.println(i + "     " + ch);
    			total = total + ch;
    			i--;
    		}
    		return total;
    	}
    
    	public static void main(String[] args) 
    	{
    		System.out.println(mystery("Allen"));
    	}
    }

### Exercise 6
A friend of yours shows you the following method and explains that if `number`
is any two-digit number, the program will output the number backwards. He claims
that if `number` is 17, the method will output 71.

Is he right? If not, explain what the program actually does and modify it so
that it does the right thing.

    int number = 17;
    int lastDigit = number % 10;
    int firstDigit = number / 10;
    System.out.println(lastDigit + firstDigit);

### Exercise 7
What is the output of the following program?

    public class Enigma 
    {
       public static void enigma(int x) 
       {
          if (x == 0) {
             return;
          } else {
             enigma(x / 2);
          }
          System.out.print(x % 2);
       }
	   
       public static void main(String[] args) 
       {
          enigma(5);
          System.out.println("");
       }
    }

Explain in 4-5 words what the method enigma really does.

### Exercise 8
A word is said to be "abecedarian" if the letters in the word appear in
alphabetical order. For example, the following are all 6-letter English
abecedarian words.

> abdest, acknow, acorsy, adempt, adipsy, agnosy, befist, behint, beknow,
> bijoux, biopsy, cestuy, chintz, deflux, dehors, dehort, deinos, diluvy, dimpsy

1. Describe a process for checking whether a given word (String) is abecedarian,
   assuming that the word contains only lower-case letters. Your process can be
   iterative or recursive.
2. Implement your process in a method called `isAbecedarian`.

### Exercise 9
A dupledrome is a word that contains only double letters, like "llaammaa" or
"ssaabb". I conjecture that there are no dupledromes in common English use. To
test that conjecture, I would like a program that reads words from the
dictionary one at a time and checks them for dupledromity.

Write a method called `isDupledrome` that takes a String and returns a boolean
indicating whether the word is a dupledrome.

## Chapter 9
### Exercise 1
1. For the following program, draw a stack diagram showing the local
   variables and parameters of `main` and `riddle`, and show any objects
   those variables refer to.
2. What is the output of this program?

    public static void main(String[] args)
    {
       int x = 5;
       Point blank = new Point(1, 2);
    
       System.out.println(riddle(x, blank));
       System.out.println(x);
       System.out.println(blank.x);
       System.out.println(blank.y);
    }
    
    public static int riddle(int x, Point p)
    {
       x = x + 7;
       return x + p.x + p.y;
    }

The point of this exercise is to make sure you understand the mechanism for
passing Objects as parameters.

### Exercise 2
1. For the following program, draw a stack diagram showing the state of the
   program just before `distance` returns. Include all variables and parameters
   and the objects those variables refer to.
2. What is the output of this program?

    public static double distance(Point p1, Point p2)
    {
       int dx = p1.x - p2.x;
       int dy = p1.y - p2.y;
       return Math.sqrt(dx*dx + dy*dy);
    }
    
    public static Point findCenter(Rectangle box)
    {
       int x = box.x + box.width/2;
       int y = box.y + box.height/2;
       return new Point(x, y);
    }
    
    public static void main(String[] args)
    {
       Point blank = new Point(5, 8);
    
       Rectangle rect = new Rectangle(0, 2, 4, 4);
       Point center = findCenter(rect);
    
       double dist = distance(center, blank);
    
       System.out.println(dist);
    }

### Exercise 3
The method `grow` is part of the `Rectangle` class. Read the documentation
[here][rectangle javadoc].

1. What is the output of the following program?
2. Draw a state diagram that shows the state of the program just before the end
   of `main`. Include all local variables and the objects they refer to.
3. At the end of `main`, are `p1` and `p2` aliased? Why or why not?

    public static void printPoint(Point p)
    {
       System.out.println("(" + p.x + ", " + p.y + ")");
    }
    
    public static Point findCenter(Rectangle box)
    {
       int x = box.x + box.width/2;
       int y = box.y + box.height/2;
       return new Point(x, y);
    }
    
    public static void main(String[] args)
    {
       Rectangle box1 = new Rectangle(2, 4, 7, 9);
       Point p1 = findCenter(box1);
       printPoint(p1);
       
       box1.grow(1, 1);
       Point p2 = findCenter(box1);
       printPoint(p2);
    }

[rectangle javadoc]: http://download.oracle.com/javase/6/docs/api/java/awt/Rectangle.html#grow(int,%20int)

## Chapter 11
### Exercise 1
In the board game Scrabble, each tile contains a letter, which is used to spell
words, and a score, which is used to determine the value of words.

1. Write a definition for a class named `Tile` that represents Scrabble
   tiles. The instance variables should be a character named `letter` and an
   integer named `value`.
2. Write a constructor that takes parameters named `letter` and `value` and
   initializes the instance variables.
3. Write a method named `printTile` that takes a `Tile` object as a parameter
   and prints the instance variables in a reader-friendly format.
4. Write a method named `testTile` that creates a Tile object with the letter Z
   and the value 10, and then uses `printTile` to print the state of the object.

The point of this exercise is to practice the mechanical part of creating a new
class definition and code that tests it.

### Exercise 2
Write a class definition for `Date`, an object type that contains three
integers, `year`, `month` and `day`. This class should provide two
constructors. The first should take no parameters. The second should take
parameters named `year`, `month` and `day`, and use them to initialize the
instance variables.

Write a `main` method that creates a new `Date` object named birthday. The new
object should contain your birthdate. You can use either constructor.

## Chapter 15
### Exercise 1
Transform the following class method into an object method.

    public static double abs(Complex c) {
       return Math.sqrt(c.real * c.real + c.imag * c.imag);
    }

### Exercise 2
Transform the following object method into a class method.

    public boolean equals(Complex b) {
       return (real == b.real && imag == b.imag);
    }

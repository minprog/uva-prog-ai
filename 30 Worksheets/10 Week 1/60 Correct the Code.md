# Correct the Code

Determine if there is an error in each of the following program segments. If there is an error, specify whether it is a logic error or a compilation error, indicate the line on which the error occurs, and write the corrected code in te space provided after each problem. If the code does not contain an error, write "no error." [*Note:* There may be more than one error in each program segment.]

1. The following program should input the value of an integer into variable `num`:

{: .language.java}
    import java.Scanner;
    
    public class Output
    {
        public static void main(String args[])
        {
            int num
            Scanner input = Scanner(in);
            
            num = input.int();
        }
    }
    
<textarea name="correct-01"></textarea>

2. The following segment of code should declare an `int` variable `number` and assign the value of the expression `(5 + 3) * 2` to the variable:

{: .language.java}
    int number;
    number = 5 + 5 * 2;

<textarea name="correct-02"></textarea>

3. The following code should determine whether variable `q` is equal to `100`:

{: .language.java}
    int q = 100;
    
    System.out.print("q is");
    
    if (q = 100)
        System.out.print(" equal to 100");
    
    if (q ! 100)
        System.out.print(" not equal to 100");

<textarea name="correct-03"></textarea>

4. The following code segment should determine whether an integer variable's value is less than zero.

{: .language.java}
    int x = 9;
    
    if (x < 0);
        System.out.println("Variable x is less than zero");

<textarea name="correct-04"></textarea>

5. The following program should output the integer value entered by the user:

{: .language.java}
    import java.util.Scanner;
    
    public class Display
    {
        public static void main(String args[])
        {
            int num1;
            Scanner input = new Scanner(System.in);
            
            System.out.println("Enter first integer:");
            
            Scanner.nextInt(num1);
            System.out.println(num1);
        }
    }

<textarea name="correct-05"></textarea>

6. The following code should compare two integers to determine if they are not equal.

{: .language.java}
    int x = 9;
    int y = 3;
    
    if (x =! y)
        System.out.println("Variable x and y are not equal");
        
<textarea name="correct-06"></textarea>

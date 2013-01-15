# Programming Output

For each of the given program segments, read the code, and write the output in the space provided below each program. [*Note:* Do not execute these programs on a computer.]

1. What is the output of the following program?
  
  {: .language-java}
      public class Operator
      {
          public static void main(String args[])
          {
              int x = 30;
              int y = 2;
              
              System.out.println(x * y + 9 / 3);
          }
      }
  
  <textarea name="output-01"></textarea>
  
2. What is output by the following line of code?
  
  {: .language-java}
      System.out.println((8 * 4 * 2 + 6) / 2 + 4);
  
  <textarea name="output-02"></textarea>
  
3. What is output by the following program for each of the input values 5, 7, 100, -7, and 0?
  
  {: .language-java}
      import java.util.Scanner;
      
      public class Output
      {
          public static void main(String args[])
          {
              int number;
              Scanner input = new Scanner(System.in);
              
              System.out.println("Enter integer: ");
              number = input.nextInt();
              
              if (number != 7)
                  System.out.print("Welcome ");
              if ((number % 5) == 0)
                  System.out.println("To Java Programming");
          }
      }
  
  <textarea name="output-03"></textarea>
  
4. What is output by the following program? Assume the user enters 12 for one execution of the program and 15 for a second execution.
  
  {: .language-java}
  
      import java.util.Scanner;
      
      public class Compares
      {
          public static void main(String args[])
          {
              int integer;
              Scanner input = new Scanner(System.in);
              
              System.out.println("Enter an integer:");
              integer = input.nextInt();
              
              if ((integer % 6) == 0)
                  System.out.println("Hello");
              else
                  System.out.println("Goodbye");
          }
      }
  
  <textarea name="output-04"></textarea>
  
5. What is output by the following program?
  
  {: .language-java}
      public class Compares
      {
          public static void main(String args[])
          {
              int x = 3;
              int y = 9;
              int z = 77;
              
              if (z == 77)
                  System.out.print("H");
              
              if (z == 99)
                  System.out.print("M");
              
              if (z < x)
                  System.out.print("J");
              
              System.out.print("E");
              
              if (y == (x * x))
                  System.out.print("LL");
              
              System.out.print("O");
              
              if (x == y)
                  System.out.print("W");
          }
      }
  
  <textarea name="output-05"></textarea>
  
6. What is output by the program in exercise 5 when `x = 5`, `y = 25`, and `z = 99`?
  <textarea name="output-06"></textarea>
  
7. What is output by the program in exercise 5 when `x = 10`, `y = 9`, and `z = 8`?
  <textarea name="output-07"></textarea>
  
8. What is output by the program in exercise 5 when `x = 10`, `y = 10`, and `z = 99`?
  <textarea name="output-08"></textarea>


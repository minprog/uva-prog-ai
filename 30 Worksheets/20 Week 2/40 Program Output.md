<!-- this worksheet covers chapters 3, 4, 5 of Deitel -->

# Program Output

1. What is the output of the following code segment?
   
~~~ java
int startingValue = 0;
int terminatingValue = 5;
int stepValue = 1;

for (int i = startingValue; i < terminatingValue; i += stepValue)
    System.out.printf("%d", i);
~~~
   <textarea name="output-01"></textarea>
2. What is the output of the following program?
   
~~~ java
public class Grade
{
    public static void main(String args[])
    {
        int grade1 = 65;
        int grade2 = 50;

        System.out.println(grade1 >= 60 ? "Passed." : "Failed");
        System.out.println(grade2 >= 60 ? "Passed." : "Failed");
    }
}
~~~
   <textarea name="output-01"></textarea>
3. What is the output of the following program?
   
~~~ java
public static void main(String args[])
{
    Account account1 = new Account(35.50);

    System.out.printf("account1 balance: $%.2f\n", account1.getBalance());
}
~~~
   <textarea name="output-01"></textarea>

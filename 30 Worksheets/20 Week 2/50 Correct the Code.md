<!-- this worksheet covers chapters 3, 4, 5 of Deitel -->

# Correct the Code

1. The for loop in Listing D should loop 10 times and compute the product of i times 2 plus 1 in each iteration. For example, if the loop counter is 4, the program should print 4 * 2 + 1 = 9.
   
~~~ java
for (int i = 1, j = 1; i <= 10 && j <= 10; i++, j++)
    System.out.printf("%d + %d = %d\n", i, j, (i + j));
~~~
   <textarea name="correct-01"></textarea>
2. The while loop in Listing E should compute the product of all the integers between 1 and 5, inclusive.
   
~~~ java
int i = 1;
int product = 1;

while (i <= 5);
    product *= i;
~~~
   <textarea name="correct-01"></textarea>
3. The while loop in Listing F should print the sum of the integers between 0 and 5, inclusive.
   
~~~ java
int sum = 0;

while (i <= 5)
{
    sum += i;
    i++;
}
System.out.printf("The sum is: %d\n", sum);
~~~
   <textarea name="correct-01"></textarea>
   

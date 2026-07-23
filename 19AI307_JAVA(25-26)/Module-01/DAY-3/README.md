# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To write a Java program that calculates the factorial of a given number using a for loop.

## ALGORITHM :
1.Start the program and read an integer n from the user.

2.Initialize a variable factorial to 1 to store the result.

3.Use a for loop from 1 to n, multiplying factorial by the loop counter in each iteration.

4.After the loop ends, print the value of factorial as the factorial of n.

5.Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Swetha S
RegisterNumber: 212224040344
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class FactorialCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  
        long factorial = 1;

        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }

        System.out.println("Factorial of " + n + " is: " + factorial);
    }
}
```


## OUTPUT:

<img width="810" height="265" alt="image" src="https://github.com/user-attachments/assets/3aa2e921-f3c7-4d25-b049-a72b26fdc541" />



## RESULT:
Therefore the program has been executed successfully.

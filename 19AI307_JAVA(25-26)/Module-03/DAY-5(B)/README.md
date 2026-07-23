# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes.
## AIM:
To write a Java program that checks whether a given number is prime by using the Integer wrapper class for parsing and handling the input.

## ALGORITHM :
Read input from the user as a string.

Use the Integer.parseInt() method (wrapper class) to convert the input into an integer.

If parsing fails, catch NumberFormatException and display an error message.

If the number is less than or equal to 1, it is not prime.

If any divisor divides the number completely, mark it as not prime.

After checking, print whether the number is prime or not.

Close the scanner.


## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Swetha S
RegisterNumber: 212224040344 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class PrimeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        String input = scanner.nextLine();

        try {
            Integer number = Integer.parseInt(input); // Using Integer wrapper class

            if (number <= 1) {
                System.out.println(number + " is not a prime number.");
            } else {
                boolean isPrime = true;
                for (int i = 2; i <= Math.sqrt(number); i++) {
                    if (number % i == 0) {
                        isPrime = false;
                        break;
                    }
                }

                if (isPrime) {
                    System.out.println(number + " is a prime number.");
                } else {
                    System.out.println(number + " is not a prime number.");
                }
            }

        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid integer.");
        }

        scanner.close();
    }
}
```
## OUTPUT:

<img width="636" height="222" alt="image" src="https://github.com/user-attachments/assets/239ff699-4dc8-4bd5-91b3-b2f857c45757" />

## RESULT:
Therefore the program has been executed successfully.



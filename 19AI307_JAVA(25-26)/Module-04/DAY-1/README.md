# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?


## AIM:
To write a Java program to demonstrate NullPointerException when calling .toString() on a null Integer object and to handle the exception using try-catch

## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Read an integer value from the user.
Assign null if the user enters 0 (or a specific case).
Try to call .toString() method on the Integer object.
.Catch the NullPointerException and display a meaningful message.
Display output and end the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class NullCheck
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        Integer num = sc.nextInt(); 
        try 
        {
            if (num == 0) 
            {
                num = null;
            }
            System.out.println(num.toString());

        } 
        catch (NullPointerException e) 
        {
            System.out.println("Null Integer");
        }
    }
}

```

## OUTPUT:

<img width="568" height="330" alt="image" src="https://github.com/user-attachments/assets/17007003-4be0-4084-a27b-b5339e19aa12" />

## RESULT:

Therefore the program has been executed successfully.

# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program that reverses a given string entered by the user.

## ALGORITHM :
1.Start the program and read a string input from the user.

2.Create a StringBuilder object with the input string.

3.Use the reverse() method of StringBuilder to reverse the string.

4.Convert the reversed StringBuilder back to a string.

5.Display the reversed string and stop the program.



## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Swetha S
RegisterNumber: 212224040344
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        String reversed = new StringBuilder(str).reverse().toString();
        System.out.println("Reversed string: " + reversed);
        scanner.close();
    }
}
```

## OUTPUT:

<img width="768" height="246" alt="image" src="https://github.com/user-attachments/assets/e660c61b-f7ab-448c-9a20-740854238166" />

## RESULT:
Therefore the program has been executed successfully.


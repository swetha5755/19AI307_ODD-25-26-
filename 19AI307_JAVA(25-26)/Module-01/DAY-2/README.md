# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.



## AIM:
To develop a Java program that checks a given floor number and displays a special message based on its divisibility by 3 and/or 5.

## ALGORITHM :
1.Start the program and read the floor number from the user.

2.Check if the floor is divisible by both 3 and 5; if true, display "Skipped".

3.Otherwise, check if the floor is divisible only by 3; if true, display "Beware!".

4.Otherwise, check if the floor is divisible only by 5; if true, display "Blessings!".

5.If none of the above conditions are met, display "Floor {floor number}", then stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Swetha S
RegisterNumber: 212224040344
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class MagicalElevator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int floor = scanner.nextInt();

        if (floor % 3 == 0 && floor % 5 == 0) {
            System.out.println("Skipped");
        } else if (floor % 3 == 0) {
            System.out.println("Beware!");
        } else if (floor % 5 == 0) {
            System.out.println("Blessings!");
        } else {
            System.out.println("Floor " + floor);
        }

        scanner.close();
    }
}
```






## OUTPUT:
<img width="533" height="326" alt="image" src="https://github.com/user-attachments/assets/7edc6c92-26a0-439e-8832-c614b0148d27" />



## RESULT:
Therefore the program has been executed successfully.

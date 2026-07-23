# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).



## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.


## ALGORITHM :
Define a class demo with two methods:

square(int n) → returns n * n. cube(int n) → returns n * square(n) by calling the square() method internally.

In the main class, read an integer input from the user.

Create an object of the demo class.

Call the cube() method using the object and print the result.

End the program.	

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.util.*;
class demo
{
    public int square(int n)
    {
        return n*n;
    }
    public int cube(int n)
    {
        return n*square(n);
    }
    
}
public class main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        demo d=new demo();
        System.out.println(d.cube(n));
    }
}

```
## OUTPUT:

<img width="347" height="227" alt="image" src="https://github.com/user-attachments/assets/3cf796d9-7f08-4f23-b6e4-3b5571544569" />

## RESULT:
Therefore the program has been executed successfully.



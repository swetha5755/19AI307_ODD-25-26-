# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To write a Java program that demonstrates thread priority by creating two threads, assigning names and priorities to them, and displaying thread execution.

## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Create a class that extends Thread.
Override the run() method to print the current thread name and priority.
Create two thread objects t1 and t2.
Set names and priorities for each thread using setName() and setPriority().
Start both threads.
End the program.


## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ThreadPriorityExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```

## OUTPUT:

<img width="817" height="238" alt="image" src="https://github.com/user-attachments/assets/33a68ce4-7666-4528-8808-1337519dd033" />



## RESULT:
Therefore the program has been executed successfully.


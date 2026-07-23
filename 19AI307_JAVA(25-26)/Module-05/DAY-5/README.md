# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Read N numbers from the user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in the same order.



## AIM:

To write a Java program that uses a Fixed Thread Pool to process a set of numbers concurrently and demonstrates synchronization by maintaining the order of results.


## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Read total number of tasks (T) from the user.
Read T numbers and store them in a list.
Create a FixedThreadPool of size 3 using Executors.newFixedThreadPool(3).
Submit tasks to multiply each number by 2 using Callable.
Keep the Future objects returned from each task to retain order.
Retrieve results using future.get() in the same order they were submitted.
Display final results.
Shutdown executor service.
End the program.


## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.util.concurrent.*;

public class FixedThreadPoolExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int T = sc.nextInt();
        List<Integer> numbers = new ArrayList<>();
        
        for (int i = 0; i < T; i++) {
            numbers.add(sc.nextInt());
        }
        ExecutorService executor = Executors.newFixedThreadPool(3);
        List<Future<Integer>> results = new ArrayList<>();
        for (int num : numbers) {
            Future<Integer> result = executor.submit(() -> num * 2);
            results.add(result);
        }
        for (Future<Integer> res : results) {
            try {
                System.out.println("Result: " + res.get());
            } catch (Exception e) {
                e.printStackTrace();
            }
        }

        executor.shutdown();
        sc.close();
    }
}
```


## OUTPUT:

<img width="467" height="546" alt="image" src="https://github.com/user-attachments/assets/f559c880-9a87-4613-9103-6bf4f127bce9" />


## RESULT:
Therefore the program has been executed successfully.

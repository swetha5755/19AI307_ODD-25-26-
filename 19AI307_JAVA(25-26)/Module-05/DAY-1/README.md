# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program that writes character data into a text file using the FileWriter class.

## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Create a FileWriter object and specify the filename.
Write characters to the file using the write() method.
Close the FileWriter to save the data.
End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Swetha S
RegisterNumber: 212224040344
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class FileWriterExampleUserInput {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            String fileName = sc.nextLine();
            String content = sc.nextLine();
            FileWriter fw = new FileWriter(fileName);
            fw.write(content);
            fw.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("Error writing to file: " + e.getMessage());
        } finally {
            sc.close();
        }
    }
}
```


## OUTPUT:

<img width="822" height="310" alt="image" src="https://github.com/user-attachments/assets/54af6091-39d1-4ff7-ab92-8ffa25052ee2" />


## RESULT:
Therefore the program has been executed successfully.

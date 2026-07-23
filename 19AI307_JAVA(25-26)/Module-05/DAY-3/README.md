# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of words in a file.



## AIM:

To write a Java program that reads a text file and counts the number of words present in the file using file handling mechanisms.


## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Create a File object to reference the input text file.
Use Scanner or FileReader to read the contents of the file.
Split the file content into words using space or delimiter.
Count the total number of words.
Display the word count.
End the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class WordCountInFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        try {
            String content = sc.nextLine();
            FileWriter fw = new FileWriter("input.txt");
            fw.write(content);
            fw.close();
            BufferedReader br = new BufferedReader(new FileReader("input.txt"));
            String line;
            int wordCount = 0;
            while ((line = br.readLine()) != null) {
                String[] words = line.trim().split("\\s+");
                if (!line.trim().isEmpty()) {
                    wordCount += words.length;
                }
            }

            br.close();
            System.out.println("Number of words in the file: " + wordCount);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            sc.close();
        }
    }
}
```

## OUTPUT:

<img width="820" height="175" alt="image" src="https://github.com/user-attachments/assets/61467676-e0fe-4be9-82d8-3e39dbbdc7ac" />

## RESULT:
Therefore the program has been executed successfully.

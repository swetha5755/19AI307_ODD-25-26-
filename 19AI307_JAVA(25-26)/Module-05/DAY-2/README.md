# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read a string from the user, compress it in memory using ByteArrayOutputStream + GZIPOutputStream, and then decompress it back using ByteArrayInputStream + GZIPInputStream.



## AIM:
To write a Java program that reads a string from the user, compresses it using GZIP compression, and then decompresses it back to its original form.



## ALGORITHM :
Start the program.
Import the necessary package 'java.util'
Read a string from the user using Scanner.
Create a ByteArrayOutputStream object to hold compressed data.
Wrap it with GZIPOutputStream and write the user string into it to perform compression.
Convert compressed data into a byte array.
Create a ByteArrayInputStream object using the compressed byte array.
Wrap it with GZIPInputStream to decompress the content.
Read decompressed bytes and convert them back into the original string.
Display original, compressed size, and decompressed results.
End the program.	



## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Swetha S
RegisterNumber:  212224040344
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;
import java.util.zip.GZIPOutputStream;
import java.util.zip.GZIPInputStream;

public class GZIPMemoryExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            String input = scanner.nextLine();

            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            GZIPOutputStream gzipOut = new GZIPOutputStream(baos);
            gzipOut.write(input.getBytes("UTF-8"));
            gzipOut.close(); 

            byte[] compressedData = baos.toByteArray();
            System.out.println("Compressed data (bytes):");
            for (byte b : compressedData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + compressedData.length);

            ByteArrayInputStream bais = new ByteArrayInputStream(compressedData);
            GZIPInputStream gzipIn = new GZIPInputStream(bais);
            InputStreamReader reader = new InputStreamReader(gzipIn, "UTF-8");
            BufferedReader br = new BufferedReader(reader);

            StringBuilder decompressed = new StringBuilder();
            String line;
            while ((line = br.readLine()) != null) {
                decompressed.append(line);
            }

            System.out.println("\nDecompressed string:");
            System.out.println(decompressed.toString());

            br.close();
            gzipIn.close();
            bais.close();

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```

## OUTPUT:

<img width="820" height="375" alt="image" src="https://github.com/user-attachments/assets/b3d72e40-aabc-4318-9057-462e1e9d43b0" />



## RESULT:
Therefore the program has been executed successfully.

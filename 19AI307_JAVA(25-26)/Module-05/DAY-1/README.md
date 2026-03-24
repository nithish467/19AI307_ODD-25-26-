# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program to write characters to a file using FileWriter.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a FileWriter object with the file name.
4.	Use the write() method to write characters or text into the file.
5.	Close the FileWriter using close() to save the file.
6.	Display a success message and stop the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteFileUsingFileWriter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String fileName = scanner.nextLine();

        String content = scanner.nextLine();

        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(content);
            writer.close();
            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }

        scanner.close();
    }
}

```






## OUTPUT:

<img width="781" height="337" alt="image" src="https://github.com/user-attachments/assets/5d1147e2-ac47-45d8-a3cd-6ec0e3f595ab" />


## RESULT:
The program successfully writes characters to a file named output.txt using FileWriter, and the content is stored in the file correctly.

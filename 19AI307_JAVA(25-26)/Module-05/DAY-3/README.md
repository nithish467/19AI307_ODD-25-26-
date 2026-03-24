# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of words in a file.

## AIM:
To write a Java program to count the number of words in a file.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Open the file using BufferedReader.
4.	Read each line from the file.
5.	Split each line into words using spaces and count them.
6.	Display the total word count and stop the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.io.FileWriter;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

public class CountWordsInFile {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String fileName = "userwords.txt";

        String input = scanner.nextLine();

        try {
            FileWriter writer = new FileWriter(fileName);
            writer.write(input);
            writer.close();
        } catch (IOException e) {
            System.out.println("Error writing to the file.");
            e.printStackTrace();
            scanner.close();
            return;
        }

        int wordCount = 0;
        try {
            FileReader reader = new FileReader(fileName);
            Scanner fileScanner = new Scanner(reader);

            while (fileScanner.hasNext()) {
                fileScanner.next();
                wordCount++;
            }

            fileScanner.close();
            reader.close();
        } catch (IOException e) {
            System.out.println("Error reading the file.");
            e.printStackTrace();
        }

        System.out.println("Number of words in the file: " + wordCount);
        scanner.close();
    }
}


```





## OUTPUT:

<img width="1065" height="260" alt="image" src="https://github.com/user-attachments/assets/22dcd15b-950a-408d-a065-0808a1e9293e" />



## RESULT:
The program successfully reads a file and counts the total number of words present in it using BufferedReader, displaying the correct word count.

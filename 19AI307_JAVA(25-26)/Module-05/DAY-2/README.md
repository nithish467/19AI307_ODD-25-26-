# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## AIM:
To write a Java program to demonstrate reading UTF strings using DataInputStream.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a file with UTF data using DataOutputStream (for writing).
4.	Open the file using DataInputStream.
5.	Use readUTF() method to read the string from the file.
6.	Display the string and close the stream, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.io.*;
import java.util.Scanner;
public class DataInputStreamUTFExample {
    public static void main(String[] args) {
        String fileName = "utfdata.dat";
        Scanner scanner = new Scanner(System.in);

        try {
            String input = scanner.nextLine();

            DataOutputStream dos = new DataOutputStream(new FileOutputStream(fileName));
            dos.writeUTF(input);
            dos.close();

            DataInputStream dis = new DataInputStream(new FileInputStream(fileName));
            String readString = dis.readUTF();
            dis.close();

            System.out.println("String read from file: " + readString);
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        scanner.close();
    }
}



```






## OUTPUT:
<img width="781" height="261" alt="image" src="https://github.com/user-attachments/assets/29edca3d-01fd-47ef-9420-dc4599bc3acc" />



## RESULT:
The program successfully demonstrates reading a UTF string from a file using DataInputStream, and the stored string is displayed correctly.

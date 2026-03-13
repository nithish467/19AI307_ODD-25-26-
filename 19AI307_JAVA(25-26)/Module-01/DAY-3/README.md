# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
A left-aligned triangle pattern is a pattern of stars (*) where each row contains an increasing number of stars, aligned to the left side.

Write a Java program that:

Prompts the user to enter the number of rows for the triangle.

Uses nested loops to print the left-aligned triangle pattern.

Ensures that each row contains stars corresponding to its row number.

## AIM:

To write and execute a Java program using nested loops to print a left-aligned triangle star pattern.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare an integer variable rows and get the number of rows from the user.
4.	Use nested loops to control rows and columns.
5.	Print stars (*) equal to the current row number and move to the next line after each row.
6.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.*;

public class LeftAlignedTriangle {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int rows = sc.nextInt();

        for (int i = 1; i <= rows; i++) {

            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }

            System.out.println();
        }

        sc.close();
    }
}





```







## OUTPUT:

<img width="603" height="498" alt="image" src="https://github.com/user-attachments/assets/8d0010a0-8437-486d-bfd4-b0d72d287315" />




## RESULT:
Thus, the Java program to print a left-aligned triangle pattern using nested loops was executed successfully and the output was verified.



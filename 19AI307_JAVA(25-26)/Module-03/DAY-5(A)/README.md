# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to find the square root of a number using Double wrapper class.

## AIM:
To write a Java program to find the square root of a number using the Double wrapper class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number as input using Double wrapper class.
4.	Convert the input into a double value if needed.
5.	Use Math.sqrt() method to calculate the square root.
6.	Display the result and stop the program.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: NITHISHKUMAR S 
RegisterNumber: 212223240109 
*/
```

## SOURCE CODE:

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double num = sc.nextDouble();

        Double number = Double.valueOf(num); 
        Double result = Math.sqrt(number);  

        System.out.println("Square root of " + number + " is: " + result);
        sc.close();
    }
}



```






## OUTPUT:
<img width="738" height="257" alt="image" src="https://github.com/user-attachments/assets/9a59a9b9-d017-4c7b-968d-4c81f8df5d5c" />



## RESULT:
The program successfully calculates the square root of a number using the Double wrapper class and displays the correct result.

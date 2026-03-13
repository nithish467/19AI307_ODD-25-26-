# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all prime numbers present in an array


## AIM:
To write and execute a Java program to find and print prime numbers from an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare variables for array size and elements.
4.	Get the array elements from the user.
5.	Traverse each element of the array.
6.	Check whether the number is prime or not.
7.	If the number is prime, print it.
8.	Repeat the process for all elements in the array.
9.	Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:
```java
import java.util.*;

public class PrimeNumbersInArray {

    public static boolean isPrime(int num) {
        if(num <= 1) return false;
        for(int i = 2; i * i <= num; i++) {
            if(num % i == 0)
                return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();
        int[] arr = new int[n];

        for(int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }

        boolean hasPrime = false;

        for(int i = 0; i < n; i++) {
            if(isPrime(arr[i])) {
                System.out.println(arr[i]);
                hasPrime = true;
            }
        }

        if(!hasPrime) {
            System.out.println("No prime numbers found");
        }
    }
}



```






## OUTPUT:

<img width="696" height="531" alt="image" src="https://github.com/user-attachments/assets/4b0e0e66-dcc9-4e86-bea1-f24b08dcb70d" />




## RESULT:
Thus, the Java program to print all prime numbers present in an array was executed successfully and the output was verified.

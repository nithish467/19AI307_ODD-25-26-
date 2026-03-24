# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To demonstrate what happens when calling .toString() on a null Integer object and how to prevent NullPointerException in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Attempt to call .toString() on the null object (may cause exception).
4.	Use a null check to avoid calling methods on null.
5.	Alternatively, use String.valueOf() to safely convert the value.
6.	Display the result and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: NITHISHKUMAR S 
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;

public class NullPointerIntegerExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int input = sc.nextInt();
        Integer num = (input == 0) ? null : input;

        try {
            System.out.println(num.toString());
        } catch (NullPointerException e) {
            System.out.println("Null Integer");
        }

        sc.close();
    }
}




```





## OUTPUT:
<img width="492" height="302" alt="image" src="https://github.com/user-attachments/assets/d67c3d62-2ad7-4a03-8f19-d49129995d37" />



## RESULT:
The program successfully demonstrates that calling .toString() on a null object causes a NullPointerException, and shows how to prevent it using a null check and String.valueOf() method.

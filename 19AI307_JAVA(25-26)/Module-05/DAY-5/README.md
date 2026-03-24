# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a thread pool to calculate and print the square of each number from input.

## AIM:
To write a Java program using a thread pool to calculate and print the square of each number from inp

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a fixed thread pool using Executors.newFixedThreadPool().
4.	Accept input numbers from the user.
5.	Submit tasks to the thread pool where each task calculates the square of a number.
6.	Print the results and shut down the thread pool, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.util.*;
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        ExecutorService executor = Executors.newFixedThreadPool(3);

        List<Future<Integer>> futures = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            int num = sc.nextInt();
            futures.add(executor.submit(() -> num * num));
        }

        for (Future<Integer> f : futures) {
            System.out.println("Square: " + f.get());
        }

        executor.shutdown();
        sc.close();
    }
}




```






## OUTPUT:
<img width="467" height="469" alt="image" src="https://github.com/user-attachments/assets/df342faa-6186-4cdc-9e41-75a1f27b8150" />



## RESULT:
The program successfully uses a thread pool to process multiple tasks concurrently and prints the square of each input number efficiently.

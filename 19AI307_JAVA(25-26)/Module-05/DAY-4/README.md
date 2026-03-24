# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To write a Java program to set the name and priority of threads and demonstrate it using two threads t1 and t2.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Override the run() method to display thread name and priority.
4.	Create two thread objects t1 and t2.
5.	Set thread names using setName() and priorities using setPriority().
6.	Start the threads and display their details, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class MyThread extends Thread {
    public MyThread(String name) {
        super(name);
    }

    public void run() {
        System.out.println(Thread.currentThread());
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        MyThread t1 = new MyThread(name1);
        MyThread t2 = new MyThread(name2);

        t1.setPriority(4);
        t2.setPriority(2);

        t1.start();
        t2.start();

        sc.close();
    }
}



```






## OUTPUT:

<img width="817" height="258" alt="image" src="https://github.com/user-attachments/assets/2db1999a-5132-4e02-845b-11d8dca08110" />




## RESULT:
The program successfully creates two threads, assigns them different names and priorities, and displays their details during execution.

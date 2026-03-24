# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

## AIM:
To create a Java class Student with variables name and rollNumber, and to use a method setDetails() to assign and display the values.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	create a class named Student with variables name and rollNumber.
4.	Create a method setDetails(String name, int rollNumber) to assign values.
5.	Inside the method, store the values in variables.
6.	Display the values using print statements.
7.	Create an object in the main method, call the method, and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;

class Student {
    String name;
    int rollNumber;

    void setDetails(String name, int rollNumber) {
        this.name = name;
        this.rollNumber = rollNumber;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Roll Number: " + rollNumber);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int rollNumber = sc.nextInt();

        Student s = new Student();
        s.setDetails(name, rollNumber);
        s.display();

        sc.close();
    }
}


```




## OUTPUT:
<img width="534" height="315" alt="image" src="https://github.com/user-attachments/assets/07265f31-1575-4063-93f8-dbb2754f4187" />




## RESULT:
The program successfully creates a Student class, assigns values using the setDetails() method, and displays the student details correctly.

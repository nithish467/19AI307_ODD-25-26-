# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to demonstrate a parameterized constructor.

## AIM:
To write a Java program to demonstrate the use of a parameterized constructor.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare variables inside the class.
4.	Create a parameterized constructor to initialize the variables.
5.	Create an object of the class and pass values while creating the object.
6.	Display the values and stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;

class Employee {

    String name;
    int id;

    Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    void display() {
        System.out.println("Employee Name: " + name);
        System.out.println("Employee ID: " + id);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int id = sc.nextInt();

        Employee e = new Employee(name, id);
        e.display();

        sc.close();
    }
}


```





## OUTPUT:
<img width="620" height="310" alt="image" src="https://github.com/user-attachments/assets/64b4be7a-5b19-4f13-a43a-0c3d9e0d30d7" />



## RESULT:
The program successfully demonstrates a parameterized constructor by initializing variables during object creation and displaying the values.

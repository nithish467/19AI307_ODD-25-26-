# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:
Get the input for radius from the user.
double getArea(double r) → calculate the area and return the area(Don't print anything in this method).
void printArea(double area) → pass the calculated area to this method and print the area of a circle.

## AIM:
To write and execute a Java program using methods to calculate and print the area of a circle.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a method getArea(double r) to calculate and return the area of the circle.
4.	Create another method printArea(double area) to print the area.
5.	In the main() method, get the radius from the user.
6.	Call getArea() to calculate the area and pass the result to printArea() to display it.
7.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109 
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Circle {

    double getArea(double r) {
        return 3.14 * r * r; 
    }

    void printArea(double area) {
        System.out.printf("%.2f", area);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double radius = sc.nextDouble();

        Circle c = new Circle();
        double area = c.getArea(radius);
        c.printArea(area);

        sc.close();
    }
}




```






## OUTPUT:
<img width="502" height="166" alt="image" src="https://github.com/user-attachments/assets/2f20f11d-809f-4e01-91b9-ff93129e663c" />



## RESULT:
Thus, the Java program to calculate and print the area of a circle using methods was executed successfully and the output was verified.

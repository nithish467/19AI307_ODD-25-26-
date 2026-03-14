# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.


## AIM: 
To create a Java class and object to store and display the details of a city.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class City with attributes cityName, population, and area and a method printDetails().
4.	In the main() method, create an object of the City class.
5.	Get input for cityName, population, and area and assign them to the object.
6.	Call printDetails() to display the details and stop the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:
```java

import java.util.Scanner;

class City {

    String cityName;
    long population;
    double area;

    void printDetails() {
        System.out.println("City Name: " + cityName);
        System.out.println("Population: " + population);
        System.out.println("Area: " + area);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        City c = new City();
        c.cityName = scanner.nextLine();  
        c.population = scanner.nextLong();
        c.area = scanner.nextDouble();

        c.printDetails();

        scanner.close();
    }
}


```






## OUTPUT:



## RESULT:
Thus, the Java program to create a class City, create an object, and print its details was executed successfully and the output was verified.

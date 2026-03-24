# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach
To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.
## AIM:
To implement the Singleton Design Pattern in Java to ensure only one instance of a Radar Control Tower exists and to register incoming flights.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class RadarControlTower with a private static instance.
4.	Make the constructor private to prevent multiple object creation.
5.	Provide a public static method getInstance() to return the single instance.
6.	Create a method registerFlight(String flightName) to count and display flight registrations.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109 
*/
```

## SOURCE CODE:

```java
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance = null;
    private int flightCount;

    private RadarControlTower() {
        flightCount = 0;
    }

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flight) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}


```






## OUTPUT:
<img width="1186" height="254" alt="image" src="https://github.com/user-attachments/assets/bfa6dc96-dfa8-4188-8bc2-b9d4dea85179" />



## RESULT:
The program successfully demonstrates the Singleton pattern, ensuring only one Radar Control Tower instance exists. All flights are registered through the same object, and the total number of flights is updated correctly.

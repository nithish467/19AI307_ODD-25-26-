# Ex.No:3(D)    INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.
AggressiveController: Allows only if "GREEN".
DefensiveController: Allows for "GREEN" or "YELLOW".

## AIM:
To develop a Java program using abstraction/polymorphism where different traffic controllers decide whether a vehicle can move based on signal color.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class TrafficController with method canMove().
4.	Create subclass AggressiveController (allows only "GREEN").
5.	Create subclass DefensiveController (allows "GREEN" or "YELLOW").
6.	Read input for signalColor and controllerType, create corresponding object.
7.	Call method and print "GO" or "STOP", then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

interface TrafficController 
{
    String decide(String signalColor);
}

class AggressiveController implements TrafficController 
{
    @Override
    public String decide(String signalColor) 
    {
        return signalColor.equals("GREEN") ? "GO" : "STOP";
    }
}

class DefensiveController implements TrafficController 
{
    @Override
    public String decide(String signalColor) 
    {
        return (signalColor.equals("GREEN") || signalColor.equals("YELLOW")) ? "GO" : "STOP";
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String signalColor = sc.next();   
        int controllerType = sc.nextInt(); 

        TrafficController controller;
        if (controllerType == 1) 
        {
            controller = new AggressiveController();
        } 
        else 
        {
            controller = new DefensiveController();
        }
        System.out.println(controller.decide(signalColor));
    }
}



```





## OUTPUT:
<img width="410" height="216" alt="image" src="https://github.com/user-attachments/assets/3e49c6de-ec5a-4f8d-a8ca-e61d65478b35" />



## RESULT:
The program successfully uses abstraction and polymorphism to determine whether a vehicle can move based on signal color and controller type, and prints "GO" or "STOP" accordingly.

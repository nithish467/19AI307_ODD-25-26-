# Ex.No:3(C) ABSTRACTION

## QUESTION:
In the land of Eldoria, two kinds of advisors (Strategic and Emergency) suggest how much resources to allocate based on the kingdom’s stress factors.
StrategicAdvisor: Advises cautiously in normal times.
EmergencyAdvisor: Takes aggressive decisions during crisis.

## AIM:
To create a Java program using abstraction to determine the advisory level (Minimal / Balanced / Critical) based on different conditions for StrategicAdvisor and EmergencyAdvisor.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class Advisor with an abstract method adviseLevel().
4.	Create subclass StrategicAdvisor and implement logic based on unrestLevel.
5.	Create subclass EmergencyAdvisor and implement logic using dangerLevel and disasterCount.
6.	In the main class, read input, create the appropriate object based on advisor type.
7.	Call adviseLevel() and display the result, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.util.*;

abstract class Advisor {
    abstract String adviseLevel();
}

class StrategicAdvisor extends Advisor {
    int unrestLevel;

    StrategicAdvisor(int unrestLevel) {
        this.unrestLevel = unrestLevel;
    }

    String adviseLevel() {
        if (unrestLevel < 3) return "Minimal";
        else if (unrestLevel <= 6) return "Balanced";
        else return "Critical";
    }
}

class EmergencyAdvisor extends Advisor {
    int dangerLevel, disasterCount;

    EmergencyAdvisor(int dangerLevel, int disasterCount) {
        this.dangerLevel = dangerLevel;
        this.disasterCount = disasterCount;
    }

    String adviseLevel() {
        if (dangerLevel + disasterCount >= 15) return "Critical";
        else if (dangerLevel >= 7) return "Balanced";
        else return "Minimal";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();

        Advisor advisor;
        if (type == 1) {
            int unrestLevel = sc.nextInt();
            advisor = new StrategicAdvisor(unrestLevel);
        } else {
            int dangerLevel = sc.nextInt();
            int disasterCount = sc.nextInt();
            advisor = new EmergencyAdvisor(dangerLevel, disasterCount);
        }

        System.out.println(advisor.adviseLevel());
        sc.close();
    }
} 

```





## OUTPUT:
<img width="418" height="255" alt="image" src="https://github.com/user-attachments/assets/234019f6-3f7c-401f-9299-4c69d38291c1" />



## RESULT:
The program successfully demonstrates abstraction, where different advisor types implement their own logic to determine and display the correct advisory level (Minimal / Balanced / Critical) based on input conditions.

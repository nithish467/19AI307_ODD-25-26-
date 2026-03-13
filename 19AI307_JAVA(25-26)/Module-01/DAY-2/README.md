# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Aliens scan DNA numbers:

If the DNA number is divisible by 2 and ends in 4, they accept it.

If the DNA number is divisible by 2 but ends in anything else, it’s a suspect.

If the DNA is odd, they reject it.

The program will print one of the following statements based on the input:

Accepted
Suspect
Rejected

## AIM:
To write and execute a Java program using conditional statements to classify a DNA number as Accepted, Suspect, or Rejected.

## ALGORITHM :
1.Start the program and import java.util.Scanner.
2.Declare an integer variable dna and get the DNA number from the user.
3.Check if the number is divisible by 2 and ends with 4.
4.If true print "Accepted", else if divisible by 2 print "Suspect".
5.Otherwise print "Rejected" and stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:
```java

import java.util.*;

public class AlienDNA {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int dna = sc.nextInt();

        if (dna % 2 != 0) {
            System.out.println("Rejected");
        } else if (dna % 10 == 4) {
            System.out.println("Accepted");
        } else {
            System.out.println("Suspect");
        }

        sc.close();
    }
}
```






## OUTPUT:
<img width="490" height="287" alt="image" src="https://github.com/user-attachments/assets/fdda0be2-568e-48c6-9e48-46fdbe25cce4" />



## RESULT:
Thus, the Java program to classify the DNA number as Accepted, Suspect, or Rejected using conditional statements was executed successfully and the output was verified.


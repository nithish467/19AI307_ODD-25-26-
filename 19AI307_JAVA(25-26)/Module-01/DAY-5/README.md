# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to compare two strings.

## AIM:
To write and execute a Java program to compare two strings using string methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare two string variables str1 and str2.
4.	Get the two strings from the user.
5.	Use the equals() method to compare the two strings.
6.	If both strings are equal, print "Strings are equal".
7.	Otherwise print "Strings are not equal".
8.	Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: NITHISHKUMAR S 
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        String s1 = sc.nextLine();
        String s2 = sc.nextLine();
        
        if (s1.equals(s2)){
            System.out.println("Strings are equal.");
        }
        else {
            System.out.println("Strings are not equal.");
        }
    }
}

```






## OUTPUT:
<img width="760" height="348" alt="image" src="https://github.com/user-attachments/assets/3dc23bb4-e09a-4f14-b820-84437ca3b10a" />




## RESULT:
Thus, the Java program to compare two strings was executed successfully and the output was verified.

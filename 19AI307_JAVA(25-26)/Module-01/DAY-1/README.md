# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has just started learning Java and is very excited about how to display messages on the screen. Her first mission is to understand how different types of print statements work:

System.out.print() → prints on the same line

System.out.println() → prints and moves to the next line

System.out.printf() → prints formatted output


## AIM:
To study the basics of Java programming, including data types, variables, and operators, and implement them using a simple Java program.

## ALGORITHM :
1. Start the program.	
2. Declare variables with different data types such as int, float, char, and double.
3. Assign values to the variables.
4. Perform arithmetic operations like addition, subtraction, multiplication, and division using operators.
5. Display the results using System.out.println().
6. Stop the program.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: NITHISHKUMAR S
RegisterNumber:  212223240109
*/
```

## Sourcecode.java:
```java

import java.util.*;
class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        int age = sc.nextInt();
        float num = sc.nextFloat();
        System.out.println("Hello, "+name);
        System.out.println("You are "+age+" years old");
        System.out.printf("Your favorite number is %.2f",num);
    }
}



```







## OUTPUT:

<img width="926" height="429" alt="image" src="https://github.com/user-attachments/assets/af5bc6db-c510-470e-8c35-0b3955b49af9" />





## RESULT:
Thus, the Java program to demonstrate data types, variables, and operators was successfully executed and the output was verified.



# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to define an enum named Department with constants like CS, IT, and ECE. Each constant should hold a full form string like "Computer Science" using a constructor.

## AIM:
To write a Java program to define an enum named Department with constants CS, IT, ECE, each storing a full form using a constructor.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare constants CS, IT, ECE with corresponding full forms.
4.	Create a private variable inside enum to store the full form.
5.	Use a constructor to initialize the full form and create a getter method.
6.	Access and display the values in the main method, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;

enum Department {
    CS("Computer Science"),
    IT("Information Technology"),
    ECE("Electronics and Communication Engineering");

    private final String fullForm;

    Department(String fullForm) {
        this.fullForm = fullForm;
    }

    public String getFullForm() {
        return fullForm;
    }

    public static Department fromCode(String code) {
        for (Department dept : Department.values()) {
            if (dept.name().equalsIgnoreCase(code)) {
                return dept;
            }
        }
        return null; // return null if not matched
    }
}

public class DepartmentEnumNoTryCatch {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String input = scanner.next();

        Department dept = Department.fromCode(input);

        if (dept != null) {
            System.out.println("Full Form: " + dept.getFullForm());
        } else {
            System.out.println("Invalid department code entered.");
        }

        scanner.close();
    }
}

```





## OUTPUT:

<img width="1192" height="307" alt="image" src="https://github.com/user-attachments/assets/b9b692b8-b50e-43bc-9241-aeea6c4cc24e" />



## RESULT:
The program successfully defines an enum with a constructor, assigns full forms to each constant, and displays them correctly.

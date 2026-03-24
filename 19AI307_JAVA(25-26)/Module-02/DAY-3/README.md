# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To create a Java class named BankAccount with private instance variables accountNumber and balance, and to provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	create a class named BankAccount with private variables accountNumber and balance.
4.	Create setter methods setAccountNumber() and setBalance() to assign values to the variables.
5.	Create getter methods getAccountNumber() and getBalance() to retrieve the values.
6.	Create the Main class, create an object of BankAccount, and use setter methods to assign values.
7.	Retrieve and print values using getter methods and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;

class BankAccount {
    private String accountNumber;
    private double balance;
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        BankAccount acc = new BankAccount();
        acc.setAccountNumber(sc.next());
        acc.setBalance(sc.nextDouble());
        System.out.println("Account Number: " + acc.getAccountNumber());
        System.out.println("Balance: " + acc.getBalance());

        sc.close();
    }
}


```





## OUTPUT:
<img width="828" height="381" alt="image" src="https://github.com/user-attachments/assets/05b8c9d9-93d0-406f-8e64-881c59592a6f" />



## RESULT:
The program successfully creates a BankAccount class with private variables and accesses them using getter and setter methods.

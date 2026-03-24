# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A food delivery application manages and processes food orders made by two categories of users: NormalUser and PrimeUser. Each food order contains basic information such as an order ID, the customer's name, the cost of the ordered items (referred to as the total amount), and the delivery charge applied to that order.

## AIM:
To develop a Java program using inheritance to calculate the final payable amount for NormalUser and PrimeUser based on delivery charges.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	create a base class Order with variables: orderId, customerName, totalAmount, and deliveryCharge.
4.	Create two derived classes NormalUser and PrimeUser that extend the Order class.
5.	In each subclass, create a method to calculate the final amount using the given formulas.
6.	In the main class, accept input for 3 orders (user type, order details).Based on user type, create the object, calculate and display details, then stop the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java

import java.util.Scanner;
import java.text.DecimalFormat;
class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;
    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }
    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }
    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}
class NormalUser extends Order {
    public NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }
    
    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }
}
class PrimeUser extends Order {
    public PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    @Override
    double calculateFinalAmount() {
        return totalAmount + (deliveryCharge * 0.5);
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNextLine()) {
            String type = sc.nextLine().trim();
            if (type.isEmpty()) break;
            String orderId = sc.nextLine();
            String customerName = sc.nextLine();
            double totalAmount = sc.nextDouble();
            double deliveryCharge = sc.nextDouble();
            sc.nextLine(); 
            Order order;
            if (type.equalsIgnoreCase("Normal")) {
                order = new NormalUser(orderId, customerName, totalAmount, deliveryCharge);
            } else {
                order = new PrimeUser(orderId, customerName, totalAmount, deliveryCharge);
            }
            order.display(type);
        }
    }
}


```





## OUTPUT:
<img width="749" height="619" alt="image" src="https://github.com/user-attachments/assets/c590bce7-ff2e-40a1-af6d-75ad88a6b2bb" />





## RESULT:
The program successfully uses inheritance to differentiate between NormalUser and PrimeUser, calculates the final payable amount based on delivery charge rules, and displays the details for three orders correctly.

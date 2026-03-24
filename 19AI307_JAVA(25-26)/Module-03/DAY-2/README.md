# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

## AIM:
To write a Java program demonstrating method overriding using a base class Animal and subclasses Dog, Cat, and Cow.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a base class Animal with a method sound().
4. Create subclasses Dog, Cat, and Cow that extend Animal.
5. Override the sound() method in each subclass with specific sounds.
6. In the main class, create objects of each subclass and call the sound() method.
7. Display outputs and stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: NITHISHKUMAR S
RegisterNumber: 212223240109
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;
class Animal {
    public void sound() {
        System.out.println("Generic animal makes a sound");
    }
}
class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}
class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    @Override
    public void sound() {
        System.out.println("Cow moos");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        if (scanner.hasNextLine()) {
            String input = scanner.nextLine().trim().toLowerCase();
            
            Animal animal = null;
            
            switch (input) {
                case "dog":
                    animal = new Dog();
                    break;
                case "cat":
                    animal = new Cat();
                    break;
                case "cow":
                    animal = new Cow();
                    break;
                default:
                    System.out.println("Unknown animal");
                    break;
            }
            
            if (animal != null) {
                animal.sound();
            }
        }
        
        scanner.close();
    }
}


```





## OUTPUT:
<img width="546" height="302" alt="image" src="https://github.com/user-attachments/assets/1d3dc7a1-db84-4df0-b5f1-f1c6b6801d04" />



## RESULT:
The program successfully demonstrates method overriding, where each subclass provides its own implementation of the sound() method, producing different outputs for Dog, Cat, and Cow.

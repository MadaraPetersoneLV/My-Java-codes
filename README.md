# My-Java-codes

## CHECK IF THE LIST HAS A PARTICULAR NAME, METHOD - BOOLEAN
```java
 HelloWorld {
    public static void main(String[] args) {
        
        // List of invited people
        String[] peopleInvited = {"Oskars", "Anna", "Andris"};
        
        // name to check
        String name = "Anna";
        
        // call a method to check whether the name is in the list
        boolean isInvited = checkList(peopleInvited, name);
        
        // conditions whether a person is or is not invited
        if (isInvited) {
            System.out.println(name + " is invited to the party and is allowed to come!");
        } else {
            System.out.println(name + " is not invited to the party.");
        }
    }

    // create a method which goes through the peopleInvited
    public static boolean checkList(String[] peopleInvited, String name) {
        for (int i = 0; i < peopleInvited.length; i++) {
            if (peopleInvited[i].equals(name)) {
                return true; // Name found in the list, return true
            }
        }
        return false; // Name not found in the list, return false
    }
}
```

## USER INPUT NUMBERS, SUM BY USING METHODS
```java
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    //call the method to get the user input
    int number1 = userInput();
    int number2 = userInput();
    int result1 = number1 + number2;
    System.out.println("The sum by simply number1+number2: " + result1);
    
    //or the same can be done with a method
    int result2 = sum(number1, number2);
    System.out.println("The sum by calling a method: " + result2);
  }
    
  //Method where user inputs a number
  public static int userInput() {
    System.out.println("Enter a number: ");
    Scanner scanner = new Scanner(System.in);
    int numberEntered = scanner.nextInt();
    return numberEntered;
  }

    // Method to calculate the sum of two numbers
  public static int sum(int num1, int num2) {
        return num1 + num2;
  }

}
```

## RECTANGULAR
```java
public class Main {
    public static void main(String[] args) {
      
      String randomWord = "|  MADARA in a rectangular  |";
      int randomWordLength = randomWord.length();

      // First line -> ==========
      for (int i = 1; i <= randomWordLength; i++) {
        System.out.print("=");
      } System.out.println("");
      
      // Second line ->   |  randomWord   |
      System.out.print("|");
      for (int i = 1; i <= randomWordLength - 2; i++) {
        System.out.print(" ");
      } System.out.print("|"); System.out.println("");
      
      // Third line -> THE WORD
      System.out.println(randomWord);

      // Fourth line ->   |  randomWord   |
      System.out.print("|");
      for (int i = 1; i <= randomWordLength - 2; i++) {
        System.out.print(" ");
      } 
      System.out.print("|"); System.out.println("");
      
      // Last line -> ==========
      for (int i = 1; i <= randomWordLength; i++) {
        System.out.print("=");
      }
  
    }

  
}
```

## Wo Tech Wotech and FOR/WHILE loop - my code improved by AI
```Java
public class Main {
    public static void main(String[] args) {
        int inputNumber = 30;

        for (int i = 1; i <= inputNumber; i++) {
            boolean divisibleBy3 = i % 3 == 0;
            boolean divisibleBy5 = i % 5 == 0;

            if (divisibleBy3 && divisibleBy5)
                System.out.println("WoTech");
            else if (divisibleBy3)
                System.out.println("Wo");
            else if (divisibleBy5)
                System.out.println("Tech");
            else
                System.out.println(i);
        }
    }
}
```
## Wo Tech Wotech and FOR/WHILE loop - my code
```java
public class Main {
  public static void main(String[] args) {
      
      // 0. Create an option for user to input a number "inputNumber"
    
    int inputNumber = 30;

       // 1. Create growing numbers sequence
      int i = 1;
      while (i <= inputNumber) {

        if (i % 3 == 0 && i % 5 == 0)
          System.out.println("WoTech");
        
        // For numbers that are divided by 3: print out "Wo" .
        else if (i % 3 == 0)
        System.out.println("Wo");
        
          // For numbers that are divided by 5: print out "Tech".
        else if (i % 5 == 0) System.out.println("Tech");
      
        else System.out.println(i);

        // continue adding 1 to i
          i = i + 1;
      }
  
    }
}
```


## User Input - Enter words and read the whole story
```java
import java.util.Scanner; // import the Scanner class 

class Main {
  public static void main(String[] args) { ///////////////////////////////////////
    Scanner myObj = new Scanner(System.in);
    String color;
    String emotion;
    String bird;
    String verb;
    String verbSecond;
    
    // Enter and press Enter
    System.out.println("Enter random color and press Enter:"); 
    color = myObj.nextLine();   

    System.out.println("Enter random emotion:"); 
    emotion = myObj.nextLine();

    System.out.println("Name a bird:"); 
    bird = myObj.nextLine();

    System.out.println("Name an action (for example - reading):"); 
    verb = myObj.nextLine();

    System.out.println("Name another action:"); 
    verbSecond = myObj.nextLine();


    // This is left for the whole story afterwards
    System.out.println("\nHere is a story that we just made up:");
    System.out.println();
    System.out.println("The sky turned " + color + " and I suddenly felt " + emotion + ".\nI looked down and saw a " + bird +
    ". It looked like it had just been " + verb + ".\nWe looked at each other for a short while and then simply started " +
    verbSecond + " together."); 
    
    /////////////////////////////////////////////////
  }
}
```

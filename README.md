# My-Java-codes

## ROCK, PAPER, SIZ - second improved version
```java
import java.util.Random;
import java.util.Scanner;

class HelloWorld 
{
    public static void main(String[] args) {
        System.out.println("ROCK, PAPER, SIZZORS game");
        System.out.println();
        // run the game by calling runGameMethod
        runGameMethod();
    }
    
    public static void runGameMethod() {
        // my choise
        Scanner scanner = new Scanner(System.in);
        System.out.print("rock / paper / siz: ");
        String me = scanner.next();
        System.out.println("Me: " + me);
   
        // computer`s choise
        String[] options = {"rock", "paper", "siz"};
        int randomIndex = new Random().nextInt(options.length);
        String computer = options[randomIndex];
        System.out.println("Computer: " + computer + "\n");
        
            //if equals - we play again
            if (me.equals(computer)) {
            System.out.println("EQUALS! Let`s play again!\n");
            runGameMethod();
            }
            // I win condition
            else if ((me.equals("rock") && computer.equals("siz")) || 
                    (me.equals("paper") && computer.equals("rock")) || 
                    (me.equals("siz") && computer.equals("paper"))) {
                System.out.println("YOU WIN! :)\n");
                
            } else {
                System.out.println("YOU LOOSE :(");
            }


    }
}
```

## ROCK, PAPER, SIZ - first functioning draft
```java
import java.util.Random;
import java.util.Scanner;

class HelloWorld {
    public static void main(String[] args) {
        String me = runGameMethod();
        System.out.println();
        System.out.println("My choise: " + me);
        
        String computer = randomMethod();
        System.out.println("Computer choise: " + computer);
    }

// create runGameMethod
    public static String runGameMethod() {
    Scanner scanner = new Scanner(System.in);
    System.out.println("rock / paper / siz: ");
    String me = scanner.next();
    scanner.close();
    return me;
    }
    
    public static String randomMethod() {
        String[] options = {"rock", "paper", "siz"};
        int randomIndex = new Random().nextInt(options.length);
        String choosenOption = options[randomIndex];
        return choosenOption;
    }
}
```

## COMPARE NUMBERS AND RETURN, WHICH IS HIGHER
```java
/* Create a function that returns smallest number of 2 numbers.

For example:
User provides 5
User provides 7

Function returns 5
Main function prints out:
5 is the smallest number
*/

import java.util.Scanner;

class HelloWorld {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter first number: ");
        int firstNumber = scanner.nextInt();
        
        System.out.print("Enter second number: ");
        int secondNumber = scanner.nextInt();
        
        if (firstNumber == secondNumber) {
            System.out.println("Numbers are equal.");
        } else {int higherNumberIs = compareNumbers(firstNumber, secondNumber);
        
        System.out.println("Higher number is: " + higherNumberIs);}
        
       
    }
    
    public static int compareNumbers(int a, int b) {
        int smallerNumber;
        if (a > b) {
            smallerNumber = a;
        }
        else if (a < b) {
            smallerNumber = b;
        }
        else {smallerNumber = a; }
        return smallerNumber;
    }
}
```

# GUESS NUMBER. FIRST ATTEMPT, SOME DETAILS WERE CORRECTED BY AI
```java
import java.util.Scanner;

class HelloWorld 
{
    public static void main(String[] args) 
    {
        // create random number
        int numberInMyMind = 50;
        
        int number; // Declare number variable outside the loop
        
        // Loop until the guess is correct
        while (true) 
        {
            // call a method guessNumber to be executed which asks user to input number
            number = guessNumberMethod();
            
            ///////////// THE CONDITION depending on the guessed number ///////
            if (number > numberInMyMind) 
            {
                System.out.println("Too high, guess again. "); 
            } 
            else if (number < numberInMyMind) 
            {
                System.out.println("Too low, guess again. ");
            } 
            // when correct - say it and break the loop 
            else 
            { 
                System.out.println("Correct!"); 
                break;
            }
        }
    }
    
    ////////////////// GUESS NUMBER METHOD ///////////////////////
    public static int guessNumberMethod() 
    {
        // create the option to ask for number and input it. Return a number.
        Scanner scanner = new Scanner(System.in);
        System.out.println("Guess number 0 - 100: ");
        int number = scanner.nextInt();
        return number;
    }
    //////////////////////////////////////////////////////////////
}
```

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

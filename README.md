# My-Java-codes I am proud of
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

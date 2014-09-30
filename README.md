RockPaperScissors
=================

RockPaperScissors Game





import java.util.Scanner;
import java.util.Random;
 
public class RockPaperScissors {
 
    public static void main(String[] args) {
 
       
        int ROCK = 0;
        int SCISSORS = 1;
        int PAPER = 2;
         
        
        int intChoice = 4;
         
        
        Scanner key = new Scanner(System.in);
         
        System.out.print("Please enter rock, paper, or scissors: ");

        String choice = new String(key.nextLine());
         

        if (choice.compareToIgnoreCase("rock") == 0)
            intChoice = ROCK;

        else if (choice.compareToIgnoreCase("paper") == 0)
            intChoice = PAPER;

        else if (choice.compareToIgnoreCase("scissors") == 0)
            intChoice = SCISSORS;       
 
        
        Random randomGenerator = new Random();

        int randomInt = randomGenerator.nextInt(3);
         
        if (intChoice == randomInt)
            System.out.println("Tie!");

        else if (intChoice == 0 && randomInt == 1)
            System.out.println("Rock beats scissors! You win!");

        else if (intChoice == 0 && randomInt == 2)
            System.out.println("Paper covers rock... You lose.");

        else if (intChoice == 1 && randomInt == 0)
                System.out.println("Rock beats scissors... you lose.");

        else if (intChoice == 1 && randomInt == 2)
                System.out.println("Scissors cuts paper! You win!");

        else if (intChoice == 2 && randomInt == 0)
            System.out.println("Paper covers rock! You win!");

        else if (intChoice == 2 && randomInt == 1)
            System.out.println("Scissors cuts paper... You lose.");
      
         }
 
}

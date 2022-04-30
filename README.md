# Number-Guessing-Game
package programs;
import java.lang.Math;
import java.util.Scanner;
public class NumberGuessingGame{
public static void main(String[] args) {
   
    int right_guess = 1 + (int)(100* Math.random());
    int turns=0;
    Scanner scan=new Scanner(System.in);
    System.out.println("Guess a number between 1 to 100, You will have 10 turns!" );
    System.out.println("Best of Luck...!");
 
    int guess;
    int i=0;
    boolean win=false;
    while(win==false) {
    guess=scan.nextInt();
    turns++;
    
    if(guess==right_guess) {
      win=true;
    }
    else if(i>8){
      System.out.println("You loose!:( ");
      System.out.println("The right answer was: "+right_guess);
      System.out.println("Better Luck Next Time!");
      return;
    }
    
    else if(guess<right_guess){
      i++;
      System.out.println("Your Guess is lower than the right guess!.. Turns left: "+(10-i));
    }
    
    else if(guess>right_guess) {
      i++;
      System.out.println("Your Guess Is Higher Than THe Right Guess!.. Turns left: "+(10-i));
    }
      
  }
    
    System.out.println("YOu Win!:)");
    System.out.println("The number was "+right_guess);
    System.out.println("You used "+turns+" turns to guess the right number.");
    System.out.println("Your score is "+((11-turns)*10)+" out of 100");
    
}
}

import java.util.Scanner;
import java.util.Random;

public class GuessingGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int minRange = 1;
        int maxRange = 100;
        int randomNumber = random.nextInt(maxRange - minRange + 1) + minRange;
        int userGuess;

        System.out.println("Welcome to the Guessing Game!");
        System.out.println("Guess a number between 1 and 100.");

        do {
            System.out.print("Enter your guess: ");
            userGuess = scanner.nextInt();

            if (userGuess == randomNumber) {
                System.out.println("Congratulations! You guessed the correct number.");
            } else if (userGuess < randomNumber) {
                System.out.println("Too low! Try guessing higher.");
            } else {
                System.out.println("Too high! Try guessing lower.");
            }
        } while (userGuess != randomNumber);

        scanner.close();
    }
}

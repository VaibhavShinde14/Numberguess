import java.util.Scanner;
public class Numberguessing {

	// Function that implements the
	// number guessing game
	public static void
	guessingNumberGame()
	{
		// Scanner Class
		Scanner sc = new Scanner(System.in);

		// Generate the numbers
		int number = 1 + (int)(100* Math.random());

		// Given K trials
		int K = 10;

		int i, guessno;

		System.out.println(
			"A number is chosen"
			+ " between 1 to 100."
			+ "Guess the number"
			+ " within " + K + " trials.");

		// Iterate over K Trials
		for (i = 0; i < K; i++) {

			System.out.println("Guess the number:");

			// Take input for guessing
			guessno = sc.nextInt();

			// If the number is guessed
			if (number == guessno) {
				System.out.println(
					"Congratulations!"
					+ " You guessed the number.");
					System.out.println("You guessed the number in "+ i +" trials");
					System.out.println("Your got "+  (10-i)*10  + " points" );					
				break;
			}
			else if (number > guessno) {
				System.out.println(
					"The number is "
					+ "greater than " + guessno);
			}
			else if (number < guessno) {
				System.out.println(
					"The number is"
					+ " less than " + guessno);
			}
		}

		if (i == K) {
			System.out.println("You have exhausted "+ K + " trials.");

			System.out.println("The number was " + number);
		}
	}

	// Driver Code
	public static void
	main(String arg[])
	{

		// Function Call
		guessingNumberGame();
	}
}

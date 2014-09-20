import java.util.InputMismatchException;
import java.util.Scanner;
public class Assingment01 {
	
	public static void main(String[] args) {
		System.out.print("Hello, in this program we're going to help you with aritmethic problems.\n"
				+ "You are going to answer some simple addition equations.\n"
				+ "Enter 0 at anytime to exit the program.\n"
				+ "Here comes your first question: ");
		// the last given answer
		int answer = 0;
		// number of answered questions
		int counter = 0;
		// number of questions answered correctly
		int rightAnswer = 0;
		Scanner input;

		// Keep asking questions until the user enters 0 to exit
		do{		
			// Generate terms and a sum
			int term1 = (int) Math.ceil(Math.random() * (20 -1));
			int term2 = (int) Math.ceil(Math.random() * (20 - term1));
			int sum = term1 + term2;
			int correctAnswer = 0;
			// A random number to decide if the user should calculate 
			// a term or the sum
			int random = (int) Math.round(Math.random()  * 2);
			// tells if the user entered the correct answer
			boolean validAnswer = false;
			
			// Add another question to the counter
			counter++;
			
			// Keep asking the question until a valid answer is given,
			// that is, an integer
			while (!validAnswer) {
				// Generate the equation string.
				// The random number decides where the question mark should be
				// and what is the correct answer
				if (random == 0) {
					System.out.println("? + " + term2 + " = " + sum);
					correctAnswer=term1;
				}
				else if (random == 1) {
					System.out.println(term1+ " + ? = " + sum);
					correctAnswer=term2;
				}
				else {
					System.out.println(term1+" + "+ term2 + " = ?");
					correctAnswer=sum;
				}
				
				// Try if the input is a valid integer.
				// If not, ask the user to enter the answer again
				try {
					input = new Scanner(System.in);
					answer = input.nextInt();
					
					validAnswer = true;
				} catch(InputMismatchException e) {
					validAnswer = false;
					System.out.println("That was not a valid number, try again!");
				}
			}
			
			// If the user enters 0 to exit the questions loop,
			// then do not count the last question
			if (answer == 0) {
				counter--;
			}
			// Find out if the correct answer was entered
			else if(answer == correctAnswer){
				rightAnswer++;
				System.out.println("Good, you answered correctly! ");
				 	 
			}
			// Execute if the entered answer was wrong
			else if(answer != correctAnswer && answer != 0) {
				 System.out.println("Wrong answer, the correct answer was " + correctAnswer);
			}
		} while (answer != 0);
		
		// Calculate the percentage of questions answered correctly
		double percentCorrect = (double) rightAnswer/counter * 100;
		// Prints the amount of (correctly) answered questions.
		// Changes "question" to "questions" if more than one question was answered.
		System.out.printf("You have answered " + rightAnswer + " of " + counter + " question" + (counter > 1 ? "s" : "") + " correctly \n"
			+ "%.2f %%", percentCorrect);
	}	
}

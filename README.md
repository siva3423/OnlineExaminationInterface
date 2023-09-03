
import java.util.Scanner;

public class OnlineExam {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

      // Questions and Answers
        String[] questions = {
            "1. What is the capital of France?",
            "2. Which planet is known as the Red Planet?",
            "3. What is the largest mammal in the world?"
        };
        String[] options = {
            "A) Paris B) London C) Berlin D) Rome",
            "A) Mars B) Venus C) Earth D) Jupiter",
            "A) Elephant B) Blue Whale C) Giraffe D) Lion"
        };
        char[] answers = {'A', 'A', 'B'};

        int score = 0;

        // Display questions and get answers
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            System.out.println(options[i]);
            System.out.print("Your answer (A/B/C/D): ");
            char userAnswer = scanner.next().toUpperCase().charAt(0);

            if (userAnswer == answers[i]) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Incorrect. The correct answer is " + answers[i] + "\n");
            }
        }

        // Display final score
        System.out.println("Quiz completed! Your score: " + score + " out of " + questions.length);

        // Close the scanner
        scanner.close();
    }
}

import java.util.Scanner;

public class LoginProgram {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String correctUsername = "bell123";
        String correctPassword = "bell123";
        int attempts = 3;

        while (attempts > 0) {
            System.out.print("Enter username: ");
            String username = scanner.next();
            System.out.print("Enter password: ");
            String password = getPasswordInput();

            if (username.equals(correctUsername) && password.equals(correctPassword)) {
                System.out.println("Login successful!");
                break;
            } else {
                System.out.println("Incorrect username or password. " + (--attempts) + " attempts left.");
                if (attempts > 0) {
                    System.out.println("Please try again.");
                } else {
                    System.out.println("Sorry, you have run out of attempts. Account locked.");
                }
            }
        }
    }

    private static String getPasswordInput() {
        Console console = System.console();
        if (console == null) {
            Scanner
            

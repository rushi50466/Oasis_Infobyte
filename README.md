# Oasis_Infobyte
import java.util.Scanner;

public class ATM {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Authenticate user
        int userId = 0;
        int userPin = 0;
        boolean isAuthenticated = false;

        while (!isAuthenticated) {
            System.out.print("Enter User ID: ");
            userId = input.nextInt();

            System.out.print("Enter User PIN: ");
            userPin = input.nextInt();

            isAuthenticated = authenticateUser(userId, userPin);

            if (!isAuthenticated) {
                System.out.println("Invalid user ID or PIN. Please try again.");
            }
        }

        // User authenticated. Display menu options.
        int choice = 0;

        while (choice != 5) {
            displayMenu();
            choice = input.nextInt();

            switch (choice) {
                case 1:
                    viewTransactionHistory();
                    break;
                case 2:
                    withdrawMoney();
                    break;
                case 3:
                    depositMoney();
                    break;
                case 4:
                    transferMoney();
                    break;
                case 5:
                    System.out.println("Thank you for using our ATM. Goodbye!");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
                    break;
            }
        }
    }

    private static boolean authenticateUser(int userId, int userPin) {
        // Code to authenticate user and return true if successful, false otherwise
        if (userId == 1234 && userPin == 5678) {
            return true; // User authenticated successfully
        } else {
            return false; // Invalid user ID or PIN
        }
    }
    

    private static void displayMenu() {
        System.out.println("Choose an option:");
        System.out.println("1. View Transaction History");
        System.out.println("2. Withdraw Money");
        System.out.println("3. Deposit Money");
        System.out.println("4. Transfer Money");
        System.out.println("5. Quit");
        System.out.print("Enter choice: ");
    }

    private static void viewTransactionHistory() {
        // Code to display transaction history
    }

    private static void withdrawMoney() {
        // Code to handle withdrawal process
    }

    private static void depositMoney() {
        // Code to handle deposit process
    }

    private static void transferMoney() {
        // Code to handle transfer process
    }
}


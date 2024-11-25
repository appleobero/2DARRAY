import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user for the number of rows and columns
        System.out.print("Mag enter ka ng Number sa rows: ");
        int rows = scanner.nextInt();

        System.out.print("Mag enter ka ng Number sa columns: ");
        int columns = scanner.nextInt();

        // Create a 2D array with the specified dimensions
        int[][] array = new int[rows][columns];

        // Populate the array using nested for loops
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                array[i][j] = i * j; // Set the element to the product of its row and column indices
            }
        }

        // Print the 2D array in a table format
        System.out.println("\nGenerated 2D Array (Product of indices):");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print(array[i][j] + "\t"); // Print each element, separated by tabs for alignment
            }
            System.out.println(); // Move to the next line after each row
        }

        // Close the scanner
        scanner.close();
    }
}

import java.util.Scanner;

public class MinimumNotes {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the change to be given to Pranav: ");
        int N = scanner.nextInt();
        int[] denominations = {100, 50, 10, 5, 2, 1};
        int count = 0;

        for (int denomination : denominations) {
            if (N >= denomination) {
                count += N / denomination;
                N %= denomination;
            }
        }

        System.out.println("The smallest number of notes that will combine to give Rs. " + N + " is: " + count);
    }
}

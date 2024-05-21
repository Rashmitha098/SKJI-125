# SKJI-125
Unlock Java challenges: currency, age validation, numerical analysis, game assistance, and chatbot creation. Master versatility with hands-on tasks.
TASK 1A
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



TASK 1B
import java.util.Scanner;

public class TicketBooking {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the age of the person: ");
        int age = scanner.nextInt();
        
        String result = (age < 15 || age > 60) ? "Not Allowed" : "Allowed";
        System.out.println(result);
    }
}



TASK 2A
import java.util.Scanner;

public class SumOfDigits {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number: ");
        long n = scanner.nextLong();
        
        int oddSum = 0;
        int evenSum = 0;
        
        String numberString = String.valueOf(n);
        for (int i = 0; i < numberString.length(); i++) {
            int digit = Character.getNumericValue(numberString.charAt(i));
            if (digit % 2 == 0) {
                evenSum += digit;
            } else {
                oddSum += digit;
            }
        }
        
        System.out.println(oddSum + " " + evenSum);
    }
}


TASK 2B
import java.util.Scanner;

public class CandyGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the candy group number: ");
        int candyGroup = scanner.nextInt();
        
        String candyStr = String.valueOf(candyGroup);
        int occurrences = 0;
        for (int i = 0; i < candyStr.length(); i++) {
            if (candyStr.charAt(i) == '4') {
                occurrences++;
            }
        }
        System.out.println("Number of occurrences of digit 4: " + occurrences);
    }
}



TASK 3
import java.util.Scanner;

public class SimpleChatBot {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Hello! I am a simple chatbot. What's your name?");
        String name = scanner.nextLine();
        System.out.println("Nice to meet you, " + name + "!");
        
        System.out.println("How are you doing today?");
        String mood = scanner.nextLine();
        System.out.println("I'm glad to hear that you're " + mood + "!");
        
        System.out.println("What would you like to talk about?");
        String topic = scanner.nextLine();
        System.out.println("Sorry, I'm still learning and don't know much about " + topic + ".");
        
        System.out.println("Well, it was nice chatting with you, " + name + "! Goodbye!");
    }
}

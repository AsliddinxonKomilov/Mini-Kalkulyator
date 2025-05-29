# Mini-Kalkulyator
Java dasturlash tilida yozilgan oddiy mini kalkulyator
import java.util.Scanner;

public class Calculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Oddiy Kalkulyator");
        System.out.print("Birinchi sonni kiriting: ");
        double num1 = scanner.nextDouble();

        System.out.print("Amalni tanlang (+, -, *, /): ");
        char operation = scanner.next().charAt(0);

        System.out.print("Ikkinchi sonni kiriting: ");
        double num2 = scanner.nextDouble();

        double result;

        switch (operation) {
            case '+':
                result = num1 + num2;
                break;

            case '-':
                result = num1 - num2;
                break;

            case '*':
                result = num1 * num2;
                break;

            case '/':
                if (num2 == 0) {
                    System.out.println("0 ga bo‘lish mumkin emas.");
                    return;
                }
                result = num1 / num2;
                break;
            default:
                System.out.println("Noto‘g‘ri amal tanlandi.");
                return;
        }
        System.out.println("Natija: " + result);
    }
}

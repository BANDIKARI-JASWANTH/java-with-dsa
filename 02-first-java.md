QUESTION-1 Write a program to print whether a number is even or odd, also take input from the user.
CODE - 
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        if (num % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }

        sc.close();
    }
}
OUTPUT -
:Enter a number: 10
Even

QUESTION -2Take name as input and print a greeting message for that particular name.
CODE- 
import java.util.Scanner;

public class Greeting {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.println("Hello, " + name + "! Welcome.");

        sc.close();
    }
}
OUTPUT-
Enter your name: John
Hello, John! Welcome.

QUESTION-3 Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
CODE-
import java.util.Scanner;

public class SimpleInterest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal: ");
        double p = sc.nextDouble();

        System.out.print("Enter Time: ");
        double t = sc.nextDouble();

        System.out.print("Enter Rate: ");
        double r = sc.nextDouble();

        double si = (p * t * r) / 100;

        System.out.println("Simple Interest = " + si);

        sc.close();
    }
}
OUTPUT-
Enter Principal: 10000
Enter Time: 2
Enter Rate: 5
Simple Interest = 1000.0

QUESTION-4 Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
CODE-
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        double a = sc.nextDouble();

        System.out.print("Enter second number: ");
        double b = sc.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        if (op == '+') {
            System.out.println("Result = " + (a + b));
        } else if (op == '-') {
            System.out.println("Result = " + (a - b));
        } else if (op == '*') {
            System.out.println("Result = " + (a * b));
        } else if (op == '/') {
            if (b != 0) {
                System.out.println("Result = " + (a / b));
            } else {
                System.out.println("Cannot divide by zero.");
            }
        } else {
            System.out.println("Invalid operator.");
        }

        sc.close();
    }
}
OUTPUT-
Enter first number: 20
Enter second number: 5
Enter operator (+, -, *, /): *
Result = 100.0

QUESTION-5 Take 2 numbers as input and print the largest number.
CODE-
import java.util.Scanner;

public class LargestNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        if (a > b) {
            System.out.println("Largest number = " + a);
        } else {
            System.out.println("Largest number = " + b);
        }

        sc.close();
    }
}
OUTPUT-
Enter first number: 45
Enter second number: 89
Largest number = 89

QUESTION-6 Input currency in rupees and output in USD.
CODE-
import java.util.Scanner;

public class RupeesToUSD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter amount in Rupees: ");
        double rupees = sc.nextDouble();

        double exchangeRate = 83.50;

        double usd = rupees / exchangeRate;

        System.out.println("USD = " + usd);

        sc.close();
    }
}
OUTPUT-
Enter amount in Rupees: 8350
USD = 100.0

Question-1: Write a program to print whether a number is Even or Odd.
Code:
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        if (num % 2 == 0) {
            System.out.println(num + " is Even.");
        } else {
            System.out.println(num + " is Odd.");
        }

        sc.close();
    }
}

Output:
Enter a number: 15
15 is Odd.

Question-2: Take name as input and print a greeting message for that particular name.
Code:
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
Output:
Enter your name: Pujitha
Hello, Pujitha! Welcome.

Question-3: Write a program to input Principal, Time, and Rate (P, T, R) from the user and find Simple Interest.
Code:
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
Output:
Enter Principal: 10000
Enter Time: 2
Enter Rate: 5
Simple Interest = 1000.0

Question-4: Take in two numbers and an operator (+, -, , /) and calculate the value (Use if conditions).
Code:
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        if (op == '+') {
            System.out.println("Result = " + (num1 + num2));
        } else if (op == '-') {
            System.out.println("Result = " + (num1 - num2));
        } else if (op == '*') {
            System.out.println("Result = " + (num1 * num2));
        } else if (op == '/') {
            if (num2 != 0) {
                System.out.println("Result = " + (num1 / num2));
            } else {
                System.out.println("Division by zero is not possible.");
            }
        } else {
            System.out.println("Invalid Operator.");
        }

        sc.close();
    }
}

Enter first number: 20
Enter second number: 5
Enter operator (+, -, *, /): *
Result = 100.0

Question-5: Take 2 numbers as input and print the largest number.
Code:
import java.util.Scanner;

public class LargestNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int num1 = sc.nextInt();

        System.out.print("Enter second number: ");
        int num2 = sc.nextInt();

        if (num1 > num2) {
            System.out.println("Largest Number = " + num1);
        } else if (num2 > num1) {
            System.out.println("Largest Number = " + num2);
        } else {
            System.out.println("Both numbers are equal.");
        }

        sc.close();
    }
}
Output:
Enter first number: 35
Enter second number: 50
Largest Number = 50

Question-6: Input currency in Rupees and output in USD.
Code:
import java.util.Scanner;

public class RupeesToUSD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter amount in Rupees: ");
        double rupees = sc.nextDouble();

        double usd = rupees / 87.0;

        System.out.println("Amount in USD = " + usd);

        sc.close();
    }
}

Output:
Enter amount in Rupees: 8700
Amount in USD = 100.0

Question-7: Calculate Fibonacci Series up to n numbers.
Code:
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of terms: ");
        int n = sc.nextInt();

        int a = 0, b = 1;

        System.out.print("Fibonacci Series: ");

        for (int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        sc.close();
    }
}
Output:
Enter number of terms: 7
Fibonacci Series: 0 1 1 2 3 5 8

Question-8: Find out whether the given String is Palindrome or not.
Code:
import java.util.Scanner;

public class StringPalindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a String: ");
        String str = sc.nextLine();

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        if (str.equalsIgnoreCase(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }

        sc.close();
    }
}
Output:
Enter a String: madam
Palindrome

Question-9: Find Armstrong Numbers between two given numbers.
Code:
import java.util.Scanner;

public class ArmstrongRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter starting number: ");
        int start = sc.nextInt();

        System.out.print("Enter ending number: ");
        int end = sc.nextInt();

        System.out.println("Armstrong Numbers:");

        for (int i = start; i <= end; i++) {
            int num = i;
            int temp = num;
            int sum = 0;

            while (temp > 0) {
                int digit = temp % 10;
                sum += digit * digit * digit;
                temp /= 10;
            }

            if (sum == num) {
                System.out.println(num);
            }
        }

        sc.close();
    }
}
Enter starting number: 1
Enter ending number: 500

Armstrong Numbers:
1
153
370
371
407

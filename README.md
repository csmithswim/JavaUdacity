Contains work with Java from Udacity and other web resources while I learn Java and begin to work with a new IDE

Chapter 1 (Variables) from Udacity:
 
Java is case sensitive.
Variable names must start with a letter, no whitespace.

Declaring        Initializing
String player = "Jack";


long integers store larger numbers.
Both don't store fractions.
double can store fractions and long numbers.
Integers are limited to 10 digits. 
int maxInt= 324235352;
long muchMore = 353535353*46464646
double = fraction = 99.275;

To make comments in Java you use // or /* */

When doing arithmetic with Java, make sure to force a decimal place if you are storing the result in a double variable, i.e. double div = 5/2.0
When a double variable gets converted to an integer, such as when 5/2, is known as truncation.
You can also truncate with casting like so. 
int approx = (int) future;
double accurate = (double) x/y;

char is a character, it stores just one character and is used with a '', single numbers such as '2' can be stored too.

String fullText = "Hello";
char answer = 'b';

boolean just contain true or false
boolean fact = true;

For variables in java you have to specify the data type, i.e. int, str, etc.

Variables can be declared like so: int sum;

To console.log something in Java it is 
System.out.println();

To declare a string variable:
String driver;
driver = "Joe"; 
This is known as a string literal

driver.length();
Counts the numbers of letters in a string

driver.toUpperCase();
Capitalizes all letters

These methods require the variable to be reassigned to be used.

The + can be used to concatanate strings.

The print line command can use variables and strings to concatenate.

Chapter 2(Control Flow)
boolean isCold = ?; // true or false

if(isCold) {
    System.out.println("it's cold, wear a coat!");
} else if(isWarm){
    System.out.println("wear a t shirt!");
} else {
    System.out.println("Don't worry, go out naked!");
}

//Begining of MOSH tutorial
package com.csmithswim;

import java.awt.*;
import java.util.Arrays;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
        System.out.print("Please enter info for mortgage calculation.\n Principal: ");
        String principal = scanner.nextLine().trim();
        System.out.println(principal);
    }
}
package com.csmithswim;

import java.text.NumberFormat;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        final byte MONTHS_IN_YEAR=12;
        final byte PERCENT = 100;

        Scanner scanner = new Scanner(System.in);

        System.out.print("Principal: ");
        int principal = scanner.nextInt();

        System.out.print("Annual Interest Rate: ");
        float annualInterestRate = scanner.nextFloat();
        float monthlyInterest = annualInterestRate / PERCENT / MONTHS_IN_YEAR;

        System.out.print("Period (Years): ");
        byte years = scanner.nextByte();
        int numberOfPayments = years * MONTHS_IN_YEAR;

        double mortgage = principal
                    * (monthlyInterest * Math.pow(1 + monthlyInterest, numberOfPayments))
                    / (Math.pow(1+monthlyInterest, numberOfPayments) -1);
        String mortgageFormatted = NumberFormat.getCurrencyInstance().format(mortgage);
        System.out.println("Mortgage: "+ mortgageFormatted);
    }
}


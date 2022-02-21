# Practice 1

- [Practice 1: If-else Statement](https://docs.google.com/document/d/1bDOstOTZsbA8Dk-2UvFMXFP-fDAAhT5L/edit#heading=h.gjdgxs)

## Exercise 2:

### Part 1:

Create a grade calculator that follows the criteria:

- A - 85 and above shows Congrats, you scored an 'A'!
- B - 75 and above shows Good Job, you scored a 'B'!
- C - 50 and above shows You scored a 'C'. Try harder next time!
- Fail - Below 50 shows You have failed. Please come and see me.

You should check if the number entered is between 0 to 100, if not show “Please enter a valid score”. (fixed score)

**Answer:**

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {
        int myMarks = 75;

        if (myMarks < 0 || myMarks> 100) {
            System.out.println("Please enter a valid score");
        }
        else if (myMarks >= 85) {
            System.out.println("Congrats, you scored an 'A'!");
        }
        else if (myMarks >= 75) {
            System.out.println("Good Job, you scored a 'B'!");
        }
        else if (myMarks >= 50) {
            System.out.println("You scored a 'C'. Try harder next time!");
        }
        else {
            System.out.println("You have failed. Please come and see me");
        }
    }
}
```

### Part 2:

Get the grade inputs from the user and show the message above depends on the score input. (Assume user keys in a number).
You should check if the number entered is between 0 to 100, if not show “Please enter a valid score”.

Get the name of the student and the grade from the user input. And show the following as example:

Jean Looi, Congrats you scored an ‘A’.

**Answer:**

```java
import java.util.Scanner;

public class ControlPracticeDemo {

    public static void main(String[] args) {
        Scanner myInput = new Scanner(System.in);

        // name input
        System.out.println("Name Input");
        String myName = myInput.nextLine();
        System.out.println(myName);

        // grade input
        System.out.println("Grade Input");
        int myMarks = Integer.parseInt(myInput.nextLine());  // convert string input to int
        System.out.println(myMarks);

        // display block
        String displayA = String.format("Congrats %s, you scored an 'A'!", myName);
        String displayB = String.format("Good Job %s, you scored a 'B'!", myName);
        String displayC = String.format("You scored a 'C'. Try harder next time %s!", myName);
        String displayD = String.format("You have failed. Please come and see me %s", myName);

        // Logic
        if (myMarks < 0 || myMarks > 100) {
            System.out.println("Please enter a valid score");
        }
        else if (myMarks >= 85) {
            System.out.println(displayA);
        }
        else if (myMarks >= 75) {
            System.out.println(displayB);
        }
        else if (myMarks >= 50) {
            System.out.println(displayC);
        }
        else {
            System.out.println(displayD);
        }
    }
}
```

---

# Practice 2

- [Practice 2: Switch Statement](https://docs.google.com/document/d/1C2OnO_Ws7Q6BFvRQ7ZFbZnGzgFRMOzPF/edit#)

## Exercise 1:

Create a switch statement that switches between the different seasons of the year (winter, spring, summer, autumn) when given a numeric input 1 - 4. (Scanner package)

_Default_ cases should read “out of bounds” when a number outside of 1 - 4 is used

**Answer:**

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {
        Scanner myInput = new Scanner(System.in);

        // seasons input
        System.out.println("Season Input");
        int mySeason = Integer.parseInt(myInput.nextLine());  // convert string input to int
        System.out.println(mySeason);

        // Logic
        switch (mySeason) {
            case 1:
                System.out.println("Winter");
                break;
            case 2:
                System.out.println("Spring");
                break;
            case 3:
                System.out.println("Summer");
                break;
            case 4:
                System.out.println("Autumn");
                break;
            default:
                System.out.println("out of bounds");
        }
    }
}
```

## Exercise 2:

Create an app that returns the name of the month given the order of the month. ex: 1 should give you January, 12 should give you December etc. Get input from the user. (User will enter a number) Show error if user enter a number that is out of bound (1-12)

(Either hardcode the months in your Switch statement, or you can try the Date package to get the month)

**Answer:**

```java
public class ControlPracticeDemo {
    public static void main(String[] args) {
        Scanner myInput = new Scanner(System.in);

        // seasons input
        System.out.println("Month Input");
        int myMonth = Integer.parseInt(myInput.nextLine());  // convert string input to int
        System.out.println(myMonth);

        // Logic
        switch (myMonth) {
            case 1:
                System.out.println("January");
                break;
            case 2:
                System.out.println("February");
                break;
            case 3:
                System.out.println("March");
                break;
            case 4:
                System.out.println("April");
                break;
            case 5:
                System.out.println("May");
                break;
            case 6:
                System.out.println("June");
                break;
            case 7:
                System.out.println("July");
                break;
            case 8:
                System.out.println("August");
                break;
            case 9:
                System.out.println("September");
                break;
            case 10:
                System.out.println("October");
                break;
            case 11:
                System.out.println("November");
                break;
            case 12:
                System.out.println("December");
                break;
            default:
                System.out.println("out of bounds");
        }
    }
}
```

---

# Practice 3

- [Practice 3: While/ Do While & For Loop](https://docs.google.com/document/d/1s_eD7F9yDYEkIf3Qt8OGT1oHnj-yOno5/edit#)

## Exercise 1:

Create a while loop with a counter that gets incremented. Limit to 10 times.

**Answer:**

```java
public static void main(String[] args) {
    int i = 1;

    do {
        System.out.println(i);
        i++;
    }
    while (i <= 10);
}
```

## Exercise 2:

Modify the content to create a while loop that prints your name 15 times.
Hint: use a counter.

**Answer:**

```java
public static void main(String[] args) {

    String myName = "wc";

    int i = 1;

    do {
        System.out.println(myName);
        i++;
    }
    while (i <= 15);
}
```

## Exercise 4:

Modify the content to create a for loop that prints your name 10 times.
Hint: use a counter and increment it.

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {
        String myName = "wc";

        for (int i = 1; i <=10; i++) {
            System.out.println(myName);

        }
    }
}
```

## Exercise 5:

Modify the content to create a for loop that prints the numbers 1-10 and skips the number 7.

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {
        for (int i = 1; i <=10; i++) {
            if (i == 7) {
                continue;   // skips 7
            }
            else {
                System.out.println(i);
            }
        }
    }
}
```

---

# Practice 4

- [Java Control Flow Challenge Practices](https://docs.google.com/document/d/1jq2fFQWLkqPxuTS94wCDXFJL6Ni-jxXz/edit#heading=h.gjdgxs)

## Part 1: Commission Calculator

- Using IntelliJ, write a Java app that takes numerical input from a user
- The app should calculate commission based on this chart used by the retail store. (For a start, let’s assume that the input is a number)
  Example: if a user enters 7677 as their sales figure, it should calculate commission at 20%.
  Output: Your commission is $xxx

```
Sales Range     Commission
Above $10000    30%         >10000
$5000 - $10000  20%         >= 5000 && <= 10000
$1000 - $4999   10%         >= 1000 && <= 4999
Below $1000     N/A         < 1000
```

**Learning point:**
Exception Handling (try & catch)

- variable is expecting an int but received a string
- handle the error (exception) >> _NumberFormatException_

Integer.parseInt()

- Integer wrapper class
- cover more in Collection
- parseInt() method converts String to integer

try {}

- try statement allows you to define a block of code to be tested for any errors while it is being executed

catch () {}

- catch statement allows you to define a block of code to be executed if an error occurs in the try block
- if there is no error in the try block, this block of codes will not execute
- example `catch (NumberFormatException e) {`

**Steps**

1. get user input (scanner)
2. input validation (check if input entered is a number)
3. if input is not a number, display an error message for the user & as the user to key in again
4. if input is a number, get the correct commission rate for the calculation
5. Perform the calculation
6. Display the commission to User

### Exception Handling

- if parseInt() method throws an exception, whatever code after the method will NOT be executed & will immediately go into catch block

**Code Block**

```java
int userInput = 0;
boolean checkInputError = true;

do {
    try {
        // User Input
        System.out.println("Please enter your sales figure: ");
        userInput = Integer.parseInt(scanner.nextLine());  // capture user entry
        checkInputError = false;
    } catch (NumberFormatException e) {
        System.out.println("Error: Please enter a number.");
    }
}
while (checkInputError);  // while checkInputError = true
```

**Logic**

1. set default userInput = 0 & checkInputError = true
2. while checkUserInput = true, do the following
3. try: to get user input
   1. if input is valid, reassign value to userInput & reassign checkInputError to false
   2. if input is invalid, move to catch block to display error & the loop repeats
4. loop will repeat while checkErrorInput = true.

**Answer:**

```java
import java.util.Scanner;

public class Commission {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Set Default
        int userInput = 0;
        boolean checkInputError = true;

        do {
            try {
                // User Input
                System.out.println("Please enter your sales figure: ");
                userInput = Integer.parseInt(scanner.nextLine());  // capture user entry
                checkInputError = false;
            } catch (NumberFormatException e) {
                System.out.println("Error: Please enter a number.");
            }
        }
        while (checkInputError);

        double commission = 0.0;
        double userCommission = 0.0;

        // (4) Calculation
        if (userInput > 10000) {
            commission = 0.3;
        }
        else if (userInput >= 5000 && userInput <= 10000) {
            commission = 0.2;
        }
        else if (userInput >= 1000 && userInput <= 4999) {
            commission = 0.1;
        }
        userCommission = userInput * commission;

        System.out.println(String.format("Your commission is $%.2f", userCommission));

    }
}
```

- Good practice: `Scanner scanner = new Scanner(System.in);`

## Part 2: Movie Discounts

Steps

1. ask user for their age
2. ask user for the amount of tickets
3. catch exception
4. perform discount calculation
5.

**Code**

```java
package org.generation.java.ControlFLowLoops;

import java.util.Scanner;

public class Commission {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Set Default
        boolean checkInputError = true;
        int userAge = 0;
        int ticketQuantity = 0;
        int ticketPrice = 7;
        // Discount
        double ageDiscount = 0.0;
        double quantityDiscount = 0.0;
        double totalDiscount = 0;
        double finalTicketPrice = 0;
        double totalPrice = 0;

        System.out.println("Enter Age");
        userAge = Integer.parseInt(scanner.nextLine());

        System.out.println("Tickets Quantity");
        ticketQuantity = Integer.parseInt(scanner.nextLine());

        System.out.println(userAge);
        System.out.println(ticketQuantity);

        if (userAge < 5) {
            ageDiscount = 0.6;
        }
        else if (userAge > 60) {
            ageDiscount = 0.55;
        }
        else if (ticketQuantity > 2) {
            quantityDiscount = 0.3;
        }
        totalDiscount = ageDiscount + quantityDiscount;
        finalTicketPrice = ticketPrice * (1 - totalDiscount );
        totalPrice = finalTicketPrice * ticketQuantity;

//        System.out.println(ageDiscount);
//        System.out.println(quantityDiscount);
//        System.out.println(totalDiscount);
//        System.out.println(finalTicketPrice);
//        System.out.println(totalPrice);

        String display = "You have purchased %d tickets. The total price is $%.2f";
        System.out.println(String.format(display, ticketQuantity, totalPrice));
    }
}
```

**Code with Exception Handling**

```java
package org.generation.java.ControlFLowLoops;

import java.util.Scanner;

public class Commission {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Set Default
        boolean checkInputError = true;
        int userAge = 0;
        int ticketQuantity = 0;
        int ticketPrice = 7;
        // Discount
        double ageDiscount = 0.0;
        double quantityDiscount = 0.0;
        double totalDiscount = 0;
        double finalTicketPrice = 0;
        double totalPrice = 0;

        do {
            try {
                System.out.println("Enter Age");
                userAge = Integer.parseInt(scanner.nextLine());

                System.out.println("Tickets Quantity");
                ticketQuantity = Integer.parseInt(scanner.nextLine());

                checkInputError = false;
            }
            catch (NumberFormatException e) {
                System.out.println("Please enter valid input");
            }
        }
        while (checkInputError);

        // System.out.println(userAge);
        // System.out.println(ticketQuantity);

        if (userAge < 5) {
            ageDiscount = 0.6;
        }
        else if (userAge > 60) {
            ageDiscount = 0.55;
        }
        else if (ticketQuantity > 2) {
            quantityDiscount = 0.3;
        }
        totalDiscount = ageDiscount + quantityDiscount;
        finalTicketPrice = ticketPrice * (1 - totalDiscount );
        totalPrice = finalTicketPrice * ticketQuantity;

//        System.out.println(ageDiscount);
//        System.out.println(quantityDiscount);
//        System.out.println(totalDiscount);
//        System.out.println(finalTicketPrice);
//        System.out.println(totalPrice);

        String display = "You have purchased %d tickets. The total price is $%.2f";
        System.out.println(String.format(display, ticketQuantity, totalPrice));
    }
}
```

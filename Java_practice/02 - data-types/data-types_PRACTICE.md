# Practice 1

- [Practice 1: Variables & Data Types](https://docs.google.com/document/d/1h2HGa6mvvdLArq-NFUzKrdnweSrvSIe5/edit)

## Exercise 1:

Create a variable that contains your name. var
Create two more variables that contain your age and email. var
Print out the value of all 3 variables as a statement in the output.

**Answer:**

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {

        String myName = "wc";
        int myAge = 29;
        String myEmail = "wc@email.com";

        String response = String.format("name: %s, age: %d, email: %s", myName, myAge, myEmail);
        System.out.println(response);
    }
}
```

## Exercise 3:

Create the following variables with their respective data types.

myGender = 'F';
isJavaFun = true;
myFloat = 1.5f;  
myDouble = 99.99d;
mySalary = 1200.50;

Using String.format, print out the following.
My gender is F, and my salary is 1200.50. Java is fun! true.

**Answer:**

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {

        String myGender = "F";
        boolean isJavaFun = true;
        float myFloat = 1.5f;
        double myDouble = 99.99d;
        double mySalary = 1200.50;

        String response = String.format("My gender is %s, and my salary is %.2f. Java is fun! %b", myGender, mySalary, isJavaFun);
        System.out.println(response);
    }
}
```

- in String.format(), %.2f will format to 2 decimal place compared to %f

---

# Practice 2

- [Practice 2: Operators](https://docs.google.com/document/d/18JRqf56WNfBD2rIqiE0eH8BNU48qYe0Y/edit)

## Exercise 1:

Create a GST calculator to calculate the inclusive price.
Create a variable (data type) that will hold the original price exclusive of GST
Create a second variable (data type) that will hold a fixed value for the GST rate (7%)
Perform calculation on these 2 variables to determine and print out the final cost inclusive of GST.
Output: The cost is $10, the final cost is $10.70.

**Answer:**

```java
public class ControlPracticeDemo {

    public static void main(String[] args) {

        double myPrice = 10;
        double myGst = 0.07;
        double finalPrice = myPrice * (1 + myGst);

        System.out.printf("%.2f", finalPrice);
    }
}
```

## Exercise 2:

Create a matching word game. Allow the user to enter a word into the console.
If the word matches, print out ‘Matched!’
If the word does not match, print out ‘Not matched!’
Create a default word first (e.g. helloworld)
Get user input
Match the default word with the user input

**Answer:**

```java
import java.util.Scanner;

public class ControlPracticeDemo {

    public static void main(String[] args) {
        Scanner myInput = new Scanner(System.in);

        String myString = "helloworld";

        System.out.println("Word Input");
        String myWord = myInput.nextLine();

        if (myWord.equals(myString)) {
            System.out.println("Matched");
        }
        else {
            System.out.println("Not matched");
        }

    }
}
```

# Java Application Memory Allocation

- there are 2 kinds of memory used in Java
  - stack memory
  - heap memory
    Stack Memory store primitive data types & addresses of objects.
    The object values are stored in the heap memory.

example

```
const t-shirt = new ProductController();  // Creating a new instance object
const pants = new ProductController();  // Creating a new instance object

// value store in heap memory, stack memory store the address of the variable

String name1 = "hello";
String name2 = "hello";

 - "hello" stored in heap memory
 - name1, name2 stored in stack memory
 - same value but different address

String s1 = "A";
String s2 = "A";
String s100 = "A";
- all point to the same "A" to save memory

(s1 == s2) or (s1 == S100)  // output is true
- comparing the location where the value is

s2 = "a"
- s2 will be pointing to another location in heap memory
- s2 (location) is stored in stack memory

(s1 == s2)  // false

String s3 = new String("A")
(s1 == s3)  // false
```

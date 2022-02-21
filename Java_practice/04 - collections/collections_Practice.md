# Practice 1

- [Practice 1: Array and Array List](https://docs.google.com/document/d/1HG9cd65RhZ7Hc-W0w1tU_ejt0ksoGe0u/edit#)

## Exercise 1: Enter the codes

```java
package org.generation.java.Collections;

import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {

        // Normal Array
        int[] arr = new int[2];
        arr[0] = 1;
        arr[1] = 2;
        System.out.println(arr[0]);

        // ArrayList
        // Create an ArrayList with initial capacity 2
        ArrayList<Integer> ArrL = new ArrayList<Integer>(2);

        // Add elements to ArrayList
        ArrL.add(1);
        ArrL.add(2);

        // Access elements of ArrayList
        System.out.println(ArrL.get(0));

    }
}
```

## Exercise 2: Enter the codes

```java
package org.generation.java.Collections;

import java.lang.reflect.Array;
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {

        // Normal Array
        int[] arr = new int[3];
        arr[0] = 1;
        arr[1] = 2;
        arr[2] = 3;
        System.out.println(Arrays.toString(arr));
        // Outputs: [1, 2, 3]

        // ArrayList
        // Create an ArrayList, no need to specify size
        ArrayList<Integer> ArrL = new ArrayList<Integer>();

        // Add elements to ArrayList
        ArrL.add(1);
        ArrL.add(2);
        ArrL.add(3);
        ArrL.add(4);

        // Access elements of ArrayList
        System.out.println(ArrL);
        // Outputs: [1, 2, 3, 4]

    }
}
```

## Exercise 3: ArrayList

```java
package org.generation.java.Collections;

import java.lang.reflect.Array;
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {

        // (1) ArrayList of type String
        ArrayList<String> cars = new ArrayList<String>();

        // (2) Adding Values to ArrayList
        cars.add("Volvo");
        cars.add("BMW");
        cars.add("Ford");
        cars.add("Mazda");

        // (3) Display ArrayList Size
        int size = cars.size();
        System.out.println("total cars: " + size);
        // Outputs: total cars: 4

        // (4) Display car in position 2
        String secondCar = cars.get(1);
        System.out.println("secondCar: " + secondCar);
        // Outputs: secondCar: BMW

        // (5) Remove car in position 2
        cars.remove(2);
        System.out.println(cars);
        // Outputs: [Volvo, BMW, Mazda]

        // (6) use for loop to iterate over car array
        for(String car: cars){
            System.out.println("car: "+ car);
            // Outputs: car: Volvo
            // Outputs: car: BMW
            // Outputs: car: Mazda
        }

    }
}
```

## Exercise 4: Create Array (Built-in)

```java
package org.generation.java.Collections;

import java.lang.reflect.Array;
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {
        int[] arrayOf5 = new int[5];

        int i = 5;
        for (int index = 0; index <= 4; index++) {
            arrayOf5[index] = i;
            i = i + 5;
        }

        System.out.println(Arrays.toString(arrayOf5));
        // Outputs: [5, 10, 15, 20, 25]

        // (2) loop through array to print
        for (int index = 0; index <= 4; index++) {
            System.out.println(Integer.toString(arrayOf5[index]));
            // Outputs: 5, 10, 15, 20, 15
        }

        int index2 = 0;
        // create new array to store old array but remove 5
        int[] arrayNumber2 = new int[4];
        for (int index = 0; index <= 3; index ++) {
            arrayNumber2[index] = arrayOf5[index2 = index + 1];
        }

        System.out.println(Arrays.toString(arrayNumber2));
        // Outputs: [10, 15, 20, 25]
    }
}
```

## Exercise 5: Create Array List

```java
package org.generation.java.Collections;

import java.lang.reflect.Array;
import java.util.ArrayList;
import java.util.Arrays;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<Integer>();

        // loop through to add to ArrayList
        for (int i = 1; i <= 10; i++) {
            numbers.add(i);
        }

        // Print ArrayList
        System.out.println(numbers);
        // Outputs: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

        // loop through to print numbers
        for (int index = 0; index <= 9; index++) {
            System.out.print(numbers.get(index) + ", ");
        }
        // Outputs: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10,

        numbers.remove(4);
        System.out.println(numbers);
        // Outputs: [1, 2, 3, 4, 6, 7, 8, 9, 10]
    }
}
```

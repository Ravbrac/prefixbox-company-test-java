# Prefixbox Test

## Short questions

- What is a package? How do you define a package?
A: A package is a collection of classes, based on either said classes roles int the MVC structure (for smaller projects),
or on what aspect of the application are they responsible for.
- What is a constructor? When is it executed?
A: A constuctor is responsible for creating an instance of a class, it is executed when a new object based on the class is created.
- How do you implement inheritance in Java?
A: By creating relevant fields for the dependencies, and then defining said fields in the constructor of the class, which depends on said
dependencies. In Spring framework there are also special anotations (like @Autowired) to help you.
- How do you prevent someone to inherit from a class?
A: By making it private.
- What is a final variable? Where you can assign value to final variables?
A: A final variable is a private variable without a setter, essentialy a "variable" which's value you shouldn't change.
- Specify the available access modifiers in Java and briefly explain them
A: -Public: Anyone can acces them, by importong the relevant class.
   -Default: Can accesed in the same package without a getter/setter.
   -Protected: Can accesed in the same class without a getter/setter.
   -Private: Cannot be accessed without a getter/setter.
- Briefly explain the mechanism of exception handling
A: The first thing you need to do, is to "catch" the exception, basically telling the compiler that you expect an exception,
and what kind of exception you expect. Then you need to specify what should happen, if said exception is thrown, like returning a relevant
error message for example.
- What is the difference between an abstract class and an interface?
A: An interface can only have abstract methods, while an abstract class can have both abstract and not abstract methods. Also, interfaces
are implemented, while abstract classes are extended.
- What is the difference between Comparator and Comparable?
A: Comparator is an interface while Comparable is a method.
- How Iterable and Iterator interface works? What methods need to exist in a
class that implements them? What is their relation to for loops?

## Programming tasks

You can write your solutions in any language, you can even write pseudo code or
using only your own words.
The point is not to make a perfectly running application, the point is the way
you think!
Don't worry if you miss a semicolon or some parantheses.
You might use the Java stream API for your solutions but none of the exercises
require them

### Palindrom

Write a function which decides whether a text is palindrom(It's the same whether
you read it forwards or backwards). E.g.: abba, rotator, stats.
You might assume that the input string is not null, the length is greater than
1 and less than one million. **Strive for the low memory complexity!**

Example:

```java
public boolean isPalindrom(String input) {

}

isPalindrom("alma"); //false
isPalindrom("görög"); //true
```

Answer:

```java
public boolean isPalindrom(String input) {
  for(i = 0, i < input.length, i++) {
    if(input(i) != input(input.length - 1 - i)) {
      return false;
    }
  }
  return true;
}
```

### Find The Duplicate

You have an array that contains strings. Every item in the array is
unique except one which is present in the array exactly twice.
Write a function which finds the string that is present twice in the array.
You might assume that the input array is not null, the length is greater
or equal to 2 and less than one million. **Strive for the low time complexity!**

Example:

```java
public String findTheDuplicate(String[] input) {

}

String[] fruitBasket = new String[] { "apple", "banana", "coconut", "durian",
"banana", "elderberry", "fig", "grapefruit" };
findTheDuplicate(fruitBasket); //should return banana
```

Answer:


```java
public String findTheDuplicate(String[] input) {
  for(i = 0, i < input.length, i++) {
    for(j = 0, j < input.length, j++) {
      if(input(i) = input(j)) {
        return input(i);
      }
    }
  }
}
```

### Count The Words

You have a long string that has some meaning on a real language. For example a
whole novel in a single string.
Write a function that counts the occurence of each word inside the string and
writes them to the output in the following format: `word: number of occurences`
You might assume that the input is not null and not empty. The order of the
words on the ouput does not matter.
The solution might be case insensitive, you don't have to differentiate
bwetween capital and non-capital letters.
The punctuation marks and line endings are not part of the words!

Example:

```java
public void countTheWords(String crazyLongString) {

}

String boci = "Boci, boci tarka, se füle, se farka.";
countTheWords(boci);

//Output:
//boci:2
//tarka:1
//se:2
//füle:1
//farka:1
```

### What Is The Output

What is the output of the following Java application? Explain your solution!

```java
package com.mycompany.myproject;

public class Person {
    public String firstName;
    public String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }  

    @Override
    public String toString() {return this.firstName + " " + this.lastName;}
}

public class Main {
    public static void main(String[] args) {
        int i = 0;
        String s = "apple";
        Person p = new Person("Jonh", "Doe");

        doSomething(i, s, p);

        System.out.println(i);
        System.out.println(s);
        System.out.println(p);
    }

    public static void doSomething(int i, String s, Person p)
    {
        i = 5;
        s += "banana";
        p.lastName = "Rambo";
    }
}

```

## SQL

- What is the PRIMARY KEY?
- What is the difference between CLUSTERED INDEX and NONCLUSTERED INDEX?
- There is a table called `Employees`. Let's assume that the columns exist
and they have the right data type.
What is going to happen if we execute the script and we destroy
the database connection during the execution? What are the possible problems
that might occure?

```sql
BEGIN TRANSACTION

UPDATE Employees
SET Salary = Salary * 1.1
WHERE
    Salary < 250000
    AND IsActiveEmployee = 1
```

## Web and HTTP

- Specify the existing HTTP request methods and describe their usage!
- What are the groups of HTTP response status codes? Write an example for each group!

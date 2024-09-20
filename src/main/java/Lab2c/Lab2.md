  # Lab2b 
[//]: # (Write down studnet nama and Student ID)
Student Name: SY, Ming Lung 
SID: 20966896
```java
package Lab2b;

/*	Comp3111LEx\Lab2b\Book.java		*/
public class Book {
    private String chapters[];
    private static final int DEFAULT_CHAPTERS = 10;

    public Book() {
        chapters = new String[DEFAULT_CHAPTERS];
        for (int i = 0; i < chapters.length; i++)
            chapters[i] = "n/a";
    }
    public Book(String argument[]) {
        /* construct the object with an array of chapter names */
        /* PLEASE ADD YOUR CODE HERE */
        // Constructor based on the array of chapter names
        chapters = new String[argument.length];
        for (int i = 0; i < argument.length; i++)
            chapters[i] = argument[i];

    }
    public String getChapter(int i) {
        /* return the chapter by the given index */
        /* PLEASE ADD YOUR CODE HERE */
        // Return the chapter by the given index
        return chapters[i];
    }
    public String[] getChapters() {
        return chapters;
    }
}
```


# lab2c explanation
> By letting MobileComputer implements Chargeable, the code will be working
without any error. It is Chargeable is an interface, while MobileComputer is a class.
To use a interface, the class must implements the interface. The interface in Java works similar
to the abstract class, but it is more flexible. The class can implement multiple interfaces, but
can only inherit from one class.

```java
package Lab2c;

/*	Comp3111LEx\Lab2c\MobileComputer.java
	Inherits from Computer, class library for Lab2 Exercise 3	*/
public class MobileComputer extends Computer implements Chargeable {
    private int battery;
    public MobileComputer() {
        secret = "MobileComputer secret";
        battery = 5;
    }
    @Override
    public void work() {
        if (battery > 0) {
            System.out.println("It is working on my lap.");
            battery--;
        } else
            System.out.println("Running out of battery");
    }
    public void charge() {
        if (battery < 10)
            battery++;
    }
}

```

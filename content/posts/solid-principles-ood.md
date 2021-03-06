+++
author = "Krishankant"
authorTwitter = ""
cover = ""
date = 2021-09-24T20:21:27Z
description = "Explaination of solid principles with example."
keywords = []
showfullcontent = false
tags = ["LLD", "OOD", "solid-principle"]
title = "Solid Principles ( OOD )"

+++
# Solid Principles

**Best** **Video** : [https://youtu.be/gumM1H4qLUM](https://youtu.be/gumM1H4qLUM)

**Best Artcile :** [https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/](https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/)

**SOLID stands for:**

* The **S**ingle Responsibility Principle
* The **O**pen-Closed Principle
* The **L**iskov Substitution Principle
* The **I**nterface Segregation Principle
* The **D**ependency Inversion Principle

### 1. Single Responsibility :

> The Single Responsibility Principle states that a class should do one thing and therefore it should have only a single reason to change.

Only one potential change (database logic, logging logic, and so on.) in the software’s specification should be able to affect the specification of the class.

This means that if a class is a data container, like a Book class or a Student class, and it has some fields regarding that entity, it should change only when we change the data model.

Example :

```java
public class Book {
    private String bookName;
    private String author;
    private String text;

    public boolean findByAuthor(String authorName){
        return author.contains(authorName);
    }
    public boolean findByName(String bookName){
        return bookName.contains(bookName);
    }
    void printToConsole(){
        // details to print
    }
}
```

Here, in this above example, `printToConsole()`  method is not related to Book. As, it may be needed in future to print in a file, then in that case we have to make changes in the class which is against the **single responsibility**.

### 2. The Open-Closed Principle

The Open-Closed Principle requires that **classes should be open for extension and closed to modification.**

Modification means changing the code of an existing class, and extension means adding new functionality.

Example:

```java
public class Operations {
    public double calculate(double a1, double a2, String operationType){
        switch(operationType){
            case "+": {
                return a1+a2;
            }
            case "-": {
                return a1-a2;
            }
            default:
        }
        return 0;
    }
}
```

In this example, lets say we need to add one more operation say division. Then in that case we have to make changes in the code of class `Operations` which can create bugs into the existing features like `+` and `-` operation. And this is violation of open-close principle.

So, to avoid any bugs and abide by the open close principle we can make following changes.

```java
public interface Operations {
    public double calculate(double a1, double a2);
}

class AddOpearation implements  Operations{
    @Override
    public double calculate(double a1, double a2){
        return a1+a2;
    }
}
class DivisionOpearation implements  Operations{
    @Override
    public double calculate(double a1, double a2){
        return a1/a2;
    }
```

So, we converted the class `Operations` into an interface and then we can implement the interface into whatever operations class that we create according to requirements.

### 3. Liskov Substitution Principle

The Liskov Substitution Principle states that subclasses should be substitutable for their base classes.

This means that, given that class B is a subclass of class A, we should be able to pass an object of class B to any method that expects an object of class A and the method should not give any weird output in that case.

```java
class Rectangle {
	protected int width, height;

	public Rectangle() {
	}

	public Rectangle(int width, int height) {
		this.width = width;
		this.height = height;
	}

	public int getWidth() {
		return width;
	}

	public void setWidth(int width) {
		this.width = width;
	}

	public int getHeight() {
		return height;
	}

	public void setHeight(int height) {
		this.height = height;
	}

	public int getArea() {
		return width * height;
	}
}
```

```java
class Square extends Rectangle {
	public Square() {}

	public Square(int size) {
		width = height = size;
	}

	@Override
	public void setWidth(int width) {
		super.setWidth(width);
		super.setHeight(width);
	}

	@Override
	public void setHeight(int height) {
		super.setHeight(height);
		super.setWidth(height);
	}
}
```

But when tester just came up with the testing function `getAreaTest()` and tells you that your `getArea` function fails to pass the test for square objects.

```java
class Test {

   static void getAreaTest(Rectangle r) {
      int width = r.getWidth();
      r.setHeight(10);
      System.out.println("Expected area of " + (width * 10) + ", got " + r.getArea());
   }

   public static void main(String[] args) {
      Rectangle rc = new Rectangle(2, 3);
      getAreaTest(rc);

      Rectangle sq = new Square();
      sq.setWidth(5);
      getAreaTest(sq);
   }
}
```

### 4. Interface Segregation Principle

Interface Segregation Principle is about separating the interfaces.

The principle states that many client-specific interfaces are better than one general-purpose interface. Clients should not be forced to implement a function they do no need.

Example :

This is a simple principle to understand and apply, so let's see an example.

```java
public interface ParkingLot {

	void parkCar();	// Decrease empty spot count by 1
	void unparkCar(); // Increase empty spots by 1
	void getCapacity();	// Returns car capacity
	double calculateFee(Car car); // Returns the price based on number of hours
	void doPayment(Car car);
}

class Car {

}
```

We modeled a very simplified parking lot. It is the type of parking lot where you pay an hourly fee. Now consider that we want to implement a parking lot that is free.

```java
public class FreeParking implements ParkingLot {

	@Override
	public void parkCar() {

	}

	@Override
	public void unparkCar() {

	}

	@Override
	public void getCapacity() {

	}

	@Override
	public double calculateFee(Car car) {
		return 0;
	}

	@Override
	public void doPayment(Car car) {
		throw new Exception("Parking lot is free");
	}
}
```

Our parking lot interface was composed of 2 things: Parking related logic (park car, unpark car, get capacity) and payment related logic.

But it is too specific. Because of that, our FreeParking class was forced to implement payment-related methods that are irrelevant. Let's separate or segregate the interfaces.

![](/uploads/ood-solid-princ.png)

We've now separated the parking lot. With this new model, we can even go further and split the **PaidParkingLot** to support different types of payment.

Now our model is much more flexible, extendable, and the clients do not need to implement any irrelevant logic because we provide only parking-related functionality in the parking lot interface.

### 5. Dependency Inversion Principle

The Dependency Inversion principle states that our classes should depend upon interfaces or abstract classes instead of concrete classes and functions.

We want our classes to be open to extension, so we have reorganized our dependencies to depend on interfaces instead of concrete classes.
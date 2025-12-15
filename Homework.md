# Part A - Understanding The Structure of OOP
## Classes
- What's a class?
**Ans:** It's a datatype that defines data and methods which are used to manipulate said data. A programmer can use the class to create instances which are usually called objects.
- What does a class contain?
**Ans:** It has properties related to whatever the class is about. For example, a car class would probably have a speed property. Classes also have methods to utilize these properties to do stuff. And in our car class example, there could be a method to move the car forward.
- Why are classes important in program design?
**Ans:** Because it allows the programmer to define a common datatype once which can be repeatedly used to create instances of it with their own data sets. All the attributes and methods are kept together instead of variables being passed around functions which reduces unnecessary dependencies and keeps everything organized.
## Objects/Instances
- What's an object/instance?
**Ans:** An instance of a class is known as an object. It has all the properties/attributes and methods of the class it's an instance from, but it has it's own set of values. Each instance has their own values.
- How is an object created from a class?
**Ans:** It depends on the language you're using but in python you do something like `<name of the object/instance> = <name of your class>(<anything that the class constructor needs>)`. The class constructor is basically the initialization function. This function is automatically executed everytime a new instance is created to basically set it up with base values and such. Obviously, what values it takes in as an argument depends on how the class constructor is defined by the programmer.
- Give a simple real-word example.
**Ans:** I'll do this in C# for fun.
```c#
using System;

class Car {
	// Properties/Attributes
	int speed;
	
	// Constructor to initialize all instances
	public Car(int speed) {
		this.speed = speed;
	}
	
	// Methods to use all the data defined in an instance
	public void getSpeed() {
		Console.WriteLine("Speed: " + speed);
	}
}

class Program {
	static void Main() {
		// Create a new instance and initialize it with all data the constructor requires
		Car car = new Car(5);
		
		// Use the method defined by the class
		car.getSpeed();
	}
}
```
# Part B - OOP Features
## Inheritance
Allows a class to inherit all the properties/attributes and methods from another class. Basically, a class can use another class as it's foundation/base and extend it further or override existing stuff with it's own attributes/properties and methods. The class that is inherited from another class is known as a child class.

Since all attributes/properties and methods are reused, there is no need to rewrite them. It also makes it easier to extend functionality keep code organized in a hierarchy while also ensuring that common behaviors are consistently implemented across related classes.
```c#
using System;

// Base class
class Ford {
	public string brand = "Ford";
}

// Child class
class Mustang : Ford {
	public string model = "Mustang";
}

class Program {
	static void Main() {
		Mustang car = new Mustang();
		Console.WriteLine(car.brand + " " + car.model);
	}
}
```
The above code will output "Ford Mustang". And as you can see, `brand` is defined in the Ford class but can be used even though the `car` instance is of the `Mustang` class. This shows that the `Mustang` class has the `brand` property defined.
## Encapsulation
Bundling all the attributes/properties and methods in a class together and controlling how it's accessed to prevent direct access to internal variables.

This protects data from being changed incorrectly making code more safe and reliable while also helping to manage complexity in larger programs. The only place encapsulated data can be changed is inside the class itself.
```c#
class BankAccount {
    private double balance;
    public void deposit(double amount) {
        balance += amount;
    }
    public double getBalance() {
        return balance;
    }
}
```
In the above code, the only way to read the value stored in `balance` is to use the `getBalance` method. Trying to directly access it causes a compile-time error.
## Polymorphism and Method Overloading
Polymorphism allows different classes to use the same method names while behaving differently.
```c#
class Animal {
    public virtual void speak() {
        Console.WriteLine("The animal makes a sound.");
    }
}
class Cat : Animal {
    public override void speak() {
        Console.WriteLine("The cat meows.");
    }
}
```
The `Cat` class defines it's own `speak` method to override the method of the same name defined by the `Animal` class. So although the `Cat` class inherits everything from the `Animal` class, the `speak` method will behave differently.
### Method Overloading
Method overloading allows multiple methods with the same name to be defined in the same class though they must have different parameters.
```c#
class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    public int add(int a, int b, int c) {
        return a + b + c;
    }
}
```
Depending on how many arguments are passed to the `add` method, a different method will be used. The `add` method accepts either 2 or 3 numbers.

Makes code more flexible and easier to extend, improves readability and allows the same functions to behave differently depending on how many arguments are passed to it.
## Data Hiding
Data hiding means restricting access to internal data by using access modifiers e.g. `private`, `protected`, and `public` in C#.
```c#
class Student {
    private int age;
    public void setAge(int value) {
        if (value > 0) age = value;
    }
    public int getAge() {
        return age;
    }
}
```
This prevents invalid data, increases security and reduces bugs caused by unintended data changes. The modifiers tells the programmer the scope in which the data of a class can be changed. For example, a programmer can be absolutely sure that all private variables can be modified only within the class itself unless a `set` function is defined for that variable. And even then the programmer can verify the variable is being set properly within that function to verify proper logic as in the code above where age cannot be set to lower than 0. Programmers can also determine whether the data can be read, set, or both.
## Reusability
Reusability is where code is written once and used everywhere applicable. This can be done by using functions and classes as these can be constantly reused.
```c#
class MathHelper {
    public int square(int number) {
        return number * number;
    }
}
```
This class can be used basically everywhere without the programmer having to rewrite the logic for the `square` method.
# Applications of Object Oriented Programming
- What types of software commonly use OOP?
**Ans:** It's widely used in large, complex programs that needs to be easily maintainable and extensible. OOP works well when software is built from many interacting parts, because real-world objects can be modelled as classes.

For example, games heavily use OOP because game elements can be represented as objects each of which have their own properties and methods which makes it easy to add new characters or items, allows code to be reused through inheritance and helps manage complex game logic.

Mobile apps use OOP to organise different parts of the app into classes e.g. user profiles, notifications, settings etc. This keeps the code structured and readable, the app easier to update and makes it easier to collaborate when many developers work on the same app.

Business software often handles large amounts of data and many rules e.g. payroll systems, inventory management, banking systems etc. Classes can be used to models real-world entities like customers and orders, improves security through encapsulation and data hiding and makes the business systems easier to maintain and scale up.

Modern web applications use OOP on both the front end and back end to separate logic into reusable components, make debugging easier and allow features to be added without rewriting existing code saving both time and effort while keeping the code lean and minimal.
- Name programming languages that use OOP.
**Ans:** Two of the most programming languages that  uses OOP is C# and Java. In these languages, you are literally forced to use OOP. But a lot of other programming languages out there offers OOP although you're not required to use it unlike C# and Java.
# Activities
![[Pasted image 20251214231809.png]]
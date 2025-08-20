# Method

## What is Method ?
- Method is used to perform certain task.
- It's a Collection that perform some specific task.
- It can be used to bring the code readability and re-usability.

![img1.png](.idea/Images/img1.png)

## How to declare method 

    public int sum(int a,int b)throws Exception{
    // method body 
    }

### Access Sprcifiers:
- Public : can be access through any any class in any package.
- Private: can be access by methods only in thr same class.
- Protected: can be access by other by other clases in same Package or other sub-classes in different package.
- Default: if we do not mention anything,then Deffalt specifier is used by Java.It can be only accessed by classes in same package.
---

### Return Type
- Method do not retrun anything use "void"
- Use Class Name or primitive data types as return type of the method.

---

### Method Name:

- It should be verb (some kind of action)
- Should start with small letter and follow camel case in case of multiple words.

---

### Parameters:
-It's a list of variable that will be used in the method.
- Parameter list can be blank too.
---

## Types of Method:
- System Defined Method :
  - Methods which are already defined and ready to use in java like Math.sqrt()

- User Defined Method
  - Method which programmer creates based upon the program necessity.
  
- Overloaded Method
    - More than one method with same name is created in same class.

- Overridden Method 
  - Subclass has the same method as the parent class.

- Static Method
  - These methods are associated with the class.
  - Can be called just with class name.
  - Static methods can not access Non Static Instance variable and methods.
  - Static method can not be overridden.

When to declare method Static :
- Methods which do not modify the state of the object can be declared Static.
- Utility Method which do not use any instance variable and compute onlt on arguments.
    - example: factory design pattern


- Final Method 
  - Final method can not be overridden in java.
  - Why?Final method means its implementation can not be changed.If child class can not change its implementation then no use of overridden.


- Abstract Method
  - it is defined only in Abstract classes.
  - Only method declaration is done 
  - its implementation is done in child classes.

    

### Variable Aruments (VARARGS):
- Variable number of inputs in the parameter.
- Only one variable argument can be present in the method.
- It should be the last argument in the list.



# Constructor 
- It is useed to create an Instance.
- Its Similar to method expect:
  - Name : Constructor name is same as Class Name 
    - Return Type : Construtor do not have any any return type.
      - Constructor can not be static or final or abstract,synchronized.

#### Example:
            // Driver Class
            class Deedbee {
    
            // Constructor
            Deedbee()
            {
                super();
                System.out.println("Constructor Called");
            }
    
            // main function
            public static void main(String[] args)
            {
                Deedbee bee = new Deedbee();
            }
            }

Frequently asked interview question on Construtor:

- Why comstrutor do no have return type?
  - Constructors do not have a return type, not even void, because their primary role is to initialize an object, not to return a value. The process of object creation implicitly returns a reference (an instance) of the class itself. This is handled by the runtime system, not by an explicit return statement in the constructor's code.
  - If a return type were added to a constructor, the compiler would treat it as a regular method that happens to have the same name as the class, not as a constructor. The absence of a return type is how the compiler distinguishes a constructor from other methods.

- Why construtor can not be final ?
  - The final keyword stops a method from being overridden in a subclass. Constructors are never inherited, so they cannot be overridden, making the final keyword irrelevant for them. 



- Why constructor can not be abstract?
    - An abstract method has no implementation and must be completed by a subclass. A constructor's entire purpose is to provide the implementation for creating an object, so it cannot be abstract.

- Why constructor can not be static?
  - A static method belongs to the class itself, not to any specific object. A constructor is fundamentally tied to creating and initializing an individual object instance, which is the opposite of what static means.


- Can we define constructor in interface?
  - Interfaces are templates that cannot be used to create objects directly (they can't be instantiated). Since constructors are for initializing objects, they have no function in an interface.


- Why construtor name is same as of class name ?
  - This is a required convention. It's how the compiler identifies the special method responsible for constructing an object, especially since it lacks a return type.

## Types of constructor :
- Default
- No Arg
- Parametrized
- Constructor Overloaded
- Private Constructor
- Constructor Changing 
  - this
  - super

### Default :
If no constructor is defined in a class, the Java compiler automatically provides a default constructor. This constructor doesn’t take any parameters and initializes the object with default values, such as 0 for numbers, null for objects

#### Example:

        // Java Program to demonstrate
        // Default Constructor

        import java.io.*;        
        // Driver class
        class DeedBee{
        // Default Constructor
        DeedBee() { 
            System.out.println("Default constructor");             
        }    
        // Driver function
        public static void main(String[] args)
        {
           Deedbee hello = new DeedBee();
        }
        }

### No Arg :

if we write a constructor with no arguments, the compiler does not create a default constructor.This type of constructor is known as No Arg Constructor

### Parametrized :

A constructor that has parameters is known as parameterized constructor. If we want to initialize fields of the class with our own values, then use a parameterized constructor.

#### Example:

        // Java Program for Parameterized Constructor
    import java.io.*;
    
    class Deedbee {

    // data members of the class
    String name;
    int id;
  
    Deedbee(String name, int id) {
        this.name = name;
        this.id = id;
     }
    }
    
    class Ddb
    {
    public static void main(String[] args)
    {
    // This would invoke the parameterized constructor
    Deedbee deed = new Deedbee("Sweta", 68);
    System.out.println("DeedName: " + deed.name+ " and DeedId: " + dee.id);
     }
    }

### Constructor Overloaded:

This is a key concept in OOPs related to constructors is constructor overloading. This allows us to create multiple constructors in the same class with different parameter lists.

#### Example:
        
        class Box {
        double length, width, height;
    
        // Constructor with no parameters
        Box() {
            length = width = height = 0; // Default values
        }
    
        // Constructor with one parameter
        Box(double side) {
            length = width = height = side; // Cube
        }
    
        // Constructor with three parameters
        Box(double length, double width, double height) {
            this.length = length;
            this.width = width;
            this.height = height; // Custom dimensions
        }
    
        // Method to calculate volume
        double calculateVolume() {
            return length * width * height;
        }
        }
        
        public class Main {
        public static void main(String[] args) {
        // Using different constructors
        Box box1 = new Box(); // Default box
        Box box2 = new Box(5); // Cube
        Box box3 = new Box(2, 3, 4); // Custom box

        // Displaying volumes
        System.out.println("Volume of box1: " + box1.calculateVolume());
        System.out.println("Volume of box2: " + box2.calculateVolume());
        System.out.println("Volume of box3: " + box3.calculateVolume());
        }
    }


## Constructor Chaining :

Constructor chaining is the process of calling one constructor from another constructor with respect to current object.
One of the main use of constructor chaining is to avoid duplicate codes while having multiple constructor (by means of constructor overloading) and make code more readable.

- Within same class: It can be done using this() keyword for constructors in the same class
- From base class: by using super() keyword to call the constructor from the base class.

Constructor Chaining within the same class using this() keyword:

![img2.png](.idea/Images/img2.png)

#### Example:

    // Java program to illustrate Constructor Chaining
    // within same class Using this() keyword
    class Temp
    {
    // default constructor 1
    // default constructor will call another constructor
    // using this keyword from same class
    Temp()
    {
    // calls constructor 2
    this(5);
    System.out.println("The Default constructor");
    }

    // parameterized constructor 2
    Temp(int x)
    {
        // calls constructor 3
        this(5, 15);
        System.out.println(x);
    }

    // parameterized constructor 3
    Temp(int x, int y)
    {
        System.out.println(x * y);
    }

    public static void main(String args[])
    {
        // invokes default constructor first
        new Temp();
        }
    }

    Constructor Chaining to other class using super() keyword :
    
                        // Java program to illustrate Constructor Chaining to
    // other class using super() keyword
    class Base
    {
    String name;
    
        // constructor 1
        Base()
        {
            this("");
            System.out.println("No-argument constructor of" + 
                                               " base class");
        }
    
        // constructor 2
        Base(String name)
        {
            this.name = name;
            System.out.println("Calling parameterized constructor" 
                                                  + " of base");
        }
        // parameterized constructor 4
    Derived(String name)
    {
        // invokes base class constructor 2
        super(name);
        System.out.println("Calling parameterized " + 
                           "constructor of derived");
    }

    public static void main(String args[])
    {
        // calls parameterized constructor 4
        Derived obj = new Derived("test");

        // Calls No-argument constructor
        // Derived obj = new Derived();
        }
    }



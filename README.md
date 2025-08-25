# Exception Handling

## What is Exception?

- It's an event,that pccurs during the excution of the program.
- It will disturb your program noraml flow
- It Creates the Exception Object,which contains information about the Error like 
  - Its Type of Exception and Message.
  - Stack trace etc.
- Runtime system use this Exception Object and find the class which can handle it.

![img.png](.idea/Images/img.png)

![img1.png](.idea/Images/img1.png)

## Exception Hierarchy:

![img2.png](.idea/Images/img2.png)

### Un-Checked/Runtime Exception:
These are the exceptions which occurs during runtime and compiler not forcing us to handle them.

![img3.png](.idea/Images/img3.png)


#### ClassCastException :

![img4.png](.idea/Images/img4.png)

#### ArithmeticException:

![img5.png](.idea/Images/img5.png)

#### IndexOutOfBoundException:

![img6.png](.idea/Images/img6.png)

#### NullPointerException:

![img7.png](.idea/Images/img7.png)

#### IllegalArgumentException:

![img8.png](.idea/Images/img8.png)

### Checked/Compile time Exception :
- Complier verifies them during the compile time of the code and if not handled properly,code compilation will fail.

![img9.png](.idea/Images/img9.png)

## throws :
"throws" tells hat,this method MIGHT throws this exception(or might not),so pls caller you handle it appropriately.

![img10.png](.idea/Images/img10.png)

![img11.png](.idea/Images/img11.png)

## try/catch block :

![img12.png](.idea/Images/img12.png)



## How to handle the exception 

Using:try,catch,finally,thorw ,throws

1. Try/Catch :
- Try block specify the code which can throw exception.
- Try block is followed either by Catch block or Finally block.
- Catch block is usec to catch all the exception which can be thrown in the try block.
- Multiple catch block can be used.

![img13.png](.idea/Images/img13.png)

![img14.png](.idea/Images/img14.png)

2. Try/catch/finally Or try/Finally block 
- Finally block can be use after try or after catch block.
- Finally block will always get executed either if you just return from try block or from catch block.\
- At most,we can add only 1 finally block.
- Mostly used for closing the object,adding logs etc.
- If JVM related issues like out of memory,system shut down or our process is forcefully killed. Then finally block do not get executed.

![img15.png](.idea/Images/img15.png)

![img16.png](.idea/Images/img16.png)


3. Throw:
- It is used to throw a new exception or 
- To re-throw the exception.

![img17.png](.idea/Images/img17.png)


Creating custom/user-defined Exception class

![img19.png](.idea/Images/img19.png)

![img18.png](.idea/Images/img18.png)


## Why we need to handle the Exception :
- It makes our code clean by separating the error handling code from regular code.
- It allows program to recover from the error.
- It allows us to add more information,which support debugging.
- Improves security,by hiding the sensitive information.

![img20.png](.idea/Images/img20.png)

![img21.png](.idea/Images/img21.png)

![img22.png](.idea/Images/img22.png)

![img23.png](.idea/Images/img23.png)


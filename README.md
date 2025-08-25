#  Java Reflection 

1. What is reflection?

This is used to examine the Classes,Methods,Fields,i=Interfaces at runtime and also possible to change the behaviour of the class too.

For Example :
- What all methods present in the class.
- What all fields present in the class.
- What is the return type of the methods.
- What is the modifier of the class.
- What all interfaces class has implemented.
- Change the value of the public and private fields of the Class etc........


2. How to do Reflection of Classes?

To reflect the class,we first need to get an Object Class.
(So,lets first understand, class then we will comeback to how to refelect the class.)

### What is this class Class?
- Instance of the class Class represents classes during runtime.
- JVM creates one Class Object for each and every class which is loaded during run time.
- This Class object,has meta data information about the particular class like its method,fields,cnostrutor etc.

### How to get perticular class Class object?
There are 3 ways :
1. Using forName()method

    ![img1.png](.idea/Images/img1.png)

2. Using .class 

![img2.png](.idea/Images/img2.png)

3. Usimg getclass() method 

![img3.png](.idea/Images/img3.png)

![img4.png](.idea/Images/img4.png)


Refelction of methods :

![img5.png](.idea/Images/img5.png)

Invoking Methods using reflection

![img6.png](.idea/Images/img6.png)

Reflection of Fields:

![img7.png](.idea/Images/img7.png)
![img8.png](.idea/Images/img8.png)
![img9.png](.idea/Images/img9.png)

Setting the value of Public field :

![img10.png](.idea/Images/img10.png)

Setting the value of private Field:(Incorrect way)

![img11.png](.idea/Images/img11.png)

Setting the value of private Field:

![img12.png](.idea/Images/img12.png)

Refelction of Comnstructor 

![img13.png](.idea/Images/img13.png)



# Java Annotation 

## What is Annotation?
- IT is kind of adding *META DATA* to tyhe java code.
- Means,its usage is *OPTIONAL*.
- We can use this Meta data information at *runtime* and can add certain logic in iur code if wanted.
- How to Read Meta data information?Using Reflection as discussed in previous video.
- Annotations can be applied at anywhere like Classes,Methods,Interface,fields,parameters etc.

![img14.png](.idea/Images/img14.png)

## Types of Annotation :

![img15.png](.idea/Images/img15.png)

### Annotations used on java code 

@Deprecated

- Usage of Deprecated Class or Method or Fields,shows you compile time *WARNING*
- Deprecation means,no further improvment is happening on this and use new alternative method or field instead.
- Can be used over:Constructoe,field,LocalVaruiable,Method,Package,Parameter,Type (class,interface,enum)

![img16.png](.idea/Images/img16.png)


@Override 
- During Complie time,it will check that the method should be Overridden.
- And throws complie time error,if it do not match with th parent method.
- Can be used over:*Methods.*

![img17.png](.idea/Images/img17.png)

@SupressWarnings
- It will tell compiler to **IGNORE** any compile time **WARNING**
- Use it safely,could led to **Run time exception** if,any valid warning is IGNORED
- Can be used over:**Field,Method,Parameter,Constructor,Local Variable,type**(Class or interface or enum)

![img18.png](.idea/Images/img18.png)
![img19.png](.idea/Images/img19.png)
![img20.png](.idea/Images/img20.png)

@Functional Interface
- Restrict Onterface to have only 1 abstract method
- Throwa Compilation error,if more than 1 abstract method found
- Can be used over:**Type**(Class or interface or enum)

![img21.png](.idea/Images/img21.png)

@SafeVarargs:
- Used to suppress "Heap pollution warning"
- Used over methods anf Constructor which has Variable Arguments as Parameter.
- Method should be either static or final(i.e methods which can not be overridden)
- In **Java9**,we can also use it on private methods too.



#### What is Heap Pollution?

Object of One Type(Example String),storing the reference of another type Object(Example Interger)

![img22.png](.idea/Images/img22.png)
![img23.png](.idea/Images/img23.png)


### Annotations used over Another Annotation (Meta-Annitations):

*@Target:*
- This meta-annotation will restrict,where to use the annotation.Either at method or Constuctor or Fields etc...

![img24.png](.idea/Images/img24.png)

Element Type:
- TYPE
- FIELD
- METHOD
- PARAMETER
- CONSTRUCTOR
- LOCAL VARIABLES
- ANNOTATION_TYPE
- PACKAGE
- TYPE_PARAMETER(allow you to apply on generic type)
- TYPE_USE(java 8 feature,allow you to use annotation at all places where type you can declare(like List<@annotation String>))


@Retention 
- This meta-annotation tells,how Annotation will be stored in java.
  - **RetentionPolicy.**SOURCE:** Annotation will be discarded by the compiler itself and will not be recoreded in .class file
  - RetentionPolicy.**CLASS:** Annotations will be recorded in .class file but will be ignore by JVM at run time
  - RetentionPolicy.**RUNTIME**:Annotation will be recorded in .class file = + availabe during run time.Usage of reflection can be done.

Example1:

![img25.png](.idea/Images/img25.png)

Example2:

![img26.png](.idea/Images/img26.png)

Example3:

![img27.png](.idea/Images/img27.png)

Example4:

![img28.png](.idea/Images/img28.png)


@Documented:
- By default,Annotations are ignored when Java Documentation is generated.
- With this meta =-annotation even Annotations will come in Java Docs.


            Not Documentated:

![img29.png](.idea/Images/img29.png)

@inherited:
- By default,Annotations applied on parent class are not availbe to child classes.
- But it is after this meta-annotation.
- This Meta-annotation has no effect,if annotation is used other than a class.

![img30.png](.idea/Images/img30.png)
![img31.png](.idea/Images/img31.png)


@Repeatable:
- Allows us to use the same annotation more than 1 at dame place.

**We can not do this before JAVA8**

![img32.png](.idea/Images/img32.png)
![img33.png](.idea/Images/img33.png)
![img34.png](.idea/Images/img34.png)

Creating an Annotation with method (its more like a field):
- No paraeter,no body
- Return type is restriced to primitive,Class,Strings,enums,annotations and array of these types.

![img35.png](.idea/Images/img35.png)
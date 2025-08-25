# Collection And Framework 

### What is an Array and its Limitation in Java?
An array is a collection of elements that are started in contiguous memory locations.

### Limitations of Array:
1. The size of an array is fixed, which means once array size is decided it can’t be increased or decreased. Whit this sometimes memory may be wasted or sometimes memory may not be sufficient. 
2. There are no predefined functions to perform operations like insertion, deletion, searching, sorting, etc. So that as a programmer we have to write our own logic. 
3. Array stores only a group of similar elements because of the problems in an array, Java comes up with a Collection Framework.


## Definition and need of Java Collections Framework:
A collection is a java object that is used to group homogeneous and heterogeneous and duplicate and unique objects without size limitation for carrying multiple objects at a time from one application to another application among multiple layers of MVC architecture as method arguments and return type.

## What are Collections?
Collections: It is a mechanism of collecting some group of objects either statically or dynamically. Collections can hold a group of objects. The size of the collection is not fixed, it means when we are inserting and deleting the elements than the size of the collection dynamically increased or decreased. Every collection internally follows data structures and contains predefined functions it means we don.t need to write new logic for performing the operations like Insertion, Deletion, Searching, Sorting, etc.

## What is a Framework?
The framework is a semi-finished reusable application that provides some common low-level services for serving reoccurring problems and that can be customized according to our requirements. For example:

1. The computer is a framework; it can be used by all people according to their requirements. 
2. Switchboard is a framework it can be used by all people according to their requirement. 
3. In java struts, hibernate, spring technologies are frameworks, all these technologies are used by different companies for developing projects according to the project requirements.
From Java Point of View, Framework means a collection/set of well-defined classes and interfaces that provides ready-made services support to our application. In order to implement a new feature or a class, there is no need to define a framework. However, an optimal object-oriented design always includes a framework with a collection of classes such that all the classes perform the same kind of task.

### Collection Object
An object is said to be a collection object if it holds or stores a group of other objects. The collection never stores any primitive values, but if we want to store primitive values we have to represent primitive values as objects.

### Collection Class
Collection class is a class whose object can store a group of other objects. Example: ArrayList, HashSet, HashMap, etc. All the collection classes are available in the “java.util” (utility) package. All the collection interfaces and collection classes together form a Collection Framework.

Java.util package contains several classes that collect homogeneous and heterogeneous objects without size limitation. These classes are usually called collection framework classes. All the collection classes are classified into the following four categories:

1. List: It is used to store a group of individual elements where the elements can be duplicated. 
2. Set: It is used to store a group of individual elements but the elements can’t be duplicated. 
3. Queue: It is used to hold multiple elements prior to processing and is dedicated to storing all the elements where the order of the elements matter. 
4. Map: It is used to store the element in the form of key-value pairs where the keys can’t be duplicated but values can be duplicated.


### Why these package classes are called Collection Framework?
This package class provides low-level services with well-defined data structures to solve collecting a heterogeneous dynamic number of objects as a single entity. Due to this reason java.util package classes are collectively called the collection framework.

All collection classes are implementing from java.io.Serializable so the collection object along with all its internal objects can be stored in a local file system or can be sent across the network to the remote computer. Here the rule is objects stored in the collection are also should be Serializable types to store collections in the file.

#### Collection stores a group of objects as follows:

![img.png](.idea/Images/img.png)

Here objects o1, o2, o3, and o4 are stored two times thereby we are wasting the memory within the JVM. To save the memory within the JVM when the objects are stored in the collection object, the JVM stores the references of the objects within the collection objects instead of storing the copy of objects directly.

![img1.png](.idea/Images/img1.png)

## Advantages of Java Collection Framework:
- It is used as a temporary data storage (avoid hitting the database for getting the same amount of data. 
- It reduces the complexity of the application (i.e. array code is reduced). That means Reduces programming effort by providing useful data structures and algorithms so we don’t have to write them by our self. 
- Increases performance by providing the high-performance implementation of useful data structures and algorithms because the various implementation of each interface are interchangeable, programs can be easily tuned by switching implementations. 
- We do not have to write code to implement these data structures and algorithms manually.
- Our code will be much more efficient as the collections framework is highly optimized.


### Collection Interfaces
The Collection interface is the root interface of the collections framework hierarchy. Java does not provide direct implementations of the Collection interface but provides implementations of its sub-interfaces like List, Set, and Queue.

## Collection Interface Hierarchy in Java
Collection Interface has the following three sub-interfaces:

1. List Interface 
2. Set Interface 
3. Queue Interface

![img2.png](.idea/Images/img2.png)

## Methods of Collection Interface in Java :

![img3.png](.idea/Images/img3.png)

## Collection vs Collections

Collection : It is part of Java Collection Framework.And its an interface,which expose various methods which is implemented by various collection class like ArrayList,Stack,LinkedList etc.

Collections : It is a Utikity class and provide static methoda,which are used to operate on collections like swapping,searching,reverse,copy etc.

![img4.png](.idea/Images/img4.png)


## Queue :
Java Queue interface orders the element in FIFO(First In First Out) manner. In FIFO, the first element is removed first and the last element is removed at last. This interface is dedicated to storing all the elements where the order of the elements matter.

The Queue interface of the Java collections framework provides the functionality of the queue data structure. It extends the Collection interface. Since the Queue is an interface, we cannot provide the direct implementation of it.

### Classes that implement Queue Interface in Java:
In order to use the functionalities of Queue, we need to use classes that implement it:

1. Priority Queue 
2. Dequeue

## Methods of Queue Interface
- add(): Inserts the specified element into the queue. If the task is successful, add() returns true, if not it throws an exception.
- offer(): Inserts the specified element into the queue. If the task is successful, offer() returns true, if not it returns false.
- element(): Returns the head of the queue. Throws an exception if the queue is empty. 
- peek(): Returns the head of the queue. Returns null if the queue is empty. 
- remove(): Returns and removes the head of the queue. Throws an exception if the queue is empty. 
- poll(): Returns and removes the head of the queue. Returns null if the queue is empty.

### Priority Queue Collection in Java:
It implements the Queue interface. The PriorityQueue class provides the functionality of the heap data structure. The PriorityQueue class provides the facility of using a queue. But it does not order the elements in a FIFO manner. It is based on Priority Heap.

The elements of the priority queue are ordered according to the natural ordering, or by a Comparator provided at queue construction time, depending on which constructor is used.

#### Creating Priority Queue
Syntax :

    PriorityQueue<Integer> numbers = new PriorityQueue<Integer>();
Here, we have created a priority queue without any arguments. In this case, the head of the priority queue is the smallest element of the queue. And elements are removed in ascending order from the queue.

Example:

            import java.util.*;
            class PriorityQueueDemo
            {
            public static void main (String args[])
            {
            PriorityQueue < String > queue = new PriorityQueue < String > ();
            queue.add ("Amit");
            queue.add ("Vijay");
            queue.add ("Karan");
            queue.add ("Jai");
            queue.add ("Rahul");
            System.out.println ("head:" + queue.element ());
            System.out.println ("head:" + queue.peek ());
            System.out.println ("Iterating the queue elements:");
            Iterator itr = queue.iterator ();
            while (itr.hasNext ())
            {
            System.out.println (itr.next ());
            }
            queue.remove ();
            queue.poll ();
            System.out.println ("After removing two elements:");
            Iterator < String > itr2 = queue.iterator ();
            while (itr2.hasNext ())
            {
            System.out.println (itr2.next ());
            }
            }
            }

### DeQueue Collection in Java
Deque is an acronym for “double-ended queue”. Java Deque Interface is a linear collection that supports element insertion and removal at both ends. The class which implements this interface is ArrayDeque. It extends the Queue interface. Deque is an interface and has two implementations: LinkedList and ArrayDeque.

#### Creating a Deque
Syntax :

        Deque dq = new LinkedList();
        Deque dq = new ArrayDeque();

### Methods of Deque
- addFirst(): Adds the specified element at the beginning of the deque. Throws an Exception if the deque is full. 
- addLast(): Adds the specified element at the end of the deque. Throws an exception if the deque is full. 
- offerFirst(): Adds the specified element at the beginning of the deque. Returns false if the deque is full. 
- offerLast(): Adds the specified element at the end of the deque. Returns false if the deque is full. 
- getFirst(): Returns the first element of the deque. Throws an exception if the deque is empty. 
- getLast(): Returns the last element of the deque. Throws an exception if the deque is empty. 
- peekFirst(): Returns the first element of the deque. Returns null if the deque is empty. 
- peekLast(): Returns the last element of the deque. Returns null if the deque is empty. 
- removeFirst(): Returns and removes the first element of the deque. Throws an exception if the deque is empty. 
- removeLast(): Returns and removes the last element of the deque. Throws an exception if the deque is empty. 
- pollFirst(): Returns and removes the first element of the deque. Returns null if the deque is empty. 
- pollLast(): Returns and removes the last element of the deque. Returns null if the deque is empty. 
- push(): Adds an element at the beginning of the deque. 
- pop(): Removes an element from the beginning of the deque. 
- peek(): Returns an element from the beginning of the deque.

## ArrayDeque Collection in Java:
The ArrayDeque class provides the facility of using deque and resizable-array. It inherits the AbstractCollection class and implements the Deque interface. This is a special kind of array that grows and allows users to add or remove an element from both sides of the queue. Array deques have no capacity restrictions and they grow as necessary to support usage. Array Implementation of Deque

Syntax : 

    Deque<String> animal1 = new ArrayDeque<String>();

Example :

    import java.util.Deque;
    import java.util.ArrayDeque;
    
    class ArrayDequeDemo {

    public static void main(String[] args) {
        // Creating Deque using the ArrayDeque class
        Deque<Integer> numbers = new ArrayDeque<>();

        // add elements to the Deque
        numbers.offer(1);
        numbers.offerLast(2);
        numbers.offerFirst(3);
        System.out.println("Deque: " + numbers);

        // Access elements of the Deque
        int firstElement = numbers.peekFirst();
        System.out.println("First Element: " + firstElement);

        int lastElement = numbers.peekLast();
        System.out.println("Last Element: " + lastElement);

        // Remove elements from the Deque
        int removedNumber1 = numbers.pollFirst();
        System.out.println("Removed First Element: " + removedNumber1);

        int removedNumber2 = numbers.pollLast();
        System.out.println("Removed Last Element: " + removedNumber2);

        System.out.println("Updated Deque: " + numbers);
    }
    }


## Difference between Comparable and comparator

![img5.png](.idea/Images/img5.png)

1. Primitive collection Sorting :

![img6.png](.idea/Images/img6.png)

2. Object collection Sorting :

![img7.png](.idea/Images/img7.png)

### DeQueue Collection in Java
Deque is an acronym for “double-ended queue”. Java Deque Interface is a linear collection that supports element insertion and removal at both ends. The class which implements this interface is ArrayDeque. It extends the Queue interface. Deque is an interface and has two implementations: LinkedList and ArrayDeque.

# Creating a Deque
Syntax :

    Deque dq = new LinkedList();
    Deque dq = new ArrayDeque();

### Methods of Deque
- addFirst(): Adds the specified element at the beginning of the deque. Throws an Exception if the deque is full. 
- addLast(): Adds the specified element at the end of the deque. Throws an exception if the deque is full. 
- offerFirst(): Adds the specified element at the beginning of the deque. Returns false if the deque is full. 
- offerLast(): Adds the specified element at the end of the deque. Returns false if the deque is full. 
- getFirst(): Returns the first element of the deque. Throws an exception if the deque is empty. 
- getLast(): Returns the last element of the deque. Throws an exception if the deque is empty. 
- peekFirst(): Returns the first element of the deque. Returns null if the deque is empty. 
- peekLast(): Returns the last element of the deque. Returns null if the deque is empty. 
- removeFirst(): Returns and removes the first element of the deque. Throws an exception if the deque is empty. 
- removeLast(): Returns and removes the last element of the deque. Throws an exception if the deque is empty. 
- pollFirst(): Returns and removes the first element of the deque. Returns null if the deque is empty. 
- pollLast(): Returns and removes the last element of the deque. Returns null if the deque is empty. 
- push(): Adds an element at the beginning of the deque. 
- pop(): Removes an element from the beginning of the deque. 
- peek(): Returns an element from the beginning of the deque.


## ArrayDeque Collection in Java:
The ArrayDeque class provides the facility of using deque and resizable-array. It inherits the AbstractCollection class and implements the Deque interface. This is a special kind of array that grows and allows users to add or remove an element from both sides of the queue. Array deques have no capacity restrictions and they grow as necessary to support usage. Array Implementation of Deque

Syntax : 

    Deque<String> animal1 = new ArrayDeque<String>();

        Example :
        
        import java.util.Deque;
        import java.util.ArrayDeque;
        
        class ArrayDequeDemo {

        public static void main(String[] args) {
            // Creating Deque using the ArrayDeque class
            Deque<Integer> numbers = new ArrayDeque<>();
    
            // add elements to the Deque
            numbers.offer(1);
            numbers.offerLast(2);
            numbers.offerFirst(3);
            System.out.println("Deque: " + numbers);
    
            // Access elements of the Deque
            int firstElement = numbers.peekFirst();
            System.out.println("First Element: " + firstElement);
    
            int lastElement = numbers.peekLast();
            System.out.println("Last Element: " + lastElement);
    
            // Remove elements from the Deque
            int removedNumber1 = numbers.pollFirst();
            System.out.println("Removed First Element: " + removedNumber1);
    
            int removedNumber2 = numbers.pollLast();
            System.out.println("Removed Last Element: " + removedNumber2);
    
            System.out.println("Updated Deque: " + numbers);
        }
        }
    
#### Difference between Priority Queue and ArrayDeque:

 ![img8.png](.idea/Images/img8.png)

## List :

In Java, the List interface is an ordered collection that allows us to store and access elements sequentially. It extends the Collection interface. In Java, we must import java.util.List package in order to use List. As a List is an interface, we cannot create objects from it.

#### New Methods define in the list interface :


#### Classes of List Interface
In order to use functionalities of the List interface, we can use these classes:

1. ArrayList 
2. LinkedList 
3. Vector 
4. Stack
These classes are defined in the Collections framework and implement the List interface.

##### ArrayList Collection in Java:
ArrayList is the implementation class of List Interface which is used to store a group of individual objects where duplicate values are allowed. ArrayList internally follows array structure, which means in ArrayList all the elements are stored in contiguous memory locations same as an array, but ArrayList size is not fixed.

ArrayList is not a synchronized class. If any object is synchronized we can access only one thread at a time but if an object is not. synchronized then we can access multiple threads.

#### Creating an ArrayList in Java

Syntax : 
        
    ArrayList<Type> al = new ArrayList<Type>();
Here, Type indicates the type of ArrayList.

ArrayList Constructors in Java

    ArrayList<E> al = new ArrayList<E>();
This constructor is used to create the new ArrayList with a default capacity of 10 and the size of ArrayList is 0.

    ArrayList<E> al = new ArrayList<E>(int capacity);
This constructor is used to create the new ArrayList with a default capacity of 10 and the size of ArrayList is 0.

    ArrayList<E> al = new ArrayList<E>(Collection obj);
This constructor is used to create the new ArrayList by copying the elements of any existing Collection (List, Set).

Points to Remember:
- size means the number of elements that are stored in Collection.
- capacity means the memory allocated for elements.
- < E > is called Generic Parameter type.                         
- E is the element type that must be a reference type but not any primitive type. 
- Methods of ArrayList: We can use all Collections Method to work with the ArrayList.

Example:
        
        import java.util.ArrayList;
        import java.util.List;
        public class ArrayListDemo
        {
        public static void main (String[]args)
        {
        // Creation of ArrayList
        ArrayList <Integer> al = new ArrayList <Integer>();

        //adding the elements into the list
        al.add (10);  //autoboxing
        al.add (new Integer (20)); //manual boxing
        al.add (30);
        al.add (40);
        al.add (50);
    
        //Display elements of the List and its Size
        System.out.println (al);
        System.out.println (al.size ());
    
        //inserting an element into the List at specified location
        al.add (1, 77);
        System.out.println (al);
        System.out.println (al.size ());
    
        //modifying the existing element of the List by specifying its value
        al.remove (new Integer (30));
        System.out.println (al);
        System.out.println (al.size ());
        
        //removing the element of the List by specifying its index position
        al.remove (0);
        System.out.println (al);
        System.out.println (al.size ());
    
        //Displaying elements of List 1 by 1 using for loop (accessing)
        for (int i = 0; i < al.size (); i++)
        {
         System.out.println (al.get (i));
        }
    
        //Displaying elements of List 1 by 1 using forEach Loop (auto-unboxing)
        for (int v:al)
        {
         System.out.println (v);
        }
    
        //Searching an element
        System.out.println (al.contains (50));
        
        //Copying the array list into another list
        ArrayList < Integer > al1 = new ArrayList < Integer > (al);
        System.out.println (al1);
    }
    }

### LinkedList Collection in Java with Examples:
LinkedList is the implementation class of List Interface which is also used to store a group of individual objects where duplicate values are allowed. LinkedList internally follows a doubly linked list structure where all the elements are stored in the form of nodes that linked each other.

The LinkedList in Java is not a synchronized class. LinkedList also supports multiple null values. This provides the functionality of LinkedList Data Structure. 

![img9.png](.idea/Images/img9.png)

Each element in a linked list is known as a node. It consists of 3 fields:

1. Prev – stores an address of the previous element in the list. It is null for the first element.
2. Next – Stores an address of the next element in the list. It is null for the last element.
3. Data – Stores the actual data

Note: Elements in linked lists are not stored in sequence. Instead, they are scattered and connected through links (Prev and Next).

### Creation of LinkedList
Syntax :
        
    LinkedList<Type> ll = new LinkedList<Type>();
Here, Type indicates the type of LinkedList.

LinkedList Constructors

    LinkedList<E> ll = new LinkedList<E>();
It is used to construct an Empty List.

    LinkedList<E> ll = new LinkedList<E>(Collection obj);
It is used to construct a list containing the elements of the specified collection, in the order, they are returned by the collection’s iterator.



Note:There is no capacity concept for LinkedList.

Methods of LinkedList: We can use all Collections Method to work with the LinkedList.

         import java.util.*;
        class LinkedListDemo
        {
        public static void main (String[]args)
        {
        LinkedList < String > animals = new LinkedList <> ();

        // Add elements to LinkedList
        animals.add ("Dog");
        animals.add ("Cat");
        animals.add ("Horse");
        System.out.println ("LinkedList: " + animals);
    
        // Get the element from the linked list
        String str = animals.get (1);
        System.out.print ("Element at index 1: " + str);
        System.out.println (" ");
    
        //Iterator method
        Iterator < String > itr = animals.iterator ();
        while (itr.hasNext ())
        {
         System.out.println (itr.next ());
        }
        }
        }


### Difference Between ArrayList and LinkedList in Java:

ArrayList is slower in insertion and deletion of elements because it internally requires shifting operations, but faster in accessing the elements because ArrayList uses index position for every element.

LinkedList is faster in insertion and deletion of elements because it just requires modifying the links of nodes instead of shifting operations, but slower in accessing the elements because LinkedList does not use any index position.

## Vector Collections in Java
Vector is an implemented class of List Interface. Vector class methods are by default synchronized. It is used to store a group of individual objects where duplicate values are allowed.

Vector is exactly similar to ArrayList but ArrayList is not a synchronized class where Vector is a synchronized class. Vector is also called legacy class because it is available from Java 1.0 Version. It is similar to the ArrayList, but with two differences-
1. The vector is synchronized. 
2. Java Vector contains many legacy methods that are not part of a collections framework.

Note: It is recommended to use ArrayList in place of Vector because vectors are not thread-safe and are less efficient.

Creation of Vector
Syntax : Vector<Type> vector = new Vector<Type>();
Here, Type indicates the type of Vector.

#### Vector Constructors

    Vector<E> v = new Vector<E>();
This constructor creates a single dimension array with a default capacity of 10.

    Vector<E> v = new Vector<E>(int capacity);
This constructor sets a given capacity as a current capacity to a single dimension array.

    Vector<E> v = new Vector<E>(Collection obj);    
This constructor is used for migrating one collection with another collection for transferring data.


### Methods of Vector
We can use all Collections Method to work with the LinkedList. We can also use legacy methods like addElement(), removeElement(), setElement(),….

        import java.util.*;
        class VectorDemo {
        public static void main(String[] args) {
        Vector<String> mammals= new Vector<>();

        // Using the add() method
        mammals.add("Dog");
        mammals.add("Horse");

        // Using index number
        mammals.add(2, "Cat");
        System.out.println("Vector: " + mammals);

        // Using addAll()
        Vector<String> animals = new Vector<>();
        animals.add("Crocodile");

        animals.addAll(mammals);
        System.out.println("New Vector: " + animals);
        
        // Using get()
        String element = animals.get(2);
        System.out.println("Element at index 2: " + element);

        // Using iterator()
        Iterator<String> iterate = animals.iterator();
        System.out.print("Vector: ");
        while(iterate.hasNext()) {
            System.out.print(iterate.next());
            System.out.print(", ");
        }
    }
    }

## Stack Collection in Java:
In Java, Stack is a class that falls under the Collection framework that extends the Vector class. The stack is a child class of Vector and implements List Interface. The stack stores a group of objects by using a mechanism called LIFO. LIFE stands for Last In First Out, which means the last inserted element deleted first.

The stack data structure has the two most important operations that are push and pop. The push operation inserts an element into the stack and the pop operation removes an element from the top of the stack.

![img10.png](.idea/Images/img10.png)

##### Creation of Stack
Syntax : 
    
    Stack<Type> stacks = new Stack<Type>();
Here, Type indicates the Stack’s type.

##### Stack Constructor
        public Stack()
The Stack class contains only the default constructor that creates an empty stack.

### Methods of Stack
We can use all Collection Methods. We can also use legacy methods of Vector Class like addElement(), removeElement(), setelementAt(), etc. But if we want to follow the LIFO mechanism we should use Stack methods like follows:

1. E push(E obj): This method will add new elements to the stack.
2. E pop(): This method deletes the top element available on Stack.
3. E peek(): This method just returns the top element available on Stack.

Example :

    import java.util.*;
    public class StackDemo {
    public static void main(String[] args) {
    Stack<Double> s = new Stack<Double>();
    s.push(10.2);
    s.push(50.2);
    s.push(30.2);
    s.push(40.2);
    s.push(70.2);
    System.out.println(s);
    System.out.println(s.pop());
    System.out.println(s);
    System.out.println(s.peek());
    System.out.println(s);
    }
    }

### Comparison Between ArrayList, LinkedList, Vector, and Stack in Java

![img11.png](.idea/Images/img11.png)


## Map Interface in java

A map is a data structure that supports the key-value pair mapping for the data. Each key and value pair is known as an entry. A Map contains unique keys. This interface doesn’t support duplicate keys because the same key cannot have multiple mappings.

A map is useful if there is data and we wish to perform operations on the basis of the key. The Map interface of the Java collections framework provides the functionality of the map data structure.

### Map Interface Hierarchy in Java

![img12.png](.idea/Images/img12.png)

### Methods of Map Interface
- V put(K obj, V obj): This method is used to add a new key-value pair to the Map. 
- V putAll(): Inserts all the entries from the specified map to this map. 
- V putIfAbsent(K obj, V obj): Inserts the association of the key K is not already associated with the value V. 
- V get(K obj): This method returns the Value object of the specified key. If the specified key is not available then it returns null. 
- V getOrDefault(K obj, defaultValue): Returns the value associated with the specified key K. If the key is not found, it returns the defaultValue. 
- V replace(K, V): Replace the value of the key K with the new specified value V. 
- V replace(K, oldValue, newValue): Replaces the value of the key K with the new value newValue only if the key K is associated with the value oldValue. -
- V remove(K): this method removes the specified key along with its value. 
- V remove(K, V): Removes the entry from the map that has key K associated with value V.
- int size(): this method returns the count of the number of Key-Value pairs available in the Map. 
- boolean isEmpty(): This method returns true if Map does not contain any Key-Value pairs otherwise it returns false. 
- void clear(): This method clears all the Key-value pairs of the map. 
- Set keyset(): This method returns all the keys available in the Map separately in the form of Set. 
- Set entrySet(): This method returns all the Key-Value or entities available in the Map separately in the form of a Set. 
- Collection values(): This method returns all the Key-Values or entities in the Map separately in the form of a Set. 
- boolean containsKey(): This method returns true if the specified Key is available in the Map otherwise it returns false. 
- boolean containsValue(V obj): This method returns true if specified Value is available in the Map otherwise it returns false.

### HashMap Collection in Java:

HashMap is the implementation class of the Map interface which is used to store a group of objects in the form of Key-Value pairs where Keys cannot be duplicated but Values can be duplicated. HashMap internally follows the hashtable data structure.

HashMap is not a synchronized class. HashMap supports only one null value for Key Objects but we can store multiple null values for Value Object. HashMap is called an unordered Map because it is not guaranteed for the insertion order of elements.


#### Creating a HashMap
Syntax : 

    HashMap<Key, Value> numbers = new HashMap<>(8, 0.6f); Here, Key – a unique identifier used to associate each element (value) in a map and Value – elements associated by keys in a map

#### HashMap Constructors

    HashMap<K,V> hm = new HashMap<K,V>(); 
It is used to construct a default HashMap.

    HashMap<K, V> hm = new HashMap<K, V>(int capacity); 
It is used to initialize the capacity of the hash map to the given integer value, capacity.

    HashMap<K, V> hm = new HashMap<K, V>(int capacity, float loadFactor); 
It is used to initialize both the capacity and load factor of the hash map by using its arguments.

    HashMap<K, V> hm = new HashMap<K, V>(Map obj); 
It is used to initialize the hash map by using the elements of the given Map object obj.

Example:

        import java.util.*;
        public class HashMapDemo
        {
        public static void main (String[]args)
        {
        HashMap < Integer, String > hm = new HashMap < Integer, String > ();
        hm.put (11, "Sachin");
        hm.put (37, "Dhoni");
        hm.put (25, "Kohli");
        hm.put (13, "Raina");
        hm.put (12, "Yuvraj");
        System.out.println (hm);
        System.out.println (hm.size ());
        Set ks = hm.keySet ();
        System.out.println (ks);
        Collection cv = hm.values ();
        System.out.println (cv);
        Set entry = hm.entrySet ();
        System.out.println (entry);
        System.out.println (hm.containsKey (12));
        System.out.println (hm.remove (25));
        System.out.println (hm);
        }
        }

### Hashtable Collection in Java:
Hashtable is synchronized. It ensures that no more than one thread can access the Hashtable at a given moment of time. The thread which works on Hashtable acquires a lock on it to make the other threads wait till its work gets completed. Hashtable doesn’t allow null keys and null values. Hashtable doesn’t guarantee any kind of order. It doesn’t maintain the mappings in any particular order.

Hashtable is the implementation class of the Map interface which is also used to store a group of objects in the form of Key-Value pairs where Keys can’t be duplicated but values can be duplicated. Hashtable is exactly similar to HashMap but Hashtable is a synchronized class where HashMap is not a synchronized class.

#### Creating a Hashtable
Syntax :

    Hashtable<Integer, String> ht = new Hashtable<Integer, String>();

#### Hashtable Constructors
- Hashtable(): It creates an empty hashtable having the initial default capacity and load factor. 
- Hashtable(int capacity): It accepts an integer parameter and creates a hash table that contains a specified initial capacity. 
- Hashtable(int capacity, float loadFactor): It is used to create a hash table having the specified initial capacity and loadFactor. 
- Hashtable(Map obj): It creates a new hash table with the same mappings as the given Map.

Example:

        import java.util.*;
        public class HashtableDemo
        {
        public static void main (String[]args)
        {
        Hashtable < Integer, String > ht = new Hashtable < Integer, String > ();
        ht.put (11, "Sachin");
        ht.put (37, "Dhoni");
        ht.put (25, "Kohli");
        ht.put (13, "Raina");
        ht.put (12, "Yuvraj");
        System.out.println (ht);
        Enumeration e = ht.keys ();
        while (e.hasMoreElements ())
        {
        System.out.println (e.nextElement ());
        }
        }
        }

### LinkedHashMap Collection in Java:
LinkedHashMap is the implementation class of the Map interface which is also used to store a group of three objects in the form of Key-Value pairs where Keys cannot be duplicated but values can be duplicated. LinkedHashMap internally follows hashtable + doubly linked list structures.

The LinkedHashMap is not a synchronized class. LinkedHashMap supports only one null value for Key Objects but we can store multiple null values for Value Objects. LinkedHashMap is called an ordered Map because it is guaranteed the insertion order of elements.

### Creating a LinkedHashMap
Syntax :

    LinkedHashMap<Integer, String> hm = new LinkedHashMap <Integer, String>();

### LinkedHashMap Constructors
- LinkedHashMap(): It is used to construct a default LinkedHashMap. 
- LinkedHashMap(int capacity): It is used to initialize a LinkedHashMap with the given capacity. 
- LinkedHashMap(int capacity, float loadFactor): It is used to initialize both the capacity and the load factor. 
- LinkedHashMap(int capacity, float loadFactor, boolean accessOrder): It is used to initialize both the capacity and the load factor with a specified ordering mode. 
- LinkedHashMap(Map obj): It is used to initialize the LinkedHashMap with the elements from the given Map class obj.


Example:

        import java.util.*;
        public class LinkedHashMapDemo {
        public static void main(String args[]) {
        // HashMap Declaration
        LinkedHashMap<Integer, String> lhmap = new LinkedHashMap<Integer, String>();

         //Adding elements to LinkedHashMap
         lhmap.put(22, "Abey");
         lhmap.put(33, "Dawn");
         lhmap.put(1, "Sherry");
         lhmap.put(2, "Karon");
         lhmap.put(100, "Jim");

         // Generating a Set of entries
         Set set = lhmap.entrySet();

         // Displaying elements of LinkedHashMap
         Iterator iterator = set.iterator();
         while(iterator.hasNext()) {
            Map.Entry me = (Map.Entry)iterator.next();
            System.out.print("Key is: "+ me.getKey() + "& Value is: "+me.getValue()+"\n");
         }
    }
    }


### TreeMap Collection in Java:
TreeMap is the implementation class of the Map interface which is also used to store a group of objects in the form of Key-Value pairs where Keys cannot be duplicated but values can be duplicated. TreeMap internally follows Tree Structure.

The TreeMap is not a synchronized class. TreeMap is called an unordered map because it is not guaranteed for the insertion order of elements, but all elements are stored in sorted order (by default ascending order based on keys). TreeMap does not support null values for Key Objects but we can store multiple null values for Value Objects.

#### Creating a TreeMap
Syntax :

    TreeMap<Key, Value> numbers = new TreeMap<Key, Value>(); Here, Key – a unique identifier used to associate each element (value) in a map and Value – elements associated by keys in a map

#### TreeMap Constructors
- TreeMap(): It is used to construct an empty treemap that will be sorted using the natural order of its key. 
- TreeMap(Comparator c): It is used to construct an empty tree-based map that will be sorted using comparator c. 
- TreeMap(Map m): It is used to initialize a treemap with the entries from m, which will be sorted using the natural order of the keys. 
- TreeMap(SortedMap sm): It is used to initialize a treemap with the entries from the SortedMap sm, which will be sorted in the same order as sm.

Example:

        import java.util.*;  
        class TreeMapDemo{  
        public static void main(String args[])
        {  
        TreeMap<Integer,String> map=new TreeMap<Integer,String>();    
        map.put(100,"Amit");    
        map.put(102,"Ravi");    
        map.put(101,"Vijay");    
        map.put(103,"Rahul");

        for(Map.Entry m:map.entrySet()){    
            System.out.println(m.getKey()+" "+m.getValue());    
        }    
       }  
    }

## Set in Collection :
The Set interface of the Java Collections framework provides the features of the mathematical set in Java. It extends the Collection interface. Unlike the List interface, sets cannot contain duplicate elements. Since Set is an interface, we cannot create objects from it.

### Classes of Set Interface
In order to use functionalities of the Set interface, we can use these classes:

1. HashSet 
2. LinkedHashSet 
3. TreeSet 
4. SortedSet
These classes are defined in the Collections framework and implement the Set interface.

### HashSet Collection in Java
The HashSet is the implementation class of the Set interface which is also used to store a group of individual objects but duplicate values are not allowed. HashSet internally follows a hashtable structure where all the elements are stored using a hashing technique which will improve the performance by reducing the waiting time.

The HashSet is not a synchronized class. HashSet supports only one null value. HashSet is called an unordered collection because it is not guaranteed for the insertion order of elements.

#### Creation of HashSet
Syntax :

    HashSet<Integer> numbers = new HashSet<>(8, 0.75);
Here, we have created a hash set named numbers.

Notice, the part new HashSet<>(8,0.75). Here, the first parameter is capacity, and the second parameter is the load factor.

1. capacity – The capacity of this hash set is 8. This means it can store 8 elements.
2. loadFactor – The load factor of this hash set is 0.6. This means, that whenever our hash set is filled by 60%, the elements are moved to a new hash table of double the size of the original hash table.


### Constructors of HashSet
    HashSet<E> hs = new HashSet<E>();
It is used to construct a default HashSet.

    HashSet<E> hs = new HashSet<E>(int capacity);
It is used to initialize the capacity of the hash set to the given integer value capacity.

    HashSet<E> hs = new HashSet<E>(int capacity, float loadFactor);
It is used to initialize the capacity of the hash set to the given integer value capacity and the specified load factor.

    HashSet<E> hs = new HashSet<E>(Collection obj);
It is used to initialize the hash set by using the elements of the collection obj.

#### Methods of HashSet Collection in Java:
1. boolean add(E obj): It adds the element e to the list. 
2. boolean remove(E obj): It removes the specified Object o from the Set. 
3. int size(): It gives the number of elements of a Set. 
4. void clear(): It removes all the elements from the list. 
5. boolean contains(E obj): It checks whether the specified Object o is present in the list or not. If the object has been found it returns true or else false. 
6. boolean isEmpty(): Returns true if there is no element present in the Set. 
7. Object clone(): This method returns a shallow copy of the HashSet.

Example:

        import java.util.*;
        public class HashSetDemo
        {
        public static void main (String[]args)
        {
        HashSet < Integer > hs = new HashSet < Integer > ();
        hs.add (17);
        hs.add (13);
        hs.add (27);
        hs.add (12);
        hs.add (45);
        System.out.println (hs);
        System.out.println (hs.size ());
        for (int e:hs)
        {
        System.out.println (e);
        }
        Iterator it = hs.iterator ();
        while (it.hasNext ())
        {
        System.out.println (it.next ());
        }
        }
        }

### LinkedHashSet Collection in Java:
LinkedHashSet is the implementation class of the Set interface which is also used to store a group of individual objects but duplicate values are not allowed. The LinkedHashSet internally follows hashtable + double linked list structures.

LinkedHashSet is not a synchronized class. LinkedHashSet supports only one null value. LinkedHashSet is called an ordered Collection because it is a guarantee for the insertion order of elements.
### Creation of LinkedHashSet

Syntax :

    LinkedHashSet<Integer> numbers = new LinkedHashSet<>(8, 0.75);
Notice, the part new LinkedHashSet<>(8,0.75). Here, the first parameter is capacity and the second parameter is loadFactor.

### LinkedHashSet Constructors
    LinkedHashSet<E> lhs = new LinkedHashSet<E>();
It is used to construct a default LinkedHashSet.

    LinkedHashSet<E> lhs = new LinkedHashSet<E>(int capacity);
It is used to initialize the capacity of the Linked hash set to the given integer value capacity.

    LinkedHashSet<E> lhs = new LinkedHashSet<E>(int capacity, float loadFactor);
It is used to initialize the capacity of the Linked hash set to the given integer value capacity and the specified load factor.

    LinkedHashSet<E> lhs = new LinkedHashSet<E>(Collection obj);
It is used to initialize the Linked hash set by using the elements of the collection obj.

Example:

        import java.util.*;
        class LinkedHashSetDemo
        {
        public static void main (String args[])
        {
        //Creating HashSet and adding elements  
        LinkedHashSet < String > set = new LinkedHashSet ();
        set.add ("One");
        set.add ("Two");
        set.add ("Three");
        set.add ("Four");
        set.add ("Five");
        Iterator < String > i = set.iterator ();
        while (i.hasNext ())
        {
        System.out.println (i.next ());
        }
        }
        }

### TreeSet Collection in Java:
TreeSet is the implementation class of the Set interface which is also used to store a group of individual objects but duplicate values are not allowed. The TreeSet internally follows the tree structure.

The TreeSet is not a synchronized class. TreeSet is called an unordered collection because it is not guaranteed for insertion order of elements but all elements are stored in sorted order (by default ascending order).

The TreeSet supports only one null value if TreeSet is empty otherwise TreeSet does not support null values because it internally performs comparison operations but we never compare a null value with any object and it will throw a RuntimeException saying NullPointerException.

The TreeSet does not allow us to store different types of objects because it internally performs comparison operations but we never compare two different types of objects and it will throw a runtime exception saying ClassCastException.

#### Creation of TreeSet
Syntax :

        TreeSet<Integer> numbers = new TreeSet<Integer>();
Here, we have created a TreeSet without any arguments. In this case, the elements in TreeSet are sorted naturally (ascending order).

#### TreeSet Constructors
    TreeSet<E> ts = new TreeSet<E>();
It is used to construct an empty tree set that will be sorted in ascending order according to the natural order of the tree set.

    TreeSet<E> ts = new TreeSet<E>(SortedSet);  
It is used to build a TreeSet that contains the elements of the given SortedSet.

    TreeSet<E> ts = new TreeSet<E>(Comparator);
It is used to construct an empty tree set that will be sorted according to the given comparator.

    TreeSet<E> ts = new TreeSet<E>(Collection obj);
It is used to build a new tree set that contains the elements of the collection obj.

### Methods of TreeSet
1. E ceiling(E e): It returns the equal or closest greatest element of the specified element from the set, or null there is no such element. 
2. E floor(E e): It returns the equal or closest least element of the specified element from the set, or null there is no such element. 
3. E higher(E e): It returns the closest greatest element of the specified element from the set, or null there is no such element. 
4. E lower (E e): It returns the closest least element of the specified element from the set, or null if there is no such element. 
5. E pollFirst(): It is used to retrieve and remove the lowest(first) element. 
   6. E pollLast(): It is used to retrieve and remove the highest(last) element.

           Example :
        
           import java.util.TreeSet;
           public class TreeSetDemo
           {
           public static void main (String args[])
           {
           // TreeSet of String Type
           TreeSet < String > tset = new TreeSet < String > ();

           // Adding elements to TreeSet<String>
           tset.add ("ABC");
           tset.add ("String");
           tset.add ("Test");
           tset.add ("Pen");
           tset.add ("Ink");
           tset.add ("Jack");

           //Displaying TreeSet
           System.out.println (tset);

           // TreeSet of Integer Type
           TreeSet < Integer > tset2 = new TreeSet < Integer > ();

           // Adding elements to TreeSet<Integer>
           tset2.add (88);
           tset2.add (7);
           tset2.add (101);
           tset2.add (0);
           tset2.add (3);
           tset2.add (222);
           System.out.println (tset2);
           }
           }   

### Comparison Between HashSet, LinkedHashSet, and TreeSet in Java

![img13.png](.idea/Images/img13.png)

#### SortedSet Collection in Java:
The SortedSet interface extends Set and declares the behavior of a set sorted in ascending order. Several methods throw a NoSuchElementException when no items are contained in the invoking set.

A ClassCastException is thrown when an object is incompatible with the elements in a set. A NullPointerException is thrown if an attempt is made to use a null object and null is not allowed in the set.

#### SortedSet Methods in Java
1. Object first(): Returns the first element in the invoking sorted set. 
2. SortedSet headSet(Object end): Returns a SortedSet containing those elements less than the end that are contained in the invoking sorted set. Elements in the returned sorted set are also referenced by the invoking sorted set. 
3. Object last(): Returns the last element in the invoking sorted set. 
4. SortedSet subSet(Object start, Object end): Returns a SortedSet that includes those elements between start and end.1. Elements in the returned collection are also referenced by the invoking object. 
5. SortedSet tailSet(Object start): Returns a SortedSet that contains those elements greater than or equal to start that are contained in the sorted set. Elements in the returned set are also referenced by the invoking object.

Example:

        import java.util.*;
        class SortedSetDemo
        {
        public static void main (String args[])
        {
        TreeSet < String > set = new TreeSet < String > ();
        set.add ("A");
        set.add ("B");
        set.add ("C");
        set.add ("D");
        set.add ("E");

        System.out.println ("Intial Set: " + set);
        System.out.println ("Head Set: " + set.headSet ("C"));
        System.out.println ("SubSet: " + set.subSet ("A", "E"));
        System.out.println ("TailSet: " + set.tailSet ("C"));
    }
    }


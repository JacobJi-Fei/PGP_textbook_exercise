**Chapter 1**
1. As a general rule, a byte is comprised of ____ bits?
> 8  

2. Four key principles of object-oriented programming?
> Abstract, Encapsulation, Polymorphism, and Inheritance.  

3. Where do Java programs begin execution?
> Java programs begin excution at main().

4. What is variable?
> A variable is a named memory location. The contents of a variable can be changed during the excution of a program.  

5. How do you create a single-line comment? and multiline comment?
> single-line bengins with // and ends at the end of this line.  
> multiline begins with /* and ends with */.  

6. How do you create a block of code?
> A block of code is started with a { and ended with a }.  

7. If you make a typing mistake when entering your program, what sort of error will result?
> A syntax error.

8. Does it matter where on a line you put a statement?
> No, Java is a free-form language.  

**Chapter 2 and 3**
1. Why does Java strictly specify the range and behavior of its primitive types?
> Java strictly specifies the range and behavior of its primitive types to *ensure portability across platforms*.  

2. What is Java's character type, and how does it differ from the character tyoe used by some other programming languages?
> Java's character type is **char**. Java character are Unicode rather than ASCII, which is used by some other computer language.

3. A boolean value can have any value you like because any non-zero value is true. True or False?
> False. A boolean value must be either **true** or **false**.  

4. In an expression, what type are byte and short promoted to ?
> In an expression, byte and short are promoted to **int**.  

5. In general, when is a cast needed?
> a cast is needed when a narrowing conversion is occuring.  

6. Does the use of redundant parentheses affect program performance?
> No.  

7. Does a block define a scope?
> Yes.  

8. What is an infinite loop?
> An infinite loop is a loop that runs indefinitely.

9. When using break with a label, must the label be on a statement or block that contains the break?
> Yes.  

**Chapter 4**
1. What is the difference between a class and an object?
> A class is a logical abstraction that describes the form and behavior of an object. An object is a physical instance of the class.

2. How is a class defined?  
> A class is defined by using the keyword **class**. Inside the **class** statement, you specify the code and data that comprise the class.

3. What does each object have its own copy of?
> Each object of a class has its own copy of the class's instance variables.

4. Using two separate statements, Declare a variable called **counter** of a class called **MyCounyter** and assign it a new object of that class.
```
MyCounter counter;
counter = new MyCounter ();
```  

5. Show how a method called **myMeth()** is declared if it has a return type of **double** and has two int parameters called a and b.
```
double myMeth(int a, int b) { // ...
```

6. How must a method return if it returns a value?
> A method that returns a value must return via the **return** statement, passing back the return value in the process.  

7. What name does a constructor have?
> A constuctor has the same name as its class. 

8. What does **new** do?
> The **new** operator allocates memory for an object and initializes it using the object's consturctor.

9. What is garbage collection and how does it work? What is finalize()?
> Garbage collection is the mechanaism that recycles unused objects so that their memory can be reused. An objects's finalize() method is called just prior to an object being recycled. It is not used by most Java programs.  

10. What is **this**?
> The **this** keyword is a reference to the object on which a method is invoked. It is automatically passed to a method.

11. Can a constructor have one or more parameters?
> Yes.

12. If a method reuturns no value, what must its return type be?
> void.

**Chapter 5**
1. Show two ways to decalre a one-dimensional array of 12 doubles.
```
double x[] = new double [12];
double[] x = new double [12];
```

2. Show how to initialize a one-dimensional array of integers to the values 1 through 5.
```
int [] x = {1, 2, 3, 4, 5 };
```  

3. What is the difference between the String methods **indexOf()** and **lastIndexOf()**?
> The **indexOf()** method finds the first occurrence of the specified substring. **lastIndexOf()** finds the last occurrence.

**Chapter 6**
1. If all objects of a class need to share the same variable, how must you declare that variable?
> Shared variables are declared as static.  

2. Why might you need to use a static block?
> A static block is used to perform any initializations related to the class, before any objects are created.

3. What is an inner class?
> An inner class is a nonstatic nested class.

4. To make a member accessibly by only other members of its class, what access modifier must be used?
> pricate.

5. The name of a method plus its parameter list consitutes the method's ________.
> signature

6. An **int** argument is passed to a method by using call-by-____.
> value

7. Can a varargs method be overloaded?
> Yes

**Chapter 7**
1. Does a superclass have access to the members of a subclass? Does a subclass have access to the members of a superclss?
> No, a suoerclass have no knowledge of its subclasses.  Yes, a subclass has access to all nonprivate members of its superclass.

2. How do you prevent a subclass from having access to a menmber of a superclass?
>  To prevent a subclass from having acccess to a superclass member, declare that member as private.

3. A superclass reference can refer to a subclass object. Explain why this is important as it is related to method overriding.
> When an overridden method is called through a superclass reference, it is the type of the object being referred to that determines which version of the method is called.

4. Describe the purpose and use of both versions of super.
> The **super** keyword has two forms. The first is used to call a superclass constructor. The general form of this usage is
> ```
> super(param-list);
> ```
> The second form of super is used to access a superclass member. It has this general forms:
> ```
> super.member;
> ```

5. What is an abstract class?
> A class with at least one abstract method is abstract.

6. How do you prevent a method from being overridden? How do you prevent a class from being inherited?
> To prevent a method from being overriden, declare it as final. To prevent a class from being inherited, declare it as final.

7. Explain how inheritance, method overriding, and abstract classes are used to support polymorphism.
> Inheritance, method overriding, and abstract classes support polymorphism by enabling you to create a generalized class structure that can be extended by a variety of classes. Thus, the abstract class defines a consistent interface that is shared by all implementing classes. This embodies the concept of "one interface, multiple methods."

8. What class is a superclass of every other class?
> The Object class.

9. A class that contains at least one abstract method must itself be declared abstract. True or False?
> True.

10. What keyword is used to create a named constant?
> final

**Chapter 8**

1. "One interface, multiple methods" is a key tenet of Java. What feature best exemplifies it?
> The interface best exemplifies the one interface, multiple methods principle in OOP.

2. How many classes can implement an interface?
> An interface can be implemented by an unlimited number of classes.

3. How many interfaces can a class implement?
> A class can implement as many interfaces as it chooses.

4. A class declares that it implements an interface by use of a/an ____.
> **implements** clause

5. Can interface be extended?  
> Yes, interfaces can be extened by other interfaces.

6. Create an interface for Vehicle class from Chapter 7. Call the interface IVehicle.
```
interface IVehicle {

    // Return the range.
    int range();
    // Computer fuel needed for a given distance.
    double fuelNeeded(int miles);

    // Accessor methods.
    int getPassengers();
    void setPassengers(int P);
    int getFuelCap();
    void setFuelCap (int f);
    int getMpg();
    void setMpg(int m);
}
```

7. Variables declared in an interface are implicitly **static** and **final**. What good are they?
> Interface varaibles create named constants that can be shared by all classes in a program.
They can be brought into view by implementing their interface.

8. Can one interface be a member of another?
> Yes.

9. Given two interfaces called Alpha and Beta, show how a class called MyClass specifies that it implements each.
```
class MyClass implements Alpha, Beta{...}
```

**Chapter 9**

1. What is a namespace? Why is it important that Java allows you to partition the namespace?
>A namespace is a declarative region. By partitioning the namespace, you can prevent name collisions.

2. Pachages are stored in _______.
> directories.

3. Explain the difference between **protected** and **default** access 
> A member with protected access can be used within its package and by a subclass in any package.  
A member with default access can be used only within its package.

4. Explain the two ways that the members of a pachage can be accessed by other packages.
>To use a member of a package, either you can fully qualify its name, or you can import it using **import**.

5. A package is, in essence, a container for classes. True or False?
> True.

6. What standard Java package is automatically imported into a program?
> java.lang

7. In your own words, what does static import do ?
> Static import brings into the global namespace the static members of a class or interface. This means that static members can be used without having to be qualified by their class or interface name.

8. What does this statement do?
```
import static somepack.SomeClass.myMethod;
```
> The statement brings into the global namespace SomeClass.myMethod(), which is part of the **somepack** package.

9. Is static import designed for special-case situations, or is it good practice to bring all static members of all classes into view?
> Static import is designed for special cases. Bringing many static memebers into view will lead to namespace collisions and destructure your code.

**Chapter 10**
1. What class is at the top of the exception hierarchy?
> **Throwable** is at the top of the exception hierarchy.

2. Briefly explain how to use **try** and **catch**.
> The try and catch work together. Program statements that you want to monitor for exceptions are contained within a try block. An excetion is caught using catch.

3. What is wrong with this fragment?
```
...
vals[18] = 10;
catch ( ArrayIndexOutOfBoundsException exc) {
    // handle error
}
```

> There is no try block preceding the catch.

4. What happens if an exception is not caught?
> If an exception is not caught, abnormal program termination results.

5. What is wrong with this fragment?
``` 
class A rxtends Exception{ ...

class B extends A { ...

// ...

try {
    // ...
}
catch (A exc) {...}
catch (B exc) {...}
```
> In the fragment, a superclass catch precedes a suclass catch. Since the superclass catch will catch all subclasses too, unreachable code is created.

6. Can an inner catch rethrow an exception to an outer catch?
> Yes, an exception can be rethrown.

7. When should you use the try-catch block in the code?
> You should use it to deal with unexpected error conditions. Do not use it to deal with simple, expected situations.

8. The **finally** block is the last bit of code excuted before your program ends. True or False? Explain your answer.
> False. The finally block is the code executed when a try block ends.

9. What type of exceptions must be explicitly declared in a throws clause of a method?
> All exceptions except those of type **RuntimeException** and **Error** must be declared in a **throws** clause.

10. What is wrong with this fragment?
```
class MyClass{ // ...}
// ...
throw new MyClass();
```
> Myclass doesn't extend Throwable. Only subclasses of Throwable can be thrown by throw.

11. What are the three ways that an exception can be generated?
> An exception can be generated by an error in the JVM, by an error in your program, or explicitly by a throw statement.

12. What are the two direct subclasses of Throwable?
> Error and Exception

13. What is the multi-catch feature?
> The multi-catch feature allows one catch clause to catch two or more exceptions.

14. Should your code typically catch exceptions of type Error?
> No. 


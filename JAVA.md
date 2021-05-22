# JAVA

## PGP 5

### Constructors vs methods

- Constructors initialise objects when they are created.
Methods perform operations on objects that already exist.
构造函数在他们被创建时就实例化他们的对象
方法 表现已经存在的对象
- Constructors are called implicitly when the new keyword creates an object.
Methods can be called directly on an existing object
- Constructors must be named with the same name as the class name
Method must be called something different to the class name
构造函数要和类的名字一样， 方法必须不一样
- Constructors can't return anything
Methods must be configured return something, although it can be void.
- Method overloading / Constructor overloading

### Static summary

- Variables, Methods and inner Classes
- Used to reduce JVM memory usage
- Make code safer ( variables change in a specified way)
- If a variable is declared static then changing it in any object changes it for all objects ( save a lot of memory in some situation)
- Static methods are methods which don't require an object of its class to be created before it can be called. 用静态方法不用提前构建对象
- Static methods can't use the this keyword as there is no instance for this to refer to.

### OOP

- Inheritance, Encapsulation, Abstraction and Polymorphism
- Why use?

	- Allow multiple developers to work on the same project more efficiently
	- Modularm, Extensible, Reusable, scaleabel, maintainable

- Why not?

	- Creating efficient Classes can be hard
	- Unforeseen interactions(emergent behaviour)
	- Performance issues and requires more code

### Inheritance

- Allow for hierarchical program structures
- Means we can make a general class with common traits
- New classes can inherit these traits but also add class specific traits
- Class that is inherited is superclass
- Class that inherits is the subclass
- Subclass inherits all the variables and methods of the superclass 
- Changes in superclass effect subclasses
- Subclasses code can change the 'intention' of the superclass code
- Each class can have at most one superclass
- A subclass cannot access the private members of its superclass( 可换成protected)
- A subclass constructor can call a superclass constructor by use of super(), before doing anythings else.
- If you do not call a superclass constructor, the no-argument constructor is automatically called

### Overriding

- 重写
- If a class inherits a method from its superclass, it has an option to override it (it is not marked final)
- If methods are rewritten with the same name they replace the original method at compile time
- Also needs the same argument list and return type.
- A method declared final or static cannot be overridden
- Constructors cannot be overridden

## PGP 6

### Inner class

- Write a class within a class
- We can make it private
- Methods in the outer class can instantiate the inner class
- These outer class methods can be called from the main method in a different class

### Inner Class2

- Static Inner Class

	-  不能使用外部类的实例变量和方法

- Inner class(Private or public)

	- Private

		- The inner class can access the private variables of the outer class.

	- public

- Method local inner class (Neither private or public)

	- A class that only exists inside a method  只能在该方法内使用
	- 不能使用访问控制符

- Anonymous inner class

	- The inner class with no name
	- Declared and instantiated at same time

### Abstract

- The process of hiding the implementation details and only showing what the object does to the user
- Abstract classes

	- 抽象类不能被实例化
	- public abstract class XYZ {...}
	- ! can be subclass
	- These extending classes are called   concrete classes
	- ! So, an abstract class has no use until it is extended by some other class

- Abstract method

	- A method with no implementation
	- Only abstract classes can contain abstract methods
	- !!! 抽象类的子类 必须包含该抽象类的所有抽象method

- Subclass of Abstract class

	- 如果抽象类的子类不能包含该抽象类的所有方法， 它必须是抽象类

## Week 6

### Abstract or Interface

- Abstract class

	- Contains abstract and Non-Abstract Methods
	- • Members can have access control (private etc)
	- • Abstract class can extend another class and implement interfaces 
	- . Final/non-final, static/non-static variables

- Interface class

	- Can have only abstract methods (Static and Default Methods added in java 8)
	- • Members are always public
	- • Interface can extend only another Java interface
	-  • Only static and final variables

### Interface

- A class implements an interface, thereby inheriting the abstract methods of the interface
- Interface is a reference type in Java. It is similar to class. It is a collection of abstract methods. A class implements an interface, thereby inheriting the abstract methods of the interface.

### Interface vs abstract

- In an interface, If you include data it must be constant*;
an abstract class can have all types of data.
- If a class extends an interface, this interface plays the same role as a superclass.

### Design a class

-  Follow standard Java programming style and naming conventions.
- • Choose informative names for classes, data fields, and methods.
- • Always place the data declaration before the constructor, and place constructors before methods.
- • Although java provides a default constructor you should always* provide a constructor and initialize variables to avoid programming errors.

### Using Visibility Modifiers

- Each class can present two contracts – one for the users of the class and one for the extenders of the class
- • Eg. make the fields private and accessor methods public if they are intended for the users of the class.
- • Eg. make the fields or method protected if they are intended for extenders of the class. (re: packages, later)
- • The contract for the extenders encompasses the contract for the users.
- • The extended class may increase the visibility of an instance method from protected to public, or refine its implementation.
- A class should use the private modifier to hide its data from direct access by clients.
- • You can use get methods and set methods to provide users with access to the private data, but only to private data you want the user to see or to modify.
- • A class should also hide methods not intended for client use.
- • get() and set() not explicitly covered in the text book

### SOLID 

- Single Responsibility Principle
- Open Closed Principle

	- 一个类允许extension 继承， 但不允许modification

- Liskov's substitution principle

	- 一个子类对每一个子类对象都行得通
	- 一个类可以被她的任意一个子类替代

- Interface Segregation Principle 接口隔离原则

	- 使用者不应该被强制implement 他们不需要的 methods
	- 尽可能让接口越小越好

- Dependency Inversion Principle

	- 抽象类不应该决定于细节，设计的时候不需要考虑细节。类可以改变但要遵循父类界限

### Generics

- The key benefit of generics

	- enable errors to be detected at compile time rather than at run time

- If you attempt to use the class or method with an incompatible object, a compile error occurs.
- What is generics

	-  Generics is the capability to parameterize types.

- Change location of bugs from runtime to compile time
-  Remove/reduce need for casting, which we will demonstrate

### Packages

- A package is a group of related classes and interfaces.
- • Packages organise your or your teams code
- • Packages control access to the code.
- • Classes defined within a package must be accessed through their package name.
- • When no package is specified, the global (default) no-name package is used
- Importing package

	- To subsequently use MyClass, you can use the fully qualified name:
 pkg1.pkg2.MyClass v = new pkg1.pkg2.MyClass();
	- Or use the import statement with general form: import pkg.MyClass;
	-     import pkg.*; 

- Static import

	- static import allow you import static members of a class
	- import static Math.sqrt;
	-     import static Math.*;

### Polymorphism

- Polymorphism is the ability of an object to take on many forms
- Method overloading(Compile time polymorphism)
-  Subclass Polymorphism(Runtime polymorphism)
- Generics in Java(Parametric polymorphism)

### java.time package

- Year

	- returns the current year (eg 2019)

- LocalDate

	- Current date (eg 2019-05-03)

- LocalTime

	- Current time (11:13:30)

- ZoneId

	- gives time-zone ID

- java.time.format package for more formatting options

	- DateTimeFormatter

## Week 7 

### Exception Handling 

- Use If statement

	-  Usually you cant just output and stop, there will be dependencies 
	- • Doesn’t scale to embedded methods
 Doesn’t scale to large programs

- Use Class to protect

	- Scales better
	- • Still doesn't allow for continuation of program
	- • You have to know exactly what you are checking for

- Use exception handling (Try, Catch)

	- Advantages

		- Enable a method to throw an exception to its caller
		- Without this capability, a method or statement must handle the exception or terminate the program
		-  Continue program execution after an exception is caught and handled
		- Meaningful Error Reporting:
• Exceptions are objects
• A description of an exception in the form of a string
		- 使得方法能够抛出一个异常，
没有这个，方法或者这个语句必须处理这个异常或者终止程序，
捕获并处理这个异常后，程序会继续运行


- Types of Exception

	- ArithmeticException 算数异常
	- InputMismatchException
	-  IndexOutOfBoundsException （array index too big/small）
	-  IllegalArgumentException (method has been passed an illegal argument)

### Exception

- Checked Exception

	- Exception that occurs at the compile time

- Unchecked Exception

	- Exception that occurs at the execution time

- Key words

	-  try // block contains set of statements where an exception can occur
	- catch // block is used to handle the uncertainty of try block
	- finally // executed after catch blocks
	- throw // transfer control from try block to catch block
	- throws // specifies the exceptions that a method can throw to the caller, doesn’t use try or catch

-  A method that is throwing an exception contains the code to handle the exception with the try-catch block or declared with throws
 • If neither, then it gives a compilation error
异常处理要包含解决这个异常的try-catch 代码 或者是声明一个throw给它抛出，要是都没有就还会有编译错误

### Error

- Linkage Error
- VirtualMachine Error

### Exception2

- RuntimeException
- IOE Exception
- ClassNotFoundException
- Many more classes

### Throw

-  throw keyword is used to explicitly throw an exception

### FileReader

### BuffReader

## Week 10

### Java.lang

### Class that correspond to primitives

- example

	- int

		- Binary representation of an integer 
		- 32 bits
		- Cannot be casted to from a string value
		- • Cannot be rebased (eg. Hex)

	- Integer

		- Wrapper class
		- • Used in collections or generics
		- 128 bits
		- • String -> Integer -> Hex
		- String st = "42";
Integer i1 = new Integer(st);

- Autoboxing

	- 当一个Method 以wrapclass 或者primitives 作为 参数parameter的时候，可以自动转换

- System Class

	- System .out
	- System.in
	- System.err
	- arraycopy(Object src, int srcPos, Object dest, int destPos, int length)

		- System.arraycopy(array1, 1, array2, 3, 2)

	- Exit(in status)
	- lineSeparator() 

### Scanner

- How scanner works

	- The Scanner object reads an entire line (from file or system) and divides the line into tokens
	- Whitespace is the default delimiter(Change using useDelimiter() method)
	-  scannerObj.nextInt(); //accepts the next int
	- • scannerObj.nextLine(); //accepts next String
	- • .nextFloat .nextBoolean

- Scanner.hasNext()
//To check if anything left

### Data Structures

- The arrangement of data and how to access and manipulate it -----Chris 马路骑士
- Examples

	- Array

		- Array is a collection of similar type of elements which has continuous memory location
		- Pros: Fixed length linear lists.
		- Access via index 通过索引访问
		-  Support fast random access to element 支持快速随机获得元素
		- 元素之间的链接是隐式的Connection between elements is implicit
- saves space, saves time

	- Stack (LIFO)

		- No random access
		- Push (put item onto stack) and pop (take item off stack)

	- Queue (FIFO)

		- No random access
		- Items added to the end but taken from the top
		- Prioritiesd Queue

			-  Items added or taken off using some priority metric
			- • Important from a research perspective (QoS, Pricing etc)

	- Linked List

		-  Elements accessed more flexibly
		- Each element also carries at least one link to the next element
		-  New elements inserted/removed by rearranging links, not the location of the data 通过改变数据间的链接来进行插入和删除元素

	- Tree

		- Root is the first item
		-  Subtree nodes from that root
		- Any node with no subtree is a ‘leaf’
		- Binary search Trea

			- 数小于node 的放左边， 大于的放右边
			-  Finding a node never greater than the depth of the tree
			- • approx. Log(n)
			- • 1 million elements = depth of 20

	- Hash Table

		- A hash code, associated with the data itself, decides the storage index
		- Hash code acts as an index
		- Insertions, deletion and searches are relatively fast

	- Graph
	- Arrays

		-  Arrays class is part of the Java Collection Framework
		- Provides static methods for array creation and access
		- Examples

			- Arrays.binarySearch(myArray, myKey))
			- Arrays.hashCode(myArray)) // returns an integer hashcode
			- Arrays.sort(myArray) // sorts in ascenfing order
			- sort
			- equal
			- toString
			- fill
			- asList()

- Which one to use?

	- If FIFO or LIFO is standard use a stack or Queue
	- • Frequent access but no sorting (eg. DNS tables) – Hash table
	- • BST for fast search of a sorted list
	- • Linked list when you will be accessing the collection sequentially and wholly with many inserts and deletes
	- • Array – fast random access, slow insertions and deletions
	- 符合LIFO 或 FIFO 就 stack 或 queue
要频繁访问但不排序（比如DNS Table）就用hash table
快速搜索 BST
添加删除就用Linked list
随机访问 慢点添加删除就Array

### Framework

- Introduction

	- Sets of pre-written code
	- • Used as templates
	- • IDEs provide some of these framework ability
	- • Predefined classes and functions！！！！
	- framework就是别人写好的你直接用的

- Examples

	- Play
	- GWT
	- Hibernate
	- Spring

### Linked list vs Array

- Array: Accessing an element takes constant time, adding an element takes n time
Linked list: Accessing an element takes n time, adding an element > 1 time
- Disadvantage of LL vs Array

	- 查找元素慢：Finding the nth element takes O(n) time
	- 用很多内存：Need the data and the link so use many memory
	- Caching/prefetching may not be useful
	- 难找bug：More difficult to program/debug

- Advantage vs Array

	- 什么类型元素都可以：Heterogeneous elements 
	- 插入和删除很容易：Inserting/Deleting an element easier 相对于Array array 就得changing all subsequent memory locations

array： Memory allocation at compile time
	- Better for multithreading
	- Changes in a linked list are naturally ‘local’， 改变两个link 一个value就行
	- Many threads can be working on one linked list
	- Can iterate while changing
	- Arrays require much more ‘locking’ due to the need to change so many elements

### ArrayList

- 支持动态数组： dynamic array
-  Automatically enlarges when needed
- 3 constructors

	- ArrayList()  //builds empty ArrayList
	- ArrayList(int capacity) //builds ArrayList with a specified initial capacity
	-  ArrayList(Collection c) //builds with elements from collection c

- benefits

	- More flexible than array but same internal process
	-  ArrayList is a good choice when the number of reads is more than the number of writes
	- Too many writes and a completely unknown size, then maybe use a LinkedList

-  ArrayList not for primitives:  If you try and use primatives in ArrayList they are autoboxed <Type> what type of elements being used

## Another

### IS-A and HAS-A elationships

- Reusable code, core for OOP
- Whenever you extend class Alpha (or implements) to produce a new class Beta then
- This is unidirectional (Alpha IS-A Beta is false)
- Whenever one class uses different public class
--Beta HAS-A Gamma
- 总结一句就是：子类或者实现借口就是 IS-A关系
用到了其他类 他们就是 HAS-a 关系

*XMind - Trial Version*
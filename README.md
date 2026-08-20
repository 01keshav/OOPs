# 📘 OOP USING JAVA — COMPLETE HANDBOOK
### Course Code 105303 | Syllabus-wise arranged | 3-0-0-3



---

# 🟦 UNIT 1 — OOP Concepts and Java Programming (5 hrs)

## 1.1 History of Java
- Java was created by **James Gosling** and team at **Sun Microsystems**, released in **1995**.
- Originally called **"Oak"** (named after an oak tree), later renamed **Java** (inspired by Java coffee).
- Made for a project called **"Green Project"** — to control smart/electronic devices (like TVs, remotes).
- Sun Microsystems was later bought by **Oracle Corporation (2010)** — Oracle now owns Java.
- Java became popular because of the internet boom (platform independence was perfect for web).

**Hinglish tip:** Java banaya tha "smart appliances" ke liye, baad me internet + enterprise apps ke liye chhaa gaya.

## 1.2 Java Buzzwords (Key Features of Java)
| Buzzword | Meaning |
|---|---|
| Simple | Easy syntax, no pointers, automatic memory management |
| Object-Oriented | Everything (almost) is treated as an object |
| Platform Independent | "Write Once, Run Anywhere" (WORA) via bytecode |
| Secure | No explicit pointers, runs inside JVM sandbox |
| Robust | Strong memory management, exception handling |
| Multithreaded | Can run multiple threads (tasks) at once |
| Architecture Neutral | Bytecode not tied to any specific CPU/OS |
| Portable | Same bytecode runs on any device with JVM |
| High Performance | Just-In-Time (JIT) compiler speeds execution |
| Distributed | Supports networking (RMI, sockets, etc.) |
| Dynamic | Can adapt/load classes at runtime |
| Interpreted | Bytecode is interpreted by JVM |

**Remember:** WORA = Write Once, Run Anywhere → sabse important buzzword hai, interview me bhi puchte hain.

## 1.3 Procedural vs Object-Oriented Programming

```
Procedural Programming              Object-Oriented Programming
--------------------------         --------------------------
Program = Functions                Program = Objects
Data & functions separate          Data & functions bundled (encapsulated)
Top-down approach                  Bottom-up approach
Less secure (global data)          More secure (data hiding)
Hard to manage large programs      Easy to manage & scale
Example: C                         Example: Java, C++, Python
```

| Feature | Procedural | OOP |
|---|---|---|
| Focus | On functions | On objects |
| Data security | Low (global access) | High (private + getters/setters) |
| Code reuse | Limited | High (inheritance) |
| Real world modeling | Difficult | Natural (objects = real entities) |

## 1.4 Need for OOP Paradigm
- Real-world problems are easier to model as **objects** (Car, Student, BankAccount).
- Helps manage **complexity** in large software.
- Promotes **code reuse** (inheritance) → less duplicate code.
- Improves **security** (encapsulation) → data hiding.
- Makes code **easier to maintain and extend**.

## 1.5 OOP Features / Advantages of OOP
- **4 Pillars:** Encapsulation, Abstraction, Inheritance, Polymorphism (full detail in Unit 2 & 3 below).
- **Advantages:**
  - Modularity (code split into classes/objects)
  - Reusability (inheritance)
  - Easy debugging & maintenance
  - Data hiding & security (encapsulation)
  - Flexibility (polymorphism)
  - Real-world problem modeling

## 1.6 JDK, JRE and JVM

```
         JDK (Java Development Kit)
   ┌───────────────────────────────────┐
   │   JRE (Java Runtime Environment)   │
   │  ┌───────────────────────────┐    │
   │  │   JVM (Java Virtual Machine)│   │
   │  │  - Runs bytecode            │   │
   │  │  - Memory management        │   │
   │  │  - Garbage Collection       │   │
   │  └───────────────────────────┘    │
   │  + Libraries (java.lang, java.util)│
   └───────────────────────────────────┘
   + Compiler (javac), Debugger, Tools
```

| Term | Full Form | What it does |
|---|---|---|
| **JVM** | Java Virtual Machine | Actually **runs** the `.class` (bytecode) file. Platform-dependent (different JVM per OS), but bytecode is same everywhere → yehi WORA possible banata hai. |
| **JRE** | Java Runtime Environment | JVM + core libraries. Needed to **run** Java programs (not to write/compile). |
| **JDK** | Java Development Kit | JRE + compiler (`javac`) + tools. Needed to **write and compile** Java programs. |

**Remember:** JDK ⊃ JRE ⊃ JVM (JDK sabse bada set hai, developer ke liye chahiye. JRE sirf user ke liye jo bas run karna chahta hai)

## 1.7 Basics of Java Programming — First Program

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
```

**Line by line:**
- `public class HelloWorld` → class name file name se match hona chahiye (`HelloWorld.java`)
- `public static void main(String[] args)` → program ka entry point, JVM yahi se run karna start karta hai
- `System.out.println()` → console pe print karta hai (with newline)

## 1.8 Data Types in Java

```
Data Types
├── Primitive (8 types)
│   ├── byte    (1 byte)
│   ├── short   (2 byte)
│   ├── int     (4 byte)
│   ├── long    (8 byte)
│   ├── float   (4 byte)
│   ├── double  (8 byte)
│   ├── char    (2 byte)
│   └── boolean (1 bit) - true/false
└── Non-Primitive (Reference types)
    ├── String
    ├── Array
    ├── Class
    └── Interface
```

```java
int age = 20;
double marks = 89.5;
char grade = 'A';
boolean isPassed = true;
String name = "Keshav";
```

**Key point:** Primitive types store **actual value**. Non-primitive (reference) types store **memory address (reference)** of the object.

## 1.9 Variables
- A variable is a **named memory location** to store data.
- Types: **Local** (inside method), **Instance** (inside class, outside method), **Static** (shared across all objects, declared with `static`).

```java
class Demo {
    int instanceVar = 10;       // instance variable
    static int staticVar = 20;  // static variable
    void show() {
        int localVar = 30;      // local variable
    }
}
```

## 1.10 Operators in Java
| Type | Operators | Example |
|---|---|---|
| Arithmetic | `+ - * / %` | `a + b` |
| Relational | `== != > < >= <=` | `a > b` |
| Logical | `&& \|\| !` | `a && b` |
| Assignment | `= += -= *= /=` | `a += 5` |
| Unary | `++ -- !` | `a++` |
| Ternary | `? :` | `a > b ? a : b` |
| Bitwise | `& \| ^ ~ << >>` | `a & b` |

## 1.11 Control Structures

**Selection (Decision Making)**
```java
if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}

switch (day) {
    case 1: System.out.println("Monday"); break;
    default: System.out.println("Invalid");
}
```

**Looping**
```java
for (int i = 0; i < 5; i++) { System.out.println(i); }

int i = 0;
while (i < 5) { System.out.println(i); i++; }

int j = 0;
do { System.out.println(j); j++; } while (j < 5);
```

## 1.12 Java Methods (intro — full detail already in your "3. METHOD" notes below in Unit 2)
- Block of reusable code performing a specific task, defined inside a class.

## 1.13 Compilation and Execution of a Simple Program

```
HelloWorld.java  --(javac HelloWorld.java)-->  HelloWorld.class (bytecode)
                                                        │
                                              (java HelloWorld)
                                                        ▼
                                                  JVM executes it
                                                        ▼
                                              Output on console
```

```bash
javac HelloWorld.java     # Compiles .java -> .class (bytecode)
java HelloWorld           # JVM runs the bytecode
```

**Remember:** Java is both **compiled** (source → bytecode) and **interpreted** (bytecode → machine code by JVM). Isi wajah se "Write Once, Run Anywhere" possible hai.

---

# 🟦 UNIT 2 — Objects, Classes and Constructors (7 hrs)

## 2.1 Class

**What is a Class?**
A class is a **blueprint or template** for creating objects. It defines a set of **attributes** (data) and **methods** (functions) that objects of the class will have.

**Key Points**
- A class does **not occupy memory**.
- It is a **user-defined data type**.
- It acts as a **blueprint** for creating objects.
- Helps in **data hiding** and **code reusability**.

**Syntax**
```java
class ClassName {
    // Attributes
    dataType attribute1;
    dataType attribute2;

    // Methods
    returnType methodName(parameters) {
        // method body
    }
}
```

**Example**
```java
class Student {
    // Attributes
    int id;
    String name;
    double marks;

    // Methods
    void display() {
        System.out.println("ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Marks: " + marks);
    }
}
```

```
             Student (Class Name)
   ┌─────────────────────────────────┐
   │ Attributes (Data):               │  → Holds Data (State)
   │   int id; String name; double marks; │
   │ Methods (Functions):             │  → Performs Actions (Behavior)
   │   void display();                │
   └─────────────────────────────────┘
```

**Remember:** A class is just a template. **No memory is allocated when a class is created.** Memory is allocated only when objects are created from the class → `Student s1 = new Student();`

## 2.2 Object

**What is an Object?**
An object is a **real-world entity** which is an **instance** of a class. It has **state** (data) and **behavior** (methods).

**Key Points**
- An object is **created** from a class.
- It **occupies memory**.
- Each object has its **own copy of data**.
- Objects can interact by **calling methods**.
- Multiple objects can be created from the same class.

**Syntax**
```java
ClassName objectName = new ClassName();
//  ↑           ↑         ↑    ↑
// Class    Object Ref   new  Constructor
```

**Example**
```java
class Student {
    int id;
    String name;
    void display() {
        System.out.println(id + " - " + name);
    }
}
public class Main {
    public static void main(String[] args) {
        // Creating objects
        Student s1 = new Student();
        Student s2 = new Student();

        // Setting values
        s1.id = 101;  s1.name = "Aman";
        s2.id = 102;  s2.name = "Riya";

        // Calling method
        s1.display();   // Output: 101 - Aman
        s2.display();   // Output: 102 - Riya
    }
}
```

```
                Student (Class)
                       │
        ┌──────────────┴──────────────┐
        ▼                             ▼
   s1 (Object)                  s2 (Object)
   id = 101, name="Aman"        id = 102, name="Riya"
```

**Real life:** Class = Mobile (blueprint), Objects = iPhone, Samsung, OnePlus (each has its own data & behavior).

## 2.3 Declaring Objects & the `new` Keyword
- `new` keyword allocates **memory on the heap** for the object and returns its reference.
- The reference (`s1`, `s2`) is stored in a variable and points to that memory location.

```
Student s1 = new Student();
   Stack:  s1 ───┐
                 ▼
   Heap:   [ id=0, name=null ]   ← actual object
```

## 2.4 Defining and Calling Methods in a Class

**What is a Method?**
A method is a **block of code** that performs a specific task. Defined inside a class, used to define the **behavior** of objects.

**Key Points**
- A method is a function that belongs to a class.
- It can access/modify the data (attributes) of the class.
- Improve code modularity and reusability.
- Can return a value or may not return anything (`void`).

**Syntax**
```java
returnType methodName(parameters) {
    // method body
    return value;   // optional
}
```

**Example**
```java
class Calculator {
    int add(int a, int b) {
        int sum = a + b;
        return sum;
    }
    void showMessage() {
        System.out.println("Hello, Java!");
    }
}
public class Main {
    public static void main(String[] args) {
        Calculator c = new Calculator();
        int result = c.add(10, 20);        // calling method with return
        System.out.println("Sum = " + result);
        c.showMessage();                    // calling void method
    }
}
```

```
Object ──calls──▶ Method (performs task) ──▶ Result / Output
```

**Real life analogy:** Remote control. Pressing a button (method) performs an action like changing channel, increasing volume — each button has a specific function.

## 2.5 Array of Objects
- Just like arrays of `int`/`String`, we can create an **array of objects** of a class.

```java
class Student {
    int id;
    String name;
    Student(int id, String name) { this.id = id; this.name = name; }
    void display() { System.out.println(id + " - " + name); }
}
public class Main {
    public static void main(String[] args) {
        // Array of 3 Student objects
        Student[] students = new Student[3];
        students[0] = new Student(1, "Aman");
        students[1] = new Student(2, "Riya");
        students[2] = new Student(3, "Kabir");

        for (Student s : students) {
            s.display();
        }
    }
}
```
**Hinglish tip:** `new Student[3]` sirf 3 **references** ka array banata hai (sab `null`), har element ko individually `new Student()` se initialize karna padta hai — warna `NullPointerException` aayega.

## 2.6 Constructor

**What is a Constructor?**
A constructor is a **special method** in a class used to **initialize objects**. It is **called automatically** when an object is created.

**Key Points**
- Constructor name is **same as class name**.
- It has **no return type**, not even `void`.
- Called **automatically** when object is created.
- Used to **initialize** object's data.
- A class can have **multiple constructors** (constructor overloading).
- If no constructor is written, Java provides a **default constructor**.

**Syntax**
```java
class ClassName {
    ClassName(parameters) {
        // initialization code
    }
}
```

**Example**
```java
class Student {
    int id;
    String name;
    // Constructor
    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
    void display() {
        System.out.println(id + " - " + name);
    }
}
public class Main {
    public static void main(String[] args) {
        Student s1 = new Student(101, "Aman");
        Student s2 = new Student(102, "Riya");
        s1.display();   // 101 - Aman
        s2.display();   // 102 - Riya
    }
}
```

```
new Student(101, "Aman")
        │
        ▼
Constructor is called
        │
        ▼
Object is created
        │
        ▼
Data is initialized
```

**Types of Constructors**
- **Default Constructor** (no-arg) — auto-provided by Java if you write none.
- **Parameterized Constructor** — takes arguments to set initial values.
- **Copy Constructor** (via parameter, manually written — Java has no built-in one like C++).

```java
// Copy constructor example
class Student {
    int id; String name;
    Student(int id, String name) { this.id = id; this.name = name; }
    Student(Student s) {          // copy constructor
        this.id = s.id;
        this.name = s.name;
    }
}
```

**Real life:** When you register on any website, your details (name, email, password) are filled automatically in the form the moment your account object is created — that's like a constructor initializing data.

## 2.7 Constructor Overloading & Method Overloading
(Full detail with diagram already covered under **Polymorphism → Compile-time Polymorphism** in Unit 3 below — same concept applies to constructors too: same class, multiple constructors, different parameter list.)

```java
class Student {
    int id; String name; double marks;
    Student() { }                                   // no-arg
    Student(int id, String name) { this.id=id; this.name=name; }        // 2 params
    Student(int id, String name, double marks) {     // 3 params
        this.id=id; this.name=name; this.marks=marks;
    }
}
```

## 2.8 Method Binding

**What is Binding?**
Binding = connecting a method **call** to the method **body (definition)**.

| Type | When resolved | Example |
|---|---|---|
| **Static Binding** (Early Binding) | At **compile time** | `static`, `private`, `final` methods, method overloading |
| **Dynamic Binding** (Late Binding) | At **runtime** | Method overriding (via parent reference → child object) |

```java
class Animal { void sound() { System.out.println("Animal sound"); } }
class Dog extends Animal { void sound() { System.out.println("Dog barks"); } }

Animal a = new Dog();
a.sound();   // Dog barks -> decided at RUNTIME = Dynamic Binding
```

**Hinglish tip:** Overloading = compile-time pe pata chal jaata hai kaunsa method call hoga (static binding). Overriding = runtime pe object dekhkar decide hota hai (dynamic binding) — JVM object ka **actual type** dekhta hai, reference type nahi.

## 2.9 Method Overriding — quick recap
(Full detail in Unit 3 → Polymorphism → Run-time Polymorphism. In short: child class redefines a parent method with the **same name, same parameters**; resolved at runtime based on actual object.)

## 2.10 Exceptions (Brief Intro — full detail in Unit 4)
- An **exception** is an unwanted/unexpected event that disrupts normal program flow (e.g., dividing by zero, invalid array index).
- Java handles it using `try-catch-finally`.
- **Full detailed coverage: Types, Hierarchy, custom exceptions, multiple catch → see Unit 4 below.**

## 2.11 Passing Objects as Parameters & Returning Objects

```java
class Point {
    int x, y;
    Point(int x, int y) { this.x = x; this.y = y; }
}
class Utility {
    // Passing object as parameter
    static void printPoint(Point p) {
        System.out.println(p.x + ", " + p.y);
    }
    // Returning an object from a method
    static Point midPoint(Point p1, Point p2) {
        return new Point((p1.x + p2.x) / 2, (p1.y + p2.y) / 2);
    }
}
public class Main {
    public static void main(String[] args) {
        Point a = new Point(0, 0);
        Point b = new Point(10, 10);
        Utility.printPoint(a);              // 0, 0
        Point mid = Utility.midPoint(a, b);
        Utility.printPoint(mid);            // 5, 5
    }
}
```
**Key point:** Objects are passed **by reference value** in Java — the method gets a copy of the reference, so it can modify the object's data, but reassigning the reference inside the method doesn't affect the caller's variable.

## 2.12 Static Members

**Key Points**
- `static` keyword means the member belongs to the **class**, not to individual objects.
- **Static variable** → single copy shared by **all objects**.
- **Static method** → can be called using **ClassName.methodName()** without creating an object; can only directly access other static members.

```java
class Counter {
    static int count = 0;   // shared across all objects
    Counter() { count++; }
}
public class Main {
    public static void main(String[] args) {
        new Counter(); new Counter(); new Counter();
        System.out.println(Counter.count);   // 3
    }
}
```

```
        Counter.count (ONE shared copy)
        ▲          ▲          ▲
       obj1       obj2       obj3
```

**Hinglish tip:** Static = "class ki property", sab objects share karte hain. Non-static (instance) = "har object ki apni copy".

## 2.13 Access Modifiers

| Modifier | Same Class | Same Package | Subclass (diff package) | Everywhere |
|---|---|---|---|---|
| `private` | ✅ | ❌ | ❌ | ❌ |
| default (no modifier) | ✅ | ✅ | ❌ | ❌ |
| `protected` | ✅ | ✅ | ✅ | ❌ |
| `public` | ✅ | ✅ | ✅ | ✅ |

```java
public class Student {
    private int id;          // only inside Student class
    String name;             // default: package only
    protected double marks;  // package + subclasses
    public String college;   // accessible everywhere
}
```

## 2.14 `this` Keyword

**Uses of `this`:**
1. Refer to **current object's** instance variable (to resolve naming conflict with parameters).
2. Call **another constructor** in the same class (`this(...)`) → constructor chaining.
3. Pass current object as an argument.
4. Return the current object from a method.

```java
class Student {
    int id; String name;
    Student(int id, String name) {
        this.id = id;        // this.id = instance var, id = parameter
        this.name = name;
    }
    Student() {
        this(0, "Unknown");  // calling parameterized constructor
    }
}
```

## 2.15 Garbage Collection & `finalize()`

**Garbage Collection (GC)**
- Java automatically **frees memory** occupied by objects that are no longer referenced (no manual `free()`/`delete()` like C/C++).
- Runs in the background (via a daemon thread), managed by JVM.
- Object becomes eligible for GC when it has **no live references** pointing to it.
- Can be **requested** (not guaranteed) using `System.gc()`.

```java
Student s1 = new Student();
s1 = null;    // now the old Student object has no reference -> eligible for GC
```

**`finalize()` method**
- Called by the garbage collector **just before** destroying an object, to do cleanup.
- Deprecated in modern Java (from Java 9+) — not recommended to use, but asked in syllabus for concept.

```java
class Demo {
    protected void finalize() {
        System.out.println("Object destroyed");
    }
}
```

**Remember:** Yeh Java ka bada advantage hai C/C++ ke against — memory leaks ka manual risk kam ho jaata hai.

## 2.16 Nested and Inner Classes

```
Nested Classes
├── Static Nested Class   (declared static, no need of outer object)
└── Inner Class (non-static)
    ├── Member Inner Class
    ├── Local Inner Class   (inside a method)
    └── Anonymous Inner Class (no name, one-time use)
```

```java
class Outer {
    int data = 10;

    class Inner {                       // non-static inner class
        void show() {
            System.out.println("Outer data: " + data);  // can access outer's members
        }
    }

    static class StaticNested {         // static nested class
        void display() { System.out.println("I am static nested"); }
    }
}
public class Main {
    public static void main(String[] args) {
        Outer o = new Outer();
        Outer.Inner in = o.new Inner();     // needs outer object
        in.show();

        Outer.StaticNested sn = new Outer.StaticNested();  // no outer object needed
        sn.display();
    }
}
```
**Why used?** Logical grouping of classes that are used only in one place, increases encapsulation.

## 2.17 Exploring the `String` Class

**Key Points**
- `String` is a class in `java.lang`, represents a sequence of characters.
- Strings in Java are **immutable** (once created, value cannot change — any "modification" creates a new String object).
- Can be created using **literal** (`"abc"` → stored in String Pool) or **`new` keyword** (creates a new object in heap, bypassing the pool).

```java
String s1 = "hello";              // string literal -> String Pool
String s2 = new String("hello");  // new object -> heap (separate memory)

System.out.println(s1 == s2);          // false (different memory)
System.out.println(s1.equals(s2));     // true  (same content)
```

**Common String Methods**
| Method | Use |
|---|---|
| `length()` | returns length |
| `charAt(i)` | char at index i |
| `substring(a,b)` | part of string |
| `toUpperCase()/toLowerCase()` | case conversion |
| `equals()/equalsIgnoreCase()` | compare content |
| `trim()` | remove leading/trailing spaces |
| `split(regex)` | splits into array |
| `concat()` / `+` | joins strings |
| `indexOf()` | position of substring |
| `replace()` | replace characters |

```java
String name = "  Keshav  ";
System.out.println(name.trim().toUpperCase());   // "KESHAV"
System.out.println(name.trim().length());         // 6
```

**Hinglish tip:** String immutable hone ka matlab: `s1.concat("world")` likhoge toh `s1` khud change nahi hoga, ek **naya** String object banega jab tak tum usse assign na karo: `s1 = s1.concat("world");`

**Bonus: StringBuilder / StringBuffer** — mutable alternative for heavy string modification (used when doing lots of concatenation in loops):
```java
StringBuilder sb = new StringBuilder("Hello");
sb.append(" Java");      // modifies same object, no new object created
System.out.println(sb);  // Hello Java
```

---

# 🟦 UNIT 3 — Inheritance, Interfaces and Packages (9 hrs)

## 3.1 Inheritance

**What is Inheritance?**
Inheritance is a mechanism where a new class (**child/subclass**) acquires the properties and behaviors (fields and methods) of an existing class (**parent/superclass**). It promotes code reusability and establishes an **IS-A relationship**.

**Key Points**
- The class whose members are inherited is called **superclass** (parent class).
- The class that inherits is called **subclass** (child class).
- The subclass can have its **own members** in addition to inherited members.
- Supports **code reusability** and **extensibility**.
- Java does **not support multiple inheritance with classes** (but supports it using interfaces).

**Syntax**
```java
class SuperClass {
    // fields and methods
}
class SubClass extends SuperClass {
    // own fields and methods
}
```

**Example**
```java
class Animal {                       // Parent Class (Superclass)
    String color = "Brown";
    void eat() { System.out.println("Animal is eating"); }
}
class Dog extends Animal {           // Child Class (Subclass)
    void bark() { System.out.println("Dog is barking"); }
}
public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();               // inherited method
        d.bark();               // own method
        System.out.println(d.color);  // inherited field
    }
}
```

```
   Animal (Superclass/Base Class)
            │  extends
            ▼
   Dog (Subclass/Derived Class)
```

**How it works:** 1) Dog **is a** Animal (IS-A). 2) Dog inherits `color` and `eat()` from Animal. 3) Dog can use inherited members AND define its own members.

**Benefits:** Code Reusability, Easy Maintenance, Extensibility, Better Organization.
**Remember:** Use `extends` to inherit. Private members are **not inherited**. Constructors are **not inherited**.

## 3.2 Inheritance Hierarchies (Types of Inheritance)

```
Single Inheritance          Multilevel Inheritance       Hierarchical Inheritance
      A                          A                              A
      │                          │                        ┌─────┼─────┐
      ▼                          ▼                        ▼     ▼     ▼
      B                          B                        B     C     D
                                 │
                                 ▼
                                 C
```

- **Single** — one class inherits from one parent (`Dog extends Animal`)
- **Multilevel** — chain of inheritance (`C extends B`, `B extends A`)
- **Hierarchical** — multiple classes inherit from the **same** parent (`Cat extends Animal`, `Dog extends Animal`)
- **Multiple Inheritance (with classes)** → ❌ **NOT supported** in Java (to avoid the "Diamond Problem" — ambiguity when two parents have the same method). ✅ Achieved instead using **interfaces** (see 3.6 below).
- **Hybrid** → combination — also achieved via interfaces since multiple class inheritance isn't allowed.

## 3.3 `super` Keyword & Member Access Rules

**Uses of `super`:**
1. Access parent class's **instance variable** (when child has variable with same name).
2. Call parent class's **method** (especially if overridden in child).
3. Call parent class's **constructor** — `super(...)` (must be the **first line** in child constructor).

```java
class Animal {
    String color = "Brown";
    Animal(String color) { this.color = color; }
    void sound() { System.out.println("Animal makes sound"); }
}
class Dog extends Animal {
    Dog(String color) {
        super(color);            // calls Animal's constructor
    }
    void sound() {
        super.sound();           // calls Animal's sound()
        System.out.println("Dog barks");
    }
}
```

**Member Access Rules in Inheritance**
| Parent member | Inherited by child? |
|---|---|
| `public` / `protected` | ✅ Yes |
| default (package) | ✅ only if same package |
| `private` | ❌ No (not inherited, but exists in memory — accessible only via parent's own methods) |
| Constructors | ❌ Never inherited |
| `static` members | ✅ Shared (accessed via class name) |

## 3.4 Preventing Inheritance — `final` Classes and Methods

- `final class` → **cannot be extended/inherited** by any other class.
- `final method` → **cannot be overridden** by a subclass.
- `final variable` → becomes a **constant**, value cannot change once assigned.

```java
final class Vehicle {          // cannot be extended
    // ...
}
// class Car extends Vehicle { }   ❌ Compile Error

class Bike {
    final void start() {       // cannot be overridden
        System.out.println("Bike started");
    }
}
```

**Hinglish tip:** `final` = "yahi last hai, aage kuch mat karo" — chahe class ho, method ho ya variable, matlab hamesha "no more change/extension allowed" hota hai.

## 3.5 Polymorphism

**What is Polymorphism?**
Polymorphism means **"many forms"**. It allows one interface to be used for different types. In Java, achieved by **Method Overloading** and **Method Overriding**.

**Types:** 1) Compile-time Polymorphism (Method Overloading)  2) Run-time Polymorphism (Method Overriding)

### 3.5.1 Compile-time Polymorphism (Method Overloading)
- Occurs in the **same class**.
- Same method name but **different parameter list** (number, type, or order).
- Resolved at **compile time**.

```java
class Calculator {
    int add(int a, int b) { return a + b; }
    int add(int a, int b, int c) { return a + b + c; }
    double add(double a, double b) { return a + b; }
}
public class Main {
    public static void main(String[] args) {
        Calculator obj = new Calculator();
        System.out.println(obj.add(10, 20));       // 30
        System.out.println(obj.add(10, 20, 30));   // 60
        System.out.println(obj.add(10.5, 20.5));   // 31.0
    }
}
```
The **compiler** decides which method to call based on the arguments passed.

### 3.5.2 Run-time Polymorphism (Method Overriding)
- Occurs in **different classes** using inheritance.
- Same method name, **same parameters**.
- Resolved at **runtime** (JVM decides based on **actual object**, not reference type).

```java
class Animal {
    void sound() { System.out.println("Animal makes sound"); }
}
class Dog extends Animal {
    @Override
    void sound() { System.out.println("Dog barks"); }
}
public class Main {
    public static void main(String[] args) {
        Animal a = new Dog();   // Reference of parent, object of child
        a.sound();               // Calls overridden method -> "Dog barks"
    }
}
```

**Rules for Overriding:**
- Method name, return type (or covariant), and parameters must match exactly.
- Access modifier of overriding method **cannot be more restrictive**.
- `private`, `static`, and `final` methods **cannot be overridden**.

| Feature | Method Overloading | Method Overriding |
|---|---|---|
| Type | Compile-time | Run-time |
| Where | Same class | Different class (Inheritance) |
| Parameters | Must differ | Must be same |
| Binding | Static | Dynamic |

**Remember:** Overloading increases readability. Overriding achieves runtime polymorphism. `@Override` annotation is good practice (catches mistakes at compile time).

## 3.6 Abstraction & Abstract Classes

**What is Abstraction?**
Abstraction is the process of **hiding implementation details** and showing only the **essential features** to the user. Reduces complexity and improves security. In Java, achieved using **abstract class** and **interface**.

**Purpose:** Hide internal details, Show only functionality, Reduce complexity, Improve maintainability.

**Abstract Class**
- A class that **cannot be instantiated**.
- Can have **abstract methods** (without body) and **concrete methods** (with body).
- Can have constructors, instance variables, static methods, final methods.
- Child class **must extend and implement** all abstract methods (or itself be declared abstract).

**Syntax / Example**
```java
abstract class Shape {
    abstract void draw();        // abstract method (no body)
    void color() {                // concrete method (has body)
        System.out.println("Color is set");
    }
}
class Circle extends Shape {
    void draw() { System.out.println("Drawing Circle"); }
}
```

**What is Allowed in Abstract Class?**
| Feature | Allowed? |
|---|---|
| Abstract Methods | ✅ |
| Concrete Methods | ✅ |
| Constructors | ✅ |
| Instance Variables | ✅ |
| Static Methods | ✅ |
| Final Methods | ✅ |
| Object Creation | ❌ |

```java
abstract class Vehicle {
    String brand;
    Vehicle(String brand) { this.brand = brand; }   // constructor allowed
    abstract void start();                             // abstract method
    void stop() { System.out.println("Vehicle Stopped"); }  // concrete method
}
```

**Important Notes**
- We **cannot** create an object of an abstract class.
- If a class extends an abstract class, it must implement all abstract methods **or** itself be declared abstract.
- Abstract class helps provide a common base + partial implementation.

## 3.7 Interface

**What is an Interface?**
An interface is a **blueprint of a class**. It defines a **contract** that implementing classes must follow. Contains only abstract methods (by default `public` and `abstract`) and constants.

**Key Points**
- A class implements an interface using the **`implements`** keyword.
- **Multiple interfaces** can be implemented by one class → this is how Java achieves multiple inheritance.
- All variables in an interface are **`public static final`** by default (constants).

```java
interface Animal {
    void sound();     // public & abstract by default
}
class Dog implements Animal {
    public void sound() { System.out.println("Dog barks"); }
}
class Main {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();     // Output: Dog barks
    }
}
```

### 3.7.1 Types of Methods in Interface (Modern Java)
| Type | Syntax | Can have body? | Since |
|---|---|---|---|
| Abstract Method | `void show();` | No (by default) | All versions |
| Default Method | `default void show(){...}` | Yes | Java 8 |
| Static Method | `static void show(){...}` | Yes | Java 8 |
| Private Method | `private void show(){...}` | Yes (helper, only inside interface) | Java 9 |

```java
interface Vehicle {
    void start();                          // abstract
    default void stop() {                  // default method
        System.out.println("Vehicle Stopped");
    }
}
class Car implements Vehicle {
    public void start() { System.out.println("Car Started"); }
    // stop() not overridden -> uses default implementation
}
```

```java
interface MathUtil {
    static int add(int a, int b) { return a + b; }   // static method
}
int res = MathUtil.add(10, 20);   // called using Interface name, not object
```

### 3.7.2 Constants in Interface
```java
interface Config {
    int MAX_LIMIT = 100;         // public static final by default
    String APP_NAME = "MyApp";
}
```

### 3.7.3 Multiple Inheritance via Interface
```java
interface Runnable2 { void run(); }
interface Serializable2 { void save(); }
class MyTask implements Runnable2, Serializable2 {   // implementing 2 interfaces
    public void run() { System.out.println("Running"); }
    public void save() { System.out.println("Saving"); }
}
```

### 3.7.4 Accessing Implementation through Interface Reference & Extending Interfaces
```java
interface Shape { void area(); }
interface Shape3D extends Shape {   // interface extending another interface
    void volume();
}
class Cube implements Shape3D {
    public void area() { System.out.println("Calculating area"); }
    public void volume() { System.out.println("Calculating volume"); }
}
Shape s = new Cube();     // interface reference, calling implementation through it
s.area();
```
**Note:** An interface can `extends` **multiple** other interfaces (unlike classes which can extend only one class).

## 3.8 Interface vs Abstract Class — Complete Comparison

| Feature | Abstract Class | Interface |
|---|---|---|
| Declaration Keyword | `abstract` | `interface` |
| Methods | abstract + concrete | only abstract (till Java 7); all types from Java 8 |
| Method Body | abstract: no body; concrete: has body | abstract: no body (default/static can have body) |
| Default Methods | ❌ | ✅ (Java 8+) |
| Static Methods | ✅ | ✅ (Java 8+) |
| Private Methods | ✅ | ✅ (Java 9+) |
| Instance Variables | ✅ | ❌ |
| Static Variables | ✅ | ✅ (as `public static final` constant) |
| Constructors | ✅ | ❌ |
| Multiple Inheritance | ❌ (extends only 1 class) | ✅ (implements many interfaces) |
| Object Creation | ❌ | ❌ |
| Access Modifiers | any | public by default |
| State (Data) | Can maintain | Cannot maintain |
| Use Case | common implementation + state | define a contract (behavior) |

```
Quick Decision Guide:
Need common implementation and state? → YES → Use Abstract Class
                                       → NO  → Need multiple implementations of same behavior?
                                                     → YES → Use Interface
                                                     → NO  → (reconsider design)
```

### 3.8.1 Functional Interface & Lambda Expressions (bonus — Java 8, useful for exams)
- An interface with **exactly one abstract method** is called a **Functional Interface** (`@FunctionalInterface`).
- Can be implemented using a **Lambda Expression** — a short way to write an implementation.

```java
@FunctionalInterface
interface MyFunctional {
    void show(String msg);
}
public class Test {
    public static void main(String[] args) {
        MyFunctional mf = (msg) -> System.out.println(msg);   // Lambda
        mf.show("Hello Java 8");
    }
}
```

| Built-in Functional Interface | Package | Method | Example |
|---|---|---|---|
| `Predicate<T>` | java.util.function | `boolean test(T t)` | `t -> t.length() > 5` |
| `Function<T,R>` | java.util.function | `R apply(T t)` | `s -> s.toUpperCase()` |
| `Consumer<T>` | java.util.function | `void accept(T t)` | `s -> System.out.println(s)` |
| `Supplier<T>` | java.util.function | `T get()` | `() -> new ArrayList<>()` |

**Remember:** Functional Interface + Lambda = Modern, Clean, Concise Java.

## 3.9 IS-A vs HAS-A Relationship

| Aspect | IS-A (Inheritance) | HAS-A (Composition) |
|---|---|---|
| Meaning | One class is a type of another | One class contains another object |
| Keyword | `extends` | Object reference (as a field) |
| Coupling | Tight | Loose |
| Reuse | via Inheritance | via Composition |
| Relationship | Parent-Child | Owner-Component |
| Flexibility | Less | More |

```java
// IS-A
class Animal { }
class Dog extends Animal { }      // Dog IS-A Animal

// HAS-A
class Engine { }
class Car {
    Engine engine = new Engine();  // Car HAS-A Engine
}
```

**Best Practice:** Prefer **Composition (HAS-A)** over Inheritance (IS-A) when possible. Use IS-A only when there's a true parent-child relationship. Use HAS-A for flexibility and loose coupling.

## 3.10 Encapsulation

**What is Encapsulation?**
Encapsulation is the mechanism of **wrapping data (variables) and code (methods) together** as a single unit, restricting direct access to some of the object's components. Helps in **data hiding**.

**Key Points**
- Achieved using **access modifiers**.
- Class variables should be **`private`**.
- Access provided through public **getter and setter** methods.
- Protects data from accidental modification. Improves maintainability & flexibility.

**Syntax**
```java
class ClassName {
    private dataType variable;
    public dataType getVariable() { return variable; }
    public void setVariable(dataType value) { variable = value; }
}
```

**Example**
```java
class Student {
    private int id;
    private String name;

    public int getId() { return id; }
    public void setId(int id) { this.id = id; }
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
}
```

```
Client Code                    Student Class
obj.setId(101); ────────▶  Private Data: id, name
int id = obj.getId(); ◀────  Public Methods: setId(), getId(), setName(), getName()
```

**Benefits:** Protects data from unauthorized access, Improves security, Allows controlled access to data, Makes code easy to maintain and modify.
**Remember:** Make variables private → Provide public getter/setter → Access & modify data only through methods.

## 3.11 Packages

**What is a Package?**
A package is a **namespace/folder** that groups related classes and interfaces together, avoiding naming conflicts and improving organization.

**Types:**
- **Built-in packages** — `java.lang`, `java.util`, `java.io`, `java.sql`, etc.
- **User-defined packages** — created by the programmer.

**Defining & Creating a Package**
```java
// File: Calculator.java   (must be first statement in file, save inside a folder named "mypack")
package mypack;

public class Calculator {
    public int add(int a, int b) { return a + b; }
}
```

**Accessing / Importing a Package**
```java
// File: Main.java
import mypack.Calculator;      // import specific class
// import mypack.*;            // import all classes of package

public class Main {
    public static void main(String[] args) {
        Calculator c = new Calculator();
        System.out.println(c.add(5, 3));
    }
}
```

**CLASSPATH**
- CLASSPATH is an **environment variable** that tells the JVM/compiler **where to look for `.class` files** (user-defined classes and packages) when compiling/running a program.
- Can be set via `-classpath` (or `-cp`) flag while compiling/running:
```bash
javac -cp . -d . Calculator.java     # -d . places compiled class in package folder structure
java -cp . Main
```

```
Package Structure Example:
project/
 ├── mypack/
 │     └── Calculator.class
 └── Main.class
```

**Compiling with packages:**
```bash
javac -d . Calculator.java   # -d . creates folder mypack/ and puts Calculator.class inside
javac Main.java
java Main
```

**Key point:** Package name convention follows **reverse domain name** in real projects, e.g. `com.company.project`.

---

# 🟦 UNIT 4 — Exception Handling (6 hrs)

## 4.1 Introduction to Error and Exception

**What is an Exception?**
An exception is an **unwanted/unexpected event** that occurs during program execution and **disrupts the normal flow** of instructions (e.g., dividing by zero, accessing invalid array index, file not found).

**Error vs Exception**
| Aspect | Error | Exception |
|---|---|---|
| Meaning | Serious problem, usually **cannot be handled** by the program | Problem that **can be caught and handled** |
| Cause | System-level (JVM/hardware issue) | Program-level (logic/input issue) |
| Examples | `OutOfMemoryError`, `StackOverflowError` | `ArithmeticException`, `NullPointerException` |
| Recovery | Usually not recoverable | Recoverable using try-catch |
| Package | `java.lang.Error` | `java.lang.Exception` |

```
                    Throwable
                    ├── Error (not handled normally)
                    └── Exception
                          ├── Checked Exception (compile-time)
                          └── RuntimeException (Unchecked, runtime)
```

## 4.2 Concepts of Exception Handling & Benefits
- Exception handling is a mechanism to **gracefully handle runtime errors**, keeping the normal flow of the application.
- **Benefits:**
  - Program **doesn't crash abruptly**.
  - Separates **error-handling code** from regular business logic.
  - Allows meaningful error messages to the user.
  - Enables **recovery** (e.g., retry, default value, log & continue).

## 4.3 Exception Types & Hierarchy

```
java.lang.Throwable
   │
   ├── java.lang.Error
   │       (StackOverflowError, OutOfMemoryError)
   │
   └── java.lang.Exception
           │
           ├── Checked Exceptions (checked at COMPILE time)
           │       IOException, SQLException, ClassNotFoundException
           │
           └── RuntimeException (Unchecked, checked at RUNTIME)
                   ArithmeticException, NullPointerException,
                   ArrayIndexOutOfBoundsException, NumberFormatException,
                   ClassCastException
```

**Checked vs Unchecked**
| Aspect | Checked Exception | Unchecked Exception |
|---|---|---|
| Checked when? | Compile time | Runtime |
| Must handle? | Yes — `try-catch` or `throws` mandatory | Not mandatory (but good practice) |
| Examples | `IOException`, `SQLException` | `ArithmeticException`, `NullPointerException` |
| Cause | External factors (file, DB, network) | Programming logic mistakes |

## 4.4 `try`, `catch`, `throw`, `throws`, `finally`

**Syntax**
```java
try {
    // risky code
} catch (ExceptionType e) {
    // handling code
} finally {
    // always executes (cleanup code)
}
```

**Example**
```java
public class Main {
    public static void main(String[] args) {
        try {
            int a = 10, b = 0;
            int result = a / b;             // throws ArithmeticException
            System.out.println(result);
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero: " + e.getMessage());
        } finally {
            System.out.println("This always runs (cleanup)");
        }
        System.out.println("Program continues normally");
    }
}
```

| Keyword | Meaning |
|---|---|
| `try` | block of code that might throw an exception |
| `catch` | handles the exception if it occurs |
| `finally` | block that **always executes** (used for cleanup — closing files/connections), whether exception occurs or not |
| `throw` | used to **manually throw** an exception (`throw new Exception("msg")`) |
| `throws` | used in method signature to **declare** that a method might throw an exception (passes responsibility to caller) |

```java
void checkAge(int age) throws Exception {     // throws - declares possibility
    if (age < 18) {
        throw new Exception("Not eligible to vote");   // throw - manually raises exception
    }
    System.out.println("Eligible to vote");
}
public static void main(String[] args) {
    try {
        new Main().checkAge(15);
    } catch (Exception e) {
        System.out.println("Caught: " + e.getMessage());
    }
}
```

## 4.5 Multiple Catch Clauses

```java
try {
    int[] arr = new int[5];
    arr[10] = 50 / 0;             // could throw multiple types
} catch (ArithmeticException e) {
    System.out.println("Arithmetic error: " + e.getMessage());
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Array error: " + e.getMessage());
} catch (Exception e) {           // generic catch, must be LAST
    System.out.println("Some other error: " + e.getMessage());
}
```
**Rule:** More specific exceptions must be caught **before** more general ones (`Exception` must always be the last catch block).

**Multi-catch (Java 7+)** — catch multiple exception types in one block:
```java
try {
    // risky code
} catch (ArithmeticException | ArrayIndexOutOfBoundsException e) {
    System.out.println("Error: " + e.getMessage());
}
```

## 4.6 Nested Try Statements

```java
try {
    System.out.println("Outer try");
    try {
        int result = 10 / 0;
    } catch (ArithmeticException e) {
        System.out.println("Inner catch: " + e.getMessage());
    }
    int[] arr = new int[3];
    arr[5] = 10;                    // will be caught by outer catch
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Outer catch: " + e.getMessage());
}
```
**Hinglish tip:** Nested try tab use hota hai jab ek risky block ke andar bhi ek aur risky operation ho, aur dono ko alag-alag handle karna ho.

## 4.7 Re-throwing Exceptions

```java
void process() throws Exception {
    try {
        int x = 5 / 0;
    } catch (ArithmeticException e) {
        System.out.println("Logging error...");
        throw e;               // re-throw same exception to caller
    }
}
public static void main(String[] args) {
    try {
        new Main().process();
    } catch (Exception e) {
        System.out.println("Handled at main: " + e.getMessage());
    }
}
```
**Why re-throw?** Sometimes you want to log/perform an action locally but let the **calling method** decide the final handling.

## 4.8 Creating Custom (User-defined) Exception Classes

```java
// Custom checked exception -> extend Exception
class InsufficientBalanceException extends Exception {
    InsufficientBalanceException(String message) {
        super(message);      // pass message to Exception's constructor
    }
}
class BankAccount {
    double balance = 1000;
    void withdraw(double amount) throws InsufficientBalanceException {
        if (amount > balance) {
            throw new InsufficientBalanceException("Insufficient balance!");
        }
        balance -= amount;
        System.out.println("Withdrawal successful. Balance: " + balance);
    }
}
public class Main {
    public static void main(String[] args) {
        BankAccount acc = new BankAccount();
        try {
            acc.withdraw(5000);
        } catch (InsufficientBalanceException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```
**Key point:** Extend `Exception` for a **checked** custom exception, or `RuntimeException` for an **unchecked** one. Always call `super(message)` to reuse the base `getMessage()` behaviour.

**Remember (Unit 4 summary):** try = risky code | catch = handle it | finally = always runs | throw = manually raise | throws = declare possibility | Custom exceptions = extend `Exception`/`RuntimeException`.

---

# 🟦 UNIT 5 — Introduction to Multithreading (7 hrs)

## 5.1 Differences: Multiple Processes vs Multiple Threads

| Aspect | Process | Thread |
|---|---|---|
| Definition | An independent running program with its own memory space | A lightweight sub-part of a process, shares memory with other threads of same process |
| Memory | Separate memory area | Shares memory with sibling threads |
| Communication | Slower (Inter-Process Communication needed) | Faster (shared memory) |
| Creation cost | Heavy (more resources) | Light (fewer resources) |
| Example | Running Chrome and VS Code = 2 processes | Chrome downloading a file while rendering a page = 2 threads of same process |

```
Process (e.g. one Java Application/JVM instance)
   ├── Thread 1 (main thread)
   ├── Thread 2
   └── Thread 3
   (all threads share the same memory/heap of the process)
```

**Why Multithreading?** Achieves **parallelism/concurrency** → better CPU utilization, faster execution of independent tasks (e.g., a game rendering graphics while also processing user input).

## 5.2 Creating Threads in Java — 2 Ways

**Way 1: Extending `Thread` class**
```java
class MyThread extends Thread {
    public void run() {                 // run() has the thread's task
        for (int i = 1; i <= 3; i++) {
            System.out.println("MyThread: " + i);
        }
    }
}
public class Main {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        t1.start();          // start() -> creates new thread, calls run() internally
    }
}
```

**Way 2: Implementing `Runnable` interface** (preferred — Java allows only single class inheritance, so this leaves room to extend another class too)
```java
class MyTask implements Runnable {
    public void run() {
        for (int i = 1; i <= 3; i++) {
            System.out.println("MyTask: " + i);
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Thread t1 = new Thread(new MyTask());
        t1.start();
    }
}
```
**Key point:** Always call `start()`, **never call `run()` directly** — calling `run()` directly just executes it like a normal method call on the current thread (no new thread is created).

## 5.3 Thread States (Life Cycle)

```
   NEW ──start()──▶ RUNNABLE ──scheduler──▶ RUNNING
                        ▲                       │
                        │                  wait()/sleep()/blocked
                        │                       ▼
                        └──────notify()───  WAITING / TIMED_WAITING / BLOCKED
                                                 │
                                          run() completes
                                                 ▼
                                            TERMINATED (DEAD)
```

| State | Meaning |
|---|---|
| **New** | Thread object created, `start()` not yet called |
| **Runnable** | Ready to run, waiting for CPU (scheduler decides) |
| **Running** | Currently executing on CPU |
| **Blocked/Waiting** | Waiting for a resource/lock, or waiting due to `wait()`, `join()`, `sleep()` |
| **Terminated (Dead)** | `run()` method has finished executing |

## 5.4 Interrupting Threads

```java
class MyTask extends Thread {
    public void run() {
        try {
            for (int i = 0; i < 5; i++) {
                System.out.println("Working... " + i);
                Thread.sleep(1000);
            }
        } catch (InterruptedException e) {
            System.out.println("Thread was interrupted!");
        }
    }
}
public class Main {
    public static void main(String[] args) throws InterruptedException {
        MyTask t = new MyTask();
        t.start();
        Thread.sleep(2500);
        t.interrupt();     // interrupts the sleeping/waiting thread
    }
}
```
**Key point:** `interrupt()` sets an interrupt flag; if the thread is sleeping/waiting, it throws `InterruptedException` immediately.

## 5.5 Thread Priorities
- Every thread has a priority (int value, 1 to 10) that **hints** the scheduler about importance — not a guarantee.

| Constant | Value |
|---|---|
| `Thread.MIN_PRIORITY` | 1 |
| `Thread.NORM_PRIORITY` | 5 (default) |
| `Thread.MAX_PRIORITY` | 10 |

```java
Thread t1 = new Thread(new MyTask());
t1.setPriority(Thread.MAX_PRIORITY);   // set priority
System.out.println(t1.getPriority());
```

## 5.6 Synchronizing Threads

**Problem:** When multiple threads access **shared data** at the same time, it can cause **data inconsistency** (race condition).

**Solution:** `synchronized` keyword — only **one thread** can execute a synchronized method/block on the same object at a time.

```java
class Counter {
    int count = 0;
    synchronized void increment() {    // synchronized method
        count++;
    }
}
class MyThread extends Thread {
    Counter counter;
    MyThread(Counter c) { this.counter = c; }
    public void run() {
        for (int i = 0; i < 1000; i++) counter.increment();
    }
}
public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();
        MyThread t1 = new MyThread(counter);
        MyThread t2 = new MyThread(counter);
        t1.start(); t2.start();
        t1.join(); t2.join();
        System.out.println("Final count: " + counter.count);   // reliably 2000
    }
}
```
**Hinglish tip:** Bina `synchronized` ke, do threads ek hi variable ko simultaneously modify kar sakte hain aur final result galat aa sakta hai (race condition) — `synchronized` ek "lock" laga deta hai taki ek time pe sirf ek thread hi us block ko execute kare.

## 5.7 Inter-Thread Communication

- Java provides `wait()`, `notify()`, `notifyAll()` (defined in `Object` class) for threads to **communicate/coordinate** with each other, typically used in Producer-Consumer type problems.

```java
class SharedResource {
    synchronized void produce() throws InterruptedException {
        System.out.println("Producing...");
        wait();       // releases lock, waits until notified
        System.out.println("Resumed after notify");
    }
    synchronized void consume() {
        System.out.println("Consuming and notifying...");
        notify();     // wakes up a waiting thread
    }
}
```

| Method | Purpose |
|---|---|
| `wait()` | Current thread releases the lock and waits |
| `notify()` | Wakes up **one** waiting thread |
| `notifyAll()` | Wakes up **all** waiting threads |
| `join()` | Makes calling thread wait until the target thread finishes |
| `sleep(ms)` | Pauses current thread for given milliseconds |

**Remember (Unit 5 summary):** `Thread` class or `Runnable` interface to create threads → `start()` not `run()` → `synchronized` to avoid race conditions → `wait()/notify()` for communication between threads.

---

# 🟦 UNIT 6 — Files, The Collections Framework & Connecting to Database (8 hrs)

## PART A: Files (`java.io`)

### 6.1 Streams — Byte Stream vs Character Stream

```
java.io Streams
├── Byte Streams  (handle raw binary data, 1 byte at a time)
│     ├── InputStream (abstract)  → FileInputStream, BufferedInputStream
│     └── OutputStream (abstract) → FileOutputStream, BufferedOutputStream
└── Character Streams  (handle text/characters, 2 bytes - unicode)
      ├── Reader (abstract)  → FileReader, BufferedReader
      └── Writer (abstract)  → FileWriter, BufferedWriter
```

| Aspect | Byte Stream | Character Stream |
|---|---|---|
| Handles | Raw binary data (images, videos, any file) | Text data (characters) |
| Base classes | `InputStream` / `OutputStream` | `Reader` / `Writer` |
| Unit | 1 byte | 1 character (2 bytes, Unicode-aware) |
| Use case | Non-text files | Text files |

### 6.2 Text Input/Output (Character Streams)

```java
import java.io.*;
public class Main {
    public static void main(String[] args) throws IOException {
        // Writing text
        FileWriter fw = new FileWriter("data.txt");
        fw.write("Hello Java File Handling!");
        fw.close();

        // Reading text
        FileReader fr = new FileReader("data.txt");
        int ch;
        while ((ch = fr.read()) != -1) {
            System.out.print((char) ch);
        }
        fr.close();
    }
}
```

**Better way — using `BufferedReader` (reads line by line, faster):**
```java
BufferedReader br = new BufferedReader(new FileReader("data.txt"));
String line;
while ((line = br.readLine()) != null) {
    System.out.println(line);
}
br.close();
```

### 6.3 Binary Input/Output (Byte Streams)
```java
import java.io.*;
public class Main {
    public static void main(String[] args) throws IOException {
        FileOutputStream fos = new FileOutputStream("data.bin");
        fos.write(65);          // writes byte value 65 -> 'A'
        fos.close();

        FileInputStream fis = new FileInputStream("data.bin");
        int data = fis.read();
        System.out.println((char) data);   // A
        fis.close();
    }
}
```

### 6.4 Random Access File Operations
- `RandomAccessFile` allows both **reading and writing** at **any position** in a file (not just sequentially from start to end) — useful for editing specific parts of large files (like a database file).

```java
import java.io.*;
public class Main {
    public static void main(String[] args) throws IOException {
        RandomAccessFile raf = new RandomAccessFile("data.txt", "rw");
        raf.seek(5);                    // move pointer to position 5
        raf.writeBytes("XYZ");          // overwrite from position 5
        raf.seek(0);
        System.out.println(raf.readLine());
        raf.close();
    }
}
```

### 6.5 File Management with the `File` class
```java
import java.io.File;
public class Main {
    public static void main(String[] args) {
        File f = new File("data.txt");
        System.out.println("Exists: " + f.exists());
        System.out.println("Name: " + f.getName());
        System.out.println("Size (bytes): " + f.length());
        System.out.println("Is Directory: " + f.isDirectory());
        f.delete();       // deletes the file
        new File("newFolder").mkdir();     // creates a directory
    }
}
```
**Key point:** `File` class doesn't read/write content — it's used for **file/folder metadata & management** (check existence, rename, delete, create directories, list files, etc.).

---

## PART B: The Collections Framework (`java.util`)

### 6.6 Collection Framework Overview
- A **Collection** is a group of objects (like a smarter, resizable array).
- The Collections Framework provides **ready-made data structures** (List, Set, Queue, Map) and **algorithms** (sorting, searching) to work with groups of objects, unlike plain arrays which have fixed size.

### 6.7 Hierarchy of the Collection Framework

```
                        Iterable
                            │
                        Collection
        ┌───────────────────┼───────────────────┐
        ▼                   ▼                   ▼
      List                 Set                 Queue
   (ordered,           (no duplicates)      (FIFO order)
   duplicates OK)           │                   │
    │      │           ┌────┼────┐              ├── PriorityQueue
    │      │           ▼         ▼              └── ArrayDeque
 ArrayList LinkedList  HashSet   TreeSet
                          │      (sorted)
                     LinkedHashSet

                (separate hierarchy, NOT part of Collection)
                            Map
                    ┌───────┼───────┐
                    ▼       ▼       ▼
                HashMap  TreeMap  LinkedHashMap
```

**Note:** `Map` is technically **not** a child of `Collection` interface — it's a separate hierarchy (key-value pairs), but it's still part of the overall Collections **Framework**.

### 6.8 Collection Interfaces

| Interface | Description |
|---|---|
| `Collection` | Root interface for List, Set, Queue |
| `List` | Ordered collection, allows duplicates, index-based access |
| `Set` | No duplicates allowed |
| `Queue` | Follows FIFO (First-In-First-Out) order |
| `Map` | Stores key-value pairs, keys are unique |

### 6.9 Collection Classes

**ArrayList** — resizable array, allows duplicates, maintains insertion order, fast random access.
```java
import java.util.*;
ArrayList<String> list = new ArrayList<>();
list.add("Aman"); list.add("Riya"); list.add("Aman");   // duplicate allowed
System.out.println(list);          // [Aman, Riya, Aman]
System.out.println(list.get(0));   // Aman
list.remove("Riya");
```

**LinkedList** — doubly linked list implementation, faster insertion/deletion than ArrayList, implements both `List` and `Deque`.
```java
LinkedList<Integer> ll = new LinkedList<>();
ll.add(10); ll.addFirst(5); ll.addLast(20);
System.out.println(ll);   // [5, 10, 20]
```

**HashSet** — no duplicates, **no guaranteed order**, backed by a hash table (fastest for lookup).
```java
HashSet<String> set = new HashSet<>();
set.add("A"); set.add("B"); set.add("A");   // duplicate ignored
System.out.println(set);      // order not guaranteed, e.g. [A, B]
```

**TreeSet** — no duplicates, elements stored in **sorted (ascending) order**.
```java
TreeSet<Integer> ts = new TreeSet<>();
ts.add(30); ts.add(10); ts.add(20);
System.out.println(ts);     // [10, 20, 30]  (auto-sorted)
```

**PriorityQueue** — elements ordered by priority (natural ordering by default = smallest first).
```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.add(30); pq.add(10); pq.add(20);
System.out.println(pq.poll());   // 10 (smallest priority first)
```

**ArrayDeque** — double-ended queue, can add/remove from **both ends**, faster than `Stack`/`LinkedList` for stack-queue operations.
```java
ArrayDeque<Integer> deque = new ArrayDeque<>();
deque.addFirst(1); deque.addLast(2);
System.out.println(deque);       // [1, 2]
deque.removeFirst();
```

**Quick Comparison Table**
| Class | Duplicates? | Order | Sorted? | Best for |
|---|---|---|---|---|
| ArrayList | Yes | Insertion order | No | Fast access by index |
| LinkedList | Yes | Insertion order | No | Frequent insert/delete |
| HashSet | No | No guarantee | No | Fast unique storage |
| TreeSet | No | Sorted | Yes | Unique + sorted data |
| PriorityQueue | Yes | Priority-based | Yes (by priority) | Task scheduling |
| ArrayDeque | Yes | Insertion order | No | Stack/Queue operations |

**Bonus — HashMap (key-value)**
```java
HashMap<Integer, String> map = new HashMap<>();
map.put(1, "Aman");
map.put(2, "Riya");
System.out.println(map.get(1));       // Aman
for (Map.Entry<Integer, String> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " -> " + entry.getValue());
}
```

**Hinglish tip:** List = order matters, duplicates chalte hain (jaise ek list of tasks). Set = duplicates nahi chahiye (jaise unique roll numbers). Map = key-value pair (jaise ek dictionary, roll number → student name).

---

## PART C: Connecting to a Database (JDBC)

### 6.10 What is JDBC?
**JDBC (Java Database Connectivity)** is an API that allows Java programs to **connect, query, and update relational databases** (MySQL, Oracle, etc.) using SQL.

```
Java Program → JDBC API → JDBC Driver → Database
```

### 6.11 Steps to Connect to a Database

```
1. Load & Register the Driver
2. Establish the Connection
3. Create a Statement
4. Execute the Query
5. Process the ResultSet
6. Close the Connection
```

```java
import java.sql.*;

public class JDBCDemo {
    public static void main(String[] args) {
        try {
            // Step 1: Load driver (auto-loaded in modern JDBC, but good to know)
            Class.forName("com.mysql.cj.jdbc.Driver");

            // Step 2: Establish connection
            Connection con = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/college_db", "root", "password");

            // Step 3: Create statement
            Statement stmt = con.createStatement();

            // Step 4: Execute query
            ResultSet rs = stmt.executeQuery("SELECT * FROM students");

            // Step 5: Process the result set
            while (rs.next()) {
                System.out.println(rs.getInt("id") + " - " + rs.getString("name"));
            }

            // Step 6: Close connection
            con.close();

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### 6.12 Querying and Updating Data with JDBC

**Reading data — `executeQuery()` (for SELECT):**
```java
ResultSet rs = stmt.executeQuery("SELECT * FROM students WHERE marks > 80");
while (rs.next()) {
    System.out.println(rs.getString("name") + " scored " + rs.getInt("marks"));
}
```

**Updating data — `executeUpdate()` (for INSERT / UPDATE / DELETE):**
```java
int rows = stmt.executeUpdate("UPDATE students SET marks = 95 WHERE id = 1");
System.out.println(rows + " row(s) updated");

stmt.executeUpdate("INSERT INTO students (id, name, marks) VALUES (5, 'Kabir', 88)");
stmt.executeUpdate("DELETE FROM students WHERE id = 5");
```

**Using `PreparedStatement`** (safer — prevents SQL Injection, precompiled, faster for repeated queries):
```java
String sql = "INSERT INTO students (id, name, marks) VALUES (?, ?, ?)";
PreparedStatement ps = con.prepareStatement(sql);
ps.setInt(1, 6);
ps.setString(2, "Neha");
ps.setDouble(3, 91.5);
ps.executeUpdate();
```

| Method | Used for | Returns |
|---|---|---|
| `executeQuery()` | `SELECT` statements | `ResultSet` |
| `executeUpdate()` | `INSERT`, `UPDATE`, `DELETE` | `int` (number of rows affected) |
| `execute()` | Any SQL (generic) | `boolean` |

**Hinglish tip:** `Statement` me tum manually string bana ke query likhte ho (SQL injection ka risk hota hai). `PreparedStatement` me `?` placeholders hote hain jo safely values set karte hain — real projects me hamesha `PreparedStatement` use karo.

**Remember (Unit 6 summary):**
- Files → Byte Stream (binary) vs Character Stream (text); `File` class for metadata; `RandomAccessFile` for random position read/write.
- Collections → `List` (ordered, duplicates), `Set` (unique), `Queue` (FIFO/priority), `Map` (key-value).
- JDBC → Load driver → Get Connection → Create Statement → Execute Query → Process ResultSet → Close Connection.

---

# 🟩 FINAL SUMMARY — All 4 OOP Pillars (Quick Revision)

OOPs is built on four main pillars. Together, they help design robust, reusable and maintainable software.

| Pillar | Meaning | Key Points | Example |
|---|---|---|---|
| **1. Encapsulation** | Wrapping data and methods together, hiding internal details | Achieved using `private` variables + public getter/setter | `class Student { private int id; public int getId(){return id;} }` |
| **2. Abstraction** | Hiding implementation details, showing only essential features | Achieved using abstract classes and interfaces | `abstract class Shape { abstract void draw(); }` |
| **3. Inheritance** | Acquiring properties/behaviors of one class into another (IS-A) | `extends` (class) / `implements` (interface); supports overriding | `class Dog extends Animal { }` |
| **4. Polymorphism** | One interface, many forms | Method Overloading (compile-time) + Method Overriding (run-time) | `void sound()` overridden in `Dog` |

**In short:**
- ✅ Encapsulation protects data and restricts access.
- ✅ Abstraction hides details and shows only essential features.
- ✅ Inheritance allows code reusability through IS-A relationship.
- ✅ Polymorphism allows one interface to work with multiple forms.

Together, these four pillars → make code reusable, reduce complexity, improve flexibility, increase security & maintainability.

---

# 🟩 Full Syllabus Coverage Checklist

- [x] Unit 1 — OOP Concepts & Java Programming (History, Buzzwords, JDK/JRE/JVM, data types, operators, control structures, compilation)
- [x] Unit 2 — Objects, Classes & Constructors (Class, Object, Methods, Array of Objects, Constructors, Method Binding, Static, Access Modifiers, `this`, GC, Nested Classes, String class)
- [x] Unit 3 — Inheritance, Interfaces & Packages (Inheritance types, `super`, `final`, Polymorphism, Abstract class, Interface, Encapsulation, Packages, CLASSPATH)
- [x] Unit 4 — Exception Handling (Error vs Exception, hierarchy, try/catch/finally/throw/throws, multiple catch, nested try, re-throw, custom exceptions)
- [x] Unit 5 — Multithreading (Process vs Thread, creating threads, thread states, interrupt, priority, synchronization, inter-thread communication)
- [x] Unit 6 — Files, Collections & JDBC (Streams, File class, RandomAccessFile, Collection hierarchy, List/Set/Queue/Map, JDBC steps, Statement vs PreparedStatement)

**Exam tip:** Har unit ke "Remember" box ko last revision ke time zaroor padhna — wahi 1-liner summary interview/viva me bhi kaam aata hai.

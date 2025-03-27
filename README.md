# CSharpProgramming
Common language stuff a developer should know.

# C# Mastery Guide – Stage 1: C# Fundamentals

Welcome to Stage 1 of mastering C#! This document focuses on the **core fundamentals** of the language, explaining every essential building block. Each section includes:

- ✅ What it is
- ❓ Why it's important
- ⚙️ Syntax and structure
- 🔧 Code examples
- 🔗 Related concepts and commands
- 🧠 Deep insights to truly master the topic

---

## 🟦 1. Variables and Data Types

### ✅ What:
Variables are containers for storing data values. C# is a statically-typed language, which means you must declare a variable’s type before using it.

### ❓ Why:
Understanding variable types ensures you use memory efficiently and avoid type errors at compile-time.

### ⚙️ Syntax:
```csharp
int age = 30;
string name = "Alice";
bool isRegistered = true;
```

### 🔧 Examples:
```csharp
// Numeric types
int year = 2024;
double pi = 3.14159;

// Text
string message = "Hello, World!";

// Boolean
bool isAdult = year > 2000;

// Character
char grade = 'A';
```

### 🔗 Related:
`var`, `const`, `readonly`, `decimal`, `float`, `long`, `byte`

### 🧠 Deep Insight:
Use `decimal` for currency, `float`/`double` for scientific, and `var` only when type is obvious. Behind the scenes, C# uses the CLR (Common Language Runtime) to assign and manage memory for these types.

---

## 🟦 2. Operators and Expressions

### ✅ What:
Operators perform actions on variables and values (e.g., math, logic).

### ❓ Why:
Expressions form the logic of your program, such as conditions and calculations.

### ⚙️ Common Operators:
```csharp
// Arithmetic
+, -, *, /, %

// Comparison
==, !=, >, <, >=, <=

// Logical
&&, ||, !

// Assignment
=, +=, -=, *=, /=
```

### 🔧 Examples:
```csharp
int x = 10, y = 5;
int sum = x + y;        // 15
bool isEqual = x == y;  // false
bool bothTrue = x > 5 && y < 10; // true
```

### 🔗 Related:
`Math` class methods (e.g., `Math.Pow`, `Math.Abs`), ternary operator `?:`

### 🧠 Deep Insight:
All expressions return a value. Even assignment (`=`) is an expression that returns the assigned value.

---

## 🟦 3. Conditionals (`if`, `else`, `switch`)

### ✅ What:
Conditionals let you make decisions in your program based on certain conditions.

### ❓ Why:
Without conditionals, your code would execute linearly. These allow branching logic.

### ⚙️ Syntax:
```csharp
if (condition) { }
else if (anotherCondition) { }
else { }

switch (variable) {
  case value1:
    break;
  default:
    break;
}
```

### 🔧 Examples:
```csharp
int score = 85;

if (score >= 90)
  Console.WriteLine("A grade");
else if (score >= 80)
  Console.WriteLine("B grade");
else
  Console.WriteLine("Needs improvement");

string role = "admin";
switch (role)
{
  case "admin": Console.WriteLine("Welcome Admin"); break;
  case "user": Console.WriteLine("Welcome User"); break;
  default: Console.WriteLine("Unknown"); break;
}
```

### 🔗 Related:
`Ternary operator`, `pattern matching in switch`, `switch expressions`

### 🧠 Deep Insight:
In modern C# (C# 8+), `switch` can return values and support pattern matching, making it more expressive.

---

## 🟦 4. Loops (`for`, `while`, `foreach`, `do-while`)

### ✅ What:
Loops repeat a block of code until a condition is met.

### ❓ Why:
They allow you to automate repetitive tasks like iterating through arrays or collections.

### ⚙️ Syntax:
```csharp
for (int i = 0; i < 5; i++) { }
while (condition) { }
do { } while (condition);
foreach (var item in collection) { }
```

### 🔧 Examples:
```csharp
for (int i = 1; i <= 3; i++)
{
  Console.WriteLine($"Loop {i}");
}

string[] colors = { "Red", "Green", "Blue" };
foreach (var color in colors)
{
  Console.WriteLine(color);
}

int n = 0;
do
{
  Console.WriteLine(n);
  n++;
} while (n < 3);
```

### 🔗 Related:
`break`, `continue`, `return`

### 🧠 Deep Insight:
Use `foreach` when iterating collections. `break` exits loop, `continue` skips to next iteration.

---

## 🟦 5. Methods (Functions in C#)

### ✅ What:
A method is a block of reusable code that performs a specific task.

### ❓ Why:
Avoid repetition and improve readability and modularity.

### ⚙️ Syntax:
```csharp
returnType MethodName(parameters)
{
  // body
}
```

### 🔧 Examples:
```csharp
void Greet(string name)
{
  Console.WriteLine($"Hello, {name}!");
}

int Add(int a, int b)
{
  return a + b;
}

// Calling
Greet("Alice");
int result = Add(5, 3);
```

### 🔗 Related:
`ref`, `out`, `params`, `static`, `local functions`

### 🧠 Deep Insight:
Methods are compiled into IL (Intermediate Language) and JIT compiled at runtime. You can overload them (same name, different parameters).

---

✅ End of Stage 1.

# C# Mastery Guide – Stage 2: Object-Oriented Programming (OOP)

Welcome to Stage 2 of mastering C#! This section introduces the **Object-Oriented Programming** paradigm. C# is built around OOP principles which help you write clean, scalable, and reusable code.

Each topic includes:
- ✅ What it is
- ❓ Why it's important
- ⚙️ Syntax and structure
- 🔧 Code examples
- 🔗 Related concepts and best practices
- 🧠 In-depth understanding

---

## 🟦 1. Classes and Objects

### ✅ What:
A class is a blueprint for creating objects. An object is an instance of a class.

### ❓ Why:
They allow you to encapsulate data and behavior together, making your code modular.

### ⚙️ Syntax:
```csharp
public class Person
{
  public string Name;
  public int Age;

  public void Introduce()
  {
    Console.WriteLine($"Hi, I'm {Name} and I'm {Age} years old.");
  }
}
```

### 🔧 Example:
```csharp
Person p1 = new Person();
p1.Name = "Alice";
p1.Age = 30;
p1.Introduce();
```

### 🔗 Related:
`object`, `new`, `this`, `fields`, `methods`

### 🧠 Deep Insight:
Objects are stored in heap memory and referenced by pointers. Constructors are used to initialize them.

---

## 🟦 2. Constructors

### ✅ What:
Special methods that are called when an object is created.

### ❓ Why:
They help you initialize an object with default or custom values.

### ⚙️ Syntax:
```csharp
public class Car
{
  public string Model;

  public Car(string model)
  {
    Model = model;
  }
}
```

### 🔧 Example:
```csharp
Car myCar = new Car("Tesla Model 3");
Console.WriteLine(myCar.Model);
```

### 🔗 Related:
`constructor overloading`, `default constructors`, `this`, `base`

### 🧠 Deep Insight:
If no constructor is defined, a default one is provided. Constructors can be overloaded for flexibility.

---

## 🟦 3. Inheritance

### ✅ What:
Allows one class to inherit members (fields, methods) from another.

### ❓ Why:
Promotes code reuse and supports polymorphism.

### ⚙️ Syntax:
```csharp
public class Animal
{
  public void Speak() => Console.WriteLine("Animal sound");
}

public class Dog : Animal
{
  public void Bark() => Console.WriteLine("Woof!");
}
```

### 🔧 Example:
```csharp
Dog d = new Dog();
d.Speak(); // Inherited
```

### 🔗 Related:
`base`, `protected`, `virtual`, `override`

### 🧠 Deep Insight:
All classes implicitly inherit from `System.Object`. Access modifiers determine visibility of inherited members.

---

## 🟦 4. Polymorphism

### ✅ What:
The ability of one interface to be used for a general class of actions.

### ❓ Why:
Allows dynamic behavior — method calls behave differently depending on the object type.

### ⚙️ Syntax:
```csharp
public class Animal
{
  public virtual void Speak() => Console.WriteLine("Animal sound");
}

public class Cat : Animal
{
  public override void Speak() => Console.WriteLine("Meow");
}
```

### 🔧 Example:
```csharp
Animal myCat = new Cat();
myCat.Speak(); // Outputs: Meow
```

### 🔗 Related:
`virtual`, `override`, `abstract`, `interface`

### 🧠 Deep Insight:
C# uses runtime binding (via v-tables) for polymorphism. Mark methods `virtual` and use `override` to customize.

---

## 🟦 5. Abstraction

### ✅ What:
Hiding complex logic and exposing only the necessary parts.

### ❓ Why:
Reduces complexity and improves security and maintainability.

### ⚙️ Syntax:
```csharp
public abstract class Shape
{
  public abstract double Area();
}

public class Circle : Shape
{
  public double Radius;
  public Circle(double r) => Radius = r;
  public override double Area() => Math.PI * Radius * Radius;
}
```

### 🔧 Example:
```csharp
Shape s = new Circle(3);
Console.WriteLine(s.Area());
```

### 🔗 Related:
`abstract`, `interface`, `virtual`, `sealed`

### 🧠 Deep Insight:
Abstract classes can't be instantiated. They enforce structure but allow shared logic.

---

## 🟦 6. Encapsulation

### ✅ What:
Restricting direct access to class members using access modifiers and properties.

### ❓ Why:
Protects internal data and keeps object state consistent.

### ⚙️ Syntax:
```csharp
public class BankAccount
{
  private decimal balance;

  public void Deposit(decimal amount)
  {
    if (amount > 0) balance += amount;
  }

  public decimal GetBalance() => balance;
}
```

### 🔧 Example:
```csharp
BankAccount acc = new BankAccount();
acc.Deposit(1000);
Console.WriteLine(acc.GetBalance());
```

### 🔗 Related:
`private`, `protected`, `public`, `properties`, `get/set`

### 🧠 Deep Insight:
Properties (auto-implemented) simplify encapsulation. Use `get; private set;` to allow read-only from outside.

---

## 🟦 7. Interfaces

### ✅ What:
Defines a contract — a set of methods/properties that implementing classes must fulfill.

### ❓ Why:
Supports polymorphism and abstraction. Interfaces decouple code.

### ⚙️ Syntax:
```csharp
public interface ILogger
{
  void Log(string message);
}

public class ConsoleLogger : ILogger
{
  public void Log(string message)
  {
    Console.WriteLine($"[LOG] {message}");
  }
}
```

### 🔧 Example:
```csharp
ILogger logger = new ConsoleLogger();
logger.Log("Hello Interface");
```

### 🔗 Related:
`interface`, `abstract`, `dependency injection`, `mocking`

### 🧠 Deep Insight:
Interfaces are compile-time contracts. Use them with DI (Dependency Injection) for better architecture.

---

✅ End of Stage 2.





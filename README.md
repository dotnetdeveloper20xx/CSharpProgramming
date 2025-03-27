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

# C# Mastery Guide – Stage 3: Advanced C# Concepts

Welcome to Stage 3 of mastering C#! In this stage, we explore the **power tools** of the language that enable expressive, flexible, and high-performance applications. You’ll learn about:
- ✅ Generics
- ✅ Collections
- ✅ Delegates & Events
- ✅ Lambda Expressions
- ✅ LINQ
- ✅ Exception Handling

Each topic includes:
- What, Why, Syntax
- Code Examples
- Internal Understanding
- Related Keywords

---

## 🟦 1. Generics

### ✅ What:
Generics allow you to define type-safe data structures and methods without committing to a specific data type.

### ❓ Why:
Avoid code duplication and increase reusability while ensuring type safety.

### ⚙️ Syntax:
```csharp
public class Box<T>
{
    public T Value;
    public void Display() => Console.WriteLine(Value);
}
```

### 🔧 Examples:
```csharp
Box<int> intBox = new Box<int> { Value = 10 };
Box<string> strBox = new Box<string> { Value = "Hello" };
intBox.Display();
strBox.Display();
```

### 🔗 Related:
`List<T>`, `Dictionary<TKey, TValue>`, `Func<T>`, `Action<T>`, `IEnumerable<T>`

### 🧠 Deep Insight:
The CLR generates IL code at runtime for the specified type when generics are used, ensuring optimal performance without boxing.

---

## 🟦 2. Collections

### ✅ What:
Collections are data structures used to store groups of related objects.

### ❓ Why:
Provide flexibility in storing, retrieving, and managing multiple objects dynamically.

### ⚙️ Common Types:
- `List<T>` – ordered, resizable array
- `Dictionary<TKey, TValue>` – key-value pair store
- `Queue<T>` – FIFO
- `Stack<T>` – LIFO

### 🔧 Examples:
```csharp
List<string> names = new List<string> { "Alice", "Bob" };
names.Add("Charlie");

Dictionary<int, string> users = new Dictionary<int, string>();
users[1] = "Admin";

Queue<int> queue = new Queue<int>();
queue.Enqueue(1);
queue.Enqueue(2);

Stack<int> stack = new Stack<int>();
stack.Push(10);
stack.Push(20);
```

### 🔗 Related:
`ICollection`, `IList`, `IDictionary`, `IEnumerable`

### 🧠 Deep Insight:
Collections under the hood use arrays, hash tables, and linked lists. `List<T>` internally uses a dynamic array that doubles in size when needed.

---

## 🟦 3. Delegates

### ✅ What:
A delegate is a reference to a method with a specific signature.

### ❓ Why:
Allows methods to be passed as parameters (like function pointers).

### ⚙️ Syntax:
```csharp
public delegate void MyDelegate(string message);

public void Greet(string msg) => Console.WriteLine($"Hello {msg}!");

MyDelegate d = Greet;
d("World");
```

### 🔗 Related:
`Func<>`, `Action<>`, `Predicate<>`, `Multicast Delegate`

### 🧠 Deep Insight:
Delegates are objects behind the scenes and support invocation list (multicast). They are type-safe wrappers to method pointers.

---

## 🟦 4. Events

### ✅ What:
Events are special delegates used to signal state changes or notify subscribers.

### ❓ Why:
They allow a publisher-subscriber model (used in GUIs, event-driven systems).

### ⚙️ Syntax:
```csharp
public event EventHandler OnDataReceived;

protected void RaiseEvent()
{
    OnDataReceived?.Invoke(this, EventArgs.Empty);
}
```

### 🔧 Example:
```csharp
class Notifier
{
    public event Action<string> OnNotify;
    public void Trigger(string msg) => OnNotify?.Invoke(msg);
}

Notifier n = new Notifier();
n.OnNotify += (m) => Console.WriteLine($"Received: {m}");
n.Trigger("Hello Events");
```

### 🔗 Related:
`EventHandler<T>`, `+=`, `-=`, `null check`, `multicast`

### 🧠 Deep Insight:
Events encapsulate a delegate field and limit access. You can only invoke from inside the defining class.

---

## 🟦 5. Lambda Expressions

### ✅ What:
Shorthand for defining anonymous functions.

### ❓ Why:
Used heavily with LINQ, delegates, and event subscriptions.

### ⚙️ Syntax:
```csharp
(parameters) => expression_or_block
```

### 🔧 Examples:
```csharp
Func<int, int> square = x => x * x;
Console.WriteLine(square(5)); // 25

Action<string> greet = name => Console.WriteLine($"Hi {name}");
greet("Alice");

Predicate<int> isEven = n => n % 2 == 0;
Console.WriteLine(isEven(4)); // true
```

### 🔗 Related:
`Func<>`, `Action<>`, `Predicate<>`, `LINQ`

### 🧠 Deep Insight:
Lambdas compile to hidden delegate classes or expression trees. They enable functional-style programming.

---

## 🟦 6. LINQ (Language Integrated Query)

### ✅ What:
Query language embedded in C# to manipulate collections, databases, XML, and more.

### ❓ Why:
Powerful and readable syntax for filtering, transforming, and aggregating data.

### ⚙️ Syntax:
```csharp
var result = from x in collection
             where x > 5
             select x;

// or
var result = collection.Where(x => x > 5).Select(x => x);
```

### 🔧 Examples:
```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };
var even = numbers.Where(n => n % 2 == 0);

var names = new[] { "Alice", "Bob", "Charlie" };
var filtered = from n in names where n.StartsWith("A") select n;

var sum = numbers.Sum();
```

### 🔗 Related:
`IEnumerable`, `IQueryable`, `Select`, `Where`, `Aggregate`, `GroupBy`, `Join`

### 🧠 Deep Insight:
LINQ uses deferred execution — the query is only executed when enumerated. `IQueryable` is for LINQ-to-SQL and remote providers.

---

## 🟦 7. Exception Handling

### ✅ What:
A structured mechanism to handle runtime errors.

### ❓ Why:
Ensures your application can gracefully recover or log issues.

### ⚙️ Syntax:
```csharp
try
{
    // code that may throw
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}
finally
{
    // cleanup
}
```

### 🔧 Examples:
```csharp
try
{
    int x = int.Parse("abc");
}
catch (FormatException ex)
{
    Console.WriteLine($"Invalid number: {ex.Message}");
}
finally
{
    Console.WriteLine("Done");
}
```

### 🔗 Related:
`throw`, `try`, `catch`, `finally`, `Exception`, `custom exceptions`

### 🧠 Deep Insight:
Exceptions bubble up the call stack until caught. Avoid using them for flow control. Use `when` filter for targeted exception catching.

---

✅ End of Stage 3.







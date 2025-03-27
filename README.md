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

# C# Mastery Guide – Stage 4: File I/O, JSON/XML, Logging & CLI Apps

Welcome to Stage 4 of mastering C#! This section focuses on **practical application development** features. You’ll learn how to handle files, work with structured data formats, log activity, and build command-line tools.

---

## 🟦 1. File I/O (Reading and Writing Files)

### ✅ What:
Use classes in `System.IO` to read/write data from/to text and binary files.

### ❓ Why:
File handling is crucial for config files, data import/export, logs, etc.

### ⚙️ Syntax:
```csharp
File.WriteAllText("file.txt", "Hello");
string content = File.ReadAllText("file.txt");
```

### 🔧 Examples:
```csharp
// Write lines
string[] lines = { "Line 1", "Line 2" };
File.WriteAllLines("output.txt", lines);

// Read lines
foreach (var line in File.ReadLines("output.txt"))
    Console.WriteLine(line);

// Append
File.AppendAllText("output.txt", "\nAppended");
```

### 🔗 Related:
`StreamReader`, `StreamWriter`, `FileStream`, `Directory`, `Path`

### 🧠 Deep Insight:
Use `using` with `StreamReader`/`StreamWriter` to handle streams safely and prevent file locks.

---

## 🟦 2. JSON Handling (Serialization/Deserialization)

### ✅ What:
Convert between JSON strings and C# objects using `System.Text.Json` or `Newtonsoft.Json`.

### ❓ Why:
JSON is a standard for config, APIs, and inter-process communication.

### ⚙️ Syntax:
```csharp
string json = JsonSerializer.Serialize(obj);
MyClass obj = JsonSerializer.Deserialize<MyClass>(json);
```

### 🔧 Example:
```csharp
public class Person
{
  public string Name { get; set; }
  public int Age { get; set; }
}

Person p = new Person { Name = "Alice", Age = 25 };
string json = JsonSerializer.Serialize(p);
Console.WriteLine(json); // {"Name":"Alice","Age":25}

Person p2 = JsonSerializer.Deserialize<Person>(json);
```

### 🔗 Related:
`System.Text.Json`, `Newtonsoft.Json`, `JsonSerializerOptions`

### 🧠 Deep Insight:
JsonSerializer uses reflection. For high-performance APIs, consider caching or source-generated serializers.

---

## 🟦 3. XML Handling

### ✅ What:
Work with XML using `System.Xml`, `XDocument`, and `XmlSerializer`.

### ❓ Why:
Legacy systems, config files, and many enterprise APIs still use XML.

### ⚙️ Syntax:
```csharp
XDocument doc = XDocument.Load("data.xml");
string name = doc.Root.Element("Name").Value;
```

### 🔧 Example:
```csharp
XElement xml = new XElement("Person",
  new XElement("Name", "Bob"),
  new XElement("Age", 30));
xml.Save("person.xml");

XDocument loaded = XDocument.Load("person.xml");
Console.WriteLine(loaded.Root.Element("Name").Value);
```

### 🔗 Related:
`XElement`, `XmlReader`, `XmlWriter`, `XmlSerializer`

### 🧠 Deep Insight:
LINQ to XML provides an elegant way to traverse and manipulate XML trees with C# syntax.

---

## 🟦 4. Logging (Using Serilog)

### ✅ What:
Logging provides insights during development and production.

### ❓ Why:
Used for debugging, monitoring, error tracking, and auditing.

### ⚙️ Serilog Setup:
```bash
Install-Package Serilog
Install-Package Serilog.Sinks.File
```

### 🔧 Example:
```csharp
using Serilog;

Log.Logger = new LoggerConfiguration()
    .WriteTo.Console()
    .WriteTo.File("app.log", rollingInterval: RollingInterval.Day)
    .CreateLogger();

Log.Information("Application started");
Log.Error("Something went wrong");
```

### 🔗 Related:
`NLog`, `ILogger`, `Microsoft.Extensions.Logging`

### 🧠 Deep Insight:
Use structured logging (`Log.Information("User {User} logged in", userId)`) for better querying.

---

## 🟦 5. Creating a CLI App

### ✅ What:
Build a command-line tool using `Main()` as the entry point.

### ❓ Why:
Used for utilities, scripts, DevOps tools, automation, etc.

### ⚙️ Syntax:
```csharp
static void Main(string[] args)
{
    Console.WriteLine("Hello CLI");
    if (args.Length > 0)
        Console.WriteLine($"Received: {args[0]}");
}
```

### 🔧 Example:
```csharp
// Save this as Program.cs and run:
// dotnet run Hello

static void Main(string[] args)
{
  if (args.Length == 0)
  {
    Console.WriteLine("Usage: mytool <name>");
    return;
  }
  Console.WriteLine($"Hello, {args[0]}!");
}
```

### 🔗 Related:
`Environment`, `Process`, `args`, `CommandLineParser` (NuGet)

### 🧠 Deep Insight:
Use libraries like `System.CommandLine` for complex argument parsing and interactive CLI design.

---

✅ End of Stage 4.

# C# Mastery Guide – Stage 5: Asynchronous and Multithreaded Programming

In Stage 5, we dive into the world of **concurrent programming** in C#. This includes async/await patterns, working with threads and tasks, parallel processing, and cancellation mechanisms.

You will learn how to:
- Build responsive apps with async/await
- Run background operations with `Task`, `Thread`, and `ThreadPool`
- Handle cancellations and exceptions in asynchronous code

---

## 🟦 1. async / await

### ✅ What:
Enables non-blocking operations by using asynchronous methods.

### ❓ Why:
Improves responsiveness and performance in I/O-bound operations like file access, HTTP calls, or database queries.

### ⚙️ Syntax:
```csharp
public async Task MyMethodAsync()
{
    await Task.Delay(1000);
    Console.WriteLine("Done");
}
```

### 🔧 Example:
```csharp
static async Task Main()
{
    Console.WriteLine("Start");
    await Task.Delay(2000);
    Console.WriteLine("Finished");
}
```

### 🔗 Related:
`Task`, `Task<T>`, `ConfigureAwait`, `async void`, `IAsyncEnumerable`

### 🧠 Deep Insight:
Async methods return control to the caller while awaiting I/O. Avoid `async void` unless for event handlers.

---

## 🟦 2. Task and Thread

### ✅ What:
`Task` represents an asynchronous operation. `Thread` represents a physical OS thread.

### ❓ Why:
Use `Task` for most async needs. Use `Thread` only when you need explicit control over thread behavior.

### ⚙️ Syntax:
```csharp
Task.Run(() => Console.WriteLine("Background Task"));

Thread t = new Thread(() => Console.WriteLine("Thread running"));
t.Start();
```

### 🔧 Example:
```csharp
await Task.Run(() =>
{
    for (int i = 0; i < 5; i++)
    {
        Console.WriteLine($"Task loop {i}");
        Thread.Sleep(500);
    }
});
```

### 🔗 Related:
`ThreadPool`, `Thread.Sleep`, `Thread.Join`, `TaskCompletionSource`

### 🧠 Deep Insight:
Prefer `Task.Run` for scalability. `Thread` is heavier and uses more memory.

---

## 🟦 3. Parallel Programming

### ✅ What:
Use multiple CPU cores to speed up data processing.

### ❓ Why:
Improves performance for CPU-bound operations like large loops and batch processing.

### ⚙️ Syntax:
```csharp
Parallel.For(0, 10, i =>
{
    Console.WriteLine(i);
});
```

### 🔧 Example:
```csharp
List<int> numbers = Enumerable.Range(1, 100).ToList();
Parallel.ForEach(numbers, n =>
{
    Console.WriteLine($"Processing {n}");
});
```

### 🔗 Related:
`Parallel.Invoke`, `PLINQ`, `System.Threading.Tasks.Parallel`

### 🧠 Deep Insight:
Use `Parallel` when tasks are independent. Avoid blocking shared resources to prevent race conditions.

---

## 🟦 4. CancellationToken

### ✅ What:
Allows cooperative cancellation between async methods or tasks.

### ❓ Why:
Gives users the ability to cancel long-running or unnecessary tasks safely.

### ⚙️ Syntax:
```csharp
CancellationTokenSource cts = new();
CancellationToken token = cts.Token;

Task t = Task.Run(() =>
{
    while (!token.IsCancellationRequested)
    {
        Console.Write(".");
        Thread.Sleep(500);
    }
}, token);

cts.CancelAfter(3000);
```

### 🔧 Example:
```csharp
public async Task LongOperation(CancellationToken token)
{
    for (int i = 0; i < 10; i++)
    {
        token.ThrowIfCancellationRequested();
        await Task.Delay(500);
        Console.WriteLine(i);
    }
}
```

### 🔗 Related:
`Task.Delay`, `token.ThrowIfCancellationRequested`, `TaskCanceledException`

### 🧠 Deep Insight:
Always pass tokens into cancellable async APIs. Avoid force-aborting threads.

---

## 🟦 5. Exception Handling in Async Code

### ✅ What:
Exceptions in async methods must be awaited to be caught.

### ❓ Why:
Uncaught exceptions in `async void` crash the app.

### ⚙️ Syntax:
```csharp
try
{
    await SomeAsyncMethod();
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}
```

### 🔧 Example:
```csharp
public async Task FailAsync()
{
    await Task.Delay(1000);
    throw new InvalidOperationException("Oops");
}

try
{
    await FailAsync();
}
catch (Exception ex)
{
    Console.WriteLine($"Handled: {ex.Message}");
}
```

### 🔗 Related:
`AggregateException`, `await`, `async Task`, `ConfigureAwait`

### 🧠 Deep Insight:
Use `try/catch` inside or around `await`. `AggregateException` is common when using `Task.WhenAll`.

---

✅ End of Stage 5.

# C# Mastery Guide – Stage 6: .NET Projects – Web APIs, EF Core, Testing, and DI

Welcome to Stage 6! Now that you've mastered core C# concepts, it's time to apply your skills by building **real-world applications** using .NET. This stage will cover:

- ✅ Creating ASP.NET Core Web APIs
- ✅ Using Entity Framework Core (EF Core)
- ✅ Applying Dependency Injection (DI)
- ✅ Writing Unit Tests
- ✅ Using Middleware, Filters, and Logging

---

## 🟦 1. ASP.NET Core Web API Basics

### ✅ What:
Framework for building HTTP-based services using REST principles.

### ❓ Why:
Used for scalable, modular web apps, mobile backends, microservices, and APIs.

### ⚙️ Startup Template:
```bash
dotnet new webapi -n MyApi
cd MyApi
dotnet run
```

### 🔧 Example: Controller
```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    [HttpGet]
    public IActionResult GetAll() => Ok(new[] { "Apple", "Banana" });

    [HttpPost]
    public IActionResult Create(string product) => Created("/api/products/1", product);
}
```

### 🔗 Related:
`[ApiController]`, `IActionResult`, `Model Binding`, `Routing`, `Swagger`

### 🧠 Insight:
Controllers are discovered via conventions. ASP.NET Core supports OpenAPI via Swashbuckle for docs.

---

## 🟦 2. Entity Framework Core (EF Core)

### ✅ What:
Object-relational mapper (ORM) to work with databases using C# objects.

### ❓ Why:
Simplifies CRUD operations, migrations, and relationship handling without raw SQL.

### ⚙️ Setup:
```bash
Install-Package Microsoft.EntityFrameworkCore.SqlServer
Install-Package Microsoft.EntityFrameworkCore.Tools
```

### 🔧 Example:
```csharp
public class AppDbContext : DbContext
{
    public DbSet<Product> Products { get; set; }
    public AppDbContext(DbContextOptions options) : base(options) { }
}

public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

### Program.cs Setup
```csharp
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("Default")));
```

### 🔗 Related:
`DbContext`, `DbSet`, `Migrations`, `LINQ`, `Fluent API`, `Seed Data`

### 🧠 Insight:
EF Core tracks entity states to generate SQL. Use `AsNoTracking()` for read-only queries to boost performance.

---

## 🟦 3. Dependency Injection (DI)

### ✅ What:
Technique to inject dependencies (services) instead of hard-coding them.

### ❓ Why:
Promotes testability, decouples components, and supports SOLID principles.

### ⚙️ Syntax:
```csharp
public interface IMessageService
{
    string Send();
}

public class EmailService : IMessageService
{
    public string Send() => "Email sent";
}
```

### Register in Program.cs
```csharp
builder.Services.AddScoped<IMessageService, EmailService>();
```

### Use in Controller
```csharp
public class NotifyController : ControllerBase
{
    private readonly IMessageService _service;
    public NotifyController(IMessageService service) => _service = service;

    [HttpGet] public string Notify() => _service.Send();
}
```

### 🔗 Related:
`AddScoped`, `AddSingleton`, `AddTransient`, `IServiceCollection`

### 🧠 Insight:
ASP.NET Core has built-in DI. Use `Scoped` for per-request, `Singleton` for app-wide, `Transient` for new instance every time.

---

## 🟦 4. Unit Testing with xUnit

### ✅ What:
xUnit is a testing framework for writing unit tests in .NET.

### ❓ Why:
Ensures your code behaves as expected and supports TDD (Test Driven Development).

### ⚙️ Setup:
```bash
dotnet new xunit -n MyApp.Tests
dotnet add reference ../MyApp/MyApp.csproj
```

### 🔧 Example:
```csharp
public class Calculator
{
    public int Add(int a, int b) => a + b;
}

public class CalculatorTests
{
    [Fact]
    public void Add_ReturnsCorrectSum()
    {
        var calc = new Calculator();
        Assert.Equal(5, calc.Add(2, 3));
    }
}
```

### 🔗 Related:
`[Fact]`, `[Theory]`, `Assert`, `Mock`, `Arrange-Act-Assert`

### 🧠 Insight:
Use mocks for dependencies. Use `[Theory]` for parameterized tests.

---

## 🟦 5. Middleware, Filters & Logging

### ✅ What:
Middleware are components that handle requests/responses. Filters apply logic before/after actions. Logging tracks activity.

### ❓ Why:
Enhances security, monitoring, and request handling.

### 🔧 Example Middleware:
```csharp
app.Use(async (context, next) =>
{
    Console.WriteLine("Request Incoming");
    await next();
    Console.WriteLine("Response Outgoing");
});
```

### 🔧 Action Filter:
```csharp
public class LogActionFilter : IActionFilter
{
    public void OnActionExecuting(ActionExecutingContext context) => Console.WriteLine("Before");
    public void OnActionExecuted(ActionExecutedContext context) => Console.WriteLine("After");
}
```

### Register Filter:
```csharp
services.AddControllers(options =>
{
    options.Filters.Add<LogActionFilter>();
});
```

### 🔧 Built-in Logging:
```csharp
public class MyController : ControllerBase
{
    private readonly ILogger<MyController> _logger;
    public MyController(ILogger<MyController> logger) => _logger = logger;

    [HttpGet] public IActionResult Get() { _logger.LogInformation("Called Get"); return Ok(); }
}
```

### 🔗 Related:
`ILogger`, `IMiddleware`, `IActionFilter`, `UseMiddleware`, `UseRouting`

### 🧠 Insight:
Middleware order matters! Always place exception handling and logging early in the pipeline.

---

✅ End of Stage 6.


# C# Mastery Guide – Stage 7: Clean Architecture, CQRS, SOLID, FluentValidation & Exception Handling

Welcome to Stage 7 – the professional level of C# mastery. Here we apply best practices and architecture patterns for building scalable, maintainable, and testable enterprise-grade .NET applications.

In this stage you'll learn:
- ✅ Clean Architecture Principles
- ✅ CQRS Pattern (Command Query Responsibility Segregation)
- ✅ SOLID Principles in Practice
- ✅ FluentValidation for Model Validation
- ✅ Global Exception Handling Middleware

---

## 🟦 1. Clean Architecture

### ✅ What:
An architecture pattern that separates the system into layers based on responsibility.

### ❓ Why:
Promotes separation of concerns, testability, and maintainability.

### 🧱 Layered Structure:
- **Domain** – Business logic & Entities
- **Application** – Use cases, Interfaces, DTOs
- **Infrastructure** – EF Core, File I/O, APIs
- **Web API** – Controllers, DI, Middleware

### 🔧 Example Project Structure:
```
MyApp
│
├── MyApp.Domain
├── MyApp.Application
├── MyApp.Infrastructure
├── MyApp.WebApi
```

### 🔗 Related:
`Interface segregation`, `Dependency inversion`, `Onion Architecture`

### 🧠 Insight:
Dependencies flow inward. Web API references Infrastructure & Application, but Domain stays isolated.

---

## 🟦 2. CQRS (Command Query Responsibility Segregation)

### ✅ What:
Split reads (queries) from writes (commands) into separate models.

### ❓ Why:
Improves scalability, separates concerns, simplifies complex business logic.

### 🔧 Example:
```csharp
// Command
public record CreateProductCommand(string Name) : IRequest<int>;

public class CreateProductHandler : IRequestHandler<CreateProductCommand, int>
{
    private readonly IAppDbContext _db;
    public CreateProductHandler(IAppDbContext db) => _db = db;

    public async Task<int> Handle(CreateProductCommand request, CancellationToken ct)
    {
        var product = new Product { Name = request.Name };
        _db.Products.Add(product);
        await _db.SaveChangesAsync(ct);
        return product.Id;
    }
}

// Query
public record GetProductByIdQuery(int Id) : IRequest<ProductDto>;

public class GetProductByIdHandler : IRequestHandler<GetProductByIdQuery, ProductDto>
{
    private readonly IAppDbContext _db;
    public GetProductByIdHandler(IAppDbContext db) => _db = db;

    public async Task<ProductDto> Handle(GetProductByIdQuery request, CancellationToken ct)
    {
        var product = await _db.Products.FindAsync(request.Id);
        return new ProductDto(product.Id, product.Name);
    }
}
```

### 🔗 Related:
`MediatR`, `IRequest`, `CommandHandler`, `QueryHandler`

### 🧠 Insight:
CQRS is great with MediatR and Clean Architecture. Apply cautiously when your app benefits from separation of read/write responsibilities.

---

## 🟦 3. SOLID Principles

### ✅ What:
A set of five principles to write better, cleaner, scalable object-oriented code.

### ❓ Why:
Improves design quality, reduces bugs, and supports maintainability.

### 🛠 Breakdown:
- **S** – Single Responsibility Principle (1 class = 1 purpose)
- **O** – Open/Closed Principle (open for extension, closed for modification)
- **L** – Liskov Substitution (subtypes should replace base types)
- **I** – Interface Segregation (prefer many specific interfaces)
- **D** – Dependency Inversion (depend on abstractions)

### 🔧 Example: SRP & DIP
```csharp
// BAD
public class InvoiceService
{
    public void SaveToDb() { }
    public void EmailInvoice() { }
}

// GOOD – SRP
public class InvoiceRepository { public void Save() { } }
public class EmailService { public void Send() { } }

// GOOD – DIP
public interface INotifier { void Notify(); }
public class EmailNotifier : INotifier { public void Notify() { } }
```

### 🔗 Related:
`IoC`, `Interfaces`, `DI Container`, `Abstraction`

### 🧠 Insight:
Use SOLID to decouple logic, reduce side effects, and write testable, clean code.

---

## 🟦 4. FluentValidation

### ✅ What:
A powerful validation library to validate models cleanly and declaratively.

### ❓ Why:
Avoids cluttering models or controllers with complex if-else checks.

### ⚙️ Install:
```bash
Install-Package FluentValidation.AspNetCore
```

### 🔧 Example:
```csharp
public class ProductDto
{
    public string Name { get; set; }
}

public class ProductValidator : AbstractValidator<ProductDto>
{
    public ProductValidator()
    {
        RuleFor(x => x.Name)
            .NotEmpty().WithMessage("Name is required")
            .MaximumLength(50);
    }
}
```

### Register in Program.cs
```csharp
builder.Services.AddFluentValidationAutoValidation()
                .AddValidatorsFromAssemblyContaining<ProductValidator>();
```

### 🔗 Related:
`RuleFor`, `Must`, `Custom`, `CascadeMode`

### 🧠 Insight:
Use `RuleSets` for conditional logic. Validation happens automatically via filters.

---

## 🟦 5. Global Exception Handling Middleware

### ✅ What:
Middleware that handles all unhandled exceptions and returns standardized error responses.

### ❓ Why:
Improves reliability, consistency, and security in error handling.

### 🔧 Example:
```csharp
public class ExceptionMiddleware : IMiddleware
{
    private readonly ILogger<ExceptionMiddleware> _logger;

    public ExceptionMiddleware(ILogger<ExceptionMiddleware> logger)
    {
        _logger = logger;
    }

    public async Task InvokeAsync(HttpContext context, RequestDelegate next)
    {
        try
        {
            await next(context);
        }
        catch (Exception ex)
        {
            _logger.LogError(ex, "Unhandled Exception");
            context.Response.StatusCode = 500;
            await context.Response.WriteAsJsonAsync(new { error = "Something went wrong" });
        }
    }
}
```

### Register Middleware
```csharp
builder.Services.AddTransient<ExceptionMiddleware>();
app.UseMiddleware<ExceptionMiddleware>();
```

### 🔗 Related:
`UseMiddleware`, `ILogger`, `ProblemDetails`, `ExceptionHandler`

### 🧠 Insight:
This is the central place to log and return error responses. Use it alongside HTTP Problem Details (RFC 7807).

---

✅ End of Stage 7.


# 🏗️ Full Clean Architecture Web API Project Using Stages 1–7

This document provides a full implementation guide to build a Clean Architecture-based ASP.NET Core Web API using everything you've learned from Stages 1–7. It combines:

- C# Fundamentals ✅
- OOP & Advanced Concepts ✅
- Async, Logging, JSON/XML ✅
- ASP.NET Core Web API ✅
- EF Core ✅
- CQRS with MediatR ✅
- FluentValidation ✅
- Global Exception Handling ✅
- SOLID, Clean Architecture, and Testing ✅

---

## ✅ Project Structure
```
MyApp
├── MyApp.Domain              → Entities only
├── MyApp.Application         → CQRS (Commands + Queries), DTOs, Interfaces
├── MyApp.Infrastructure      → EF Core, I/O logic, Services
├── MyApp.WebAPI              → Controllers, Middleware, Program.cs
├── MyApp.Tests               → Unit tests (xUnit + Moq)
```

---

## 1️⃣ Domain Layer – `MyApp.Domain`
```csharp
namespace MyApp.Domain.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
    }
}
```

---

## 2️⃣ Application Layer – `MyApp.Application`

### DTO
```csharp
public class ProductDto
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

### Command + Handler (CQRS)
```csharp
public record CreateProductCommand(string Name) : IRequest<int>;

public class CreateProductHandler : IRequestHandler<CreateProductCommand, int>
{
    private readonly IAppDbContext _context;
    public CreateProductHandler(IAppDbContext context) => _context = context;

    public async Task<int> Handle(CreateProductCommand request, CancellationToken ct)
    {
        var entity = new Product { Name = request.Name };
        _context.Products.Add(entity);
        await _context.SaveChangesAsync(ct);
        return entity.Id;
    }
}
```

### Query + Handler
```csharp
public record GetProductByIdQuery(int Id) : IRequest<ProductDto>;

public class GetProductByIdHandler : IRequestHandler<GetProductByIdQuery, ProductDto>
{
    private readonly IAppDbContext _context;
    public GetProductByIdHandler(IAppDbContext context) => _context = context;

    public async Task<ProductDto> Handle(GetProductByIdQuery request, CancellationToken ct)
    {
        var entity = await _context.Products.FindAsync(request.Id);
        return new ProductDto { Id = entity.Id, Name = entity.Name };
    }
}
```

### Validation (FluentValidation)
```csharp
public class ProductValidator : AbstractValidator<CreateProductCommand>
{
    public ProductValidator()
    {
        RuleFor(x => x.Name)
            .NotEmpty().WithMessage("Name is required")
            .MaximumLength(50);
    }
}
```

---

## 3️⃣ Infrastructure Layer – `MyApp.Infrastructure`
```csharp
public interface IAppDbContext
{
    DbSet<Product> Products { get; }
    Task<int> SaveChangesAsync(CancellationToken ct);
}

public class AppDbContext : DbContext, IAppDbContext
{
    public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }
    public DbSet<Product> Products => Set<Product>();
    public async Task<int> SaveChangesAsync(CancellationToken ct) => await base.SaveChangesAsync(ct);
}
```

---

## 4️⃣ Web API Layer – `MyApp.WebAPI`

### Controller
```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    private readonly IMediator _mediator;
    public ProductsController(IMediator mediator) => _mediator = mediator;

    [HttpGet("{id}")]
    public async Task<IActionResult> Get(int id) => Ok(await _mediator.Send(new GetProductByIdQuery(id)));

    [HttpPost]
    public async Task<IActionResult> Post(CreateProductCommand cmd) => Ok(await _mediator.Send(cmd));
}
```

### Global Exception Middleware
```csharp
public class ExceptionMiddleware : IMiddleware
{
    private readonly ILogger<ExceptionMiddleware> _logger;
    public ExceptionMiddleware(ILogger<ExceptionMiddleware> logger) => _logger = logger;

    public async Task InvokeAsync(HttpContext context, RequestDelegate next)
    {
        try { await next(context); }
        catch (Exception ex)
        {
            _logger.LogError(ex, "Unhandled error");
            context.Response.StatusCode = 500;
            await context.Response.WriteAsJsonAsync(new { error = ex.Message });
        }
    }
}
```

### Program.cs
```csharp
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddControllers();
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();

builder.Services.AddDbContext<AppDbContext>(o => o.UseInMemoryDatabase("MyDb"));
builder.Services.AddScoped<IAppDbContext>(provider => provider.GetRequiredService<AppDbContext>());
builder.Services.AddMediatR(typeof(CreateProductCommand).Assembly);
builder.Services.AddFluentValidationAutoValidation();
builder.Services.AddValidatorsFromAssemblyContaining<ProductValidator>();
builder.Services.AddTransient<ExceptionMiddleware>();

var app = builder.Build();

app.UseSwagger();
app.UseSwaggerUI();
app.UseMiddleware<ExceptionMiddleware>();
app.UseAuthorization();
app.MapControllers();
app.Run();
```

---

## 5️⃣ Testing Layer – `MyApp.Tests`

### Unit Test Example
```csharp
public class CreateProductHandlerTests
{
    [Fact]
    public async Task Should_Save_Product()
    {
        var mockDb = new Mock<IAppDbContext>();
        var mockSet = new Mock<DbSet<Product>>();

        mockDb.Setup(x => x.Products).Returns(mockSet.Object);
        var handler = new CreateProductHandler(mockDb.Object);

        var result = await handler.Handle(new CreateProductCommand("Test"), CancellationToken.None);
        Assert.True(result >= 0);
    }
}
```

---

# 🏗️ Full Clean Architecture Web API Project Using Stages 1–7 + Advanced Topics

This document provides a full implementation guide to build a Clean Architecture-based ASP.NET Core Web API using everything from beginner to advanced topics. It includes:

- C# Fundamentals ✅
- OOP & Advanced Concepts ✅
- Async, Logging, JSON/XML ✅
- ASP.NET Core Web API ✅
- EF Core ✅
- CQRS with MediatR ✅
- FluentValidation ✅
- Global Exception Handling ✅
- SOLID, Clean Architecture, and Testing ✅
- Advanced Topics (below) 🔥

---

## 🚀 Advanced Topics for Senior Developers

### ✅ Advanced EF Core Techniques
- Use `AsNoTracking()` for performance
- Apply `Query Filters` at the DbContext level
- Use `ValueConverters` for encrypted or formatted fields

### ✅ Entity Configuration with Fluent API
```csharp
protected override void OnModelCreating(ModelBuilder modelBuilder)
{
    modelBuilder.Entity<Product>().HasIndex(p => p.Name).IsUnique();
    modelBuilder.Entity<Product>().Property(p => p.Name).HasMaxLength(100);
}
```

### ✅ Use of Async Streams
```csharp
public async IAsyncEnumerable<Product> GetAllAsync()
{
    await foreach (var product in _context.Products.AsAsyncEnumerable())
        yield return product;
}
```

### ✅ Global Response Wrapping (Standard API Result)
```csharp
public class ApiResponse<T>
{
    public bool Success { get; set; }
    public string Message { get; set; }
    public T Data { get; set; }
}

// Controller usage
return Ok(new ApiResponse<ProductDto> { Success = true, Data = product });
```

### ✅ Versioning the API
```csharp
builder.Services.AddApiVersioning(opt =>
{
    opt.DefaultApiVersion = new ApiVersion(1, 0);
    opt.AssumeDefaultVersionWhenUnspecified = true;
    opt.ReportApiVersions = true;
});
```

### ✅ Automapper Integration
```csharp
public class MappingProfile : Profile
{
    public MappingProfile()
    {
        CreateMap<Product, ProductDto>();
        CreateMap<CreateProductCommand, Product>();
    }
}
```
```csharp
builder.Services.AddAutoMapper(typeof(MappingProfile));
```

### ✅ Authentication and Authorization (JWT)
```csharp
builder.Services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(opt =>
    {
        opt.TokenValidationParameters = new TokenValidationParameters
        {
            ValidateIssuer = true,
            ValidateAudience = true,
            ValidateLifetime = true,
            ValidateIssuerSigningKey = true,
            ValidIssuer = "yourapp",
            ValidAudience = "yourapp",
            IssuerSigningKey = new SymmetricSecurityKey(Encoding.UTF8.GetBytes("yourSecretKey"))
        };
    });
```

### ✅ Caching (MemoryCache)
```csharp
builder.Services.AddMemoryCache();

// In Controller or Service
var cached = _cache.GetOrCreate("product_list", entry =>
{
    entry.AbsoluteExpirationRelativeToNow = TimeSpan.FromMinutes(5);
    return _context.Products.ToList();
});
```

### ✅ Background Jobs (Hosted Services)
```csharp
public class CleanupService : BackgroundService
{
    protected override async Task ExecuteAsync(CancellationToken stoppingToken)
    {
        while (!stoppingToken.IsCancellationRequested)
        {
            Console.WriteLine("Running background job...");
            await Task.Delay(TimeSpan.FromMinutes(10));
        }
    }
}

builder.Services.AddHostedService<CleanupService>();
```

---

# 📁 Clean Architecture Project Folder Structure + 🧪 Interview Challenges

This document outlines a production-ready folder/file structure for a full Clean Architecture Web API application using .NET 7+, plus senior-level interview questions based on each module and concept.

---

## 📂 Project Folder Layout
```
MyApp
│
├── MyApp.Domain
│   └── Entities
│       └── Product.cs
│
├── MyApp.Application
│   ├── DTOs
│   │   └── ProductDto.cs
│   ├── Interfaces
│   │   └── IAppDbContext.cs
│   ├── Commands
│   │   └── CreateProductCommand.cs
│   ├── Queries
│   │   └── GetProductByIdQuery.cs
│   └── Validators
│       └── ProductValidator.cs
│
├── MyApp.Infrastructure
│   ├── Persistence
│   │   └── AppDbContext.cs
│   └── Services
│       └── JwtTokenService.cs (optional)
│
├── MyApp.WebAPI
│   ├── Controllers
│   │   └── ProductsController.cs
│   ├── Middleware
│   │   └── ExceptionMiddleware.cs
│   ├── Program.cs
│   └── appsettings.json
│
├── MyApp.Tests
│   └── Application
│       └── Handlers
│           └── CreateProductHandlerTests.cs
│
└── MyApp.sln
```

---

## 🧪 Senior-Level Interview Challenges by Module

### 🔹 Clean Architecture
**Q:** Explain the dependency flow in Clean Architecture. Why should the Domain project have no dependencies?
**Q:** How would you structure a feature module that interacts with external APIs while preserving Clean Architecture?

### 🔹 CQRS & MediatR
**Q:** What are the benefits of separating Commands and Queries in a complex domain?
**Q:** How would you handle validation and authorization inside a MediatR pipeline?

### 🔹 EF Core & Fluent API
**Q:** How do you enforce multi-field uniqueness in EF Core without annotations?
**Q:** What is the purpose of `AsNoTracking()`? When should it be used?

### 🔹 FluentValidation
**Q:** How would you write a validator for a nested object or collection?
**Q:** What are the benefits of using FluentValidation over manual model validation?

### 🔹 Exception Middleware
**Q:** How do you log exceptions globally while keeping your API secure?
**Q:** How would you structure your middleware to return RFC7807 ProblemDetails responses?

### 🔹 AutoMapper
**Q:** How can you configure conditional mapping in AutoMapper?
**Q:** How do you map between two deeply nested object trees?

### 🔹 JWT Authentication
**Q:** How do you secure a multi-tenant API using JWT claims?
**Q:** How would you handle token expiration and refresh securely?

### 🔹 Caching
**Q:** How would you use MemoryCache with expiration policies?
**Q:** When should you prefer distributed caching (like Redis) over in-memory caching?

### 🔹 Background Jobs
**Q:** When would you use `IHostedService` vs. a message queue background worker?
**Q:** How can you safely retry failed background jobs?

### 🔹 Testing (xUnit + Moq)
**Q:** How do you mock DbSet in EF Core for testing?
**Q:** How do you test async exception scenarios?

---

# 📦 Full .NET Solution with Ready-to-Run Files + 🧱 Swagger, JWT Auth, Docker Setup

This guide helps you bootstrap a full Clean Architecture Web API project with:
- ✅ Working .NET 7+ Solution
- ✅ Swagger UI
- 🔐 JWT Role-based Authentication
- 🐳 Docker Support

---

## ✅ Step-by-Step Project Bootstrap (CLI)
```bash
dotnet new sln -n MyApp

# Create projects
cd MyApp

dotnet new classlib -n MyApp.Domain

dotnet new classlib -n MyApp.Application

dotnet new classlib -n MyApp.Infrastructure

dotnet new webapi -n MyApp.WebAPI

dotnet new xunit -n MyApp.Tests

# Add to solution
dotnet sln add MyApp.Domain/MyApp.Domain.csproj

dotnet sln add MyApp.Application/MyApp.Application.csproj

dotnet sln add MyApp.Infrastructure/MyApp.Infrastructure.csproj

dotnet sln add MyApp.WebAPI/MyApp.WebAPI.csproj

dotnet sln add MyApp.Tests/MyApp.Tests.csproj

# Add references
cd MyApp.Application

dotnet add reference ../MyApp.Domain/MyApp.Domain.csproj

cd ../MyApp.Infrastructure

dotnet add reference ../MyApp.Application/MyApp.Application.csproj

dotnet add reference ../MyApp.Domain/MyApp.Domain.csproj

cd ../MyApp.WebAPI

dotnet add reference ../MyApp.Application/MyApp.Application.csproj

dotnet add reference ../MyApp.Infrastructure/MyApp.Infrastructure.csproj
```

---

## 🔍 Install Essential Packages
```bash
# CQRS
Install-Package MediatR.Extensions.Microsoft.DependencyInjection

# FluentValidation
Install-Package FluentValidation.AspNetCore

# EF Core
Install-Package Microsoft.EntityFrameworkCore
Install-Package Microsoft.EntityFrameworkCore.InMemory

# JWT Auth
Install-Package Microsoft.AspNetCore.Authentication.JwtBearer

# Swagger
Install-Package Swashbuckle.AspNetCore
```

---

## 🧱 Swagger Configuration
In `Program.cs` of `MyApp.WebAPI`:
```csharp
builder.Services.AddSwaggerGen(opt =>
{
    opt.SwaggerDoc("v1", new() { Title = "MyApp API", Version = "v1" });
    opt.AddSecurityDefinition("Bearer", new OpenApiSecurityScheme
    {
        Name = "Authorization",
        Type = SecuritySchemeType.Http,
        Scheme = "Bearer",
        BearerFormat = "JWT",
        In = ParameterLocation.Header,
        Description = "JWT Authorization header using the Bearer scheme."
    });
    opt.AddSecurityRequirement(new OpenApiSecurityRequirement {
        {
            new OpenApiSecurityScheme {
                Reference = new OpenApiReference {
                    Type = ReferenceType.SecurityScheme,
                    Id = "Bearer"
                }
            },
            new string[] {}
        }
    });
});
```

---

## 🔐 JWT Role-Based Auth (Configure in `Program.cs`)
```csharp
builder.Services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(options =>
    {
        options.TokenValidationParameters = new TokenValidationParameters
        {
            ValidateIssuer = true,
            ValidateAudience = true,
            ValidateLifetime = true,
            ValidateIssuerSigningKey = true,
            ValidIssuer = "MyApp",
            ValidAudience = "MyApp",
            IssuerSigningKey = new SymmetricSecurityKey(Encoding.UTF8.GetBytes("MySuperSecretKey"))
        };
    });
```

Use roles in controller:
```csharp
[Authorize(Roles = "Admin")]
[HttpPost("admin-only")]
public IActionResult AdminOnlyEndpoint() => Ok("Welcome Admin");
```

---

## 🐳 Dockerfile
In `MyApp.WebAPI`:
```Dockerfile
FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base
WORKDIR /app
EXPOSE 80

FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /src
COPY ["MyApp.WebAPI/MyApp.WebAPI.csproj", "MyApp.WebAPI/"]
COPY ["MyApp.Application/MyApp.Application.csproj", "MyApp.Application/"]
COPY ["MyApp.Infrastructure/MyApp.Infrastructure.csproj", "MyApp.Infrastructure/"]
COPY ["MyApp.Domain/MyApp.Domain.csproj", "MyApp.Domain/"]
RUN dotnet restore "MyApp.WebAPI/MyApp.WebAPI.csproj"
COPY . .
WORKDIR "/src/MyApp.WebAPI"
RUN dotnet build "MyApp.WebAPI.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "MyApp.WebAPI.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "MyApp.WebAPI.dll"]
```

---
# 📦 Full .NET Solution with Ready-to-Run Files + 🧱 Swagger, JWT Auth, Docker Setup + 🧪 Postman & CI/CD

This guide helps you bootstrap a full Clean Architecture Web API project with:
- ✅ Working .NET 7+ Solution
- ✅ Swagger UI
- 🔐 JWT Role-based Authentication
- 🐳 Docker Support
- 🧪 Postman API Testing
- 🚀 GitHub Actions CI/CD

---

## ✅ Step-by-Step Project Bootstrap (CLI)
(unchanged...)

---

## 🧪 Postman Collection (Testing)

Create a `MyApp.postman_collection.json` with the following sample structure:
```json
{
  "info": {
    "name": "MyApp API",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
  },
  "item": [
    {
      "name": "Create Product",
      "request": {
        "method": "POST",
        "header": [
          {
            "key": "Authorization",
            "value": "Bearer {{token}}",
            "type": "text"
          }
        ],
        "url": {
          "raw": "{{baseUrl}}/api/products",
          "host": ["{{baseUrl}}"],
          "path": ["api", "products"]
        },
        "body": {
          "mode": "raw",
          "raw": "{\"name\": \"Test Product\"}"
        }
      }
    }
  ]
}
```

Export this file with the repo or use in your API documentation.

---

## 🧪 E2E Test Scaffold (Example)
```csharp
public class ProductsApiTests : IClassFixture<WebApplicationFactory<Program>>
{
    private readonly HttpClient _client;
    public ProductsApiTests(WebApplicationFactory<Program> factory)
    {
        _client = factory.CreateClient();
    }

    [Fact]
    public async Task Should_Return_Created_Product()
    {
        var response = await _client.PostAsJsonAsync("/api/products", new { name = "e2e test" });
        response.EnsureSuccessStatusCode();
        var result = await response.Content.ReadAsStringAsync();
        Assert.Contains("e2e test", result);
    }
}
```

Add this to your `MyApp.Tests` project.

---

## 🚀 GitHub Actions CI/CD Pipeline (YAML)
`.github/workflows/dotnet.yml`
```yaml
name: Build & Deploy ASP.NET Core API

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Setup .NET
        uses: actions/setup-dotnet@v3
        with:
          dotnet-version: '7.0.x'

      - name: Restore dependencies
        run: dotnet restore MyApp.sln

      - name: Build
        run: dotnet build MyApp.sln --no-restore --configuration Release

      - name: Test
        run: dotnet test MyApp.Tests --no-build --verbosity normal

      - name: Publish
        run: dotnet publish MyApp.WebAPI/MyApp.WebAPI.csproj -c Release -o release

      - name: Upload Artifacts
        uses: actions/upload-artifact@v3
        with:
          name: webapi
          path: release
```

---

# 📦 Full .NET Solution with Ready-to-Run Files + 🧱 Swagger, JWT Auth, Docker Setup + 🧪 Postman & CI/CD + ☁️ Azure Deploy & 🔐 Role-Secured Swagger

This guide helps you bootstrap a full Clean Architecture Web API project with:
- ✅ Working .NET 7+ Solution
- ✅ Swagger UI with JWT Role Support
- 🔐 JWT Role-based Authentication
- 🐳 Docker Support
- 🧪 Postman API Testing + E2E
- 🚀 GitHub Actions CI/CD
- ☁️ Azure Web App Deployment

---

## ☁️ Azure App Service Deployment via GitHub Actions
`.github/workflows/azure-deploy.yml`
```yaml
name: Azure Web App CI/CD

on:
  push:
    branches:
      - main

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Setup .NET
        uses: actions/setup-dotnet@v3
        with:
          dotnet-version: '7.0.x'

      - name: Restore
        run: dotnet restore MyApp.sln

      - name: Build
        run: dotnet build MyApp.sln --no-restore

      - name: Test
        run: dotnet test MyApp.Tests --no-build

      - name: Publish WebAPI
        run: dotnet publish MyApp.WebAPI/MyApp.WebAPI.csproj -c Release -o publish

      - name: Deploy to Azure
        uses: azure/webapps-deploy@v2
        with:
          app-name: YOUR_APP_NAME_HERE
          slot-name: production
          publish-profile: ${{ secrets.AZURE_WEBAPP_PUBLISH_PROFILE }}
          package: ./publish
```

To use:
1. Go to Azure > Web App > Deployment Center > Get publish profile
2. Add to GitHub repo secrets as `AZURE_WEBAPP_PUBLISH_PROFILE`

---

## 🔐 Enable JWT Support in Swagger UI
In `Program.cs` (after `AddSwaggerGen`):
```csharp
builder.Services.AddSwaggerGen(opt =>
{
    opt.SwaggerDoc("v1", new() { Title = "MyApp API", Version = "v1" });
    opt.AddSecurityDefinition("Bearer", new OpenApiSecurityScheme
    {
        Name = "Authorization",
        Type = SecuritySchemeType.Http,
        Scheme = "Bearer",
        BearerFormat = "JWT",
        In = ParameterLocation.Header,
        Description = "Enter a valid JWT token. Format: Bearer {token}"
    });
    opt.AddSecurityRequirement(new OpenApiSecurityRequirement
    {
        {
            new OpenApiSecurityScheme
            {
                Reference = new OpenApiReference { Type = ReferenceType.SecurityScheme, Id = "Bearer" }
            },
            Array.Empty<string>()
        }
    });
});
```

Use `[Authorize(Roles = "Admin")]` in controllers to restrict endpoint access.

---

## ✅ Final Project Checklist
- ✅ Swagger with secure token input
- ✅ Role-based endpoint visibility
- ✅ Postman + E2E test coverage
- ✅ GitHub Actions CI/CD with Azure push
- ✅ Docker build file ready

# 📦 Clean Architecture Web API – Full Solution + 🔐 Auth + ☁️ Azure + 🧬 Multi-Tenant + Feature Flags

This extended guide adds enterprise-grade features to your solution:
- ✅ ASP.NET Core Identity integration
- 🔐 IdentityServer support
- 🧬 Multi-tenant strategy
- 🎛️ Feature flag toggles using config or LaunchDarkly

---

## 🔐 ASP.NET Core Identity Integration

### 📦 Install Identity
```bash
Install-Package Microsoft.AspNetCore.Identity.EntityFrameworkCore
```

### 🧱 Identity Models
```csharp
public class ApplicationUser : IdentityUser {}
public class ApplicationRole : IdentityRole {}
```

### 🏗️ Modify DbContext
```csharp
public class AppDbContext : IdentityDbContext<ApplicationUser, ApplicationRole, string>, IAppDbContext
{
    public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) {}
    public DbSet<Product> Products => Set<Product>();
}
```

### 🔌 Program.cs Setup
```csharp
builder.Services.AddIdentity<ApplicationUser, ApplicationRole>()
    .AddEntityFrameworkStores<AppDbContext>()
    .AddDefaultTokenProviders();
```

---

## 🔐 IdentityServer Setup

### 📦 Install Packages
```bash
Install-Package Duende.IdentityServer.AspNetIdentity
Install-Package Duende.IdentityServer.EntityFramework
```

> Note: IdentityServer is a commercial offering from Duende Software as of .NET 6+

Configure clients, scopes, users, and resources via `Config.cs`. Run it as a separate Identity Server project (e.g., `MyApp.Identity`).

Use token issuance from IdentityServer and validate JWT in your API with:
```csharp
builder.Services.AddAuthentication("Bearer")
    .AddJwtBearer("Bearer", options =>
    {
        options.Authority = "https://localhost:5001";
        options.TokenValidationParameters = new TokenValidationParameters
        {
            ValidateAudience = false
        };
    });
```

---

## 🧬 Multi-Tenant Support (Basic Strategy)

### 📦 Tenant Middleware
```csharp
public class TenantMiddleware : IMiddleware
{
    public async Task InvokeAsync(HttpContext context, RequestDelegate next)
    {
        var tenantId = context.Request.Headers["X-Tenant-ID"].FirstOrDefault();
        context.Items["TenantId"] = tenantId ?? "default";
        await next(context);
    }
}
```

### 🛠 Register Middleware
```csharp
builder.Services.AddTransient<TenantMiddleware>();
app.UseMiddleware<TenantMiddleware>();
```

### 🧠 Access Tenant in Service
```csharp
var tenantId = httpContextAccessor.HttpContext?.Items["TenantId"]?.ToString();
```

---

## 🎛️ Feature Flag Toggle (Using `IConfiguration`)

### 📁 appsettings.json
```json
{
  "Features": {
    "EnableBetaFeature": true
  }
}
```

### 🧪 Feature Check
```csharp
if (_config.GetValue<bool>("Features:EnableBetaFeature"))
{
    // Run beta logic
}
```

### 🎯 Optional: LaunchDarkly/Feature Management
```bash
Install-Package Microsoft.FeatureManagement
```
```csharp
services.AddFeatureManagement();
```
```csharp
if (await featureManager.IsEnabledAsync("EnableBetaFeature"))
{
    // Feature gated code
}
```

---

## ✅ Summary
- 🔐 ASP.NET Core Identity + IdentityServer for enterprise auth
- 🧬 Multi-tenant ready via custom header and DI
- 🎛️ Feature flags via config or LaunchDarkly
















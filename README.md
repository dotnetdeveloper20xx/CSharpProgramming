**Mastering C# with a Project: ShopRight – Enterprise E-Commerce Application**

---

**Objective:**
Build a full-scale, real-world **enterprise-level e-commerce application** called **ShopRight**, while learning and mastering **every C# concept, keyword, and feature** from beginner to advanced level.

**Approach:**
Each phase introduces C# concepts in-depth with:
1. **What** – Definition in plain English
2. **Why** – Real-world relevance
3. **How** – Implementation and code examples
4. **Where** – Application inside the ShopRight system

---

## ✅ PHASE 1: C# LANGUAGE FUNDAMENTALS – Console App + Syntax
### 🎯 Goal: Understand how a C# program works, basic syntax, and app interaction

| Concept | C# Keywords / Features | Use in ShopRight |
|--------|--------------------------|------------------|
| Entry Point | `Main()`, `args`, `static`, `void` | CLI tool for admin functions |
| Console I/O | `Console.WriteLine`, `Console.ReadLine`, `$""` | Input user/product info |
| Data Types | `string`, `int`, `bool`, `char`, `decimal`, `var` | Product, Price, Quantity |
| Operators | `+`, `-`, `*`, `/`, `%`, `==`, `!=`, `<`, `>`, `&&`, `||`, `!`, `^` | Pricing, filtering |
| Nullables | `?`, `??`, `??=`, `?.` | Optional properties like discount |
| String Handling | `Substring`, `Replace`, `ToUpper`, `ToLower` | Search, formatting |
| Type Checking | `is`, `as`, `typeof`, `GetType()` | Product category check |
| Pattern Matching | `switch`, `when`, `switch expressions` | Role-based navigation |
| Time Management | `DateTime`, `DateOnly`, `TimeSpan` | Order creation time, delivery slots |
| Enums | `enum`, `ToString()`, `Enum.Parse()` | OrderStatus, UserRole |

**Mini Project:** CLI Product Browser + Role-Based Entry Point

---

## ✅ PHASE 2: OBJECT-ORIENTED PROGRAMMING – Domain Modeling & Encapsulation
### 🎯 Goal: Master OOP principles using ShopRight’s business logic

| Concept | C# Keywords / Features | Use in ShopRight |
|--------|--------------------------|------------------|
| Class & Objects | `class`, `object`, `new`, `this`, `readonly`, `init` | Define domain models |
| Constructors | `constructor`, overloads, default, static ctor | Initialize valid entities |
| Access Modifiers | `public`, `private`, `protected`, `internal`, `private protected` | Proper encapsulation |
| Inheritance | `:`, `virtual`, `override`, `sealed`, `base` | Specialized user types |
| Interfaces | `interface`, `implements`, `explicit interface` | Services: IPaymentService, ICartService |
| Abstraction | `abstract`, `abstract class`, `override` | Payment base logic |
| Static Members | `static class`, `static method`, `const`, `readonly static` | Utility classes |
| Object Equality | `==`, `!=`, `Equals()`, `ReferenceEquals`, `GetHashCode()` | Cart item comparison |
| Records (C# 9+) | `record`, `with`, `init` | Immutable value types like Address |

**Mini Project:** Shopping Cart Engine with OOP Principles

---

## ✅ PHASE 3: COLLECTIONS, GENERICS, LINQ – Inventory, Search, Reporting
### 🎯 Goal: Handle and process data collections for catalog and cart operations

| Concept | C# Keywords / Features | Use in ShopRight |
|--------|--------------------------|------------------|
| Collections | `List<T>`, `Dictionary<K,V>`, `HashSet<T>`, `Queue<T>` | Products, Orders, Cache |
| LINQ Basics | `Select()`, `Where()`, `OrderBy()`, `First()`, `Any()` | Search and filter catalog |
| LINQ Advanced | `GroupBy()`, `Join()`, `Aggregate()`, `Distinct()` | Sales reports, grouping |
| Generic Constraints | `where T : class` | Reusable services and logic |
| Sorting Interfaces | `IComparable`, `IComparer`, custom sort | Product listings |
| Extension Methods | `static`, `this` param | Add filtering logic to services |

**Mini Project:** Product Catalog with Search & Reports

---

## ✅ PHASE 4: EXCEPTION HANDLING, FILE I/O, LOGGING
### 🎯 Goal: Ensure application resilience through proper exception flow & logs

| Concept | C# Keywords / Features | Use in ShopRight |
|--------|--------------------------|------------------|
| Error Handling | `try`, `catch`, `finally`, `throw`, `Exception` | Handle invalid actions |
| Custom Exceptions | `class CustomException : Exception` | OutOfStock, PaymentFailure |
| File I/O | `File`, `FileStream`, `StreamWriter`, `StreamReader` | Export logs, invoices |
| Logging | `using`, `IDisposable`, `Dispose()` | Resource cleanup |

**Mini Project:** File-Based Error Logging + Invoice Export

---

## ✅ PHASE 5: ASYNC, TASKS, THREADING – Background Processing
### 🎯 Goal: Implement concurrency and async behavior for heavy tasks

| Concept | C# Keywords / Features | Use in ShopRight |
|--------|--------------------------|------------------|
| Async Programming | `async`, `await`, `Task`, `Task<T>`, `ConfigureAwait` | API calls, async DB ops |
| Cancellation | `CancellationToken`, `ThrowIfCancellationRequested()` | Cancel long processes |
| Threading | `Thread`, `ThreadPool`, `Parallel.ForEach()` | Concurrent order processing |
| Safety | `lock`, `Monitor`, `Interlocked` | Prevent race conditions in cart |

**Mini Project:** Background Stock Sync & Discount Processor

---

## ✅ PHASE 6: ARCHITECTURE – SOLID, DESIGN PATTERNS, DI
### 🎯 Goal: Implement scalable, loosely coupled software architecture

| Concept | C# / Design Concepts | Use in ShopRight |
|--------|------------------------|------------------|
| SOLID Principles | SRP, OCP, LSP, ISP, DIP | Clean code enforcement |
| Dependency Injection | `IServiceCollection`, `AddScoped`, `Constructor Injection` | Plug in services |
| Design Patterns | Factory, Strategy, Singleton, Decorator | Payments, Discounts, Promo Logic |
| Clean Architecture | Layers: Domain, Application, Infra | System separation |

**Mini Project:** Checkout Pipeline with Pluggable Business Rules

---

## ✅ PHASE 7: EF CORE & DATABASE ACCESS – SQL Persistence
### 🎯 Goal: Persist and retrieve data using EF Core ORM

| Concept | EF Core + C# Features | Use in ShopRight |
|--------|------------------------|------------------|
| ORM Setup | `DbContext`, `DbSet<T>`, `OnModelCreating()` | Access entities |
| Relationships | `HasOne`, `HasMany`, `WithOne`, `Include()` | Order -> OrderItems, etc. |
| Migrations | `Add-Migration`, `Update-Database` | Schema versioning |
| CRUD + Async | `AddAsync`, `SaveChangesAsync`, `Remove`, `Update()` | Product, order persistence |

**Mini Project:** Fully Functional Relational Order DB

---

## ✅ PHASE 8: SECURITY & AUTHORIZATION
### 🎯 Goal: Secure login and authorization logic

| Concept | C# + Security Concepts | Use in ShopRight |
|--------|------------------------|------------------|
| Hashing | `SHA256`, `BCrypt`, `Convert.ToBase64String()` | Password encryption |
| Role Management | `enum`, `switch`, `IsInRole()` | Admin, Customer Roles |
| Validation | `TryParse`, `string.IsNullOrWhiteSpace()` | Prevent invalid inputs |
| Identifiers | `Guid.NewGuid()`, `ToString()` | Order ID, Session Token |

**Mini Project:** Secure Login + Role Authorization System

---

## ✅ PHASE 9: UNIT TESTING, MOCKING & TDD
### 🎯 Goal: Validate and maintain software quality

| Concept | Testing Frameworks | Use in ShopRight |
|--------|------------------------|------------------|
| Unit Testing | `xUnit`, `NUnit`, `[Fact]`, `Assert.Equal` | Validate services |
| Mocking | `Moq`, `.Setup()`, `.Returns()`, `.Verify()` | Mock APIs and dependencies |
| TDD Workflow | Arrange-Act-Assert, test-first | Build robust business logic |

**Mini Project:** Fully Tested Cart & Checkout Logic

---

## 📅 STEP-BY-STEP COURSE FLOW

| Week | Phase | Deliverable |
|------|-------|-------------|
| Week 1 | Phase 1 | CLI App + Syntax Mastery |
| Week 2 | Phase 2 | Domain Models (OOP) |
| Week 3 | Phase 3 | Product Catalog + LINQ Reports |
| Week 4 | Phase 4 | File Logging + Error Control |
| Week 5 | Phase 5 | Async Stock Service |
| Week 6 | Phase 6 | Modular Checkout Architecture |
| Week 7 | Phase 7 | EF Core Integration |
| Week 8 | Phase 8 | Secure Role Login System |
| Week 9 | Phase 9 | Unit Tests + Mocks |

---

## ✅ PHASE 1: C# LANGUAGE FUNDAMENTALS – Console App + Syntax
### 🎯 Goal: Understand how a C# program works, basic syntax, and app interaction

### 👨‍🏫 Audience:
This phase is written for junior developers aiming to become C# gurus. We explain **not just the syntax**, but the **reasoning and real-world purpose** of each concept.

---

### ✅ 1.1 Program Entry – `Main()` Method

**🔍 What:**  
The `Main` method is the starting point of every C# application. It tells the compiler where the program begins execution.

**🎯 Why:**  
You need this method to run your code. Think of it as the front door to your application.

**🔧 How:**  
```csharp
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Welcome to ShopRight!");
    }
}
```

**📦 Where in ShopRight:**  
We’ll use this `Main()` method to drive the console version of the ShopRight Admin Panel for testing logic and operations.

---

### ✅ 1.2 Console Input/Output – `Console.WriteLine`, `Console.ReadLine`

**🔍 What:**  
These are built-in methods to display messages (`WriteLine`) and capture user input (`ReadLine`).

**🎯 Why:**  
User interaction is key. We use these methods to gather user details or control application flow.

**🔧 How:**
```csharp
Console.WriteLine("Enter your role:");
string role = Console.ReadLine();
Console.WriteLine($"You are logged in as {role}");
```

**📦 Where in ShopRight:**  
Used for admin CLI, testing product logic, and simulating early app behavior.

---

### ✅ 1.3 Data Types and Variables (Deep Dive)

**🔍 What:**  
Data types define what kind of data a variable can store. C# is a statically typed language, meaning every variable has a type defined at compile time.

**🎯 Why:**  
Choosing the correct type helps you store, manage, and process data safely and efficiently.

#### ✅ Common C# Data Types:
| Type | Description | Default Value | Range |
|------|-------------|----------------|--------|
| `int` | Whole number | 0 | -2,147,483,648 to 2,147,483,647 |
| `long` | Large whole number | 0L | Very large integers |
| `float` | Decimal (less precision) | 0.0f | ~±3.4E38 (7 digits) |
| `double` | Decimal (default) | 0.0d | ~±1.7E308 (15-16 digits) |
| `decimal` | High-precision decimal (money) | 0.0m | ±79E28 (28-29 digits) |
| `bool` | True/false | false | `true` or `false` only |
| `char` | Single character | '\0' | Unicode character |
| `string` | Text data | null | Sequence of characters |

#### ✅ Best Practices:
- Use `int` for counts or identifiers.
- Use `decimal` for currency (financial transactions).
- Use `bool` for flags or conditions.
- Use `string` for names, descriptions.
- Always **initialize** variables before use.
- Prefer `var` when the type is obvious for **readability**.

**🔧 Examples:**
```csharp
int stock = 50;
decimal price = 149.99m;
bool isAvailable = true;
string productName = "Laptop";
```

**Anti-pattern:** Don’t use float for money:
```csharp
// ❌ Wrong
float salary = 2999.99f; // Risk of precision loss
// ✅ Correct
decimal salary = 2999.99m;
```

**📦 Where in ShopRight:**  
Used everywhere to model domain data like products, orders, and users.

---

### ✅ 1.4 Control Flow – `if`, `else`, `switch`

**🔍 What:**  
Conditional statements let us decide what code to run based on logical expressions.

**🎯 Why:**  
We need decision-making logic for access roles, product filters, etc.

**🔧 Examples:**
```csharp
if (userRole == "admin")
{
    Console.WriteLine("Access granted to admin dashboard");
}
else
{
    Console.WriteLine("Access denied.");
}
```
```csharp
switch (paymentMethod)
{
    case "paypal": Console.WriteLine("Redirect to PayPal"); break;
    case "card": Console.WriteLine("Enter card details"); break;
    default: Console.WriteLine("Unsupported payment method"); break;
}
```

#### ✅ Best Practices:
- Use `if/else` for boolean decisions.
- Use `switch` for fixed value comparisons like enums or strings.
- Avoid deeply nested `if/else` (use early returns or `switch`).

**📦 Where in ShopRight:**  
Used in authentication, permission validation, feature toggles, etc.

---

### ✅ 1.5 Loops – `for`, `foreach`, `while`, `do-while`

**🔍 What:**  
Loops let you repeat operations while a condition is true.

**🎯 Why:**  
Use them to iterate product lists, apply actions on carts, retry until valid input.

**🔧 Examples:**
```csharp
// Loop through products
string[] products = {"Laptop", "Mouse", "Keyboard"};
foreach (var item in products)
{
    Console.WriteLine(item);
}
```
```csharp
// Ask until 'exit' entered
string input;
do
{
    Console.WriteLine("Type 'exit' to quit:");
    input = Console.ReadLine();
} while (input != "exit");
```

#### ✅ Best Practices:
- Use `foreach` for read-only iteration.
- Use `for` when index is needed.
- Avoid infinite loops: always define an **exit condition**.
- Prefer `do-while` when at least one iteration is needed.

**📦 Where in ShopRight:**  
Product listing, retry mechanisms, paginated fetches.

---

### ✅ 1.6 Summary of Keywords & Concepts Introduced

- **Entry & Execution:** `Main`, `static`, `void`
- **Input/Output:** `Console.WriteLine`, `Console.ReadLine`, `$"{}`
- **Variables/Data Types:** `string`, `int`, `decimal`, `bool`, `char`, `float`, `double`, `var`, `long`
- **Operators:** `+`, `-`, `*`, `/`, `%`, `==`, `!=`, `<`, `>`, `&&`, `||`, `!`, `??`, `?:`
- **Conditions:** `if`, `else`, `switch`, `case`, `default`
- **Loops:** `for`, `foreach`, `while`, `do-while`, `break`, `continue`
- **Utilities:** `.ToUpper()`, `.ToLower()`, `.Substring()`, `.Replace()`, `.Length`

---

✅ Now that we’ve mastered the **core language building blocks**, we’ll move to **Phase 2**, where we begin to structure our e-commerce system using **Object-Oriented Programming**.




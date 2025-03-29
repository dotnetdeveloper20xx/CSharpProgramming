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

**Phase 2 – OOP Masterclass: Domain Modeling & Encapsulation in C#**

---

## 🎯 Goal:
To provide a detailed, beginner-to-expert guide to mastering **Object-Oriented Programming (OOP)** in C# using the ShopRight e-commerce project. This phase introduces the foundational keywords and concepts of OOP in C# with practical applications.

For every keyword or concept, we explain:
- **What** it means
- **Why** it exists (background + real-world problem it solves)
- **How** to use it (syntax + examples)
- **Where** it's applied in the ShopRight project
- **Best practices**, Do's and Don'ts

---

## ✅ 2.1 Class & Objects

### 🔍 What is a Class?
A `class` is a blueprint for creating objects. It defines properties (data) and methods (behavior) that the object will have. Think of it as the design of a product in ShopRight.

### 🔍 What is an Object?
An `object` is an instance of a class. It's the real product created from that design.

### 🔧 C# Keywords:
- `class`, `object`, `new`, `this`, `readonly`, `init`

### 🔬 How:
```csharp
public class Product
{
    public string Name { get; init; }
    public decimal Price { get; set; }
    public readonly string SKU;

    public Product(string sku)
    {
        SKU = sku;
    }
}
```
```csharp
Product p = new Product("ABC123") { Name = "Laptop", Price = 1200 };
```

### 📦 In ShopRight:
- Every domain model: `Product`, `User`, `Order`, `Cart`, `Inventory` is a `class`.
- `readonly` is used to protect fields like `SKU`, which should not change after creation.
- `init` is used for immutable property initialization.

### ✅ Best Practices:
- Always use PascalCase for class names.
- Group related fields/methods together for readability.
- Use `init` for properties you want to be set only at object creation.

---

## ✅ 2.2 Constructors

### 🔍 What is a Constructor?
A constructor is a special method that is automatically called when an object is created using the `new` keyword. It initializes the class with valid default or required data.

### 🔧 Keywords:
- `constructor`, `this`, `overload`, `default`, `static constructor`

### 🔬 How:
```csharp
public class User
{
    public string Name { get; set; }
    public bool IsAdmin { get; set; }

    public User(string name)
    {
        Name = name;
    }

    public User(string name, bool isAdmin) : this(name)
    {
        IsAdmin = isAdmin;
    }
}
```

### 📦 In ShopRight:
- Constructor ensures a `User` always has a `Name`.
- Overloads support admin or customer use cases.

### ✅ Best Practices:
- Use constructors to enforce domain rules.
- Avoid doing business logic in constructors.
- Use `static` constructors for initializing shared values.

---

## ✅ 2.3 Access Modifiers

### 🔍 What are Access Modifiers?
They control the visibility and accessibility of classes and members.

### 🔧 Keywords:
- `public`, `private`, `protected`, `internal`, `private protected`

### 🔬 How:
```csharp
public class Cart
{
    private List<Product> _items = new();
    public IReadOnlyList<Product> Items => _items;

    public void Add(Product product)
    {
        _items.Add(product);
    }
}
```

### 📦 In ShopRight:
- Prevents direct manipulation of cart items from outside.
- Exposes only what’s needed.

### ✅ Best Practices:
- Default to `private`. Open up only what needs exposure.
- `protected` = extendable; `internal` = within the assembly.

---

## ✅ 2.4 Inheritance

### 🔍 What is Inheritance?
Allows a class to derive from another, inheriting its members and allowing customization.

### 🔧 Keywords:
- `:`, `virtual`, `override`, `sealed`, `base`

### 🔬 How:
```csharp
public class User
{
    public virtual string GetRole() => "Customer";
}

public class AdminUser : User
{
    public override string GetRole() => "Admin";
}
```

### 📦 In ShopRight:
- `User`, `AdminUser`, and `GuestUser` extend the base `User` class.

### ✅ Best Practices:
- Use `sealed` to prevent further inheritance if not needed.
- Override only virtual methods.
- Use base constructors for consistency.

---

## ✅ 2.5 Interfaces

### 🔍 What is an Interface?
An interface defines a contract that classes must follow. It supports abstraction and polymorphism.

### 🔧 Keywords:
- `interface`, `implements`, `explicit interface implementation`

### 🔬 How:
```csharp
public interface IPaymentService
{
    void Pay(decimal amount);
}

public class StripeService : IPaymentService
{
    public void Pay(decimal amount)
    {
        Console.WriteLine($"Paid {amount} via Stripe");
    }
}
```

### 📦 In ShopRight:
- Used for `IPaymentService`, `ICartService`, `INotificationService` to allow flexible implementations.

### ✅ Best Practices:
- Keep interfaces small and focused.
- Use `I` prefix conventionally.

---

## ✅ 2.6 Abstraction

### 🔍 What is Abstraction?
Hiding internal details and exposing only the essential methods through interfaces or abstract classes.

### 🔧 Keywords:
- `abstract`, `abstract class`, `override`, `base`

### 🔬 How:
```csharp
public abstract class Discount
{
    public abstract decimal Calculate(decimal total);
}

public class PercentageDiscount : Discount
{
    public override decimal Calculate(decimal total) => total * 0.9m;
}
```

### 📦 In ShopRight:
- `Discount`, `PaymentMethod`, `Notification` systems follow abstraction.

### ✅ Best Practices:
- Abstract for base rules and shared templates.
- Combine with interfaces for flexibility.

---

## ✅ 2.7 Static Members

### 🔍 What are Static Members?
They belong to the class, not instances. Useful for utility or shared values.

### 🔧 Keywords:
- `static class`, `static method`, `const`, `readonly static`

### 🔬 How:
```csharp
public static class Utils
{
    public static string GenerateSlug(string name) => name.ToLower().Replace(" ", "-");
}
```

### 📦 In ShopRight:
- Shared helpers like `IdGenerator`, `StringUtils`, `MathUtils`

### ✅ Best Practices:
- Use static for pure functions only (no state).
- Use `const` for compile-time constants; `readonly static` for runtime.

---

## ✅ 2.8 Object Equality

### 🔍 What is Object Equality?
Determines how objects are compared: by reference or value.

### 🔧 Keywords:
- `==`, `!=`, `Equals()`, `ReferenceEquals()`, `GetHashCode()`

### 🔬 How:
```csharp
public class Product
{
    public string SKU { get; set; }

    public override bool Equals(object obj)
    {
        return obj is Product p && SKU == p.SKU;
    }

    public override int GetHashCode() => SKU.GetHashCode();
}
```

### 📦 In ShopRight:
- Avoid duplicate products in cart or catalog.

### ✅ Best Practices:
- Always override both `Equals()` and `GetHashCode()`.
- Use `ReferenceEquals` only for checking exact memory location.

---

## ✅ 2.9 Records (C# 9+)

### 🔍 What are Records?
Records are immutable reference types designed for value-based equality.

### 🔧 Keywords:
- `record`, `with`, `init`

### 🔬 How:
```csharp
public record Address(string Street, string City);

var address1 = new Address("123 Main", "LA");
var address2 = address1 with { City = "NY" };
```

### 📦 In ShopRight:
- Used for shipping address, order summary, read models.

### ✅ Best Practices:
- Use records for data contracts, DTOs, view models.
- Always use `with` and `init` for changes.

---

## ✅ Mini Project: Shopping Cart Engine

- Create models: `Product`, `CartItem`, `Cart`, `User`, `Discount`
- Use interfaces for extensibility (`ICartService`, `IDiscountEngine`)
- Apply abstraction via abstract discount types
- Use static helpers for ID generation
- Compare cart items using equality overrides
- Apply SOLID principles throughout

---

✅ Phase 2 equips developers with the real-world mastery of OOP required to model scalable enterprise systems like ShopRight.







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

**Phase 3 – Mastering Collections, Generics & LINQ in C#**

---

## 🎯 Goal:
To teach a junior developer how to work with C# collections, generics, and LINQ for handling product catalogs, cart operations, filters, and reports in the ShopRight project.

Each keyword or concept will be explained with:
- ✅ What (definition)
- ✅ Why (background and use case)
- ✅ How (code with examples)
- ✅ Where (used in ShopRight)
- ✅ Best practices, related topics, dos and don’ts

---

## ✅ 3.1 COLLECTIONS – `List<T>`, `Dictionary<K,V>`, `HashSet<T>`, `Queue<T>`

### 🔍 What:
Collections are C# types that store groups of objects.
- `List<T>`: An ordered, resizable list.
- `Dictionary<K,V>`: A key-value pair collection.
- `HashSet<T>`: A collection of unique elements.
- `Queue<T>`: A first-in-first-out (FIFO) collection.

### 🔬 How:
```csharp
List<string> productNames = new List<string> { "Laptop", "Mouse" };
Dictionary<string, int> stock = new Dictionary<string, int> { ["Laptop"] = 5 };
HashSet<string> categories = new HashSet<string> { "Electronics", "Gadgets" };
Queue<string> shippingQueue = new Queue<string>();
```

### 📦 Where in ShopRight:
- `List<Product>` for catalog
- `Dictionary<string, int>` for stock management
- `HashSet<string>` for tag filtering
- `Queue<Order>` for processing shipments

### ✅ Best Practices:
- Use `Dictionary` when lookup by key is frequent.
- Use `HashSet` to avoid duplicates.
- Avoid using `List<T>` for random key lookup (prefer Dictionary).

---

## ✅ 3.2 GENERICS & CONSTRAINTS – `T`, `where T : class`

### 🔍 What:
Generics allow classes and methods to operate on types specified at runtime.
Constraints ensure only certain types can be used.

### 🔬 How:
```csharp
public class Repository<T> where T : class
{
    private List<T> _items = new();
    public void Add(T item) => _items.Add(item);
    public IEnumerable<T> GetAll() => _items;
}
```

### 📦 Where in ShopRight:
- `GenericRepository<T>` for managing products, orders, users

### ✅ Best Practices:
- Use constraints to limit type usage.
- Use generics to reduce duplication and enforce type safety.

### ❌ Don’t:
- Don’t overuse generics when simple inheritance works.

---

## ✅ 3.3 LINQ BASICS – `Select()`, `Where()`, `OrderBy()`, `First()`, `Any()`

### 🔍 What:
LINQ (Language Integrated Query) allows querying collections using expressive, readable syntax.

### 🔬 How:
```csharp
var expensive = products.Where(p => p.Price > 1000);
var names = products.Select(p => p.Name);
var first = products.First();
var hasLaptop = products.Any(p => p.Name == "Laptop");
```

### 📦 Where in ShopRight:
- Product search filters
- Sorting product lists by price
- Checking product existence

### ✅ Best Practices:
- Chain LINQ queries for readability.
- Use `FirstOrDefault()` to avoid exceptions.

---

## ✅ 3.4 LINQ ADVANCED – `GroupBy()`, `Join()`, `Aggregate()`, `Distinct()`

### 🔍 What:
Advanced LINQ operators allow summarization, grouping, and relational data querying.

### 🔬 How:
```csharp
var salesByCategory = products.GroupBy(p => p.Category)
    .Select(g => new { Category = g.Key, TotalSales = g.Sum(p => p.Price) });

var allCategories = products.Select(p => p.Category).Distinct();
```

### 📦 Where in ShopRight:
- Sales reports
- Category summaries
- Customer-product join tables

### ✅ Best Practices:
- Use `GroupBy()` for dashboards.
- Use `Join()` only when absolutely needed; prefer navigation properties with EF Core.

---

## ✅ 3.5 ENUMERABLE TYPES – `IEnumerable<T>` vs `IQueryable<T>`

### 🔍 What:
- `IEnumerable<T>`: In-memory iteration.
- `IQueryable<T>`: Remote query (e.g., EF Core, database).

### 🔬 How:
```csharp
IEnumerable<Product> products = productService.GetAll();
IQueryable<Product> query = dbContext.Products;
```

### 📦 Where in ShopRight:
- `IQueryable<T>` for DB queries.
- `IEnumerable<T>` for in-memory cart filtering.

### ✅ Best Practices:
- Avoid calling `.ToList()` too early (deferred execution).
- Use `IQueryable<T>` until you need data.

---

## ✅ 3.6 LAZY LOADING & DEFERRED EXECUTION

### 🔍 What:
- **Lazy loading**: Load related data on-demand.
- **Deferred execution**: LINQ queries are only executed when enumerated.

### 🔬 How:
```csharp
var query = products.Where(p => p.Price > 1000); // Not executed yet
foreach (var item in query) { Console.WriteLine(item.Name); } // Now it executes
```

### 📦 Where in ShopRight:
- Related data like `Product.Images` or `Order.Items` is loaded only when accessed.

### ✅ Best Practices:
- Be mindful of N+1 problems in lazy loading.
- Use `ToList()` only when you really need it.

---

## ✅ 3.7 PROJECTIONS & ANONYMOUS TYPES

### 🔍 What:
Projection is reshaping data. Anonymous types are unnamed objects created with `new {}`.

### 🔬 How:
```csharp
var results = products.Select(p => new {
    p.Name,
    PriceWithTax = p.Price * 1.1m
});
```

### 📦 Where in ShopRight:
- Generating product cards
- Creating lightweight summaries for UI

### ✅ Best Practices:
- Use anonymous types in read-only views.
- Avoid passing anonymous types outside method scope.

---

## ✅ 3.8 SORTING – `IComparer`, `IComparable`, `OrderBy()`

### 🔍 What:
Sorting in C# can be done through interfaces or LINQ extensions.

### 🔬 How:
```csharp
products.Sort(); // if Product implements IComparable<Product>

var sorted = products.OrderBy(p => p.Price);
```

### 📦 Where in ShopRight:
- Sort by price, name, rating in catalog

### ✅ Best Practices:
- Prefer `OrderBy()` for simple sorts.
- Use `IComparer<T>` for complex logic.

---

## ✅ 3.9 EXTENSION METHODS – `static`, `this` parameter

### 🔍 What:
Extension methods add methods to existing types without modifying them.

### 🔬 How:
```csharp
public static class ProductExtensions
{
    public static bool IsOnSale(this Product p) => p.Price < 100;
}
```

### 📦 Where in ShopRight:
- `IsFreeShipping`, `IsOnSale`, `GetDisplayPrice()` helpers

### ✅ Best Practices:
- Keep logic focused and single-purpose.
- Avoid adding too many unrelated extensions.

---

## ✅ MINI PROJECT – PRODUCT CATALOG SEARCH & REPORTS

You will:
- Store products in a `List<Product>`
- Filter by category using `Where()`
- Project results to name/price only
- Group results with `GroupBy()`
- Sort by price or name
- Create extension method `IsInStock()`

---

## 📚 Comprehensive Guide to Collections and LINQ in C#

Collections and LINQ are foundational topics that every C# developer must master. 

### 🗃️ Collections

Collections manage groups of related objects, simplifying data handling and manipulation.

### 1. List<T>

- **Characteristics:** Ordered, allows duplicates, dynamically resizable.
- **Methods:** `Add`, `Insert`, `Remove`, `RemoveAt`, `Contains`, `Clear`, `IndexOf`, `Find`, `Sort`.

**Example:**
```csharp
List<int> scores = new List<int>();
scores.Add(10);
scores.AddRange(new[] { 20, 30, 40 });
scores.Insert(2, 25); // Inserts 25 at index 2
scores.Remove(30);
```

### 2. Dictionary<TKey, TValue>

- **Characteristics:** Key-value pairs, fast lookups by unique keys.
- **Methods:** `Add`, `Remove`, `ContainsKey`, `ContainsValue`, `TryGetValue`, `Keys`, `Values`.

**Example:**
```csharp
Dictionary<string, int> ages = new Dictionary<string, int>();
ages.Add("Alice", 25);
ages["Bob"] = 30;
if (ages.TryGetValue("Alice", out int age))
{
    Console.WriteLine(age); // 25
}
```

### 3. HashSet<T>

- **Characteristics:** Unordered, unique elements, efficient set operations.
- **Methods:** `Add`, `Remove`, `Contains`, `UnionWith`, `IntersectWith`, `ExceptWith`.

**Example:**
```csharp
HashSet<string> cities = new HashSet<string>();
cities.Add("New York");
cities.Add("Los Angeles");
cities.Add("New York"); // Ignored duplicate
```

### 4. Queue<T>

- **Characteristics:** FIFO (First-In-First-Out).
- **Methods:** `Enqueue`, `Dequeue`, `Peek`, `Clear`.

**Example:**
```csharp
Queue<string> printJobs = new Queue<string>();
printJobs.Enqueue("Document1.pdf");
printJobs.Enqueue("Document2.pdf");
string nextJob = printJobs.Dequeue(); // Document1.pdf
```

### 5. Stack<T>

- **Characteristics:** LIFO (Last-In-First-Out).
- **Methods:** `Push`, `Pop`, `Peek`, `Clear`.

**Example:**
```csharp
Stack<int> history = new Stack<int>();
history.Push(1);
history.Push(2);
int lastVisited = history.Pop(); // 2
```

### Related Concepts:
- **ArrayList** (non-generic)
- **LinkedList<T>** (doubly-linked list)
- **SortedList<TKey, TValue>** (sorted dictionary)
- **Concurrent Collections** (`ConcurrentDictionary`, `ConcurrentQueue`)

---

### 🧠 LINQ (Language Integrated Query)

LINQ provides intuitive query capabilities directly in C# for filtering, ordering, and grouping data.

### Basics:

- **Where:** Filters items based on conditions.
```csharp
var adults = people.Where(p => p.Age >= 18);
```

- **Select:** Projects items into a new form.
```csharp
var names = people.Select(p => p.Name);
```

- **Any:** Checks if any item matches a condition.
```csharp
bool hasSeniors = people.Any(p => p.Age > 65);
```

### Advanced Concepts:

- **GroupBy:** Groups items by a specified key.
```csharp
var groupedByCity = people.GroupBy(p => p.City);
```

- **Join:** Combines two sequences based on matching keys.
```csharp
var employeeDepartments = employees.Join(departments,
    e => e.DepartmentId,
    d => d.Id,
    (e, d) => new { e.Name, d.DepartmentName });
```

- **Aggregate:** Performs accumulation.
```csharp
var total = numbers.Aggregate((sum, next) => sum + next);
```

- **OrderBy / OrderByDescending:** Sorts sequences.
```csharp
var orderedNames = names.OrderBy(n => n);
```

- **Skip / Take:** Implements pagination.
```csharp
var pageItems = items.Skip(20).Take(10);
```

### Related LINQ Keywords and Methods:

- **Distinct:** Removes duplicates.
- **First / FirstOrDefault:** Retrieves first element.
- **Last / LastOrDefault:** Retrieves last element.
- **Count:** Counts elements matching criteria.
- **Sum / Average / Min / Max:** Aggregation functions.
- **SelectMany:** Flattens collections.

### Query Syntax Example:
```csharp
var query = from p in people
            where p.Age > 18
            orderby p.Name
            select p;
```

### Method Syntax Example:
```csharp
var query = people.Where(p => p.Age > 18)
                  .OrderBy(p => p.Name);
```

---

### 📌 Important Best Practices

- Prefer generic collections (`List<T>`, `Dictionary<TKey, TValue>`) for type safety and performance.
- Choose appropriate collections based on data operations (e.g., use `HashSet<T>` for unique data).
- Use LINQ for cleaner and more maintainable code.
- Be aware of LINQ's deferred execution (query runs only when iterated).
- Optimize LINQ queries (avoid unnecessary operations, consider indexing).

---

### 🚀 Summary

Mastering collections and LINQ significantly improves your ability to efficiently manage and query data. Understanding the characteristics and appropriate use cases of each collection type, combined with powerful LINQ querying techniques, empowers you to write clean, readable, and optimized C# code.




### ⚙️ Generics & Constraints

**Generics** in C# provide a way to design classes, methods, or data structures with a placeholder for the type of data they store or use. Instead of specifying exact types (like `int` or `string`), generics allow you to define functionality for any type.

**Why Use Generics?**
- Reusability of code
- Type Safety
- Improved performance by avoiding boxing/unboxing for value types

**Detailed Example:**

```csharp
public class Repository<T> where T : class, new()
{
    private List<T> _items = new List<T>();

    public void Add(T item)
    {
        _items.Add(item);
    }

    public T CreateNew()
    {
        return new T();
    }

    public IEnumerable<T> GetAll()
    {
        return _items;
    }
}

// Usage:
var repo = new Repository<Person>();
repo.Add(new Person { Name = "Alice", Age = 30 });
var person = repo.CreateNew();
person.Name = "Bob";
repo.Add(person);
```

**Constraints** specify rules about types that generics accept:
- `where T : class` (Reference types)
- `where T : struct` (Value types)
- `where T : new()` (Default constructor)
- `where T : InterfaceName` (Implement an interface)

---

### 🔁 Lazy Loading & Deferred Execution

**Lazy Loading** delays object initialization or data retrieval until it’s needed.

**Detailed Example:**

```csharp
public class Customer
{
    public int Id { get; set; }
    private Lazy<List<Order>> _orders;

    public Customer()
    {
        _orders = new Lazy<List<Order>>(() => LoadOrders());
    }

    public List<Order> Orders => _orders.Value;

    private List<Order> LoadOrders()
    {
        Console.WriteLine("Orders loaded.");
        return new List<Order> { new Order { OrderId = 1 }, new Order { OrderId = 2 } };
    }
}

// Usage:
var customer = new Customer();
// Orders are NOT loaded yet
var orders = customer.Orders;  // NOW orders are loaded.
```

**Deferred Execution** postpones query execution until explicitly iterated.

```csharp
var numbers = new List<int> { 1, 2, 3, 4, 5 };
var evenNumbers = numbers.Where(n => {
    Console.WriteLine($"Checking {n}");
    return n % 2 == 0;
});

// Query is defined but not executed yet.
foreach (var num in evenNumbers)
{
    Console.WriteLine($"Even: {num}");
}
// Execution happens here!
```

---

### 🕵️ Interfaces: IEnumerable, IQueryable

**IEnumerable**: Represents in-memory collection iteration.

```csharp
IEnumerable<string> fruits = new List<string> { "Apple", "Banana", "Cherry" };
foreach (var fruit in fruits)
{
    Console.WriteLine(fruit);
}
```

**IQueryable**: Represents queries against data sources, translating queries to SQL.

```csharp
// Imagine Entity Framework context
IQueryable<User> usersQuery = dbContext.Users.Where(u => u.IsActive);

// SQL not executed yet!
var users = usersQuery.ToList();  // SQL executes now
```

**Key Differences:**
- `IEnumerable` executes queries on the client side (in memory).
- `IQueryable` executes queries on the server side (database), optimizing performance.

---

### 🧩 Sorting: OrderBy, IComparable, IComparer

**OrderBy**: Quick sorting via LINQ.

```csharp
var scores = new[] { 70, 90, 50, 85 };
var sortedScores = scores.OrderBy(s => s);  // 50, 70, 85, 90
```

**IComparable**: Defines default sorting order within a class.

```csharp
public class Product : IComparable<Product>
{
    public string Name { get; set; }
    public decimal Price { get; set; }

    public int CompareTo(Product other)
    {
        return Price.CompareTo(other.Price);
    }
}

var products = new List<Product>
{
    new Product { Name = "Laptop", Price = 1200m },
    new Product { Name = "Phone", Price = 800m }
};

products.Sort(); // Phone (800), Laptop (1200)
```

**IComparer**: Defines external custom sorting logic.

```csharp
public class NameComparer : IComparer<Product>
{
    public int Compare(Product x, Product y)
    {
        return x.Name.CompareTo(y.Name);
    }
}

products.Sort(new NameComparer()); // Sorted by name: Laptop, Phone
```

---

### 📌 Summary

- **Generics & Constraints**: Reusable, type-safe classes and methods with rules.
- **Lazy Loading & Deferred Execution**: Data loaded only when explicitly accessed.
- **Interfaces (`IEnumerable`, `IQueryable`)**: Iterating collections and querying efficiently.
- **Sorting (`OrderBy`, `IComparable`, `IComparer`)**: Various ways to implement and control sorting logic in applications.

This document equips you with advanced, real-world C# knowledge essential for becoming a proficient developer.










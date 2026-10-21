# `Main` Method in C#

### What is the `Main` Method?

> The `Main` method is the entry point of every C# application.
>
> When a program is started, the Common Language Runtime (CLR) begins execution with the `Main` method.
>
> Without a valid `Main` method, an application cannot be started directly.

### General Syntax

```csharp
public static void Main(string[] args)
{

    // Code to be executed

}
```

### Understanding the Keywords

```csharp
public static void Main(string[] args)
```

- `public`
  - Makes the method accessible to the runtime.

- `static`
  - Allows the method to be called without creating an object of the class.

- `void`
  - Indicates that the method does not return a value.

- `Main`
  - The predefined method name recognized as the program entry point.

- `string[] args`
  - Stores command-line arguments passed to the application.

### Example `Main` Method

The `Main` method is the first method executed when a C# application starts.

```csharp
using System;

public class Program
{

    // Main Method
    public static void Main(string[] args)
    {

        Console.WriteLine("Hello World!");

    }

}
```

**Output:**

```text
Hello World!
```

### Example with Variables

Variables can be declared and used inside the `Main` method like in any other method.

```csharp
using System;

public class Person
{

    // Main Method
    public static void Main(string[] args)
    {

        string name = "Alex";
        int age = 25;

        Console.WriteLine("Name: " + name);
        Console.WriteLine("Age: " + age);

    }

}
```

**Output:**

```text
Name: Alex
Age: 25
```

### Example Calling Another Method

The `Main` method is often used to start the application's logic by calling other methods.

```csharp
using System;

public class Application
{

    // Main Method
    public static void Main(string[] args)
    {

        GreetUser();

    }

    public static void GreetUser()
    {

        Console.WriteLine("Welcome!");

    }

}
```

**Output:**

```text
Welcome!
```

### Important Notes

> The `Main` method is the starting point of every C# application.
>
> The CLR automatically executes the `Main` method when the program starts.
>
> The method signature is commonly written as `public static void Main(string[] args)`.
>
> The `Main` method can contain statements, variables, loops, conditions, and method calls.
>
> A class can contain many methods, but program execution begins with the `Main` method.

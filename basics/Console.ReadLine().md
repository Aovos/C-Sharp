# `Console.ReadLine()` in C#

### What is `Console.ReadLine()`?

> `Console.ReadLine()` is a method provided by the `Console` class in the `System` namespace.
>
> It is commonly used to read input from the keyboard in console applications.
>
> The method always returns the entered value as a `string`.

### Why Use `Console.ReadLine()`?

- Read user input from the console.
- Create interactive applications.
- Collect data entered by the user.
- Combine user input with variables and program logic.

### General Syntax

```csharp
string userInput = Console.ReadLine();
```

### Example Reading a `string`

`Console.ReadLine()` can be used to read text entered by the user.

```csharp
using System;

public class Person
{

    // Main Method
    public static void Main(string[] args)
    {

        Console.Write("Enter your name: ");
        string name = Console.ReadLine();

        Console.WriteLine("Hello " + name + "!");

    }

}
```

**Example Input:**

```text
Alex
```

**Output:**

```text
Hello Alex!
```

### Example Reading an `int`

Since `Console.ReadLine()` returns a `string`, the input must be converted to an integer.

```csharp
using System;

public class Person
{

    // Main Method
    public static void Main(string[] args)
    {

        Console.Write("Enter your age: ");
        int age = int.Parse(Console.ReadLine());

        Console.WriteLine("You are " + age + " years old.");

    }

}
```

**Example Input:**

```text
25
```

**Output:**

```text
You are 25 years old.
```

### Example Reading Multiple Values

Multiple values can be entered and stored in different variables.

```csharp
using System;

public class Person
{

    // Main Method
    public static void Main(string[] args)
    {

        Console.Write("Enter your name: ");
        string name = Console.ReadLine();

        Console.Write("Enter your age: ");
        int age = int.Parse(Console.ReadLine());

        Console.WriteLine("Name: " + name);
        Console.WriteLine("Age: " + age);

    }

}
```

**Example Input:**

```text
Alex
25
```

**Output:**

```text
Name: Alex
Age: 25
```

### Example Using `TryParse()`

`TryParse()` is a safer alternative to `Parse()` because it prevents exceptions when invalid values are entered.

```csharp
using System;

public class Person
{

    // Main Method
    public static void Main(string[] args)
    {

        Console.Write("Enter your age: ");

        if (int.TryParse(Console.ReadLine(), out int age))
        {
            Console.WriteLine("Age: " + age);
        }
        else
        {
            Console.WriteLine("Invalid input.");
        }

    }

}
```

### Common Conversion Methods

| Method | Description |
|----------|-------------|
| `int.Parse()` | Converts a string to an `int`. |
| `double.Parse()` | Converts a string to a `double`. |
| `bool.Parse()` | Converts a string to a `bool`. |
| `int.TryParse()` | Safely converts a string to an `int`. |
| `double.TryParse()` | Safely converts a string to a `double`. |

### Important Notes

> `Console.ReadLine()` always returns a value of type `string`.
>
> Numeric values must be converted before they can be stored in numeric variables.
>
> `Parse()` throws an exception when invalid data is entered.
>
> `TryParse()` is generally recommended when reading user input because it safely handles invalid values.
>
> `Console.ReadLine()` is one of the most commonly used methods for handling user input in C# console applications.

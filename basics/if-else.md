# `if` Statements in C#

### What are `if` Statements?

> `if` statements are control structures that allow a program to make decisions based on conditions.
>
> Depending on whether a condition is `true` or `false`, different code blocks can be executed.
>
> This makes programs more flexible and allows them to react to user input, data, or other situations.

### General Syntax

`if`

```csharp
if (condition)
{
    // Code executed if the condition is true
}
```

`if-else`

```csharp
if (condition)
{
    // Code executed if the condition is true
}
else
{
    // Code executed if the condition is false
}
```

`if | else-if | else`

```csharp
if (condition1)
{
    // Code executed if condition1 is true
}
else if (condition2)
{
    // Code executed if condition1 is false
    // and condition2 is true
}
else
{
    // Code executed if all conditions are false
}
```

### Example `if`

An `if` statement can be used on its own when code should only be executed if a condition is true.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int age = 20;

        if (age >= 18)
        {
            Console.WriteLine("You are allowed to vote.");
        }
    }
}
```

**Output:**

```text
You are allowed to vote.
```

### Example `if-else`

A standalone `if` statement only defines what happens when a condition is `true`.
By adding an `else` block, you can also define what should happen when the condition is `false`.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int age = 16;

        if (age >= 18)
        {
            Console.WriteLine("You are an adult.");
        }
        else
        {
            Console.WriteLine("You are a minor.");
        }
    }
}
```

**Output:**

```text
You are a minor.
```

### Example `if | else-if | else`

When multiple conditions need to be checked, `else if` can be used to evaluate additional conditions before falling back to the `else` block.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int score = 85;

        if (score >= 90)
        {
            Console.WriteLine("Grade: A");
        }
        else if (score >= 80)
        {
            Console.WriteLine("Grade: B");
        }
        else if (score >= 70)
        {
            Console.WriteLine("Grade: C");
        }
        else if (score >= 60)
        {
            Console.WriteLine("Grade: D");
        }
        else if (score >= 50)
        {
            Console.WriteLine("Grade: E");
        }
        else
        {
            Console.WriteLine("Grade: F");
        }
    }
}
```

**Output:**

```text
Grade: B
```

### Important Notes

> The condition inside the parentheses `()` must evaluate to a boolean value (`true` or `false`).
>
> An `if` statement can be used without `else` or `else if`.
>
> The `else` block is optional and only runs when all previous conditions are false.
>
> Multiple conditions can be checked using `else if`.
>
> Curly braces `{}` are recommended even when only a single statement is executed.

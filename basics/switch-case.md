# `switch-case` in C#

### What are `switch-case` statements?

> `switch-case` statements are control structures that allow a program to execute different code blocks based on the value of a single expression.
>
> They provide a cleaner alternative to long chains of `if`, `else if`, and `else` statements when comparing the same variable against multiple values.
>
> This makes code easier to read, maintain, and extend.

### General Syntax

```csharp
switch (expression)
{
    case value1:
        // Code executed when expression matches value1
        break;

    case value2:
        // Code executed when expression matches value2
        break;

    default:
        // Code executed when no case matches
        break;
}
```

### Example `switch`

A `switch` statement is useful when the same variable needs to be compared against multiple possible values.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int day = 3;

        switch (day)
        {
            case 1:
                Console.WriteLine("Monday");
                break;

            case 2:
                Console.WriteLine("Tuesday");
                break;

            case 3:
                Console.WriteLine("Wednesday");
                break;

            case 4:
                Console.WriteLine("Thursday");
                break;

            case 5:
                Console.WriteLine("Friday");
                break;

            case 6:
                Console.WriteLine("Saturday");
                break;

            case 7:
                Console.WriteLine("Sunday");
                break;

            default:
                Console.WriteLine("Invalid day");
                break;
        }
    }
}
```

**Output:**

```text
Wednesday
```

### Example `switch` with Multiple Cases

Multiple cases can execute the same code block.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int month = 7;

        switch (month)
        {
            case 12:
            case 1:
            case 2:
                Console.WriteLine("Winter");
                break;

            case 3:
            case 4:
            case 5:
                Console.WriteLine("Spring");
                break;

            case 6:
            case 7:
            case 8:
                Console.WriteLine("Summer");
                break;

            case 9:
            case 10:
            case 11:
                Console.WriteLine("Autumn");
                break;

            default:
                Console.WriteLine("Invalid month");
                break;
        }
    }
}
```

**Output:**

```text
Summer
```

### Example `default`

The `default` section can be used to handle values that do not match any defined case.

```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        int number = 99;

        switch (number)
        {
            case 1:
                Console.WriteLine("One");
                break;

            case 2:
                Console.WriteLine("Two");
                break;

            case 3:
                Console.WriteLine("Three");
                break;

            default:
                Console.WriteLine("Unknown number");
                break;
        }
    }
}
```

**Output:**

```text
Unknown number
```

### Important Notes

> A `switch` statement evaluates a single expression and compares it against multiple values.
>
> The `default` section is optional and is executed when no case matches.
>
> Multiple cases can share the same code block.
>
> The `break` statement is commonly used to exit the switch after a matching case has been executed.
>
> A `switch` statement can often be used as a cleaner alternative to long `if | else-if | else` chains.
>
> The `default` section should usually be placed at the end of the statement.

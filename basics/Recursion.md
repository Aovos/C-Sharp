# `Recursion`

### What is `Recursion`?

> Recursion is a programming technique where a method calls itself.
>
> It is commonly used to solve a problem by breaking it down into smaller versions of the same problem until a stopping condition is reached.

### General Syntax

```csharp
public static void MethodName(parameter)
{
    if (baseCondition)
    {
        return;
    }

    // Code block

    MethodName(modifiedParameter);
}
```

### Example: Basic Recursion

A recursive method can perform a task repeatedly by calling itself.

```csharp
public static void CountDown(int number)
{
    if (number == 0)
    {
        return;
    }

    Console.WriteLine(number);
    CountDown(number - 1);
}
```

```csharp
CountDown(5);
```

**Output:**

```text
5
4
3
2
1
```

### Understanding `Recursion`

```csharp
public static void CountDown(int number)
{
    if (number == 0)
    {
        return;
    }

    Console.WriteLine(number);
    CountDown(number - 1);
}
```

#### Method Components

- `number` is the value used by the recursive method.
- `if (number == 0)` is the **base case** that stops the recursion.
- `CountDown(number - 1)` is the **recursive call** that calls the method again with a modified value.

#### How the Recursion Executes

The method follows these steps:

1. Check the base case.

```csharp
if (number == 0)
{
    return;
}
```

2. If the base case is not met, execute the code block.

```csharp
Console.WriteLine(number);
```

3. Call the method again with a modified value.

```csharp
CountDown(number - 1);
```

4. Repeat until the base case is reached.

#### Execution Example

```text
CountDown(5)
→ Print 5
→ CountDown(4)

CountDown(4)
→ Print 4
→ CountDown(3)

CountDown(3)
→ Print 3
→ CountDown(2)

CountDown(2)
→ Print 2
→ CountDown(1)

CountDown(1)
→ Print 1
→ CountDown(0)

CountDown(0)
→ Base case reached
→ Stop
```

### Example: Repeating a Message

Recursion can be used to repeat an action a specific number of times.

```csharp
public static void PrintMessage(int times)
{
    if (times == 0)
    {
        return;
    }

    Console.WriteLine("Hello World");
    PrintMessage(times - 1);
}
```

```csharp
PrintMessage(3);
```

**Output:**

```text
Hello World
Hello World
Hello World
```

### Important Notes

> Every recursive method should have a **base case** that stops the recursion.
>
> Without a base case, the method will continue calling itself indefinitely.
>
> Each recursive call should move closer to the base case.
>
> Recursive solutions can often be replaced with loops.
>
> Recursion is useful when a problem can be divided into smaller versions of itself.

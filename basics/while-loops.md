# `while` Loops

### What is a `while` Loop?

> A `while` loop is a control structure that repeatedly executes a block of code as long as a specified condition remains `true`.
>
> It is commonly used when the number of iterations is not known in advance and the loop should continue until a condition becomes `false`.

### General Syntax

```csharp
while (condition)
{
    // Code block
}
```

### Example: Basic `while` Loop

A `while` loop can be used to execute a block of code repeatedly while a condition is `true`.

```csharp
int i = 0;

while (i < 5)
{
    Console.WriteLine(i);
    i++;
}
```

**Output:**

```text
0
1
2
3
4
```

### Understanding the `while` Loop

```csharp
int i = 0;

while (i < 5)
{
    Console.WriteLine(i);
    i++;
}
```

#### Loop Components

- `int i = 0` initializes the loop variable.
- `i < 5` is the condition that controls the loop.
- `i++` increases the loop variable by `1` after each iteration.

#### How the Loop Executes

The loop follows these steps:

1. Check the condition.

```csharp
i < 5
```

2. If the condition is `true`, execute the code block.

```csharp
Console.WriteLine(i);
i++;
```

3. Return to step **1** and check the condition again.

4. Repeat until the condition becomes `false`.

#### Execution Example

```text
i = 0 → Check condition → true  → Print 0 → i becomes 1
i = 1 → Check condition → true  → Print 1 → i becomes 2
i = 2 → Check condition → true  → Print 2 → i becomes 3
i = 3 → Check condition → true  → Print 3 → i becomes 4
i = 4 → Check condition → true  → Print 4 → i becomes 5
i = 5 → Check condition → false → Loop stops
```

### Example: Counting Backwards

A `while` loop can also count backwards by decreasing the loop variable.

```csharp
int i = 5;

while (i > 0)
{
    Console.WriteLine(i);
    i--;
}
```

**Output:**

```text
5
4
3
2
1
```

### Example: Searching for an Item

A `while` loop can be used to continue searching until an item is found.

```csharp
bool itemFound = false;

while (!itemFound)
{
    Console.WriteLine("Searching...");

    // Simulate finding the item
    itemFound = true;
}

Console.WriteLine("Item found.");
```

**Output:**

```text
Searching...
Item found.
```

### Example: User Input Validation

A common use case for a `while` loop is repeating an action until a valid condition is met.

```csharp
string password = "";

while (password != "CSharp123")
{
    Console.Write("Enter password: ");
    password = Console.ReadLine();
}

Console.WriteLine("Access granted.");
```

### Important Notes

> A `while` loop checks its condition before each iteration.
>
> If the condition is `false` from the beginning, the code block will never execute.
>
> The condition should eventually become `false`; otherwise, an infinite loop may occur.
>
> Unlike a `for` loop, the initialization, condition, and update expressions are typically written separately.
>
> Use a `while` loop when the number of iterations is not known in advance.

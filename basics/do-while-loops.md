# `do-while` Loops

### What is a `do-while` Loop?

> A `do-while` loop is a control structure that executes a block of code first and checks the condition afterwards.
>
> Unlike a `while` loop, a `do-while` loop always executes at least once, even if the condition is `false`.

### General Syntax

```csharp
do
{
    // Code block
}
while (condition);
```

### Example: Basic `do-while` Loop

A `do-while` loop can be used to execute a block of code repeatedly until a condition becomes `false`.

```csharp
int i = 0;

do
{
    Console.WriteLine(i);
    i++;
}
while (i < 5);
```

**Output:**

```text
0
1
2
3
4
```

### Understanding the `do-while` Loop

```csharp
int i = 0;

do
{
    Console.WriteLine(i);
    i++;
}
while (i < 5);
```

#### Loop Components

- `do` marks the beginning of the loop.
- `Console.WriteLine(i);` is the code that will be executed.
- `i++` updates the loop variable after each iteration.
- `while (i < 5)` is the condition checked after the code block has been executed.

#### How the Loop Executes

The loop follows these steps:

1. Execute the code block.

```csharp
Console.WriteLine(i);
i++;
```

2. Check the condition.

```csharp
i < 5
```

3. If the condition is `true`, return to step **1**.

4. Repeat until the condition becomes `false`.

#### Execution Example

```text
i = 0 → Print 0 → i becomes 1 → Check condition → true
i = 1 → Print 1 → i becomes 2 → Check condition → true
i = 2 → Print 2 → i becomes 3 → Check condition → true
i = 3 → Print 3 → i becomes 4 → Check condition → true
i = 4 → Print 4 → i becomes 5 → Check condition → false
Loop stops
```

### Example: First Attempt Always Allowed

A `do-while` loop is useful when an action should happen at least once before checking a condition.

```csharp
bool retry = false;

do
{
    Console.WriteLine("Attempting connection...");
}
while (retry);
```

**Output:**

```text
Attempting connection...
```

### Example: User Input Validation

A common use case for a `do-while` loop is asking for user input until valid data is entered.

```csharp
string password;

do
{
    Console.Write("Enter password: ");
    password = Console.ReadLine();
}
while (password != "CSharp123");

Console.WriteLine("Access granted.");
```

### `while` vs. `do-while`

| Loop | Condition Checked |
|--------|------------------|
| `while` | Before the code block executes |
| `do-while` | After the code block executes |

#### Example

```csharp
int number = 10;

while (number < 5)
{
    Console.WriteLine(number);
}
```

**Output:**

```text
(nothing)
```

The condition is already `false`, so the code block never executes.

```csharp
int number = 10;

do
{
    Console.WriteLine(number);
}
while (number < 5);
```

**Output:**

```text
10
```

The code block executes once before the condition is checked.

### Important Notes

> A `do-while` loop always executes at least once.
>
> The condition is evaluated after each iteration.
>
> If the condition becomes `false`, the loop terminates.
>
> A semicolon `;` is required after the `while` condition.
>
> Use a `do-while` loop when the code should run at least once before checking a condition.
`

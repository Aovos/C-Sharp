# `foreach` Loops

### What is a `foreach` Loop?

> A `foreach` loop is a control structure that iterates through every element in a collection or array.
>
> It provides a simple and readable way to access each element without manually managing an index variable.

### General Syntax

```csharp
foreach (DataType item in collection)
{
    // Code block
}
```

### Example: Basic `foreach` Loop

A `foreach` loop can be used to iterate through all elements of an array.

```csharp
string[] cars = { "Volkswagen", "BMW", "Audi" };

foreach (string car in cars)
{
    Console.WriteLine(car);
}
```

**Output:**

```text
Volkswagen
BMW
Audi
```

### Understanding the `foreach` Loop

```csharp
string[] cars = { "Volkswagen", "BMW", "Audi" };

foreach (string car in cars)
{
    Console.WriteLine(car);
}
```

#### Loop Components

- `string[] cars` is the collection being iterated.
- `string car` represents the current element.
- `in` connects the current element to the collection.

#### Choosing the Loop Variable Name

The loop variable should describe the type of element being processed.

A common convention is to use the singular form of the collection name.

```csharp
string[] cars = { "Volkswagen", "BMW", "Audi" };

foreach (string car in cars)
{
    Console.WriteLine(car);
}
```

- Collection: `cars`
- Current element: `car`

Another example:

```csharp
int[] numbers = { 10, 20, 30 };

foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

- Collection: `numbers`
- Current element: `number`

You can technically use any valid variable name:

```csharp
foreach (string x in cars)
{
    Console.WriteLine(x);
}
```

However, meaningful names such as `car`, `number`, `student`, or `person` make the code easier to read and understand.

#### How the Loop Executes

The loop follows these steps:

1. Take the first element from the collection.

```csharp
"Volkswagen"
```

2. Store it in the loop variable.

```csharp
car = "Volkswagen"
```

3. Execute the code block.

```csharp
Console.WriteLine(car);
```

4. Move to the next element and repeat.

5. Stop when all elements have been processed.

#### Execution Example

```text
car = "Volkswagen" → Print Volkswagen
car = "BMW"        → Print BMW
car = "Audi"       → Print Audi
No more elements   → Loop stops
```

### Example: Iterating Through Numbers

A `foreach` loop can also be used with arrays of numbers.

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };

foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

**Output:**

```text
10
20
30
40
50
```

### Example: Calculating a Sum

A common use case is processing every element in a collection.

```csharp
int[] numbers = { 10, 20, 30, 40 };

int sum = 0;

foreach (int number in numbers)
{
    sum += number;
}

Console.WriteLine($"Sum: {sum}");
```

**Output:**

```text
Sum: 100
```

### `for` vs. `foreach`

| Loop | Best Used When |
|--------|-------------|
| `for` | You need access to the element index or want full control over the iteration |
| `foreach` | You simply need to process every element in a collection |

### Important Notes

> A `foreach` loop automatically iterates through all elements of a collection.
>
> No counter variable is required.
>
> The elements are processed in the order they appear in the collection.
>
> The loop stops automatically after the last element has been processed.
>
> By convention, the loop variable is usually the singular form of the collection name (e.g., `car` in `cars`, `student` in `students`).
>
> Use a `foreach` loop when you do not need the element index.

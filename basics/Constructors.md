# `Constructors` in C#

### What is a `Constructor`?

> A `constructor` is a special block of code in a class that is called when a new object of that class is created.
>
> The main purpose of a `constructor` is to set the initial states of the object's attributes and to initialize resources.
>
> `Constructors` always have the exact same name as the class and do not have any return type, not even `void`.

### General Syntax

```csharp
public class ClassName 
{
    // Class properties
    public DataType PropertyName { get; set; }

    // Constructor
    public ClassName(DataType parameter) 
    {
        PropertyName = parameter;
    }
}
```

### Example: `Constructor`

`Constructors` allow parameters to be passed in to initialize the properties of an object at the exact time of its creation.

```csharp
// Creating a new Car object using the constructor
Car myCar = new Car("Volkswagen", "Golf", 2020);
myCar.Display();

public class Car 
{
    // C# Properties
    public string Brand { get; set; }
    public string Model { get; set; }
    public int Year { get; set; }

    // Constructor
    public Car(string brand, string model, int year) 
    {
        Brand = brand;
        Model = model;
        Year = year;
    }

    // C# Method (PascalCase and separate line for braces)
    public void Display() 
    {
        // Modern C# String Interpolation
        Console.WriteLine($"Brand: {Brand}, Model: {Model}, Year: {Year}");
    }
}
```

**Output:**
```text
Brand: Volkswagen, Model: Golf, Year: 2020
```

### Important Notes

> A `constructor` is automatically invoked when the `new` keyword is used to instantiate an object.
>
> If you do not write any `constructor`, C# automatically provides a hidden, no-argument **Default `Constructor`**.
>
> As soon as you define at least one custom `constructor`, the automatic default `constructor` disappears.
>
> In C#, `constructors` usually initialize **Properties** rather than raw fields, which often makes the `this` keyword unnecessary if casing (PascalCase vs. camelCase) separates them clearly.
>
> A class can have multiple `constructors` with different parameter lists (known as **`Constructor` Overloading**).

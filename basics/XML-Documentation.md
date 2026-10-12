# XML Documentation in C#

### What is XML Documentation?

> XML Documentation is a built-in feature in C# that allows developers to generate HTML or XML documentation directly from special comments written in the source code.
>
> It helps developers understand classes, methods, properties, and fields via IntelliSense in IDEs (like Visual Studio or Rider) without reading the implementation details.
>
> XML documentation comments are written using the `///` syntax and use XML tags to structure the information.

### XML Class Documentation

```csharp
/// <summary>
/// The Javadoc class represents a brief description of the class.
/// </summary>
/// <remarks>
/// Optional: Additional detailed information about the class goes here.
/// </remarks>
class SampleClass
{
    //...
}
```

### XML Method Documentation

```csharp
//...

/// <summary>
/// Adds two numbers together.
/// </summary>
/// <remarks>
/// This method takes two double values as parameters and returns their sum.
/// It can be used for basic arithmetic operations in a calculator application.
/// </remarks>
/// <param name="num1">The first number to be added.</param>
/// <param name="num2">The second number to be added.</param>
/// <returns>The sum of num1 and num2.</returns>
public double Add(double num1, double num2)
{
    return num1 + num2;
}

//...
```

### Core XML Documentation Tags

| Tag | Description |
|------|------------|
| `<summary>` | A brief description of the type (class, interface) or member (method, property) |
| `<remarks>` | Detailed narrative descriptions supplementing the summary |
| `<param>` | Describes a method's parameter (requires a `name` attribute) |
| `<returns>` | Describes the return value of a method |
| `<exception>` | Documents which exceptions a method can throw (requires a `cref` attribute) |
| `<see>` | Inserts an inline link to another type or member (uses `cref="..."`) |
| `<seealso>` | Places a link in the "See Also" section at the end of the documentation |
| `<c>` | Marks a brief text fragment as code (similar to `<code>` inline) |
| `<code>` | Marks multiple lines of text as code snippets |
| `<value>` | Describes a property's value |
| `<paramref>` | Refers to a parameter name within other tags (uses `name="..."`) |
| `<typeparam>` | Describes a generic type parameter for generic classes or methods |


### Important Notes

> XML documentation comments must begin with `///` and are placed directly above the code element.
>
> The compiler can validate these tags and extract them into a `.xml` file during the build process, which can then be converted into HTML using tools like DocFX or Sandcastle.
>
> Tags like `<param>` and `<exception>` use attributes like `name` and `cref` to reference code elements, allowing the IDE to automatically rename them during refactoring.
>
> Unlike Java, C# does not have standard built-in tags for `@author` or `@version`; this metadata is typically handled via source control (Git) or project configuration (`.csproj`).
>
> Clear and well-written XML comments directly power IDE IntelliSense, showing tooltips to other developers while they type.

# Modifier

### Access Modifiers

| Modifier    | Description                                                          |
|-------------|----------------------------------------------------------------------|
| `public`    | The element is accessible from anywhere                              |
| `protected` | The element is accessible within the same class and derived classes  |
| `private`   | The element is accessible only within the same class                 |
| `internal`  | The element is accessible only within the same assembly              |

### Non-Access Modifiers

| Modifier   | Description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| `static`   | The element belongs to the class rather than instances of the class and can be accessed without creating an object |
| `readonly` | The value can only be assigned during declaration or within a constructor                   |
| `const`    | The value is constant and must be assigned at compile time                                  |
| `abstract` | Used for classes and methods that must be extended or implemented by derived classes        |
| `sealed`   | Prevents a class from being inherited or a method from being overridden                     |
| `virtual`  | Allows a method to be overridden in a derived class                                         |
| `override` | Provides a new implementation of a virtual or abstract member inherited from a base class   |

# Data-Types

### Introduction

> In C#, primitive data types are the most basic data types that represent single values.
>
> They are predefined by the language and are used to store simple data such as numbers, characters, and truth values.
>
> Primitive data types can be categorized into several groups based on their characteristics:
> integer types, floating-point types, character types, and boolean types.
>
> Below are tables that organize these data types by their groups and sort them by size within each group.
>
> This organization provides a clear overview of the primitive data types in C#, their sizes, and their respective descriptions and examples.

### Integer Types

| Data Type | Size (in Bits) | Description                                                                        | Example            |
|-----------|----------------|------------------------------------------------------------------------------------|--------------------|
| sbyte     | 8              | Signed integer value ranging from -128 to 127                                     | sbyte b = 100;     |
| byte      | 8              | Unsigned integer value ranging from 0 to 255                                      | byte b = 100;      |
| short     | 16             | Signed integer value ranging from -32,768 to 32,767                               | short s = 1000;    |
| ushort    | 16             | Unsigned integer value ranging from 0 to 65,535                                   | ushort us = 1000;  |
| int       | 32             | Signed integer value ranging from -2,147,483,648 to 2,147,483,647                 | int number = 10;   |
| uint      | 32             | Unsigned integer value ranging from 0 to 4,294,967,295                            | uint u = 10;       |
| long      | 64             | Signed integer value ranging from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | long l = 100000L; |
| ulong     | 64             | Unsigned integer value ranging from 0 to 18,446,744,073,709,551,615              | ulong ul = 100000UL; |

### Floating-Point Types

| Data Type | Size (in Bits) | Description                            | Example             |
|-----------|----------------|----------------------------------------|---------------------|
| float     | 32             | Single-precision floating-point number | float f = 5.75f;    |
| double    | 64             | Double-precision floating-point number | double pi = 3.14;   |
| decimal   | 128            | High-precision decimal number          | decimal d = 5.75m;  |

### Character Type

| Data Type | Size (in Bits) | Description              | Example            |
|-----------|----------------|--------------------------|--------------------|
| char      | 16             | Single Unicode character | char letter = 'A'; |

### Boolean Type

| Data Type | Size (in Bits) | Description                           | Example                |
|-----------|----------------|---------------------------------------|------------------------|
| bool      | 8              | Represents a truth value (true/false) | bool isTrue = true;    |

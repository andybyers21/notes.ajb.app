---
layout: note
title: Var Data Type and Anonymous Type
parent: C#
grand_parent: Home
---

# Var Data Type and Anonymous Type

`var` is used to declare an implicitly typed _local_ variable, basically this means that the computer has to figure out what type of variable it is at completion time. It can make your code smaller, more structured and standardized, and easier to maintain by allowing you to replace explicit [[Simple Types]] (`int, bool, string` etc.) with a universal keyword.

When using var you need to give the compiler enough information in the assigned value to determine the correct type to be assigned. [[Number Types]] should be given the correct literal suffix so that the compiler can understand.

**A var variable must be initialized at the time of declaration.** For example:

```cs
var str = "hello";
var num = 21;
var anotherNum = 4.5;
var yetMore = 3.0M;
```

On compile will be converted to:

```cs
string str = "hello";
int num = 21;
double anotherNum = 4.5;
decimal yetMore = 3.0M;
```

## When to use Var?

- `var` is only applicable under local scope where declaration and initiation are in the same place.

- Since compiler has to know data type immediate based upon data to be assigned. If the variable is not immediately assigned then compiler will throw an error.

- `var` cannot be used at class or global level.

- `var` cannot be used in initialization expression

Use implicit typing for local variables when the type of the variable is obvious from the right side of the assignment, or when the precise type is not important. Use of var is encouraged if it aids readability by avoiding type names that are noisy, obvious, or unimportant:

When the type is obvious:

```cs
// in the declaration.
var var1 = "This is clearly a string.";
var var2 = 27;
var var3 = Convert.ToInt32(Console.ReadLine());
var apple = new Apple();
var request = Factory.Create<HttpRequest>();
```

For transient variables that are only passed directly to other methods, e.g:

```cs
var item = GetItem(); ProcessItem(item);
```

## When NOT to use var

**Do not use implicit typing to determine the type of the loop variable in foreach loops.**

Do not use var when the type is not apparent from the right side of the assignment. When the type of a variable is not clear from the context, use an explicit type.

```cs
int var4 = ExampleClass.ResultSoFar();
```

Do not rely on the variable name to specify the type of the variable.

```cs
// Naming the following variable inputInt is misleading.
// It is a string?
var inputInt = Console.ReadLine();
Console.WriteLine(inputInt);
```

## When var is discouraged:

Working with basic types:

```cs
var success = true;
```

Working with compiler-resolved built-in numeric types:

```cs
var number = 12 * ReturnsFloat();
```

When users would clearly benefit from knowing the type:

```cs
var listOfItems = GetList();
```

---

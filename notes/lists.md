---
layout: note
title: Lists
parent: C-Sharp
grand_parent: Home
---

# Lists

Create a new variable.
(Note, `List<type>` == `(List<T>)`):

```cs
var names = new List<string> { "<name>", "Ana", "Felipe" };
```

For each "name" in names, print to the console.
(NOTE: `<name>` will default to item if not present):

```cs
foreach (var name in names)
{
  Console.WriteLine($"Hello {name.ToUpper()}!");
}
// Hello <NAME>!
// Hello ANA!
// Hello FELIPE!
```

Modify the List.
(`.Add` will add the name to the end of a list):

```cs
Console.WriteLine();
names.Add("Bill"); // to the end of the list
names.Add("George");
names.Remove("Ana");
foreach (var name in names) // var name, you are declaring the variable name of the elements.
{
  Console.WriteLine($"Hello {name.ToUpper()}!");
}
// Hello <NAME>!
// Hello FELIPE!
// Hello BILL!
// Hello GEORGE!
```

Referance items by index:

```cs
Console.WriteLine($"My name is {names[0]}."); // My name is <name>.
Console.WriteLine($"I've added {names[2]} and {names[3]} to the list."); // I've added Bill and George to the list.
```

Check how long the list is using the "count" property:

```cs
Console.WriteLine(names.Count()); // 4
```

`IndoxOf();` returns the list position of an element (the "index of"):

```cs
Console.WriteLine(IndoxOf("Bill")); // 2
```

```cs
var whereIsFil = names.IndexOf("Felipe");
if (whereIsFil != -1)
  Console.WriteLine($"The name {names[whereIsFil]} is at index {whereIsFil}"); // The name Felipe is at index 1
```

```cs
var notFound = names.IndexOf("Not Found");
  Console.WriteLine($"When an item is not found, IndexOf returns {notFound}"); // When an item is not found, IndexOf returns -1
```

The "Sort" method can be used to sort items in a list to their normal order.
(Normal order is alphabetically for strings. Numeric order for numbers):

```cs
names.Sort();
foreach (var name in names);

Console.WriteLine($"Hello {name.ToUpper()}!");
// Hello < NAME > !
// Hello BILL!
// Hello FELIPE!
// Hello GEORGE!
```

---

---
layout: note
title: Strings
parent: C-Sharp
grand_parent: Home
---

# Handling strings in C-Sharp

Variables in C-Sharp are typed:

```cs
string hello = "Hello Baby";
Console.WriteLine(hello);
```

**String Interpolation:**

```cs
string myDog = "Dave";
Console.WriteLine($"Hello {myDog}"); // "Hello Dave"
```

As long as the expression inside of the `{ }` produces a value it will work, for example `{ 2 + 2 }`. However it is much more common to use a variable making it much easier to manipulate should you need to in the future.

**String [[Methods]]:**

```cs
string someText = "      Here lies some text       ";
```

**.Trim:**

```cs
Console.WriteLine(someText.Trim()); // "Here lies some text"
Console.WriteLine(someText.TrimStart()); // "Here lies some text      "
Console.WriteLine(someText.TrimEnd()); // "      Here lies some text"
```

**.Replace:**

```cs
Console.WriteLine(sometext.Replace("lies", "is")); // "Here is some text"
```

**Case manipulation:**

```cs
Console.WriteLine(sometext.ToUpper());
Console.WriteLine(sometext.ToLower());
```

**Search strings => Return booleans:**

```cs
string aBlockOfText = "Friendship is everything. Friendship is more than talent. It is more than the government. It is almost the equal of family.- Don Corleone";

Console.WriteLine(aBlockOfText.Contains("Friendship")); // true
Console.WriteLine(aBlockOfText.Contains("shotguns")); // false
// is case sensitive:
Console.WriteLine(aBlockOfText.Contains("FRIENDSHIP")); // false

Console.WriteLine(aBlockOfText.StartsWith("Friendship")); // true
Console.WriteLine(aBlockOfText.StartsWith("government")); // false
Console.WriteLine(aBlockOfText.EndsWith("Corleone")); // true

Console.WriteLine(aBlockOfText.StartsWith("friendship")); // false
```

_NOTE that when searching strings that full sentences will probably end with a period "."_

---

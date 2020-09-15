---
layout: note
title: Numbers
parent: C#
nav_exclude: true
---
# Numbers
Numbers in C# have BODMAS precedence. 
Division will return only a whole number (definition of an integer).
```cs
int a = 5;
int b = 4;
int c = 5 / 4;
Console.WriteLine(c); // 1
```

Use `%` to find remainders, e.g:
```cs
int d = 5 % 4;
Console.WriteLine($"{c} remainder: {d}"); // 1 remainder: 1
```

Use the "double" type to represent floating point numbers:
```cs
double a = 5;
double b = 4;
double c = 2;
double d = (a + b) / c;
Console.WriteLine(d); // 4.5
```
- Double-precision is the use of twice the binary digits to compute the sum (Single precision numbers are declared using the "float" keyword). 


`Math.PI;` is a public const double. E.g, Find the radius of a circle:

```cs
double Radius = 2.5;
double area = (Radius * Radius) * Math.PI;
Console.WriteLine(area); // 19.6349540849362
```

### [[Number Types]]## Backlinks
* [[Number Types]]
	* ([[Numbers]]).
* [[Default Values]]
	* Thee default value of all [[Numbers]] is `0`.


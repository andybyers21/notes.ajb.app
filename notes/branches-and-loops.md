---
layout: note
title: Branches and Loops
parent: C-Sharp
grand_parent: Home
---

# Branches and Loops

## If...Else Statements

_(One time evaluation statements)_
If...else statements are commonly written as follows:

```cs
int a = 5;
int b = 3;
int c = 4;
if ((a + b + c > 10) && (a == b))
{
  Console.WriteLine("The answer is greater than 10");
  Console.WriteLine("And the first number is equal to the second");
}
else
{
  Console.WriteLine("The answer is not greater than 10");
  Console.WriteLine("Or the first number is not equal to the second");
}
```

_Recursive Bugs_ - Returning to the method in an if else statement is a bad idea, the code will create a copy of the method in the stack causeing a stack overflow.
Brackets are not required when there is only one condition:

```cs
if (index != -1)
  Console.WriteLine($"The name {names[index]} is at index {index}");
```

## While loops

Checks a condition and executes code while the condition is true:

```cs
int counter = 0;
while (counter < 10)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
  counter++;
}
```

do...while loops - executes the code first, then checks the condition:

```cs
int counter = 0;
do
{
  Console.WriteLine($"Hello World! The counter is {counter}");
  counter++;
} while (counter < 10);
```

Note;

```cs
int counter = 0;
while (counter < 10)
```

Can be written as;

```cs
while (counter++ < 10)
```

## For loops

```cs
for (int counter = 0; counter < 10; counter++)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
}
```

For loops can be nested:

```cs
for (int row = 0; row < 10; row++)
{
  for (char column = 'a'; column < 'k'; column++)
  {
    Console.WriteLine($"The cell is ({row}, {column})");
  }
}
```

For example, find the sum of all int's divisible by 3:

```cs
int sum = 0;
for (int i = 1; i <= 20; i++)
{
  if (i % 3 == 0)
  {
    sum = sum + i;
  }
}

Console.Write(sum);
```

---

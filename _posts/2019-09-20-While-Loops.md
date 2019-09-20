---
layout: post
title: While Loops
categories: C# Programming Iteration
---
While loops are another type of iteration. They execute while a condition is met.
```csharp
int x = 0;
while (x<=100)
{
  Console.WriteLine(x);
  x++;
}
Console.Readline();
```
While x is less than or equal to 100, the program will display the value of x, then add 1.

```csharp
int x = 0;
while (x<=100)
{
  Console.WriteLine(x);
}
Console.Readline();
```
if you leave out the 'x++;', C# may lock up causing you to lose any unsaved work as the program will never stop, don't forget to save,.

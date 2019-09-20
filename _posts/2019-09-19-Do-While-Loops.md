---
layout: post
title: Do While Loops
categories: C# Programming Iteration
---
Do While is similar to a while loop, however unlike a while loop, the command will always be executed at least once.
```csharp
int x = 4;
do
{
  Console.WriteLine("Hello");
  x++;
}
while (x<3);
Console.ReadLine();
```
This will always execute at least once, even when x is greater than 3

```csharp
int x = 4;
while (x<3)
{
  Console.WriteLine("Hello");
}
Console.Readline();
```
This will never write Hello, because x is checked before the command is executed; in a Do...While loop the variable is checked after the command is executed.

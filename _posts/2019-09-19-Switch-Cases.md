---
layout: post
title: Switch/Case
categories: C# Programming
---
Switch/Case allows you to make a program do different things depending on the value of a variable. 
In certain situations it can be used instead of if statements.

```csharp
Console.WriteLine("Please neter a number from 1-3");
int x = Convert.ToInt32(Console.ReadLine());

switch (x)
{
  case 1:
    Console.WriteLine("You selected 1");
    break;
  case 2:
    Console.WriteLine("You selected 2");
    break;
  case 3:
    Console.WriteLine("You selected 3");
    break;
  default:
    Console.WriteLine("You entered the wrong number fool");
    break;
}
Console.ReadLine
```
'default' is whatever the switch case defaults to when a value out of the range of expected cases is entered.
'break' is a requirement for a switch/case to work, otherwise you will recieve a build error 

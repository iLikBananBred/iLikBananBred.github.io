---
layout: post
title: IF Statements
categories: C# Programming
---
'if' is a logical operation that compares two values, it will then produce and output based on wether or not the criteria is met
```csharp
if (mark >= 60)
{
    Console.WriteLine("PASSED");
}
```
If statements can be used in conjunction with else-if or else statements to create a series of checks
```csharp
if (mark >= 60)
{
    Console.WriteLine("PASSED");
}
else
{
    Console.WriteLine("FAILED");
}
```

---
layout: post
title: Handling Exceptions
categories: C# Programming
---
There are 2 main types of programming error, a compile (time) error or a runtume error. Time errors occur from incorrect coding (Syntax errors) whereas runtime errors allow the code to compile but crash when the code is run.
Runtime errors will cause "exceptions". An exception is a lump of data which describes something bad which has just happened and you can use it to find out why your program has just failed. Alternatively you can ignore it.
Exceptions are thrown by a program or by the run time system and if they are not caught your program will fail.

Converting a string into an integer and someone has entered "Ten" instead of "10"
Trying to access element 10 when an array is 0 to 9

You can catch potential errors using the following code.

```csharp
int i;

try
{
  i = Convert.ToInt32("one");
}

catch
{
  Console.WriteLine("Invalid Entry");
}

Console.ReadLine();
```

This will catch all exceptions but not inform the user of the nature of the exception, to solve this we use

```csharp
catch (Exception e)
{
  Console.WriteLine(e.Message);
  Console.WriteLine(e.Data);
}



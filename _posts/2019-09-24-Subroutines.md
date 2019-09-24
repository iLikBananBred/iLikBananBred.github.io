---
layout: post
title: Subroutines
categories: C# Programming
---
A subroutine is a named block of code which can be called at any point in the program by writing its name.
```csharp
public static void greeting()
{
  Console.WriteLine("Hello");
}
```
Subroutines can become even more useful when they take in arguments, for example: 
```csharp
static void Main(string[] args)
{
  greeting("Alice");
  greeting("Tayyiba");
  Console.ReadLine();
}
public static void greeting(string name)
{
  Console.WriteLine("Hello " + name); 
  Console.WriteLine("Pleased to meet you");
}
```
When the () is filled in as you call the subroutine, it defines the name variable as whatever is within the (). This is then pulled through the subroutine as a variable.
For example, this code will ask for the length of one side and produce a shape.
```csharp
static void Main(string[] args)
{
  Console.WriteLine("Enter square side length");
  int l = Convert.ToInt32(Console.ReadLine());
  square(l);
  Console.WriteLine("");
  Console.ReadLine();
}
        
public static void square(int l)
{
  string output = "";
  for (int i = 0; i < l; i++)
  {
    for (int x = 0; x < l; x++)
    {
      output = output + "#";
    }
    Console.WriteLine(output);
    output = "";
  }
```

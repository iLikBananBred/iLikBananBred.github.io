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
When you pass a variable through a subroutine, by default any changes made to that variable within the subroutine do not update the original value in the main routine.
```csharp
static void Main(string[] args)
{
  Console.WriteLine("Enter a number");
  int l = Convert.ToInt16(Console.Readline());
  square(l);
  Console.WriteLine(l);
  Console.ReadLine();
            
}

public static void multiply(int l)
{
  l = l * l;
  Console.WriteLine(l);
}
```
The two different .WriteLine(l) statements will produce two different values, this is because in the first .WriteLine(l) statement, the value for l has not changed, but in the second one in the subroutine has had its value changed.
To fix this, we use the ref argument.
```csharp
ref int l = Convert.ToInt16(Console.ReadLine());
```
```csharp
public static void multiply(ref int l)
```
This will carry over any changes made within the subroutine

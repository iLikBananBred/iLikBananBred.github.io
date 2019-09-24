---
layout: post
title: Functions
categories: C# Programming
---
A function is like a subroutine except it returns an answer, for example: random, substring, round.
Those are all examples of subroutines.
```csharp
static void Main(string[] args)
{
  int number = Convert.ToInt32(Console.ReadLine());
  int fourtimesnumber = quadruple(number);
  Console.WriteLine("Four times " + number + " is:");
  Console.WriteLine(fourtimesnumber);
  Console.ReadLine();
}

public static int quadruple(int x)
{
  int answer = x * 4;
  return answer;
}
```
A function returns a value because instead of 'public static' being followed by 'void', it is followed by a datatype.
The return line tells the function to 'return' an answer.


---
layout: post
title: String Manipulation
categories: C# Programming
---
Concatenation is when you join two string together, the '+' sybol is used to do this
```csharp
string name = "Jeb";
Console.WriteLine("Hello " + name);
```
You can use the .Length command to get the length of a string in characters
```csharp
string sample = "Pretzel"
int sampleLength= sample.Length
Console.WriteLine(sampleLength)
```

Substrings allow us to extract a chunk of each string. Each character is given a number starting from zero.
The string "Your mother" would be numbered 0-11

```csharp
srting x = "Hello Bob"
string extract = x.substring(3,4)
Console.Writeline(extract)
```

3 is where the substring starts from, this would be the second 'l'. 4 is the length of the substring. 
The substring shown above will display as 'lo B'

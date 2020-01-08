---
layout: post
title: Binary Files
categories: C# Programming Storing_Data
---
Text files cannot store any data other than strings, this is not very useful. A binary file can store any data types within itself.
Some sample variables are defined, assigned and stored below.
The library System.IO is required for binary file writing.

```csharp
int i = 25;
double d = 3.14157;
bool b = true;
string s = "I am happy";

BinaryWriter bw = new BinaryWriter(new FileStream("mydata", FileMode.Create));

bw.Write(i);
bw.Write(d);
bw.Write(b);
bw.Write(s);

bw.Close();
```

You can also call lines written in binary files and assign them as variables.
```csharp
BinaryReader bw = new BinaryReader(new FileStream("mydata", FileMode.Open));
```

Instead of using .Create we use .Open

```csharp
i = br.ReadInt32();
Console.WriteLine(i)

d = br.ReadDouble();
Console.WriteLine(d);

b = br.ReadBool();
Console.WriteLine(b);

s = br.ReadString();
Console.WriteLine(s);
br.Close();
```
A binary reader will keep track of which line it reads, incrementing after each .Read argument.
If you were to read it out of order, you may not always get an error, for example a bool may be saved as 1 or 0, which could be interpreted as an integer also


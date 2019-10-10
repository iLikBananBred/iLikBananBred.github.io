---
layout: post
title: Binary Files
categories: C# Programming Storing_Data
---
Text files cannot store any data other than strings, this is not very useful. A binary file can store any data types within itself.
Some sample variables are defined, assigned and stored below.
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

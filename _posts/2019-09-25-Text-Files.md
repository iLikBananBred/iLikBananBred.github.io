---
layout: post
title: Text Files
categories: C#, Programming, [Storing Data]
---
When you write to text files, you want to use the library System.IO. The IO stands for input output. 

```csharp
using (StreamWriter sw = new StreamWriter("TextFile.txt"))
{
  sw.WriteLine("HelloWorld");
}
```

When you wish to write to a text file, you can use the above code. The 'using' command ensures that the specified text file is opened and then closed once you are done with it.

```csharp
using (StreamReader sr = new StreamReader("TextFile.txt"))
{
  string line = sr.ReadLine();
  Console.WriteLine(line);
  Console.ReadLine();
}
```

This is the code to read a file, however, this will cause problems if you try to read a line that does not yet exist, we solve these problems by using the following code: 

```
using (StreamReader sr = new StreamReader("TextFile.txt"))
{
  string line;
  while ((line = sr.ReadLine()) != null)
  {
    Console.WriteLine(line);
  }
  Console.ReadLine();
}
```

This checks if the line exists, the 'While' statement says if the line specified is not null (non existant) then the program can read.

There is yet another possible problem with reading files, and that is if you try reading before creating a file, problems will arise, to fix this, c# has a command to check the existance of an object.

```
if (File.Exists("textFile.txt"))
{
  Console.WriteLine("File exists")
}
```


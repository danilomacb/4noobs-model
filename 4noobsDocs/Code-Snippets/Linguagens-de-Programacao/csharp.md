[Roadmap](../../../README.md)

```csharp
var names = new List<string>() { "John", "Tom", "Peter" };
foreach (string name in names)
{
  if (name == "Tom") {
    continue;
  }
  Console.WriteLine(name);
}
```

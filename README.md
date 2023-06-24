# What is Cyrus?
Cyrus *(pronounced **sigh-res**)* is a framework for building modern CLI programs with C#. It is AOT-friendly, with a focus on simplicity and nice DX.

## Installation:

```shell
dotnet add package Cyrus
```

Mr. Cli — the simple .NET framework for building command-line applications
```csharp
app.MapCommand("restore {projectPath?}", (
    CommandContext ctx,
    string projectPath = ".",
    [StandardInput] string? content = null,
    [Name("foo")] bool shouldHaveFoo,
    [Alias("q")] bool quiet = false,
) =>
{
    return $"Done! {projectPath}";
});
```

# Intro:
Cyrus *(pronounced **sigh-res**)* is a framework for building modern CLI programs with C#. It is AOT-friendly, with a focus on simplicity and nice DX.

## Features:
- 👌 Simple, elegant, minimalistic — you'll pick it up in an hour
- 💎 Inspired by ASP.NET Core's Minimal API — a familiar and elegant interface
- 🔥 Robust argument parser — compliant with `getopt`
- 💉 Support for dependency injection and .NET's configuration abstractions — use the official tried-and-tested libraries
- ⚡ Performant and meticulously optimized — Cyrus has been coded with performance and snappiness in mind
- 💨 AOT-friendly — make your fully-C# CLI program as snappy as those written in Go, Rust, etc.
- 0️⃣ Zero dependencies — Cyrus is written from scratch, no bloat whatsoever

# Installation:

You can use the [NuGet package]([url](https://www.nuget.org/packages/Cyrus/)):
```shell
dotnet add package Cyrus
```

Alternatively, you can install and then use Cyrus's project template:
```
dotnet new install Cyrus.Template
dotnet new cli
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

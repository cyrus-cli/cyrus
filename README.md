# Intro:
Cyrus *(pronounced **sigh-res**)* is a framework for building modern CLI programs with C#. It is AOT-friendly, with a focus on simplicity and nice DX.

## Features:
- Simple and minimalistic — you'll pick it up in an hour
- Inspired by ASP.NET Core's Minimal API — a familiar interface
- Robust argument parser — compliant with `getopt`
- Performant and meticulously optimized — Cyrus has been coded with performance and snappiness in mind
- AOT-friendly — make your fully-C# CLI program as snappy as those written in Go, Rust, etc.
- Zero dependencies — Cyrus is written from scratch, no bloat whatsoever

# Installation:

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

# Intro:
Cyrus *(pronounced **sigh-res**)* is a framework for building modern CLI programs with C#.

Cyrus uses source generators for everything that other frameworks resort to reflection for. That way, it creates the most optimized flow for your app for startup and runtime, and more importantly, it makes it AOT-friendly out of the box; so that your program will feel as snappy as possible and respond instantaneously when you hit *Enter*!

## Features:
- 💎 Simple, elegant, minimalistic — you'll pick it up in an hour, things just _make sense_
- 🔥 Robust and *fast* argument parser — compliant with the de-facto standard [`getopts`](https://en.wikipedia.org/wiki/Getopts)
- ✔ 100% reflection-free — to waste absolutely no time on startup!
- 💉 Support for dependency injection and .NET's configuration abstractions — use the official tried-and-tested libraries
- ⚡ Performant and meticulously optimized — being fast is Cyrus's main claim to fame!
- 💨 AOT-friendly — compile your fully-C# CLI programs to native code, making them as snappy as those written in Go, Rust, etc.
- 👌 Zero dependencies — Cyrus is written from scratch, no bloat whatsoever

# Installation:

You can use the [NuGet package](https://www.nuget.org/packages/Cyrus/):
```shell
dotnet add package Cyrus
```

Alternatively, you can install and then use Cyrus's project template:
```
dotnet new install Cyrus.Template
dotnet new cli
```

# Concepts:

### Overview:
Cyrus apps (and most command-line apps in general) consist of three components:
- **Commands** represent actions your program performs
- **Arguments** are values passed to commands
- **Options** modify the behavior of commands
For example, in a Git command like `git clone URL --bare`:
- `git` is the program/executable
- `clone` is the command
- `URL` is the argument
- `--bare` is the option/flag

### Commands:
Commands are the m

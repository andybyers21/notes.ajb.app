---
layout: note
title: .NET
parent: C-Sharp
grand_parent: Home
---

# .NET

.Net is an open source developer platform. (A platform simply means that it contains the languages and libraries needed to build your apps.) Supported languages are C-Sharp, F#, and VB.

**NuGet** is a package manager for .NET

There is a number of .NET implementations depending on what you are working on. The

color is

## .NET Core

Runs on any OS (Mac, Windows, Linux).

## .NET Framework

Supports websites and desktop app building on windows.

## Xamarin / Mono

.NET for mobile.

**When using any of the above frameworks you write in the .NET standard** for a hassle free workflow. .NET standard is a base set of API's common to all implementations. Each implementation can also expose API's that are specific to the platform you are working on.

---

## Create a .NET apps

```shell
$ dotnet new console -o appname
```

- Creates a new app with the console template.
- `-o` creates the directory 'appname'

```shell
$ dotnet run
```

Runs the application in terminal

---

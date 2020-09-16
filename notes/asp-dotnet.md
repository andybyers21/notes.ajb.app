---
layout: note
title: ASP.NET
parent: C-Sharp
grand_parent: Home
---

# ASP.NET

- Create new web app: `$ dotnet new webapp -o asp-net-core-Tutorial`

---

Trust the HTTPS development certificate:

```shell
$ dotnet dev-certs https --trust
```

This will install the the ASP.NET Core HTTPS development certificate on your system keychain. (Only required on first run or a new environment).

---

- Run the app with the following command: `dotnet watch run`. After the command has executed you can view your app at `https://localhost:5001`.

- index HTML can be modified at _Pages/Index.cshtml_

---

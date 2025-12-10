# VideoShare

ASP.NET Core & Entity Framework Core solution for a layered **video sharing** web application.

---

## Important

**Authors:** Ferran Hendriks, Nick van Hoesel

---

## Table of Contents

- [Overview](#overview)
- [Solution Structure](#solution-structure)
- [Technologies](#technologies)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
  - [Run with Visual Studio](#run-with-visual-studio)
  - [Run with .NET CLI](#run-with-net-cli)
- [Running Tests](#running-tests)
- [Further Documentation](#further-documentation)
- [About](#about)
- [Ownership & License](#ownership--license)

---

## Overview

**VideoShare** is a sample application built with **ASP.NET Core** and **Entity Framework Core**.

It demonstrates:

- A layered architecture (web UI, business logic, data access, domain entities)  
- Integration with **SQL Server** via Entity Framework Core  
- A clean solution structure suitable as a reference for similar projects  

---

## Solution Structure

The repository is organized as follows:

- `Source/` – main .NET solution and projects (including the `VideoSharing` web project)  
- `Test/VideoSharing-tests/` – test project for automated tests  
- `Docs/` – optional documentation and project-related notes  
- `Pipelines/` – CI/CD pipeline configuration (e.g., for Azure DevOps)  
- `src/` – additional source code (non-core to the ASP.NET project, currently including some Java code)  

Root configuration files:  
- `.gitignore`  
- `.gitattributes`  
- `README.md` (this file)  

---

## Technologies

- **ASP.NET Core**  
- **Entity Framework Core**  
- **.NET Core / .NET SDK**  
- **C#** (primary language)  
- **SQL Server**  

---

## Prerequisites

Originally noted:  
- Visual Studio 2017 (or higher)  
- .NET Core SDK  
- SQL Server  

In practice, a modern setup such as **Visual Studio 2019/2022** with a recent **.NET SDK** and a **SQL Server** instance (local or remote) will work fine.

---

## Getting Started

### Run with Visual Studio

1. **Clone the repository**
   ```bash
   git clone https://github.com/ferrannl/VideoShare.git
   cd VideoShare
   ```

2. **Open the solution**  
   Open `Source/VideoSharing.sln` in Visual Studio  

3. **Restore NuGet packages**  
   Visual Studio usually restores packages automatically.  
   If not, right-click the solution and choose **Restore NuGet Packages**  

4. **Set startup project**  
   Set the `VideoSharing.Web` project as the Startup Project  

5. **Configure database (if needed)**  
   - Check the connection string in the web project configuration (e.g., `appsettings.json`)  
   - Point it to your SQL Server instance  
   - Ensure the database exists and migrations (if any) are applied  

6. **Build and run**  
   - Build the solution  
   - Run the application (**F5 / Ctrl+F5**)  
   - Open the URL shown in the output (usually `https://localhost:xxxx`)  

---

### Run with .NET CLI

1. **Clone the repository**
   ```bash
   git clone https://github.com/ferrannl/VideoShare.git
   cd VideoShare
   ```

2. **Restore and build**
   ```bash
   dotnet restore Source/VideoSharing.sln
   dotnet build Source/VideoSharing.sln -c Release
   ```

3. **Configure the database**  
   Update the connection string in the `VideoSharing.Web` project configuration to point to your SQL Server  

4. **Run the web project**
   ```bash
   cd Source/VideoSharing
   dotnet run
   ```

The app will start and listen on the configured ports (shown in the console output).

---

## Running Tests

Automated tests live under `Test/VideoSharing-tests/`.  

From the repository root you can run:
```bash
dotnet test Source/VideoSharing.sln
```

This will:
- Build the solution (if needed)  
- Run all tests in the `VideoSharing-tests` project  

---

## Further Documentation

See the `Docs/` directory for additional project documentation, design notes, or diagrams related to **VideoShare**.

---

## About

This repository showcases an ASP.NET Core & Entity Framework Core application with a clean, layered architecture.  
It can be used as:

- A reference implementation  
- A starting point for similar business applications  
- A learning resource for ASP.NET Core + EF Core projects  

---

## Ownership & License

**Authors:** Ferran Hendriks, Nick van Hoesel  

No explicit license file is included.  
Assume all rights reserved unless a license is added later.
```

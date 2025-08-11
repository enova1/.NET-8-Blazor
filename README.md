# BlazorWorks – Example Blazor WebAssembly Application

⚠️ **Note:** This repo contains the *project structure and file descriptions only* — no functional code is included here. A working demo is available at:
🌐 **[Live Example](https://ctate-gbhta6fedebjfcf9.canadaeast-01.azurewebsites.net/)**

---

## 📌 Overview

**BlazorWorks** demonstrates a typical Blazor WebAssembly project layout for a small application.
The sample app’s purpose (in a working version) would be to:

* Display a list of baseball players and their statistics
* Allow adding and editing players through a reusable modal
* Display a list of employees
* Use dependency injection and service abstractions for data access
* Support swapping between **in-memory** and **API-based** data sources

Even without the code, this folder structure illustrates **best practices for separation of concerns** in Blazor.

---

## 🗂 Project Structure

```
BlazorApp1
│
├── wwwroot/                          # Static files (CSS, JS, images, favicon)
│
├── Layout/                           # App layout components
│   ├── MainLayout.razor
│   └── NavMenu.razor
│
├── Models/                           # Data models
│   ├── EmployeeAddresses.cs
│   ├── EmployeePhones.cs
│   ├── Employees.cs
│   └── Player.cs
│
├── Pages/                            # Routable pages
│   ├── Employees/                    # Employee Manager example
│   │   ├── Create.razor
│   │   ├── Edit.razor
│   │   └── Index.razor
│   ├── PlayerStats/                  # Player Stats example
│   ├── Todo/                         # Additional example
│   ├── About.razor
│   ├── Examples.razor
│   └── Home.razor
│
├── Services/                         # Business logic & data services
│   ├── AuthorizedHttpClientService.cs
│   ├── EmployeeService.cs
│   ├── IStatsService.cs
│   ├── JwtStorageService.cs
│   ├── MockStatsService.cs
│   └── PlayerApiService.cs
│
├── Shared/                           # Shared UI components
│   └── PlayerModal.razor
│
├── App.razor                         # Root component
├── Program.cs                        # App startup & DI config
└── .gitignore

```

---

## ⚙️ How It Works (Conceptually)

1. **UI Layer**

   * Pages (`/Pages`) handle routing and page-level logic.
   * Shared components (`/Shared`) provide reusable UI elements like modals and navigation.

2. **Data Models**

   * `/Models` contains POCO classes with optional validation via data annotations.

3. **Service Layer**

   * `/Services` handles all data access and business logic.
   * An interface (`IStatsService`) abstracts the implementation, allowing for different data sources (in-memory or API).

4. **Startup & DI**

   * `Program.cs` configures the app, registers services in DI, and starts the Blazor WebAssembly runtime.

---

## 🚀 Why This Example is Useful

* Demonstrates **clean separation of concerns**
* Shows **best practices for folder organization** in Blazor
* Helps new developers visualize **how Blazor apps are structured**
* Makes it easy to swap **mock data** for **real API calls**

---

## 📖 Resources for Learning Blazor

* [Blazor WebAssembly Documentation](https://learn.microsoft.com/aspnet/core/blazor/?view=aspnetcore-8.0)
* [Introduction to Razor Components](https://learn.microsoft.com/aspnet/core/blazor/components/?view=aspnetcore-8.0)
* [Dependency Injection in Blazor](https://learn.microsoft.com/aspnet/core/blazor/fundamentals/dependency-injection)



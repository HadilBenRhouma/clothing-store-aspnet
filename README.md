# Online Clothing Store — ASP.NET Core MVC 🛍️

Team school project (ENIS, 2023) with [Chaima Maalej](https://github.com/chaimamaalej): an e-commerce web application with a product catalogue, shopping cart, orders and an admin back office, built with ASP.NET Core MVC and Entity Framework Core.

![.NET 7](https://img.shields.io/badge/.NET%207-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/EF%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white)

## Features

- **Catalogue** — products by category, search, product detail pages with images
- **Shopping cart** — add / remove items, clear the cart, payment and confirmation
- **Orders** — order and order-line management
- **Accounts** — registration and login with ASP.NET Core Identity
- **Back office** — role management and user-role assignment, product and category CRUD with image upload, customer list

## Architecture

```
Controllers/        Account, Admin, Product, Category, ShoppingCart, Command, Client, User…
Models/             Entities (Product, Category, Command, CartItem, Client…) + AppDbContext
Models/Repositories Repository pattern: one interface + implementation per aggregate
ViewModels/         Form models (login, register, cart, payment, roles…)
Views/              Razor views
Migrations/         EF Core migrations
```

## Run locally

Requirements: .NET 7 SDK and SQL Server LocalDB (installed with Visual Studio).

```bash
dotnet tool install --global dotnet-ef   # once
dotnet ef database update                # creates MyProductDB from the migrations
dotnet run
```

The connection string is in `appsettings.json` (`ProductDBConnection`).

## Author

**Hadil Ben Rhouma** — [Portfolio](https://portfilio-gules-three.vercel.app/?utm_source=github) · [LinkedIn](https://www.linkedin.com/in/hadil-benrhouma/)

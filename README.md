# ASP.NET Core Department Management System

This project is a simple **Department Management Panel** built with **ASP.NET Core MVC** and **Entity Framework Core**.  
It provides full **CRUD operations** for departments stored in a SQL Server database and includes a clean admin interface using Bootstrap and a sidebar layout.

---

## Features

- ✓ List departments  
- ✓ Add new department  
- ✓ Update existing department  
- ✓ Delete department  
- ✓ Admin panel with sidebar navigation  
- ✓ Entity Framework Core (Code-First)  
- ✓ SQL Server integration  

---

## Technologies Used

- **ASP.NET Core MVC**
- **Entity Framework Core**
- **SQL Server**
- **Bootstrap 4**
- **Font Awesome**
- **Razor View Engine**

---

## Project Structure

### Controllers

#### **DepartController**
Handles all department operations:
- `PageDepartman()` — List departments  
- `YeniDepartman()` — GET/POST: Add a new department  
- `SilDepartman(int ID)` — Delete department  
- `GuncelleDepartman(int ID)` — GET/POST: Update department  

#### **HomeController**
- `Index()` — Displays all departments on the homepage.

---

### Models

#### **departmanlar**
| Property       | Type            | Description          |
|----------------|-----------------|----------------------|
| ID             | int (Primary Key) | Auto-increment       |
| DepartmanAd    | VARCHAR(50)     | Department name      |
| Detay          | VARCHAR(250)    | Description          |

#### **personel**
| Property | Type          | Description            |
|----------|---------------|------------------------|
| perid    | int (PK)      | Auto-increment         |
| ad       | VARCHAR(30)   | First name             |
| soyad    | VARCHAR(30)   | Last name              |
| sehir    | VARCHAR(50)   | City                   |
| departid | int           | Department ID (future FK) |



---

### Database Context (AppDbContext)

- `DbSet<departmanlar> GorevDepartmans`
- `DbSet<personel> Personeller`
- Uses **DefaultConnection** from `appsettings.json`
- Configured with SQL Server

---

## Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/ahmetfurkaneq/Simple-Department-Management-Dashboard-ASP.NET-Core-MVC-.git
cd WEB-PROJE-master

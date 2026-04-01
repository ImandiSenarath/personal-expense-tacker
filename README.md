    # Expense Tracker - ASP.NET Core MVC

## Project Description

Expense Tracker is a simple web application developed using **ASP.NET Core MVC** that allows users to register, log in, and manage their personal expenses. Each user can add, edit, delete, search, and filter their own expenses. The application also provides a dashboard with summary cards and charts to help users understand their spending patterns.

This project is designed as a beginner-friendly learning project to understand **MVC architecture**, **Entity Framework Core**, **SQL Server**, **authentication**, and **basic web application development** in C# using Visual Studio.

---

## Brief Description of MVC

**MVC** stands for:

- **Model**
- **View**
- **Controller**

It is a design pattern used to organize an application into three separate parts.

### 1. Model
The **Model** represents the data and business rules of the application.

Example in this project:
- `Expense`
- `User`

These classes define what data is stored in the database.

### 2. View
The **View** is the user interface of the application.  
It displays data to the user and collects user input.

Example in this project:
- Login page
- Register page
- Expense list page
- Dashboard page

### 3. Controller
The **Controller** handles user requests, communicates with the model, and returns the correct view.

Example in this project:
- `AccountController`
- `ExpenseController`
- `DashboardController`

### Simple MVC Flow
1. User interacts with the page
2. Controller receives the request
3. Controller uses Model/data
4. Controller sends result to View
5. View shows output to the user

---

## Limitations of MVC

Although MVC is very useful, it also has some limitations:


### 2. Controllers can become too large
If business logic and database logic are written directly in controllers, they can become difficult to manage.

### 3. More files and structure
MVC requires more folders and files than small simple applications, which may feel heavy for tiny projects.

### 4. Separation must be maintained properly
If developers mix logic carelessly, MVC structure loses its advantage.

### 5. Not always enough for large applications
For bigger projects, MVC alone is often not enough. Additional patterns like:
- Repository pattern
- Service pattern
- Dependency Injection
- Identity
are often needed.

---

## Features

This Expense Tracker application includes the following features:

### User Management
- User registration
- User login
- User logout
- Password hashing using BCrypt
- Multi-user support

### Expense Management
- Add expense
- Edit expense
- Delete expense
- View all personal expenses
- Category dropdown
- Search expenses by title or category
- Filter expenses by date range
- Total expense calculation

### Dashboard
- Total expense summary
- Total number of records
- Current month total
- Expense by category chart
- Monthly expense trend chart

### UI Features
- Bootstrap styled pages
- Responsive layout
- Dashboard-like summary cards
- Improved tables and forms

---

## Technologies Used

The following technologies were used in this project:

### Backend
- **C#**
- **ASP.NET Core MVC**
- **Entity Framework Core**
- **SQL Server**

### Frontend
- **Razor Views (.cshtml)**
- **HTML**
- **CSS**
- **Bootstrap**
- **JavaScript**
- **Chart.js**

### Authentication and Security
- **Session-based authentication**
- **BCrypt.Net** for password hashing

### Development Tools
- **Visual Studio**
- **NuGet Package Manager**
- **SQL Server / LocalDB**

---

## Project Structure

```text
ExpenseTracker/
│
├── Controllers/
│   ├── AccountController.cs
│   ├── DashboardController.cs
│   ├── ExpenseController.cs
│   └── HomeController.cs
│
├── Data/
│   └── AppDbContext.cs
│
├── Models/
│   ├── Expense.cs
│   ├── User.cs
│   ├── LoginViewModel.cs
│   ├── RegisterViewModel.cs
│   └── ErrorViewModel.cs
│
├── Views/
│   ├── Account/
│   │   ├── Login.cshtml
│   │   └── Register.cshtml
│   ├── Dashboard/
│   │   └── Index.cshtml
│   ├── Expense/
│   │   ├── Index.cshtml
│   │   ├── Create.cshtml
│   │   ├── Edit.cshtml
│   │   └── Delete.cshtml
│   ├── Home/
│   └── Shared/
│
├── wwwroot/
│   ├── css/
│   ├── js/
│   └── lib/
│
├── appsettings.json
├── Program.cs
└── ExpenseTracker.csproj

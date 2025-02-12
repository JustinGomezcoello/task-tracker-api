# TaskTracker.API - Backend

## 🚀 Project Overview
TaskTracker.API is a powerful and scalable backend API built with **ASP.NET Core** and **Entity Framework Core**, designed to efficiently manage task tracking with role-based access control. This API enables users to create, update, delete, and mark tasks as completed while ensuring secure authentication using **JWT (JSON Web Token)**.

## 🌟 Key Features
- **🔐 Secure Authentication**: Implements **JWT-based authentication** to manage user sessions securely.
- **🛡️ Role-Based Authorization**: Different access permissions for **Admin** and **User** roles.
- **📌 Task Management**:
  - Users can **add, update, delete**, and **mark tasks as completed**.
  - Admins have full CRUD access, while regular users have restricted permissions.
- **📡 RESTful API**: Well-structured endpoints for seamless integration with any frontend.
- **📄 Database Integration**: Uses **SQL Server** via **Entity Framework Core**.
- **📖 Swagger UI**: Interactive documentation for easy API testing.
- **🛠️ CORS Support**: Allows frontend applications to communicate with the API securely.

---

## ⚙️ Tech Stack
- **.NET 7 / .NET Core**
- **Entity Framework Core** (ORM for database interactions)
- **JWT Authentication**
- **SQL Server** (Database)
- **Swagger UI** (API documentation & testing)
- **ASP.NET Identity** (User role management)

---

## 📌 API Endpoints
### 🔑 Authentication (AuthController)
- **POST** `/api/Auth/login` → Authenticates a user and returns a JWT token.

### 📌 Task Management (TasksController)
- **GET** `/api/Tasks` → Fetch all tasks (Authenticated users only)
- **POST** `/api/Tasks` → Create a new task (**User role only**)
- **PUT** `/api/Tasks/{id}` → Update an existing task (**Admin & User roles**)
- **DELETE** `/api/Tasks/{id}` → Delete a task (**Admin role only**)
- **PATCH** `/api/Tasks/{id}/complete` → Mark a task as completed (**User role only**)

---

## 🚀 Getting Started
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-repository/TaskTracker.API.git
cd TaskTracker.API
```

### 2️⃣ Configure Database Connection
Modify the **`appsettings.json`** file to set up your **SQL Server connection string**:
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=TaskTrackerDB;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

### 3️⃣ Run Migrations & Update Database
```sh
dotnet ef database update
```

### 4️⃣ Run the API
```sh
dotnet run
```

### 5️⃣ Access Swagger UI (API Documentation)
Once the API is running, open your browser and navigate to:
```
http://localhost:5088/swagger/index.html
```

---

## 🔑 Role-Based Access Control
| Action | User | Admin |
|--------|------|-------|
| **Login & Get Token** | ✅ | ✅ |
| **View Tasks** | ✅ | ✅ |
| **Create Tasks** | ✅ | ❌ |
| **Update Tasks** | ✅ | ✅ |
| **Delete Tasks** | ❌ | ✅ |
| **Complete Tasks** | ✅ | ❌ |

---

## 📜 License
This project is licensed under the **MIT License**.

---

## 🤝 Contributing
Want to contribute? Feel free to **fork** this repository and submit a **pull request**!

---

## 📧 Contact
For any inquiries or issues, reach out at **justingomezcoello@gmail.com* or open an issue on GitHub.





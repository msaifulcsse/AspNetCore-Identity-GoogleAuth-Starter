# 🚀 ASP.NET Core Identity & Google Authentication Starter (.NET 9)

**Project Name:** OAuth2App
**Author:** M SAIFUL ISLAM (msaifulcsse)

A minimal, ready-to-use template demonstrating how to integrate **ASP.NET Core Identity (Individual Accounts)** with **Microsoft SQL Server** and configure **Google OAuth 2.0** external authentication using the latest .NET 9 framework. This project is ideal for developers starting with secure user management.

## ✨ Key Features

* **ASP.NET Core 9 MVC:** Built on the latest stable framework.
* **Identity Scaffolding:** Uses the built-in Identity UI.
* **Database:** Configured for MS SQL Server.
* **Google Authentication:** Pre-configured Google OAuth 2.0 setup.

---

## 🛠️ Getting Started

### 1. Prerequisites

* .NET 9 SDK (or later)
* SQL Server (LocalDB, Express, or remote instance)

### 2. Configuration (`appsettings.json`)

Update your `appsettings.json` with your database connection details and Google API credentials.

**A. Database Connection String**

Modify the `DefaultConnection` string. **IMPORTANT:** For local development, it's highly recommended to add `TrustServerCertificate=True` to bypass SSL certificate errors.

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=oauth2_db_dev;User Id=YourDbUser;Password=YourDbPassword;MultipleActiveResultSets=true;TrustServerCertificate=True"
},
````

**B. Google Authentication Secrets**

Set your Client ID and Client Secret obtained from the Google Developer Console.

```json
"Authentication": {
  "Google": {
    "ClientId": "YOUR_GOOGLE_CLIENT_ID_HERE.apps.googleusercontent.com",
    "ClientSecret": "YOUR_GOOGLE_CLIENT_SECRET_HERE"
  }
}
```

### 3\. Run Database Migrations

From the project root directory (`OAuth2App/`):

```bash
# Apply all pending migrations to the SQL Server database
dotnet ef database update
```

### 4\. Run the Application

```bash
dotnet run
```

-----

## 🌐 Connect with the Author

  * **Name:** M SAIFUL ISLAM
  * **Email:** saifulbdjoy@gmail.com
  * **GitHub:** [msaifulcsse](https://github.com/msaifulcsse/)
  * **LinkedIn:** [linkedin.com/in/msaifulcsse](https://www.google.com/search?q=https://linkedin.com/in/msaifulcsse)
  * **Contact:** +8801750-5333131

-----

## ⚖️ License

See the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

````
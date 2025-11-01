# 🚀 ASP.NET Core 9 Identity + Google OAuth2 Starter

### ✅ `OAuth2App` — Secure Login (Identity + Google Login) | SQL Server | .NET 9 MVC

A production-ready starter template that integrates:

- 🔐 **ASP.NET Core Identity (Individual Accounts)**
- 🌐 **Google OAuth 2.0 Authentication**
- 🧠 **ASP.NET Core MVC (.NET 9)**
- 🗄️ **Microsoft SQL Server**
- 🎯 **Fully Ready Authentication system with Login/Register UI**
- 🏗️ Identity scaffolding option to customize UI

Perfect for developers looking to build **secure enterprise-ready authentication systems** fast.

---

## ✨ Features

| Feature | Description |
|-------|------------|
🔑 Authentication | ASP.NET Identity + Google OAuth2  
💾 Database | SQL Server (Local/Cloud)  
🌍 Framework | .NET 9 MVC  
📁 Identity UI | Built-in + scaffolding support  
⚙️ Configurable | appsettings.json based setup  
🏁 Ready to Run | Just migrate DB + run project  

---

## 📁 Project Structure

```

OAuth2App/
├── Controllers/
├── Data/
├── Views/
├── appsettings.json
└── Program.cs

````

---

## 🧰 Prerequisites

| Tool | Version |
|------|--------|
✅ .NET SDK | **9.x**  
✅ SQL Server | LocalDB / Express / Remote  
✅ EF Core Tools | `dotnet tool install`  

---

## ⚙️ Setup Guide

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/msaifulcsse/AspNetCore-Identity-GoogleAuth-Starter.git
cd AspNetCore-Identity-GoogleAuth-Starter/OAuth2App
````

---

### 2️⃣ Update Database Connection

Edit `appsettings.json` 👇

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=oauth2_db_dev;User Id=YOUR_DB_USER;Password=YOUR_DB_PASSWORD;MultipleActiveResultSets=true;TrustServerCertificate=True"
}
```

> ⚠ Replace with your SQL credentials

---

### 3️⃣ Configure Google OAuth Credentials

#### ➤ Go to Google Cloud Console

[https://console.cloud.google.com/](https://console.cloud.google.com/)

**Path:**
`APIs & Services > Credentials > Create Credentials > OAuth client ID`

Set:

| Key                     | Value                                  |
| ----------------------- | -------------------------------------- |
| Application type        | Web application                        |
| Authorized redirect URI | `https://localhost:5001/signin-google` |

✅ Copy **Client ID** & **Client Secret** → put in `appsettings.json`

```json
"Authentication": {
  "Google": {
    "ClientId": "YOUR_CLIENT_ID",
    "ClientSecret": "YOUR_CLIENT_SECRET"
  }
}
```

---

### 4️⃣ Run EF Core Migration

```bash
dotnet tool install --global dotnet-ef
dotnet ef database update
```

> Creates Identity tables + DB

---

### 5️⃣ Run the App 🚀

```bash
dotnet run
```

Open Browser:

```
https://localhost:5001
```

Login → you'll see **Google Sign-In button** ✅

---

## 🛠 Optional: Scaffold Identity Pages (for customization)

```bash
dotnet aspnet-codegenerator identity -dc OAuth2App.Data.ApplicationDbContext
```

This generates:

* Login.cshtml
* Register.cshtml
* Manage pages
* Account controllers

> Edit UI / policies / password rules as needed 🎨

---

## 📸 Preview (Auth Flow)

| Screen         | Description                      |
| -------------- | -------------------------------- |
| 🔐 Login       | Username/Password + Google Login |
| 📝 Register    | Individual account creation      |
| 🎫 Identity DB | MSSQL tables created by EF       |

---

## 🧪 Test Credentials

✅ Local account signup
✅ Google login
✅ Email verified usage supported

---

## 🧠 Pro Tip

Add role support after setup:

```csharp
services.AddDefaultIdentity<IdentityUser>()
    .AddRoles<IdentityRole>()
    .AddEntityFrameworkStores<ApplicationDbContext>();
```

---

## 📞 Contact / Community

| Contact     | Link                                                                       |
| ----------- | -------------------------------------------------------------------------- |
| 👤 Name     | **M SAIFUL ISLAM**                                                         |
| 📧 Email    | [saifulbdjoy@gmail.com](mailto:saifulbdjoy@gmail.com)                      |
| 🌐 GitHub   | [https://github.com/msaifulcsse](https://github.com/msaifulcsse)           |
| 🔗 LinkedIn | [https://linkedin.com/in/msaifulcsse](https://linkedin.com/in/msaifulcsse) |
| 📱 Phone    | +8801750-533313                                                            |

---

## 🧾 License

MIT License — Use freely. Credit appreciated ❤️

---
# CommBank Server

A RESTful banking backend built with **C# / ASP.NET Core 6** and **MongoDB**. The API manages users, accounts, transactions, tags, and goal-based financial tracking.

## Tech Stack

- C# / .NET 6
- ASP.NET Core Web API
- MongoDB Atlas
- MongoDB.Driver
- Swagger / OpenAPI
- BCrypt.Net

## Features

- REST APIs for users, accounts, transactions, tags, and financial goals
- MongoDB persistence through Atlas
- Goal tracking with target amount, target date, balance, and transactions
- Optional public `Icon` field for goals
- CORS support and Swagger-based API exploration

## Local Setup

1. Install the .NET 6 SDK.
2. Clone the repository.
3. Create a local `CommBank-Server/Secrets.json` file using the template below.
4. Add your MongoDB Atlas connection string.
5. Restore and run the API.

### Secrets.json

```json
{
  "ConnectionStrings": {
    "CommBank": "YOUR_MONGODB_CONNECTION_STRING"
  }
}
```

> `Secrets.json` is intentionally ignored by Git and must never be committed with real credentials.

## Run

```powershell
dotnet restore
dotnet run --project .\CommBank-Server\CommBank.csproj
```

The API runs on the local HTTP endpoint shown by ASP.NET Core at startup.

## Project Context

This repository is a backend implementation exercise focused on connecting a .NET REST API to MongoDB and extending the Goal data model with an optional public icon field.

# TaskManager API

Full-stack Task Manager SaaS backend — ASP.NET Core 8, Clean Architecture, EF Core, PostgreSQL, JWT authentication. Deployed on Azure with CI/CD via GitHub Actions.

🔗 **Live API (Swagger):** https://taskmanager-api-ss-gtgdhqgwgugebnhx.centralindia-01.azurewebsites.net/swagger/index.html
🔗 **Live app (frontend):** https://yellow-mushroom-0ffe14400.7.azurestaticapps.net
🔗 **Frontend repo:** https://github.com/ss235/TaskManager.Client
## Architecture

Clean Architecture with 4 layers:
- **Domain** — entities, enums (TaskItem, User, Priority, TodoStatus)
- **Application** — service interfaces, DTOs
- **Infrastructure** — EF Core, PostgreSQL, repositories, migrations
- **API** — controllers, JWT auth, Swagger

## Tech stack

ASP.NET Core 8 · Entity Framework Core · PostgreSQL · JWT Bearer Auth · Azure App Service · Azure Database for PostgreSQL · GitHub Actions CI/CD

## Features

- User registration & login with JWT authentication
- Task CRUD, scoped per authenticated user
- Task priority and status tracking
- Automated build & deploy pipeline on every push to `main`

## Local setup

1. Clone the repo
2. Update connection string via `dotnet user-secrets` (see below)
3. Run migrations: `dotnet ef database update --project TaskManager.Infrastructure --startup-project TaskManager.API`
4. `dotnet run --project TaskManager.API`


## CI/CD

GitHub Actions builds and deploys to Azure App Service on every push to `main`. See `.github/workflows/`.

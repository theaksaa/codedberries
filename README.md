# Codedberries

Codedberries is a university team project management web application built with Angular and .NET. The goal of the application is to help project managers and team members organize projects, manage tasks, assign responsibilities, follow progress, and collaborate more efficiently.

The project was inspired by tools such as Asana and Jira, and was developed as a student team project.

## Project Overview

The application is divided into two main parts:

- Frontend: Angular application located in `Src/FE/angular-app`
- Backend: ASP.NET Core Web API located in `Src/BE/Codedberries/Codedberries`

The backend uses SQLite through Entity Framework Core, exposes REST API endpoints, enables Swagger in development, and includes SignalR support for real-time features.

## Main Features

- User authentication and session handling
- Project creation and project overview
- Task creation, editing, filtering, and tracking
- Task dependencies
- Milestones
- Project roles and permissions
- Team member assignment and collaboration
- Comments and activity tracking
- Priorities, statuses, and categories
- User invitations
- Progress tracking and reporting

## Technology Stack

- Angular 17
- Angular Material
- .NET 8 / ASP.NET Core Web API
- Entity Framework Core
- SQLite
- SignalR
- Docker and Docker Compose

## Repository

Clone the project from GitHub:

```bash
git clone https://github.com/theaksaa/codedberries.git
```

## Project Structure

```text
codedberries/
|-- Src/
|   |-- FE/angular-app          # Angular frontend
|   |-- BE/Codedberries/...     # .NET backend
|   `-- docker-compose.yaml     # Container setup
|-- Documentation/              # Additional project documentation
|-- Sandbox/                    # Experimental/team work folders
`-- Uputstvo za upotrebu alata.pdf
```

## Requirements

To run the project locally, install:

- Node.js and npm
- Angular CLI
- .NET 8 SDK

Angular CLI can be installed with:

```bash
npm install -g @angular/cli
```

## Running the Project Locally

The easiest way to run the project for development is to start the backend and frontend separately in two terminals.

### 1. Start the backend

Open a terminal in:

```bash
Src/BE/Codedberries/Codedberries
```

Run:

```bash
dotnet restore
dotnet run
```

Notes:

- The backend runs in development mode with Swagger enabled.
- Based on the current frontend configuration, the local API is expected at `http://localhost:5285/api`.
- Swagger is available at:

```text
http://localhost:5285/swagger
```

### 2. Start the frontend

Open another terminal in:

```bash
Src/FE/angular-app
```

Run:

```bash
npm install
ng serve
```

The frontend runs by default at:

```text
http://localhost:4200
```

## Local Configuration

The current development configuration in the repository points to:

- Frontend: `http://localhost:4200`
- Backend API: `http://localhost:5285/api`

Relevant files:

- `Src/FE/angular-app/src/environments/environment.development.ts`
- `Src/BE/Codedberries/Codedberries/appsettings.Development.json`

## Running with Docker

The repository also contains a Docker Compose file:

```text
Src/docker-compose.yaml
```

You can build and start the project from the `Src` folder with:

```bash
docker compose up --build
```

If needed, adjust exposed ports and environment-specific settings before using containers in your own environment.

## Documentation

Additional user documentation is available here:

- [Uputstvo za upotrebu alata.pdf](https://github.com/theaksaa/codedberries/blob/master/Uputstvo%20za%20upotrebu%20alata.pdf)

There are also supporting materials inside the `Documentation` folder.

## Test User Credentials

The original project includes the following example user accounts:

- Super user: `petar.simic@gmail.com` / `password1`
- Project owner: `zoran.gajic@gmail.com` / `password3`
- Project manager: `lazar.milojevic@gmail.com` / `password3`
- Employee: `ana.dacic@gmail.com` / `password3`
- Viewer: `mina.markovic@gmail.com` / `password3`

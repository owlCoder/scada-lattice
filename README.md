# SCADALattice

A modular SCADA platform for monitoring and controlling simulated physical processes.

Course: Information Security of Infrastructure Systems, Faculty of Technical Sciences, University of Novi Sad.

## Scope

- Create SCADA projects with tags, HMI screens, alarms, and access permissions.
- Build HMI screens and bind visual elements to process signals.
- Connect independent process models through a Simulator SDK.
- Record telemetry, trends, commands, alarms, and security events.

## Architecture

The specification requires Clean Architecture and SOLID principles. Process models integrate through a stable SDK; adding a simulator must not require changes to the SCADA core, tag service, or HMI logic.

## Specification

[Technical specification (PDF, Serbian)](docs/SCADALattice_Tehnicka_specifikacija.pdf)

The PDF defines the requirements, acceptance tests, and reference scenario.

## Repository layout

```
backend/        ASP.NET Core Web API (.NET 8), Clean Architecture
  ScadaLattice.sln
  ScadaLattice.Domain/          entities, value objects, invariants, ports (no references)
  ScadaLattice.Application/     use cases and ports
  ScadaLattice.Infrastructure/  database access, local services
  ScadaLattice.Adapters/        REST API, DTOs
frontend/       Vite + React + TypeScript (src/editor, runtime, trends, alarms)
simulators/     process models that use the SDK (tank_example)
contracts/      manifest, telemetry and API schemas
tests/          domain, contract, integration and scenario tests
docs/           technical specification
```

## Development setup

Prerequisites: Git, .NET SDK 8 or newer, Node 20.19+ or 22.12+, Docker Desktop, Visual Studio 2022 17.8+ (backend), VS Code (everything else).

### 1. Local configuration

From the repository root:

```bash
cp .env.example .env
```

Set `POSTGRES_PASSWORD` in `.env` to a local password. `.env` is git-ignored.

### 2. Database

Start Docker Desktop, then from the repository root:

```bash
docker compose up -d
docker compose ps
```

The `postgres` service should become `healthy`. PostgreSQL listens on `localhost:5432`. The values in `.env` are applied only on the first start. To reset the database (deletes all data):

```bash
docker compose down -v
```

### 3. Backend

Open `backend/ScadaLattice.sln` in Visual Studio, set `ScadaLattice.Adapters` as the startup project and run it with the `https` profile. Swagger opens at `https://localhost:<port>/swagger`.

### 4. Frontend

```bash
cd frontend
npm install
npm run dev
```

Open `http://localhost:5173/`.

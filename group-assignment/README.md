# SeedShare Garden — Group Assignment

Backend Development Fundamentals group assignment (JP-GAI2C-G02).

## Project files

- `server.js` — Express API and SQLite database initialization.
- `seedShareGarden.db` — SQLite database file.
- `app.http` — sample API requests for the VS Code REST Client extension.
- `package.json` and `package-lock.json` — project scripts and dependency versions.

## Requirements

- Node.js and npm

## Setup and run

From this directory, install the dependencies and start the API:

```bash
npm install
npm start
```

The server listens at `http://localhost:3000`. On startup, it creates any missing tables and inserts the sample gardeners, plots, and leases.

## API endpoints

| Method | Path | Description |
|---|---|---|
| GET | `/gardeners/` | List gardeners |
| GET | `/gardeners/:gardenerId/` | Get a gardener |
| GET | `/plots/` | List plots; optionally filter with `?soil_type=Loamy` |
| GET | `/plots/:plotId/` | Get a plot |
| POST | `/plots/` | Add a plot |
| PUT | `/plots/:plotId/` | Update a plot |
| DELETE | `/plots/:plotId/` | Delete a plot |
| GET | `/leases/` | List leases with gardener and plot names |

Use the requests in `app.http` to exercise the API with the VS Code REST Client extension.

## Repository notes

The repository root ignores `node_modules/` and editor settings. Install packages locally after cloning; generated dependencies are not included.

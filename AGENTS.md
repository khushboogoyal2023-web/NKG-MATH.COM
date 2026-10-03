# Base44 Dev Environment

## Project Overview
This is a static website (a scraped copy of poki.com). It consists of an `index.html` file and an `assets/` directory containing CSS and JS files. There is no backend, database, or build step.

## Running the App
```bash
docker compose -f docker-compose.base44.yml up -d
```
Serves the static files via nginx:alpine on host port 3000.

## Key Notes
- The repo root directory must have `755` permissions so nginx's worker process can read the bind-mounted files.
- Source files (`index.html`, `assets/`) are bind-mounted read-only into the container — edits appear immediately without rebuild.
- No external credentials or secrets are needed.
- No migrations or seeds required.

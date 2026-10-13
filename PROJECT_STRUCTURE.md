# CRM Backend - Structured Layout


## Active FastAPI backend

- `app/` - active FastAPI application
  - `main.py` - FastAPI application entry point
  - `api/` - API routers/endpoints
  - `models/` - SQLAlchemy models
  - `schemas/` - Pydantic request/response schemas
  - `services/` - business/service logic
  - `config.py` - application configuration
  - `db.py` - database/session setup
  - `dependencies.py` - FastAPI dependencies
  - `credits_config.py` - credit configuration
- `alembic/` - database migrations
- `scripts/` - import/seed scripts
- `data_*.csv` - source/seed data
- `Dockerfile`, `docker-compose.yml`, `render.yaml` - deployment/container configuration
- `requirements.txt` - Python dependencies

## Preserved code

The previous nested `CRM_BackEnd_FastAPI/` project was **not deleted**. It has been moved intact to:

`archive/CRM_BackEnd_FastAPI_original/`

It is kept as a backup/reference copy and is not part of the active application path. This avoids having two competing `app/` and `alembic/` directories in the active project while preserving all original source files.

## Run the active backend

From the project root:

```bash
uvicorn app.main:app --reload
```

## Database migrations

```bash
alembic upgrade head
```



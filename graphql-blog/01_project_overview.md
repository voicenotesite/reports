# GraphQL Blog — Project Overview

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 1/20  


## Overview
GraphQL-powered blog with Strawberry, SQLAlchemy, PostgreSQL, and full CRUD.

## Purpose
Serves as a GraphQL-based blog platform with user management and post CRUD.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• GraphQL API with Strawberry
• User auth via JWT
• Post CRUD with pagination
• PostgreSQL database

## Entry Points
`docker compose up` or via daemon


---


## Detailed Architecture

### Project Structure
```
app/main.py (FastAPI + Strawberry), app/schema.py (GraphQL types + resolvers), app/models.py, app/auth.py
```

### Technology Stack
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Backend Framework | FastAPI | REST/API server |
| Database | SQLite | Data persistence |
| Auth | JWT | Authentication & authorization |
| Frontend | None | User interface |
| Deployment | Render.com + GitHub Pages | Hosting & CI/CD |

### Module Breakdown
See project structure above.

### Data Flow
1. Request enters via HTTP (REST, GraphQL, or WebSocket)
2. Authentication middleware validates JWT token (if required)
3. Router dispatches to appropriate handler
4. Handler processes business logic with database queries
5. Response formatted and returned to client
6. Frontend renders response in appropriate view

### Entry Points
- **Server:** `uvicorn app.main:app`
- **Port:** 8000 (default)
- **Health check:** `GET /health`

## Configuration

### Environment Variables
| Variable | Description | Default |
|----------|-------------|---------|
| DATABASE_URL | Database connection string | sqlite:///./data.db |
| SECRET_KEY | JWT signing secret | (required) |
| CORS_ORIGINS | Allowed CORS origins | * |
| DEBUG | Debug mode flag | false |

## Deployment

### Requirements
- Python 3.10+
- pip dependencies (see requirements.txt)
- SQLite (or PostgreSQL for production)

### Startup Commands
```bash
# Development
uvicorn app.main:app --reload

# Production
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

## Related Reports
- Report 02: Architecture Analysis (detailed component diagram)
- Report 05: Tech Stack & Dependencies (version-specific)
- Report 13: Deployment Guide (Docker, CI/CD)


<!-- EXPANDED -->
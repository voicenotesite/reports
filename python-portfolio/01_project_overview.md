# Python Portfolio — Project Overview

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 1/20  


## Overview
Unified FastAPI API combining URL shortener, blog, chat, queue, and RAG modules.

## Purpose
Unifies 5 portfolio project APIs (shortener, blog, chat, queue, RAG) under one FastAPI app.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• 5 integrated modules: shortener, blog, chat, queue, RAG
• Unified auth (JWT)
• Shared database schema
• CORS enabled
• Optional frontend serving

## Entry Points
`uvicorn app.main:app`


---


## Detailed Architecture

### Project Structure
```
app/main.py (FastAPI init + auth + frontend), app/shortener/router.py, app/blog/schema.py, app/chat/router.py, app/queue/router.py, app/rag/router.py, frontend/dist/ (unified SPA)
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
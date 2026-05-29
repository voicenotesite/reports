# CV Maker — Project Overview

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 1/20  


## Overview
Full-stack CV builder with job scraping, two frontends (React/Vite + Svelte), and PDF generation.

## Purpose
Builds professional CVs from scraped job data, with dual frontend support.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• Job scraping from remote OK
• CV generation with multiple templates
• Dual frontends: React/Vite + Svelte
• PDF export
• User authentication

## Entry Points
Backend: `main.py`; Frontend Svelte: `cd svelte-frontend && npm run dev`; Frontend React: `cd frontend && npm run dev`


---


## Detailed Architecture

### Project Structure
```
backend/main.py (FastAPI), frontend/ (React/Vite), svelte-frontend/ (Svelte), scraper/ (Playwright), requirements.txt, .env
```

### Technology Stack
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Backend Framework | FastAPI | REST/API server |
| Database | PostgreSQL | Data persistence |
| Auth | JWT | Authentication & authorization |
| Frontend | React | User interface |
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
- **Server:** `uvicorn backend.main:app`
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
uvicorn backend.main:app --reload

# Production
uvicorn backend.main:app --host 0.0.0.0 --port 8000
```

## Related Reports
- Report 02: Architecture Analysis (detailed component diagram)
- Report 05: Tech Stack & Dependencies (version-specific)
- Report 13: Deployment Guide (Docker, CI/CD)


<!-- EXPANDED -->
# Portfolio Daemon — Project Overview

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 1/20  


## Overview
Background daemon managing multiple backend services with SSH tunnels and health monitoring.

## Purpose
Manages local backend services and SSH tunnels for remote development.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• Auto-start backend services
• SSH tunnel management
• Health monitoring via /health
• File-watch restart
• PM2 integration

## Entry Points
`python main.py` (daemon)


---


## Detailed Architecture

### Project Structure
```
daemon.py (main loop), config.py, services/ (per-service config), monitor.py (health checks), ssh.py (tunnel management)
```

### Technology Stack
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Backend Framework | Python | REST/API server |
| Database | SQLAlchemy + SQLite | Data persistence |
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
- **Server:** `python daemon.py`
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
python daemon.py --reload

# Production
python daemon.py --host 0.0.0.0 --port 8000
```

## Related Reports
- Report 02: Architecture Analysis (detailed component diagram)
- Report 05: Tech Stack & Dependencies (version-specific)
- Report 13: Deployment Guide (Docker, CI/CD)


<!-- EXPANDED -->
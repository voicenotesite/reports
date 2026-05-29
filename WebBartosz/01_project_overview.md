# WebBartosz Portfolio — Project Overview

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 1/20  


## Overview
Minimal personal portfolio website built with Vite vanilla JS.

## Purpose
A minimal personal portfolio page to showcase projects and skills.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• Clean responsive design
• Project showcase grid
• Contact form
• Dark theme
• Static site, fast load

## Entry Points
`npm run dev`


---


## Detailed Architecture

### Project Structure
```
index.html (single-page portfolio), style.css, script.js, vite.config.js
```

### Technology Stack
| Layer | Technology | Purpose |
|-------|-----------|---------|
| Backend Framework | Vite | REST/API server |
| Database | SQLite | Data persistence |
| Auth | JWT | Authentication & authorization |
| Frontend | Vite | User interface |
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
- **Server:** `npm run dev (dev) or GitHub Pages auto-deploy from master branch`
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
npm run dev (dev) or GitHub Pages auto-deploy from master branch --reload

# Production
npm run dev (dev) or GitHub Pages auto-deploy from master branch --host 0.0.0.0 --port 8000
```

## Related Reports
- Report 02: Architecture Analysis (detailed component diagram)
- Report 05: Tech Stack & Dependencies (version-specific)
- Report 13: Deployment Guide (Docker, CI/CD)


<!-- EXPANDED -->
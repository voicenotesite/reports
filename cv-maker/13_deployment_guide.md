# CV Maker — Deployment Guide

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 13/20  


## Local Development
```bash
# Backend
uvicorn main:app --reload

# Frontend (React)
cd frontend && npm run dev

# Frontend (Svelte)
cd svelte-frontend && npm run dev
```

## Production
- Dockerize backend
- Build frontends to `dist/` and serve via nginx
- Set up PostgreSQL with backups

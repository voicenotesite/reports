# CV Maker — Architecture Analysis

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 2/20  


## Architecture Type
Full-stack monorepo with separate backend and two frontends

## Layers
Frontend (React/Svelte) → REST API → Service Layer → SQLAlchemy → PostgreSQL + Playwright Scraper

## Design Patterns
Service layer pattern, repository pattern for DB access

## Scalability
Can scale horizontally with PostgreSQL backend; frontends are decoupled

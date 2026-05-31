# CV Maker — API Endpoints

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 3/20  


## Backend REST API

| Method | Path | Description |
|--------|------|-------------|
| POST | `/token` | Auth (OAuth2 password) |
| POST | `/register` | User registration |
| POST | `/scrape` | Trigger job scraping |
| GET | `/jobs` | List scraped jobs |
| GET | `/jobs/{id}` | Job details |
| POST | `/cvs` | Create CV |
| GET | `/cvs` | List CVs |
| GET | `/cvs/{id}` | Get CV |
| POST | `/generate-pdf` | Export CV as PDF |
| GET | `/templates` | List templates |

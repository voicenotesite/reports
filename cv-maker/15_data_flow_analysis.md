# CV Maker — Data Flow Analysis

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 15/20  


## Request Flow

```
User → Frontend (React/Svelte) → REST API → FastAPI
  ├── Playwright → Scrape Jobs → PostgreSQL
  └── WeasyPrint → Generate PDF → Download
```

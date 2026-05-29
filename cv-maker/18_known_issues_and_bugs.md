# CV Maker — Known Issues and Bugs

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 18/20  



1. **Two frontends** — double maintenance burden
2. **Playwright scraping** — blocking operation, no background task queue
3. **No scraper error handling** — failed scrapes may not report correctly
4. **No database migrations** — schema managed in code
5. **Large codebase** with inconsistent patterns

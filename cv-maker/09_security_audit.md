# CV Maker — Security Audit

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 9/20  



| Issue | Severity | Description |
|-------|----------|-------------|
| JWT auth | Good | bcrypt passwords |
| Scraper abuse potential | Medium | No rate limiting on scrape |
| DB injection | Good | Prevented by SQLAlchemy |
| CORS likely permissive | Low | Review for production |

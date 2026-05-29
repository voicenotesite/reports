# CV Maker — Error Handling Review

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 14/20  



| Aspect | Status |
|--------|--------|
| Approach | Mixed: HTTPException + try/except |
| Global handler | Not present |
| Consistency | Varies across endpoints |
| Scraper errors | May not propagate well |

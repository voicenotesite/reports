# URL Shortener — Security Audit

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 9/20  



| Issue | Severity | Description |
|-------|----------|-------------|
| No auth | High | Anyone can create/delete URLs |
| No rate limiting | Medium | Potential spam abuse |
| Predictable short codes | Low | Not cryptographically random |
| SQLite concurrency | Medium | Not safe for concurrent writes |

# Python Portfolio — Security Audit

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 9/20  



| Issue | Severity | Description |
|-------|----------|-------------|
| Shared JWT across modules | Medium | One compromised key = all modules |
| No refresh tokens | Medium | Long-lived JWT |
| CORS allows all origins | Medium | Should restrict in production |
| SQLAlchemy prevents injection | Good | ORM usage |

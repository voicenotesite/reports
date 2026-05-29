# Python Portfolio — Known Issues and Bugs

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 18/20  



1. **SQLite** — single-writer bottleneck for 5 modules
2. **No database migrations** — schema created at startup
3. **Shared JWT secret** — all modules share auth
4. **Single process** — crash takes down all 5 modules
5. **No rate limiting** on any endpoint

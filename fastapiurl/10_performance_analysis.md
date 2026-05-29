# URL Shortener — Performance Analysis

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 10/20  



| Aspect | Assessment |
|--------|------------|
| SQLite | Single-writer bottleneck |
| Caching | None — every request hits DB |
| Redirect speed | Instant (302) |
| Pagination | None on `/list` — degrades over time |

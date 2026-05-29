# URL Shortener — Data Flow Analysis

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 15/20  


## Request Flow

```
Client → POST /shorten → FastAPI → SQLite (insert)
Client → GET /{code}  → FastAPI → SQLite (query) → 302 Redirect
Client → GET /{code}/stats → FastAPI → SQLite (count) → JSON
```

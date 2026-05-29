# URL Shortener — API Endpoints

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 3/20  


## Endpoints Overview

| Method | Path | Description |
|--------|------|-------------|
| POST | `/shorten` | Create short URL |
| GET | `/{short_code}` | Redirect to original URL |
| GET | `/{short_code}/stats` | Get click stats |
| GET | `/{short_code}/json` | Get JSON info |
| GET | `/{short_code}/html` | Get HTML page |
| GET | `/list` | List all URLs |
| DELETE | `/{short_code}` | Delete URL |

# URL Shortener — Deployment Guide

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 13/20  


## Local Development
```bash
uvicorn main:app --reload --port 8000
```

## Production
- Run with `gunicorn -k uvicorn.workers.UvicornWorker main:app`
- Use nginx as reverse proxy
- Set up systemd service

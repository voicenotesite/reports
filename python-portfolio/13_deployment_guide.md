# Python Portfolio — Deployment Guide

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 13/20  


## Local Development
```bash
uvicorn app.main:app --reload
```

## Production
- Run with `gunicorn -k uvicorn.workers.UvicornWorker app.main:app`
- Use nginx as reverse proxy
- Set up systemd service

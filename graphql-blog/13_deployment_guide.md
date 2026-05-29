# GraphQL Blog — Deployment Guide

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 13/20  


## Local Development
```bash
docker compose up --build
```

## Production
- Use Docker Compose with production settings
- Set up PostgreSQL with persistent volume
- Use nginx as reverse proxy with SSL

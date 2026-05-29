# GraphQL Blog — Configuration and Environment

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 8/20  



## Environment + Docker Compose
```yaml
services:
  db: postgres:15
  app: build: . ports: 8000:8000
  nginx: ...
```
PostgreSQL connection via environment variables.

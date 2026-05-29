# GraphQL Blog — Tech Stack and Dependencies

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 5/20  


## Primary Stack
Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL

## Key Dependencies
- `fastapi` — API framework
- `strawberry-graphql` — GraphQL
- `sqlalchemy` — ORM
- `psycopg2-binary` — PostgreSQL driver
- `python-jose` — JWT auth
- `passlib` — password hashing
- `alembic` — migrations


---


## Technology Stack Details

### Framework Versions
| Component | Technology | Version | Purpose |
|-----------|-----------|---------|---------|
| Backend | FastAPI | API server |
| Database | SQLite | Persistence |
| Auth | JWT | Security |
| Frontend | None | UI |
| Hosting | Render.com + GitHub Pages | Deployment |

### Core Dependencies

```
# Core dependencies
fastapi>=0.115.0
sqlalchemy>=2.0.0
pydantic>=2.0.0
uvicorn[standard]>=0.30.0
```


### Dependency Justification
| Package | Why | Alternative Considered |
|---------|-----|----------------------|
| fastapi | Modern ASGI framework | Flask, Django |
| sqlalchemy | Mature ORM with async | peewee, tortoise-orm |
| pydantic | Validation + serialization | marshmallow |
| jose | JWT handling | PyJWT |

### Development Dependencies
| Package | Purpose |
|---------|---------|
| pytest | Testing framework |
| httpx | Async HTTP client for tests |
| uvicorn | ASGI server |
| python-dotenv | Environment variable loading |

### External Services
| Service | Purpose | Integration Point |
|---------|---------|------------------|
| OpenAI | AI chat completion | /v1/chat/completions proxy |
| GitHub Pages | Static hosting | git push deployment |

### Version Constraints
- Python 3.10+ required (type hints, pattern matching)
- Pydantic v2 for improved validation performance
- SQLAlchemy 2.0+ for modern async support


<!-- EXPANDED -->
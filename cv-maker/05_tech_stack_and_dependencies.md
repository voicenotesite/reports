# CV Maker — Tech Stack and Dependencies

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 5/20  


## Primary Stack
Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper

## Backend Dependencies
- `fastapi` — API framework
- `sqlalchemy` — ORM
- `psycopg2` — PostgreSQL driver
- `playwright` — web scraper
- `jinja2` — PDF templating
- `weasyprint` — PDF generation
- `python-jose` — JWT
- `passlib` — password hashing

## Frontend (React): `react`, `vite`, `react-router-dom`, `axios`, `tailwindcss`
## Frontend (Svelte): `svelte`, `vite`, `svelte-routing`, `chart.js`


---


## Technology Stack Details

### Framework Versions
| Component | Technology | Version | Purpose |
|-----------|-----------|---------|---------|
| Backend | FastAPI | API server |
| Database | PostgreSQL | Persistence |
| Auth | JWT | Security |
| Frontend | React | UI |
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
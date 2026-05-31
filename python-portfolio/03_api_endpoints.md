# Python Portfolio — API Endpoints

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 3/20  


## Unified Portfolio API

| Method | Path | Description |
|--------|------|-------------|
| POST | `/auth/register` | Register user |
| POST | `/auth/login` | Login |
| GET | `/auth/me` | Current user |
| GET | `/health` | Health check |

**Module Endpoints:**
- **Shortener:** POST `/shorten`, GET `/{code}`, GET `/{code}/stats`
- **Blog:** POST `/graphql`
- **Chat:** POST `/api/chat/` (WebSocket or SSE)
- **Queue:** POST `/api/queue/task`, GET `/api/queue/status/{id}`
- **RAG:** POST `/api/rag/query`, POST `/api/rag/ingest`

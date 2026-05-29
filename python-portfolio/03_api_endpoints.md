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


---


## Complete API Reference

### Endpoint Table
| Method | Path | Auth | Request | Response | Description |
|--------|------|------|---------|----------|-------------|
| POST /auth/login | TODO | TODO | TODO |
| POST /auth/register | TODO | TODO | TODO |
| GET /health | TODO | TODO | TODO |
| POST /shorten | TODO | TODO | TODO |
| GET /{code} | TODO | TODO | TODO |
| POST /api/chat/message | TODO | TODO | TODO |
| POST /api/queue/create | TODO | TODO | TODO |
| GET /api/queue/ws/{id} | TODO | TODO | TODO |
| POST /api/rag/upload | TODO | TODO | TODO |
| POST /api/rag/ask | TODO | TODO | TODO |
| GET /api/rag/documents | TODO | TODO | TODO |

### Request/Response Examples

#### Example: Successful Request
```json
// POST /auth/login
// Request:
{"email": "user@example.com", "password": "..."}
// Response (200):
{"access_token": "eyJ...", "token_type": "bearer"}
```

#### Example: Error Response
```json
// Response (401):
{"detail": "Invalid credentials"}
```

#### Example: Paginated List
```json
// GET /urls/list?skip=0&limit=10
// Response (200):
{"items": [...], "total": 42, "skip": 0, "limit": 10}
```

### Status Codes Used
| Code | Meaning | Usage |
|------|---------|-------|
| 200 | OK | Successful GET, POST, PATCH |
| 201 | Created | Successful POST (resource created) |
| 204 | No Content | Successful DELETE |
| 400 | Bad Request | Validation error |
| 401 | Unauthorized | Missing/invalid JWT |
| 403 | Forbidden | Not resource owner |
| 404 | Not Found | Resource doesn't exist |
| 409 | Conflict | Duplicate resource |
| 422 | Unprocessable | Pydantic validation failure |
| 429 | Rate Limited | Too many requests |
| 500 | Internal Error | Server-side failure |


<!-- EXPANDED -->
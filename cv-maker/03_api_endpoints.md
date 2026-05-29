# CV Maker — API Endpoints

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 3/20  


## Backend REST API

| Method | Path | Description |
|--------|------|-------------|
| POST | `/token` | Auth (OAuth2 password) |
| POST | `/register` | User registration |
| POST | `/scrape` | Trigger job scraping |
| GET | `/jobs` | List scraped jobs |
| GET | `/jobs/{id}` | Job details |
| POST | `/cvs` | Create CV |
| GET | `/cvs` | List CVs |
| GET | `/cvs/{id}` | Get CV |
| POST | `/generate-pdf` | Export CV as PDF |
| GET | `/templates` | List templates |


---


## Complete API Reference

### Endpoint Table
| Method | Path | Auth | Request | Response | Description |
|--------|------|------|---------|----------|-------------|
| POST /api/cv/generate | TODO | TODO | TODO |
| GET /api/cv/{id} | TODO | TODO | TODO |
| POST /api/scrape | TODO | TODO | TODO |
| GET /api/templates | TODO | TODO | TODO |
| POST /api/auth/login | TODO | TODO | TODO |
| POST /api/auth/register | TODO | TODO | TODO |

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
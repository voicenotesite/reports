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


---


## Complete API Reference

### Endpoint Table
| Method | Path | Auth | Request | Response | Description |
|--------|------|------|---------|----------|-------------|
| POST /auth/register | TODO | TODO | TODO |
| POST /auth/login | TODO | TODO | TODO |
| GET /auth/me | TODO | TODO | TODO |
| POST /urls/shorten | TODO | TODO | TODO |
| GET /{short_code} | TODO | TODO | TODO |
| GET /urls/stats/{code} | TODO | TODO | TODO |
| GET /urls/list | TODO | TODO | TODO |
| DELETE /urls/{code} | TODO | TODO | TODO |
| PATCH /urls/{code}/toggle | TODO | TODO | TODO |

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
# WebBartosz Portfolio — API Endpoints

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 3/20  


## Static Site (no API)

| Page | Route | Description |
|------|-------|-------------|
| Home | `/` | Landing page |
| Projects | `/projects` | Project showcase |
| Contact | `/contact` | Contact form |


---


## Complete API Reference

### Endpoint Table
| Method | Path | Auth | Request | Response | Description |
|--------|------|------|---------|----------|-------------|
| None (static GitHub Pages site) | TODO | TODO | TODO |

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
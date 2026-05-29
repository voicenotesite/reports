# GraphQL Blog — API Endpoints

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 3/20  


## GraphQL Endpoint

| Endpoint | Description |
|----------|-------------|
| POST `/graphql` | GraphQL query/mutation |

**Queries:** `posts`, `post(id)`, `users`, `user(id)`, `me`
**Mutations:** `createPost`, `updatePost`, `deletePost`, `register`, `login`, `createComment`


---


## Complete API Reference

### Endpoint Table
| Method | Path | Auth | Request | Response | Description |
|--------|------|------|---------|----------|-------------|
| POST /graphql (GraphQL queries + mutations) | TODO | TODO | TODO |
| GET /health | TODO | TODO | TODO |

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
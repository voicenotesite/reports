# AI Chat Proxy — Authentication and Authorization

**Project:** AI Chat Proxy  
**Technology:** JavaScript, Node.js, Express, OpenAI API  
**Location:** `/home/dominic/Documents/ai-chat-proxy`  
**Report #:** 6/20  


## No Authentication
Public proxy. OpenAI API key stored in environment.


---


## Authentication & Authorization System

### Auth Flow
```
Client                    Server
  │                         │
  │── POST /auth/login ────→│  Validate credentials
  │                         │──→ Verify password (bcrypt)
  │                         │──→ Generate JWT (HS256)
  │←── {access_token} ─────│  Return token
  │                         │
  │── GET /protected ──────→│  Authorization: Bearer <token>
  │                         │──→ Decode JWT
  │                         │──→ Verify signature + expiry
  │                         │──→ Load user from DB
  │←── {data} ─────────────│
```

### JWT Configuration
| Parameter | Value | Notes |
|-----------|-------|-------|
| Algorithm | HS256 | Symmetric signing |
| Expiry | 30 days | Configurable via ACCESS_TOKEN_EXPIRE |
| Header | Authorization: Bearer <token> | Standard Bearer scheme |
| Payload | {"sub": user_id, "exp": timestamp} | Standard JWT claims |

### Password Security
- Hashing algorithm: bcrypt (via passlib)
- Salt: automatic (bcrypt built-in)
- Minimum password length: 8 characters
- No plaintext storage ever

### Protected Routes

- POST /urls/shorten (JWT required)
- GET /urls/list (JWT required)
- DELETE /urls/{code} (JWT + ownership)
- POST /api/chat/message (JWT required)
- POST /api/rag/upload (JWT required)


### Permission Model
- Resource ownership: users can only modify their own resources
- No role-based access currently (admin/user distinction not implemented)
- Future: add is_admin flag for elevated permissions

### Security Headers (Recommended)
| Header | Value | Purpose |
|--------|-------|---------|
| X-Content-Type-Options | nosniff | Prevent MIME sniffing |
| X-Frame-Options | DENY | Prevent clickjacking |
| Strict-Transport-Security | max-age=31536000 | Force HTTPS |


<!-- EXPANDED -->
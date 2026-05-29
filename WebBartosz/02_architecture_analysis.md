# WebBartosz Portfolio — Architecture Analysis

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 2/20  


## Architecture Type
Static single-page application

## Layers
Static HTML/CSS/JS → Vite Build → Deployed to static host

## Design Patterns
SPA with hash-based routing

## Scalability
Static site, infinitely scalable via CDN


---


## System Architecture

### Layer Architecture
```
┌─────────────────────────────────────┐
│         Client Layer                │
│  Browser / Mobile / API Client     │
├─────────────────────────────────────┤
│         API Gateway / Proxy         │
│  FastAPI middleware stack:          │
│  CORS → Auth → Rate Limit → Router │
├─────────────────────────────────────┤
│         Application Layer           │
│  Routes → Handlers → Services      │
├─────────────────────────────────────┤
│         Data Layer                  │
│  SQLAlchemy ORM → SQLite/PostgreSQL│
└─────────────────────────────────────┘
```

### Component Interaction

```
WebBartosz Component Architecture
├── API Layer (FastAPI)
├── Service Layer (Business Logic)
├── Data Layer (SQLAlchemy + SQLite)
└── Client Layer (Vite)
```


### Request Lifecycle
1. **HTTP Request** arrives at FastAPI
2. **CORS middleware** checks origin headers
3. **Auth dependency** extracts and validates JWT
4. **Rate limiter** checks request count per IP
5. **Router** matches path to handler
6. **Handler** executes business logic
7. **Database session** commits or rolls back
8. **Response** returned to client

### Dependency Graph

```
WebBartosz Dependency Flow:
Client → FastAPI → Router → Handler → SQLite → Response
```


### Design Patterns Used
| Pattern | Location | Purpose |
|---------|----------|---------|
| Dependency Injection | FastAPI Depends() | DB sessions, auth |
| Repository Pattern | SQLAlchemy models | Data abstraction |
| Middleware Chain | FastAPI middleware | Cross-cutting concerns |
| Router Module | APIRouter include | Separation of concerns |


<!-- EXPANDED -->
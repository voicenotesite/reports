# GraphQL Blog — Security Audit

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 9/20  



| Issue | Severity | Description |
|-------|----------|-------------|
| No refresh tokens | Medium | JWT tokens are long-lived |
| No email verification | Medium | Anyone can register |
| CORS likely permissive | Low | May need tightening |
| No SQL injection | Good | Prevented by SQLAlchemy |

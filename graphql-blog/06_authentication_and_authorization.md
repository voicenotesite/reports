# GraphQL Blog — Authentication and Authorization

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 6/20  


## JWT Authentication
Uses `python-jose` with HS256 algorithm. Token includes `sub` (user ID).

**Protected:** Post mutations (create, update, delete)
**Open:** Registration, login, public post queries
**Password storage:** bcrypt via passlib

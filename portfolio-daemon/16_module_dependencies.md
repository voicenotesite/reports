# Portfolio Daemon — Module Dependencies

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 16/20  



```
main.py → manager.py → tunnel.py
        → config.py   → monitor.py
```


---


## Module Dependencies

### Import Graph

```
main.py
├── database.py → SQLAlchemy
├── auth.py → jose, passlib
├── shortener/router.py → models, schemas
├── blog/schema.py → models, strawberry
├── chat/router.py → models, openai
├── queue/router.py → models, asyncio
└── rag/router.py → models, sklearn
```


### Dependency Matrix
| Module | Depends On | Used By |
|--------|-----------|---------|
| app.main | auth, database | All routers |
| auth | database | main, all routers |
| shortener | models, auth | main |
| blog | models, auth | main |
| chat | models, auth | main |
| queue | models, auth | main |
| rag | models, auth | main |

### Circular Dependencies
None found.

### External Library Dependencies
```txt
# requirements.txt
fastapi>=0.115.0
sqlalchemy>=2.0.0
pydantic>=2.0.0
python-jose[cryptography]>=3.3.0
passlib[bcrypt]>=1.7.4
httpx>=0.27.0
python-multipart>=0.0.9
uvicorn[standard]>=0.30.0
```

### Internal Module Coupling
| Module | Incoming Edges | Outgoing Edges | Cohesion |
|--------|---------------|----------------|----------|
| app.main | 0 | 6 | High (hub) |
| auth | 1 | 2 | Medium |
| shortener | 2 | 1 | Low |
| blog | 2 | 1 | Low |

### Package Health
| Package | Version | Latest | Status |
|---------|---------|--------|--------|
| fastapi | 0.115.0 | 0.115.x | ✅ |
| sqlalchemy | 2.0.x | 2.0.x | ✅ |
| pydantic | 2.0.x | 2.x | ✅ |
| python-jose | 3.3.x | 3.3.x | ✅ |
| passlib | 1.7.x | 1.7.x | ✅ |

### Dependency Recommendations
1. Update to latest patch versions for security fixes
2. Consider replacing python-jose with PyJWT for active maintenance
3. Add dependency pinning in requirements.txt
4. Use pip-audit for vulnerability scanning


<!-- EXPANDED -->
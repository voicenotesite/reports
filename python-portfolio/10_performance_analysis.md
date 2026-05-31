# Python Portfolio — Performance Analysis

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 10/20  



| Aspect | Assessment |
|--------|------------|
| SQLite | Single-writer bottleneck |
| Memory | All 5 modules share one process |
| Caching | None — repeated DB hits |
| LLM calls | High latency (RAG/chat modules) |

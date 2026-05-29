# Python Portfolio — Data Flow Analysis

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 15/20  


## Request Flow

```
Client → Auth Router → JWT
      → Shortener Router → SQLite
      → Blog Router (GraphQL) → SQLite
      → Chat Router → OpenAI
      → Queue Router → Task Queue
      → RAG Router → ChromaDB + OpenAI
```

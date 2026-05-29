# Python Portfolio — Database Schema

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 4/20  


## Database Engine: SQLite

### Shared User Model
```python
class User(Base):
    id: int (PK)
    email: str (unique)
    username: str (unique)
    hashed_password: str
```

Plus module-specific tables for shortener, chat, queue, and RAG modules.
Schema auto-created via `Base.metadata.create_all()` on startup.

# URL Shortener — Database Schema

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 4/20  


## Database Engine: SQLite

### Table: `urls`
```python
class URL(Base):
    __tablename__ = "urls"
    id: int (PK)
    original_url: str
    short_code: str (unique, indexed)
    created_at: datetime
    clicks: int (default 0)
```

**Indexes:** `short_code` (unique)

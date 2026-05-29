# CV Maker — Database Schema

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 4/20  


## Database Engine: PostgreSQL

### Tables
```python
class User(Base):
    id: int (PK)
    username: str (unique)
    email: str (unique)
    hashed_password: str

class Job(Base):
    id: int (PK)
    title: str
    company: str
    location: str
    description: text
    url: str
    source: str
    scraped_at: datetime

class CV(Base):
    id: int (PK)
    user_id: FK → users.id
    title: str
    template: str
    sections: JSON
    created_at: datetime
    updated_at: datetime

class Template(Base):
    id: int (PK)
    name: str
    config: JSON
```

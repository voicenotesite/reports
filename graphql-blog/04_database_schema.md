# GraphQL Blog — Database Schema

**Project:** GraphQL Blog  
**Technology:** Python, FastAPI, Strawberry GraphQL, SQLAlchemy, PostgreSQL  
**Location:** `/home/dominic/Documents/graphql-blog`  
**Report #:** 4/20  


## Database Engine: PostgreSQL

### Tables
```python
class User(Base):
    id: int (PK)
    username: str (unique)
    email: str (unique)
    hashed_password: str
    posts: relationship

class Post(Base):
    id: int (PK)
    title: str
    content: text
    published: bool
    author_id: FK → users.id
    created_at: datetime
    updated_at: datetime

class Comment(Base):
    id: int (PK)
    content: text
    post_id: FK → posts.id
    author_id: FK → users.id
    created_at: datetime
```

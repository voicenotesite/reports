# URL Shortener — Known Issues and Bugs

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 18/20  



1. **No rate limiting** — anyone can spam the shortener
2. **No auth** — anyone can delete any URL
3. **SQLite concurrency** — not safe for concurrent writes
4. **Short codes** are not cryptographically random
5. **No click analytics** beyond simple counter

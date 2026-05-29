# URL Shortener — Improvement Recommendations

**Project:** URL Shortener  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic  
**Location:** `/home/dominic/Documents/fastapiurl`  
**Report #:** 19/20  



### Short-term
- Add rate limiting
- Add basic auth or API keys
- Use more random short codes (UUID prefix)

### Medium-term
- Switch to PostgreSQL for concurrency
- Add click analytics (referrer, user-agent, timestamp)
- Write tests with pytest

### Long-term
- Add user accounts and URL ownership
- Add custom domains per short URL
- Add expiration dates

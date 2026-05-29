# CV Maker — Configuration and Environment

**Project:** CV Maker  
**Technology:** Python/FastAPI backend, React/Vite + Svelte frontends, PostgreSQL, SQLAlchemy, Playwright scraper  
**Location:** `/home/dominic/Documents/CV MAKER`  
**Report #:** 8/20  



## Environment Variables
```
DATABASE_URL=postgresql://...
SECRET_KEY=...
OPENAI_API_KEY=...
SCRAPER_CONFIG=...
```
PostgreSQL connection string, JWT secret, API keys.


---


## Configuration & Environment

### Environment Files

```
# .env (example)
DATABASE_URL=sqlite:///./data.db
SECRET_KEY=your-secret-key-here
DEBUG=false
CORS_ORIGINS=*
```


### Configuration Loading
```python
# Pattern used across projects
from pydantic_settings import BaseSettings

class Settings(BaseSettings):
    database_url: str = "sqlite:///./data.db"
    secret_key: str = "change-me"
    debug: bool = False
    cors_origins: str = "*"

    model_config = {"env_file": ".env", "env_file_encoding": "utf-8"}
```

### Runtime Configuration
| Parameter | Source | Default | Description |
|-----------|--------|---------|-------------|
| DATABASE_URL | .env | sqlite:///./data.db | DB connection |
| SECRET_KEY | .env | (required) | JWT signing |
| DEBUG | .env | false | Dev mode |
| CORS_ORIGINS | .env | * | CORS policy |

### Deployment-Specific Config
Render Web Service (free tier):
- CPU: Shared
- RAM: 512 MB
- Disk: 1 GB
- Region: Frankfurt
- Auto-deploy: On push to main

### Sensitive Values
| Variable | Risk | Mitigation |
|----------|------|------------|
| SECRET_KEY | JWT forgery | Use strong random value, rotate periodically |
| OPENAI_API_KEY | Cost, data exposure | Server-side only, rate-limited |
| DATABASE_URL | Data access | Never commit to git |


<!-- EXPANDED -->
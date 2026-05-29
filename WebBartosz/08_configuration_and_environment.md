# WebBartosz Portfolio — Configuration and Environment

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 8/20  


## No configuration — fully static. Build config in `vite.config.js`.


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
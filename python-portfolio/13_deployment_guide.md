# Python Portfolio — Deployment Guide

**Project:** Python Portfolio  
**Technology:** Python, FastAPI, SQLAlchemy, SQLite, Pydantic, JWT  
**Location:** `/home/dominic/Documents/python-portfolio`  
**Report #:** 13/20  


## Local Development
```bash
uvicorn app.main:app --reload
```

## Production
- Run with `gunicorn -k uvicorn.workers.UvicornWorker app.main:app`
- Use nginx as reverse proxy
- Set up systemd service


---


## Deployment Guide

### Prerequisites
- Python 3.10+
- pip dependencies installed
- Render.com account (or alternative hosting)
- Git repository access

### Local Development
```bash
# Clone repository
git clone https://github.com/voicenotesite/python-portfolio.git
cd python-portfolio

# Install dependencies
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Configure environment
cp .env.example .env
# Edit .env with your settings

# Run server
uvicorn app.main:app --reload
```

### Docker Deployment
```dockerfile
# Example Dockerfile
FROM python:3.12-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
EXPOSE 8000
CMD ["uvicorn app.main:app"]
```

### Render.com Deployment
1. Create new Web Service in Render dashboard
2. Connect GitHub repository
3. Configure:
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `uvicorn app.main:app`
   - Environment: Python 3.12
   - Region: Frankfurt (Europe)
4. Add environment variables in Render dashboard
5. Deploy (first deploy may take 2-3 minutes)
6. Service auto-deploys on push to main branch

### GitHub Pages Deployment
- Used for: WebBartosz, Reports
- Auto-deploys from master branch
- No build step required (static files)
- Custom domain possible via CNAME file

### Health Checks
- Endpoint: `GET /health`
- Expected: `{"status": "ok"}`
- Render uses this for service monitoring
- WebBartosz pings all services every 60 seconds

### Cold Start Mitigation
- Render free tier spins down after 15 min idle
- First request after idle: 30-60s delay
- Mitigation: WebBartosz pings every 60s keep services warm


<!-- EXPANDED -->
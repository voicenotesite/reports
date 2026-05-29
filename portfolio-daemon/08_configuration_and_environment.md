# Portfolio Daemon — Configuration and Environment

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 8/20  



## YAML Config + Environment
```yaml
# config.yaml
services:
  - name: portfolio
    command: python app/main.py
    tunnel: true
    port: 8000
```

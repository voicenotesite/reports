# Portfolio Daemon — Deployment Guide

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 13/20  


## Local Development
```bash
python main.py
```

## Production
- Run as systemd service
- Configure SSH keys properly
- Set up log rotation

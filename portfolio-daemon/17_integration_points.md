# Portfolio Daemon — Integration Points

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 17/20  



| Integration | Type | Risk |
|-------------|------|------|
| SSH | Remote access | Key management |
| Local processes | Service mgmt | Port conflicts |
| File system | Watching | Permissions |

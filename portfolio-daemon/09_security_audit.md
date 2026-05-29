# Portfolio Daemon — Security Audit

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 9/20  



| Issue | Severity | Description |
|-------|----------|-------------|
| No auth on daemon | Medium | Local machine only |
| SSH key management | High | Keys must be properly secured |
| No process sandboxing | Medium | Subprocesses run without isolation |

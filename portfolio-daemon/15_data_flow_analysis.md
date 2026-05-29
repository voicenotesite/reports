# Portfolio Daemon — Data Flow Analysis

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 15/20  


## Request Flow

```
Config (YAML) → Daemon → Start/Stop Services
                     → SSH Tunnel → Remote Server
                     → File Watcher → Restart on Change
```

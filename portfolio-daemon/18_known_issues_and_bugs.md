# Portfolio Daemon — Known Issues and Bugs

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 18/20  



1. **No health check** for the daemon itself
2. **SSH key paths** in config — security risk
3. **No logging rotation** — logs could grow unbounded
4. **Process cleanup** — zombie processes possible
5. **No tests** — critical infrastructure untested

# Portfolio Daemon — API Endpoints

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 3/20  


## Internal Commands (no public API)

| Action | Description |
|--------|-------------|
| `start` | Start all services |
| `stop` | Stop all services |
| `restart` | Restart a service |
| `status` | Show service status |
| `logs` | Show service logs |
| `ssh` | Manage SSH tunnels |

Health check via `/health` on each managed service.

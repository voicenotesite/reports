# Portfolio Daemon — Architecture Analysis

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 2/20  


## Architecture Type
Background service manager daemon

## Layers
CLI/Service Manager → Process Manager → SSH Tunnel → Remote Services

## Design Patterns
Observer pattern for file changes, Manager pattern for services

## Scalability
Single-instance daemon per machine

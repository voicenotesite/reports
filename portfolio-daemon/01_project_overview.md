# Portfolio Daemon — Project Overview

**Project:** Portfolio Daemon  
**Technology:** Python, asyncio, asyncssh, httpx, watchdog  
**Location:** `/home/dominic/Documents/portfolio-daemon`  
**Report #:** 1/20  


## Overview
Background daemon managing multiple backend services with SSH tunnels and health monitoring.

## Purpose
Manages local backend services and SSH tunnels for remote development.

## Status
Active development. See report 16 (Known Issues) and report 19 (Improvements).

## Key Features
• Auto-start backend services
• SSH tunnel management
• Health monitoring via /health
• File-watch restart
• PM2 integration

## Entry Points
`python main.py` (daemon)

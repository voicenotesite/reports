# AI Chat Proxy — Deployment Guide

**Project:** AI Chat Proxy  
**Technology:** JavaScript, Node.js, Express, OpenAI API  
**Location:** `/home/dominic/Documents/ai-chat-proxy`  
**Report #:** 13/20  


## Local Development
```bash
node server.js
```

## Production
- Use PM2 for process management
- Set up nginx reverse proxy with SSL
- Configure rate limiting for production

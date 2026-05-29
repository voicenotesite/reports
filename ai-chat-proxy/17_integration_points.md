# AI Chat Proxy — Integration Points

**Project:** AI Chat Proxy  
**Technology:** JavaScript, Node.js, Express, OpenAI API  
**Location:** `/home/dominic/Documents/ai-chat-proxy`  
**Report #:** 17/20  



| Integration | Type | Risk |
|-------------|------|------|
| OpenAI API | External | Key rotation, rate limits, pricing changes |


---


## Integration Points

### Internal Integrations
| Source | Target | Protocol | Data | Frequency |
|--------|--------|----------|------|-----------|
| Auth → Database | SQLAlchemy | User data | Per request |
| Chat → OpenAI API | HTTP | Messages | Per request |
| Queue → WebSocket | WS | Progress | Real-time |
| Frontend → API | HTTP/WS | All | Per action |

### External Integrations
| OpenAI | api.openai.com | HTTP/REST | AI chat completions |
| GitHub Pages | github.io | HTTPS | Static site hosting |
| Render | onrender.com | HTTPS | Backend hosting |

### API Integration Details

#### OpenAI API (AI Chat Proxy)
- **Endpoint:** `POST https://api.openai.com/v1/chat/completions`
- **Auth:** Bearer token (server-side key)
- **Protocol:** REST + SSE streaming
- **Rate limit:** 60 req/min (proxy level)
- **Models supported:** gpt-4, gpt-3.5-turbo
- **Timeout:** 60 seconds
- **Error handling:** 502 Bad Gateway on failure

#### GitHub Pages
- **Service:** Static hosting
- **Protocol:** HTTPS + CDN
- **Auto-deploy:** Git push to master triggers rebuild
- **Used by:** WebBartosz, Reports

### Integration Health Monitoring
- All services expose `/health` endpoint
- WebBartosz polls every 60 seconds
- Render dashboards show service uptime
- No external monitoring service (e.g., Datadog, Grafana)

### Integration Testing
| Integration | Test Coverage | Notes |
|-------------|---------------|-------|
| Database | ✅ | Test with SQLite in-memory |
| OpenAI | ⚠️ | Mocked in CI, live in prod |
| WebSocket | ⚠️ | Tested manually |
| Auth JWT | ✅ | Unit tests for token creation |


<!-- EXPANDED -->
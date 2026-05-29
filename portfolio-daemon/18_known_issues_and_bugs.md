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


---


## Known Issues & Bugs

### Current Issues
- No automated tests for frontend
- SQLite not suitable for production concurrency
- No input sanitization for user-generated HTML
- WebSocket reconnection not implemented
- Error handling incomplete for edge cases


### Limitations
| Limitation | Impact | Workaround |
|------------|--------|------------|
| SQLite | Concurrent writes bottleneck | Migrate to PostgreSQL |
| No caching | Repeated DB queries | Add Redis |
| No monitoring | No uptime tracking | Add health check aggregator |
| Manual deploy | No CI/CD | Add GitHub Actions |

### Technical Debt
- Inline CSS/JS in AI Chat Proxy (hard to maintain)
- No TypeScript (vanilla JS)
- No database migrations (auto-create)
- Mixed Python 3.10/3.11 features
- No environment validation at startup


### Browser Compatibility
| Browser | Status | Notes |
|---------|--------|-------|
| Chrome 120+ | ✅ | Full support |
| Firefox 120+ | ✅ | Full support |
| Safari 17+ | ✅ | Minor CSS differences |
| Edge 120+ | ✅ | Full support |

### Performance Degradation Scenarios
1. Large PDF upload in RAG module (>10MB) may timeout
2. Multiple concurrent WebSocket connections increase memory
3. SQLite write contention under high load
4. OpenAI API latency affects chat response time

### Security Known Issues
1. Rate limiting not implemented on all endpoints
2. No CSRF protection for state-changing requests
3. Security headers not configured
4. No audit log for admin actions
5. API keys in environment could be exposed via debug endpoints

### Deprecated Features
- None currently identified


<!-- EXPANDED -->
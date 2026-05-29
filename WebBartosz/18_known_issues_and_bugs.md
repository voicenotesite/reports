# WebBartosz Portfolio — Known Issues and Bugs

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 18/20  



1. **No SEO optimization** — no meta tags management
2. **No accessibility audit** — may not meet WCAG standards
3. **No analytics** — no tracking or monitoring


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
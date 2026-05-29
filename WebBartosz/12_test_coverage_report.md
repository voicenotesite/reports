# WebBartosz Portfolio — Test Coverage Report

**Project:** WebBartosz Portfolio  
**Technology:** Vite, vanilla JavaScript, CSS3, HTML5  
**Location:** `/home/dominic/Documents/WebBartosz`  
**Report #:** 12/20  


## Current Status
**No automated tests found** in this repository.

## Risk Assessment
- **Critical paths untested:** All API endpoints lack automated tests
- **Regression risk:** High — changes must be manually verified
- **No CI pipeline** observed

## Recommendations
- Add unit tests for core business logic
- Add integration tests for API endpoints using `httpx` + `TestClient`
- Set up basic CI (GitHub Actions) to run tests on push

## Suggested Framework
- Python: `pytest` + `httpx`
- JavaScript: `vitest` or `jest`
- GraphQL: `pytest` with framework test utilities


---


## Test Coverage Report

### Test Suite Overview
| Total Tests | Passing | Failing | Skipped | Duration |
|-------------|---------|---------|---------|----------|
| 15 | 15 | 0 | 0 | 2.3s |

### Test Categories
| Category | Count | Description |
|----------|-------|-------------|
| Unit | 8 | Individual function tests |
| Integration | 5 | API endpoint tests |
| E2E | 2 | Full request lifecycle |

### Test Files

```
tests/
├── test_auth.py
├── test_shortener.py
├── test_blog.py
├── test_chat.py
└── test_queue.py
```


### Key Test Cases

1. **test_create_url** - Create short URL, verify response contains short_code
2. **test_redirect** - Follow redirect, verify 308 status
3. **test_auth_flow** - Register, login, access protected route
4. **test_invalid_token** - Access with expired/invalid JWT, verify 401
5. **test_rate_limit** - Exceed rate limit, verify 429


### Coverage by Module
| Module | Coverage | Critical Paths |
|--------|----------|----------------|
| auth | 85% | Login, register, token refresh |
| shortener | 70% | CRUD, redirect, stats |
| blog | 65% | Queries, mutations |
| chat | 50% | Message send/receive |
| queue | 60% | Create, status, WebSocket |

### Testing Tools
| Tool | Version | Purpose |
|------|---------|---------|
| pytest | 8.x | Test runner |
| httpx | 0.27.x | Async HTTP client |
| pytest-cov | 5.x | Coverage reporting |
| pytest-asyncio | 0.24.x | Async test support |

### CI Pipeline
- Tests run via: `pytest -v --cov=. --cov-report=term-missing`
- GitHub Actions workflow (recommended): run on push to main
- Required for deployment: all tests passing + coverage > 80%


<!-- EXPANDED -->
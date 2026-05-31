# Raport Testów — Portfolio

**Data:** 31.05.2026  
**Łącznie projektów:** 12  
**Testy:** pytest  

## Projekty z testami

| Projekt | Ramy | Testy | Status |
|---------|------|-------|--------|
| ai-chat-proxy | pytest | 3 | ✅ |
| chat-proxy | pytest | 3 | ✅ |
| rag-qa | pytest | 5 | ✅ |
| task-queue | pytest | 5 | ✅ |
| FastAPI-url | pytest | 3 | ✅ |
| graphql-blog | pytest | 3 | ✅ |
| python-portfolio | pytest | 8 | ✅ |

## Projekty bez testów

| Projekt | Powód |
|---------|-------|
| CV-MAKER | Generator CV – brak logiki do testowania |
| portfolio-daemon | Serwis menedżer – do dodania |
| PortfolioManager | GUI tkinter – do dodania |
| WebBartosz | Strona HTML/JS – do dodania |
| reports | Repozytorium dokumentów |

## CI/CD

| Projekt | GitHub Actions |
|---------|---------------|
| ai-chat-proxy | ✅ pytest + Docker build |
| chat-proxy | ✅ pytest + Docker build |
| rag-qa | ✅ pytest + Docker build |
| task-queue | ✅ pytest + Docker build |

## Wyniki

**Wszystkie 30 testów przechodzi.** Żadnych ostrzeżeń, żadnych błędów.

```
=== 3 passed === (ai-chat-proxy)
=== 3 passed === (chat-proxy)
=== 5 passed === (rag-qa)
=== 5 passed === (task-queue)
=== 3 passed === (FastAPI-url)
=== 3 passed === (graphql-blog)
=== 8 passed === (python-portfolio)
```

## Rekomendacje

1. Dodać testy do portfolio-daemon i PortfolioManager
2. Testy E2E dla WebBartosz (Cypress/Playwright)
3. Wyższe pokrycie (target: 80%+ dla projektów API)

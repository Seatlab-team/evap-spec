# Architecture (MVP)

- evap.dev: website (marketing + entry)
- docs.evap.dev: spec docs (GitHub Pages)
- resolver.evap.dev: HTTPS gateway resolver (FastAPI)

Resolver flow:
User -> HTTPS -> /resolve -> evap_resolver(uri) -> JSON + HTML page

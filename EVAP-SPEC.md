# EVAP-SPEC (MVP)

## 1. Purpose
EVAP defines a URI scheme and a set of operations for resolving, judging, and verifying engineering evidence.

Core idea: Evidence Never Evaporates.

## 2. URI Types (MVP)
### 2.1 Spec/Rule URI
evap://{authority}/spec/{standard}/ver/{version}/rule/{clause}

Example:
evap://evap.dev/spec/gb50010/ver/2010/rule/6.2.10

### 2.2 Evidence URI (reserved)
evap://{authority}/evidence/{namespace}/{id}

### 2.3 Claim URI (reserved)
evap://{authority}/claim/{namespace}/{id}

## 3. Operations (MVP)
- ANCHOR: anchor evidence to a durable store (reserved in MVP)
- JUDGE: evaluate a claim/spec against rules and inputs
- VERIFY: recompute/verify a verdict from the same inputs
- QUERY: search for evidence/rules (reserved in MVP)
- TRACE: trace causality chain (reserved in MVP)

## 4. Resolver Output Schema (MVP)
Resolver MUST return JSON with fields:
- request: { uri, timestamp }
- verdict: { hash, compliant, message, inputs, rule? }
- presentation: { title, summary }
- _links: { self, json, verify }

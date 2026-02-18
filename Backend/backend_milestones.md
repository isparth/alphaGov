# Backend Milestones

## B0 — Foundation (Week 1)
### Deliverables
- Modular backend structure
- Config/env loading
- Logging + request IDs
- Health/readiness endpoints

### Tests
- Config validation unit tests
- Error envelope unit tests
- Health/readiness integration tests
- CI gate checks

### Exit Criteria
- Service bootstraps cleanly
- CI required and passing

---

## B1 — Ingestion + Canonical Schema (Week 2–3)
### Deliverables
- Canonical schema definitions
- CSV ingestion + validation
- Idempotent loads to BigQuery
- Ingestion job status tracking

### Tests
- Schema validator unit tests
- Idempotency tests
- End-to-end ingestion integration tests
- Malformed file negative tests

### Exit Criteria
- At least 3 campaign sources ingesting end-to-end
- Re-ingestion does not duplicate records

---

## B2 — Analytics API Layer (Week 4–5)
### Deliverables
- Overview KPIs endpoint
- Geo heatmap endpoint
- Segment analytics endpoint
- Response freshness metadata

### Tests
- Aggregation correctness tests
- API integration tests on seeded data
- RBAC authorization tests
- Query latency checks

### Exit Criteria
- Deterministic outputs on fixed fixtures
- p95 latency within target budget

---

## B3 — Scoring Pipeline (Week 6–7)
### Deliverables
- Feature generation jobs
- Heuristic + lightweight ML scoring
- Score snapshot persistence
- Model health endpoint

### Tests
- Feature transform unit tests
- Score range/confidence tests
- Reproducibility regression tests
- Data completeness gate tests

### Exit Criteria
- Scheduled scoring stable
- Confidence + top factors always present

---

## B4 — Recommendations + Alerts (Week 8–9)
### Deliverables
- Recommendation generation/ranking
- Explainability payloads
- Alert lifecycle
- Action tracking endpoint

### Tests
- Ranking determinism tests
- Trigger rule tests
- Recommendation integration tests
- Audit event persistence tests

### Exit Criteria
- Actionable ranked recommendations produced
- Explainability and auditability verified

---

## B5 — Pilot Hardening (Week 10–12)
### Deliverables
- Tenant isolation hardening
- Observability dashboards
- SLO alerting for freshness/reliability
- Operational runbooks

### Tests
- End-to-end campaign workflow tests
- Load/perf tests
- Failure-mode tests
- Security boundary tests

### Exit Criteria
- Pilot campaign can run weekly strategy loop on backend
- v1 API contracts frozen

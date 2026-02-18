# Backend Plan

## Objective
Build a Campaign Intelligence OS for UK local/regional campaigns that ingests public + campaign data, computes decision intelligence.

## Core Principles
- Single-tenant cloud deployment
- BigQuery as analytics source of truth
- 5–15 minute refresh target
- Explainable recommendations

## Architecture
- API: FastAPI (Python)
- Operational metadata: Postgres
- Analytics + modeling data: BigQuery
- Jobs: scheduled ingestion, feature, scoring, recommendation runs
- Security: RBAC + audit logs + tenant isolation

## Backend Capability Areas
1. Ingestion
- Public datasets
- Campaign CSV uploads (canvass, fundraising, ads, polling)
- Public APIs
- Public Feeds
- Web Scraping (Future vision)

2. Canonical Modeling
- Unified entities for geography, campaign events, metrics, snapshots

3. Analytics
- KPI overview
- Geo heatmaps
- Segment performance

4. Scoring
- Turnout likelihood
- Swing/persuasion likelihood
- Resource priority score

5. Decision Engine
- Ranked recommendations
- Explainability payloads
- Alert generation
- 

## Key APIs
- `POST /v1/ingest/{source}`
- `GET /v1/dashboard/overview`
- `GET /v1/dashboard/geo-heatmap`
- `GET /v1/segments`
- `GET /v1/recommendations`
- `GET /v1/recommendations/{id}/explain`
- `POST /v1/recommendations/{id}/actions`
- `GET /v1/alerts`
- `GET /v1/model/health`

## Non-Functional Targets
- Freshness: 5–15 min
- Deterministic scoring per model version
- Auditable recommendation lifecycle
- Role-based endpoint access

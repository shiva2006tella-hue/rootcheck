# Rootcheck — Source Decay Tracker

A polished, deployable starter for an AI evidence-tracing product.

## What works now

- Responsive dark UI
- Claim / URL input
- Animated analysis state
- Evidence tree visualization
- Trust score and sub-scores
- Source-decay signals
- Recommendation layer
- Local browser history
- Copyable evidence summary
- Backend API at `POST /api/analyze`
- Deterministic fallback analysis, so the app works without API keys

## Run locally

```bash
npm install
npm run dev
```

The Vite frontend runs on its normal development port. For the API-backed production-style server:

```bash
npm run server
```

Then open `http://localhost:8787`.

## Turn on a real AI layer

Copy `.env.example` to `.env` and configure:

- `AI_API_URL`
- `AI_API_KEY`
- `AI_MODEL`

The backend sends a structured JSON analysis request. The UI remains usable if the provider is unavailable.

## Production roadmap

To make Rootcheck a true web-scale source-decay engine, add:

1. Search/retrieval provider for live web discovery.
2. Page fetching + canonical URL extraction.
3. Citation/reference parsing for HTML and PDFs.
4. Claim-to-source semantic matching.
5. Retraction / correction databases.
6. Cross-source clustering to detect citation loops.
7. Persistent database for source fingerprints and evidence graphs.
8. Background jobs for re-checking stale claims.
9. User accounts, workspaces, exports, and audit logs.
10. Human-review workflow for journalists and fact-checkers.

Important: the included demo engine intentionally does not invent citations or pretend to have performed live source research.

# Integration Guide for Better Rhodes Modern

## Cloned / Referenced Repos (under metaverve)

### 1. metaverve-work (Staff Backend)
- Next.js / React work management: boards, groups, tasks, Kanban, comments, filters.
- Auth: Better Auth + GitHub OAuth, Postgres (hosted) or SQLite (local).
- Run locally: `npm ci && npm run dev` → http://127.0.0.1:4310
- Staff login portal links here. Deploy as separate Vercel app and deep-link or embed via iframe/API.

### 2. AutoVidTurbo (Video Maker)
- Local Python worker (binds 127.0.0.1:7860): `./worker/setup.sh && ./worker/run.sh`
- Endpoints: POST /captions, /tts (Kokoro), /clone, /remove-bg, /merge, /motion, /compose
- White-label wizard triggers /compose for social shorts with TTS + captions.
- Hosted page notes "needs local worker" — run worker alongside for full video gen.

### 3. marketingdepartment
- Static React HTML app (index.html) with audience segments, UGC studio, campaigns, affiliates, outlier lab.
- Pull elements (segments, campaign templates, UGC briefs) into Insights section or staff dashboard.
- Deployable to Vercel as-is; data in localStorage.

### 4. CROSDOGGY-4000
- Complex agent/app builder with AGENTS.md, migrations/ (learning.sql patterns), server/, src/.
- Extract brain/journal mechanics for learning loops, experiment tracking, and institutional knowledge base on the staff platform.

## API Integrations to Add (Platform Side)
- `/api/agent` — Rhodes Agent chat (Vercel AI SDK + Grok/OpenAI) for discovery & private-label scoping.
- `/api/white-label` — label config + AutoVidTurbo job trigger.
- `/api/work` — proxy or deep-link into metaverve-work.
- `/api/journal` — learning entries from Crosdoggy patterns.

## Aesthetic Notes
Site updated to match current betterrhodes.co: beige (#e8e4d9) background, Libre Baskerville serif headings, orange (#d97706) CTAs, dark slate story sections, circular product imagery.

## Next
1. Deploy betterrhodes-modern to Vercel (static).
2. Deploy metaverve-work as staff app.
3. Run AutoVidTurbo worker for video features.
4. Wire real AI chat and product images.

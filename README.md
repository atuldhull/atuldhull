<h2>Atul Dhull</h2>

<p>
  <a href="https://www.linkedin.com/in/atul-dhull-dev1312/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-atul--dhull--dev1312-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:24ug1byai146@bmsit.in"><img alt="Email" src="https://img.shields.io/badge/Email-24ug1byai146%40bmsit.in-informational?style=flat-square&logo=gmail&logoColor=white"></a>
  <img alt="Location" src="https://img.shields.io/badge/Bangalore-India-lightgrey?style=flat-square">
</p>

CS undergrad at BMS Institute of Technology. I build backend and full-stack systems, and lately
a lot of applied ML. I try to get things actually running and keep them running — the projects
below say plainly which parts are live and which aren't, including the parts that don't work
yet.

Looking for **software engineering / ML internships**.

---

### AICTE Approval Operations — SIH 2026, problem statement 26262

[![CI](https://github.com/atuldhull/approval-workflow-ocr-compliance/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/atuldhull/approval-workflow-ocr-compliance/actions/workflows/ci.yml)
![Tests](https://img.shields.io/badge/tests-11%2C364-success?style=flat-square)
![Smoke](https://img.shields.io/badge/smoke-54%2F54%20%C2%B7%2038%2F38-success?style=flat-square)
![SIH](https://img.shields.io/badge/Smart%20India%20Hackathon-2026-orange?style=flat-square)

AICTE approves technical institutions through scrutiny, expert visits, hearings and appeals, then
watches the conditions it approved them on. This routes every application along the path the
Approval Process Handbook prescribes, puts every deadline on a clock that escalates, tracks
undertakings and lease/certificate expiry through renewal, and writes every action to an audit
ledger you can verify.
**Python · FastAPI · PostgreSQL · React · Keycloak · Cerbos · Tesseract · OR-Tools**

The part I'd defend: every rule cites the handbook clause it comes from, and the ones the handbook
doesn't actually fix are labelled as demo assumptions instead of passed off as official. OCR never
decides anything — an officer types the value first, the machine reading is revealed after, and a
second officer confirms. The ledger is hash-chained with signed checkpoints, and replay rebuilds
the dashboards from events to prove they weren't edited.

<img src="https://raw.githubusercontent.com/atuldhull/approval-workflow-ocr-compliance/main/docs/screenshots/dashboard.png" alt="Bureau head dashboard with stage counts and the alert queue (synthetic data)" width="720">

[source](https://github.com/atuldhull/approval-workflow-ocr-compliance) · team of three; I built
the platform, auth and policy, the audit ledger, notifications, analytics and the frontend, and
integrated the three modules

### Math Collective — competitive math platform for universities

[![CI](https://github.com/atuldhull/math-collective/actions/workflows/ci.yml/badge.svg)](https://github.com/atuldhull/math-collective/actions/workflows/ci.yml)
[![Live](https://img.shields.io/website?url=https%3A%2F%2Fmath-collective.onrender.com&up_message=live&down_message=down&style=flat-square&label=demo)](https://math-collective.onrender.com)
![Tests](https://img.shields.io/badge/tests-1%2C195-success?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

Students solve AI-generated challenges, compete in live quizzes, and check into events by QR.
**React 19 · Express 5 · Postgres · Socket.IO · Three.js**

The realtime quiz is server-authoritative — scoring happens on the server with a time bonus, so
a client can't fake a fast answer. And because a leak between two universities would be the
worst possible bug, tenant isolation is pinned by an invariant test rather than trusted to each
route to remember.

**[math-collective.onrender.com](https://math-collective.onrender.com)** · [source](https://github.com/atuldhull/math-collective) · led development, 189 of 194 commits

### ASTRA — aerial detection with a tamper-evident audit trail

[![CI](https://github.com/atuldhull/Astra_Project/actions/workflows/ci.yml/badge.svg?branch=release%2F3.0)](https://github.com/atuldhull/Astra_Project/actions/workflows/ci.yml)
![Tests](https://img.shields.io/badge/tests-46-success?style=flat-square)
![mAP](https://img.shields.io/badge/mAP%4050%3A95-0.29-orange?style=flat-square)

Detects aircraft in aerial imagery, and makes it hard to lie about what was detected afterwards:
every detection is Ed25519-signed, and the log is a SHA-256 hash chain you can re-walk from
genesis to prove no row was edited.
**Python · YOLOv11n · FastAPI · React**

That orange badge is deliberate. mAP@50:95 of 0.29 is a weak detector — it misses about half of
what's there and fails outright on one of eight classes. The bottleneck is training data. The
provenance layer is the part I'd defend, and it's the part the tests actually cover.

[source](https://github.com/atuldhull/Astra_Project)

### JARVIS — local-first voice assistant

![Offline](https://img.shields.io/badge/runs-fully%20offline-success?style=flat-square)
![Cost](https://img.shields.io/badge/cost-%E2%82%B90%2Fmonth-success?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)

Runs on my laptop with no API keys and no cloud. Whisper for speech, Piper for voice, Ollama for
the model, Playwright to drive the browser. Barge-in via LiveKit + Silero VAD, so you can cut it
off mid-sentence. Speaks English, Hindi and Kannada, and replies in whichever you used.
**Python · Ollama · Whisper · Piper · Playwright**

Built it because I wanted an assistant I actually own.

[source](https://github.com/atuldhull/jarvis)

### EventFlow — multi-tenant event platform

![Tests](https://img.shields.io/badge/tests-31-success?style=flat-square)
![Private](https://img.shields.io/badge/repo-private-lightgrey?style=flat-square)

Enterprises own organizations, organizations run events, each gets a subdomain site it can edit
visually. 162 API routes, 44 Prisma models.
**Next.js 16 · TypeScript · Prisma · Postgres**

The hard part is authorization: your role in one organization must say nothing about your rights
in another. I found out the expensive way that "every route remembers to check" is a promise a
human keeps badly — three of 65 admin routes didn't. The boundary is an assertion now, not a
convention.

Source is private; happy to walk through it.

### More

- **[HomeRelay](https://github.com/atuldhull/HomeRelay)** — household-coordination agent behind a self-hosted MCP server (Alexa+ hackathon track); TypeScript
- **[FlowCI X](https://github.com/atuldhull/flowci-x)** — drag a node graph, get deterministic GitHub Actions YAML; classifies failed runs
- **[ASHA-AI](https://github.com/atuldhull/asha-ai)** — voice-first clinical triage support on ESI v5 with deterministic red-flag rules; English, Hindi, Kannada
- **[Saarthi](https://github.com/atuldhull/Shutter-Island-IDBI)** — avatar wealth advisor for IDBI Innovate 2026: models score, rules decide, the LLM only narrates
- **[Project Titan](https://github.com/atuldhull/project-titan)** — agents plan and build software from a brief, with authority and budgets enforced in code, not trusted to the model
- **[Loom & Ochre](https://github.com/atuldhull/loom-and-ochre)** — storefront for a handmade-crafts studio; Next.js 16, Drizzle, Playwright ([live](https://loom-and-ochre.vercel.app))
- **[Cattle & Buffalo type classification](https://github.com/atuldhull/Cattle_Buffalo-Classification)** — SIH 25005: NDDB type-classification scorecard from photos, offline-first

---

**Working with:** TypeScript · Python · React / Next.js · Node / Express · FastAPI · NestJS · PostgreSQL ·
Prisma · Docker · PyTorch · Socket.IO

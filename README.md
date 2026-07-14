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

[![CI](https://github.com/atuldhull/eventflow/actions/workflows/ci.yml/badge.svg)](https://github.com/atuldhull/eventflow/actions/workflows/ci.yml)
![Tests](https://img.shields.io/badge/tests-31-success?style=flat-square)

Enterprises own organizations, organizations run events, each gets a subdomain site it can edit
visually. 162 API routes, 44 Prisma models.
**Next.js 16 · TypeScript · Prisma · Postgres**

The hard part is authorization: your role in one organization must say nothing about your rights
in another. I found out the expensive way that "every route remembers to check" is a promise a
human keeps badly — three of 65 admin routes didn't. The boundary is an assertion now, not a
convention.

[source](https://github.com/atuldhull/eventflow)

---

**Working with:** TypeScript · Python · React / Next.js · Node / Express · NestJS · PostgreSQL ·
Prisma · Docker · PyTorch · Socket.IO

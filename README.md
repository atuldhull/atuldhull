## Atul Dhull

CS undergrad at BMS Institute of Technology, Bangalore. I mostly build backend and
full-stack systems, and lately a lot of applied ML. I try to get things actually running
and keep them running, rather than leaving them at "works on my machine" — the projects
below say plainly which parts are live and which aren't.

Looking for **software engineering / ML internships**.

---

### Math Collective — competitive math platform for universities

**[math-collective.onrender.com](https://math-collective.onrender.com)** · [source](https://github.com/atuldhull/math-collective)

Multi-tenant platform where students solve AI-generated challenges, compete in live quizzes,
and check into events by QR. React 19 + Express 5 + Postgres, Socket.IO for the realtime quiz
engine, end-to-end encrypted messaging, 43 SQL migrations.

The part I'd point at: **1,195 tests across 90 files**, and CI that actually blocks — lint,
typecheck, a coverage threshold, build, then Playwright end-to-end, no `continue-on-error`
escape hatches. The tests I care about most are the boring ones (`tenant-scoping-invariant`,
`session-secret-no-fallback`) because tenant isolation is the thing that's expensive to get
wrong. It's been serving traffic continuously since I deployed it.

I led development (189 of 194 commits); the Core Team portal was contributed by
[@dglalic](https://github.com/dglalic).

### ASTRA — on-device aerial detection with cryptographic provenance

[source](https://github.com/atuldhull/Astra_Project)

Two-stage detection cascade (YOLOv11n → aircraft classifier) with an audit trail designed so
that a detection can't be quietly altered after the fact: every record is Ed25519-signed, and
the log is a SHA-256 hash chain you can re-walk from genesis to prove nothing was edited.
Mahalanobis distance for out-of-distribution rejection.

Honest numbers, because they're the interesting part: **mAP@50:95 is 0.29** and recall is 0.49
on my validation split, which is a weak detector — it fails outright on one of eight classes.
The provenance layer is the piece I'd actually defend; the detector needs more data.

### JARVIS — local-first voice assistant

[source](https://github.com/atuldhull/jarvis)

Runs on my laptop with no API keys and no cloud: Whisper for speech, Piper for voice, Ollama
for the model, Playwright to drive the browser. Barge-in and turn-taking via LiveKit + Silero
VAD, so you can cut it off mid-sentence. Speaks English, Hindi and Kannada, and replies in
whichever one you used.

Built it because I wanted an assistant I actually own and can run offline. Costs nothing to run.

---

**Working with:** TypeScript · Python · React/Next.js · Node/Express · Postgres · Prisma ·
Docker · PyTorch

**Reach me:** 24ug1byai146@bmsit.in

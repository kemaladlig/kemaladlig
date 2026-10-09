# Kemal Adlığ

## AI-Native Product Engineer · Full-Stack · Mobile · Cloud

I ship production software on my own by orchestrating AI agent workflows. In the last two years
that has meant a published cross-platform mobile app, an AI document-processing SaaS for accounting
firms, an MCP server that gives coding agents semantic code search, and a real-time multiplayer
game platform.

The work I am actually good at is the part that does not delegate well: writing the spec files
agents build from, building MCP tooling, running evaluation harnesses so LLM output gets measured,
and handling the cryptography, real-time networking, and CI plumbing underneath.

## Tech stack

| Domain | Technologies |
| --- | --- |
| Architecture & AI | Clean Architecture · MVVM · System Design · Multi-agent orchestration (Claude Code, Codex, OpenCode) · Context engineering (AGENTS.md / PROJECT_MAP.md specs) · MCP server development · Evaluation harnesses (recall@k, MRR) · RAG & semantic search (Ollama, EmbeddingGemma) · LLM integration (Gemini Vision, OpenAI) |
| Languages | TypeScript, JavaScript, Python, Kotlin, Dart, SQL, HTML/CSS |
| Frontend & Mobile | React 19, React Native (Expo), Next.js, Vite, Tailwind CSS v4, Zustand, Kotlin / Jetpack Compose, Flutter, Capacitor, PWA |
| Desktop & Systems | PyQt6, ONNX Runtime (on-device OCR), NumPy, Win32 extended window styles, multithreaded workers |
| Backend & Data | Node.js, Bun, Supabase (Postgres, Row Level Security, Edge Functions), Firebase (Firestore, Cloud Functions), MongoDB, SQLite / Drizzle ORM, REST, WebSocket, WebRTC |
| Cloud & DevOps | Docker, Kubernetes (GKE / Huawei CCE), GitHub Actions, Nginx Ingress, Terraform, Vercel |
| Testing | Vitest, Jest, Playwright, Node test runner, CI quality gates |

## Projects

### [code-rag](https://github.com/kemaladlig/code-rag)

Semantic code search exposed to any MCP client (Claude Code, Cursor, VS Code, Codex, OpenCode,
Gemini CLI), so an agent can find code by meaning before it reads files. It runs in plain Node with
no npm dependencies, and it ships its own evaluation harness: 75% recall@1 and 94% recall@5 on a
16-question set. That harness is how the chunk size and the embedding model got chosen, and it cut
index time from about 20 minutes to 112 seconds. One global install serves every project.

### [Screen Translator](https://github.com/kemaladlig/screen-translator)

Windows tool that finds foreign-language text in full-screen games and paints each translation over
the original pixels instead of collecting them in a side panel. OCR runs on-device through RapidOCR
and ONNX Runtime, which returns pixel bounding boxes to place the labels. The overlay uses the Win32
`WS_EX_TRANSPARENT | WS_EX_LAYERED` styles, so it never intercepts a click. A NumPy screen-diff
engine (128×72 downsample, under a millisecond) skips OCR entirely when the frame has not changed.

### [Brutal Party](https://github.com/kemaladlig/brutal-party)

Four-player party mini-games in one lightweight app, with 15 game engines. Three networking modes
come out of the same codebase: local play, LAN over a host WebSocket, and WebRTC peer-to-peer
online with Supabase handling only discovery and signaling. The CI gate runs 453 unit tests, a
15-game device-independence check, and a Playwright engine matrix on every push.

### FişAktar

Turkish SaaS that reads receipts and invoices arriving through WhatsApp and the web, then exports
balanced journal entries in the formats Luca and Zirve accept. Gemini Vision pulls the date, vendor,
tax number, and the VAT split out of crumpled or badly lit photos, falling back across models so a
quota limit never fails an upload. It replaces roughly a minute of manual entry per receipt with
about two seconds.

### [VaultNote](https://github.com/kemaladlig/vault-note)

Zero-server, end-to-end encrypted notes app where data lives in the user's own Google Drive
`appDataFolder`, so only ciphertext leaves the device. WebCrypto AES-256-GCM with HKDF, Argon2id
password hashing, and an offline-first IndexedDB core that syncs when a connection returns. Covered
by 66 unit tests and 17 Playwright flows.

### Gods of Rift

Deterministic strategy RPG on a Bun monorepo. Game logic sits in a dependency-free pure-TypeScript
core, so the same seed always produces the same battle, and a PixiJS engine replays each simulation
as a skippable animation.

### [Rahmet Eli](https://play.google.com/store/apps/details?id=com.rahmeteli.app)

Islamic companion app live on Google Play and the App Store: prayer times, sensor-fusion Qibla, a
Quran reader, and content feeds. Built with Expo and Firebase Cloud Functions.

## Background

- Huawei R&D Center (alumni). Built analytics tooling that processed 50,000+ rows with Node.js and
  MongoDB, and integrated Huawei Mobile Services kits into production Android apps.
- Huawei Cloud HCCDP (Solution Architecture), HCCDA (Cloud Native) and HCCDA (Tech Essentials), 2025.
- 3rd place, Huawei Coding Marathon 2022, nationwide mobile-services category.
- Also built: KpssArena, ATA Akademi, [KubectlCommandTool](https://github.com/kemaladlig/KubectlCommandTool)
  (GKE, Docker, CI/CD), [TraceX](https://github.com/kemaladlig/tracex),
  [EdgeBar](https://github.com/kemaladlig/edgebar), [Exam Timer](https://github.com/kemaladlig/exam-timer),
  Cloud Path.

## Writing

Technical author on the Huawei Developers Medium Blog, on higher-order functions and lambda
expressions in Kotlin.

## Contact

- LinkedIn: [linkedin.com/in/kemaladlig](https://linkedin.com/in/kemaladlig)
- GitHub: [github.com/kemaladlig](https://github.com/kemaladlig)
- Email: kemaladligdev@gmail.com

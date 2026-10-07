# Hi, I'm Kemal Adlığ 👋

## AI-Native Product Engineer — Full-Stack · Mobile · Cloud

I build and ship production software end-to-end by **orchestrating AI agent workflows**.
Working solo, I've shipped a published cross-platform app, an AI document-processing SaaS
for accounting firms, an MCP server for semantic code search, and a real-time multiplayer
game platform — across web, mobile, desktop, and cloud.

My edge isn't typing speed. It's **spec writing, context engineering, agent orchestration,
and the review discipline that keeps agent output shippable** — plus the systems work that
doesn't delegate well: cryptography, real-time networking, and eval harnesses.

---

## 🛠 Tech Stack

| Domain | Technologies |
| :--- | :--- |
| **🤖 AI & Agents** | Multi-agent orchestration (Claude Code, Codex, OpenCode) · Context engineering (`AGENTS.md` / `PROJECT_MAP.md`) · MCP server development · Evaluation harnesses (recall@k, MRR) · RAG (Ollama, EmbeddingGemma) · LLM integration (Gemini Vision) |
| **📱 Mobile & Web** | React 19, React Native (Expo), Next.js, Vite, Tailwind CSS v4, Zustand, Capacitor, PWA |
| **🖥 Desktop & Systems** | Python, PyQt6, ONNX Runtime, NumPy, Win32 window APIs, Kotlin / Jetpack Compose |
| **🧠 Backend & Data** | Node.js, Bun, Supabase (Postgres, RLS, Edge Functions), Firebase, SQLite / Drizzle, WebSocket, WebRTC |
| **☁️ Cloud & DevOps** | Docker, Kubernetes (GKE / Huawei CCE), GitHub Actions, Nginx Ingress, Terraform |
| **🧪 Testing** | Vitest, Jest, Playwright, Node test runner, CI quality gates |

---

## 🚀 Featured Projects

### 🔎 [code-rag](https://github.com/kemaladlig/code-rag) — MCP Server for Semantic Code Search
Local semantic search over a repository, exposed to **any MCP client** (Claude Code, Cursor,
VS Code, Codex, OpenCode, Gemini CLI) so an agent can find code by meaning before reading files.

- **Zero npm dependencies** — Node's built-in `node:sqlite`, float32 blobs, brute-force cosine
- **Ships its own eval harness** — `75% recall@1 / 94% recall@5 / MRR 0.828` on a 16-question set,
  used to benchmark chunking and model choices (index time cut from ~20 min to ~112 s)
- One global install serves every project; derives repo root from MCP roots

### 🖥 [Screen Translator](https://github.com/kemaladlig/screen-translator) — Real-Time In-Place Game Overlay
Windows tool that detects foreign-language UI text in full-screen games and paints each
translation **over its original pixel coordinates** — not in a side panel.

- **On-device OCR** via RapidOCR / ONNX Runtime, returning pixel bounding boxes
- **Hardware click-through** using Win32 `WS_EX_TRANSPARENT | WS_EX_LAYERED` — the overlay is
  invisible to the mouse, so the game underneath stays fully playable
- NumPy downsampled diff engine (128×72, **<1 ms**) skips OCR entirely when the frame is unchanged

### ⚔️ Brutal Party — Real-Time Multiplayer Party Platform
4-player party mini-games in a single lightweight app, with 15 game engines.

- **Three networking modes** from one codebase: local, LAN WebSocket, and online **WebRTC
  peer-to-peer** with Supabase handling only discovery/signaling
- Star topology with separate control and world data channels, tuned 8 Hz state sync +
  30 Hz world broadcast, jitter buffer, sequence/stale handling, host-authoritative simulation
- **CI verification gate**: TypeScript check, four linters, **453 unit tests**, a 15-game
  device-independence quality gate, production build, and a Playwright engine matrix

### 🧾 FişAktar — AI Document-Processing SaaS
Turkish SaaS that reads receipts and invoices arriving via WhatsApp and web, and exports
balanced journal entries in the formats **Luca** and **Zirve** accept.

- **Gemini Vision** extracts date, vendor, tax number, and 1% / 10% / 20% VAT breakdowns from
  crumpled, angled, or low-light photos
- Multi-model fallback so quota limits never fail a user's request
- Turns a ~1-minute manual per-receipt process into ~2 seconds

### 🔐 VaultNote — Zero-Server, End-to-End Encrypted Notes
Cross-device, local-first notes app where data lives in your own Google Drive `appDataFolder`
and **only ciphertext ever leaves the device**.

- WebCrypto **AES-256-GCM + HKDF** with **Argon2id** hashing
- Offline-first IndexedDB core, syncing via the Drive REST v3 `drive.appdata` scope
- Verified with **66 unit tests + 17 end-to-end flows**

### 🎮 Gods of Rift — Deterministic Turn-Based Strategy RPG
Hybrid web/mobile RPG on a **headless-core + thin-client** architecture in a Bun monorepo.

- All game logic lives in a dependency-free pure-TypeScript core — **same seed always yields
  the same battle result**
- Custom PixiJS battle engine replaying one simulation as a skippable, timed animation

### 📖 [Rahmet Eli](https://play.google.com/store/apps/details?id=com.rahmeteli.app) — Published Cross-Platform App
Islamic companion app live on **Google Play** and the **App Store**: prayer times, sensor-fusion
Qibla, Quran reader, and content feeds (Expo + Firebase Cloud Functions).

---

## 💼 Background

- **Huawei R&D Center (Alumni)** — built enterprise data visualization tooling processing
  **50,000+ rows** with Node.js / MongoDB; integrated Huawei Mobile Services kits into
  production Android apps
- **Certifications** — Huawei Cloud **HCCDP (Solution Architecture)** and **HCCDA (Cloud Native)**, 2025
- **🥉 3rd Place, Huawei Coding Marathon 2022** — nationwide mobile-services category
- Also shipped: KpssArena, ATA Akademi, KubectlCommandTool (GKE + Docker + CI/CD),
  TraceX, EdgeBar, Exam Timer, Cloud Path

---

## ✍️ Writing

Technical author on the **Huawei Developers Medium Blog** —
*Kotlin: Higher-Order Functions and Lambda Expressions*.

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-kemaladlig-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/kemaladlig)
[![GitHub](https://img.shields.io/badge/GitHub-kemaladlig-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/kemaladlig)
[![Email](https://img.shields.io/badge/Email-kemaladligdev@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:kemaladligdev@gmail.com)

> *Architect the intent, review the output, ship the product.*

# Hey, I'm Cory Pierson

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=D93A4C&vCenter=true&width=460&lines=Cybersecurity+%40+Northeastern;Building+RateMyHusky;Applied+crypto+%2B+web+security)](https://github.com/Cory585)
 
Cybersecurity @ Northeastern University (2029) | New York -> Massachusetts
 
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?logo=linkedin&logoColor=white&style=flat-square)](https://www.linkedin.com/in/cory-pierson-15925a384/)
[![Email](https://img.shields.io/badge/-Email-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:pierson.c@northeastern.edu)

---

## Public Projects

### <img src="assets/ratemyhusky.png" alt="" height="32" align="center"> RateMyHusky

[GitHub](https://github.com/RateMyHusky/RateMyHusky) · [ratemyhusky.com](https://ratemyhusky.com)

**Oasis @ Northeastern · Team project**

A professor and course discovery site for Northeastern students, with pages for about 9,300 professors. Each professor gets one profile that combines RateMyProfessors ratings, Reddit discussion, Northeastern's course schedule (every term since Fall 2021), the course catalog, and teaching awards. Search, filtering, and side-by-side comparison sit on top. React 19 + TypeScript on Vercel, Flask on Railway, PostgreSQL 16 + pgvector on an Oracle Cloud VM. AGPL-3.0.

![React](https://img.shields.io/badge/React_19-61DAFB?logo=react&logoColor=black&style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white&style=flat-square)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white&style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-4169E1?logo=postgresql&logoColor=white&style=flat-square)
![Google OAuth](https://img.shields.io/badge/Google_OAuth_2.0-4285F4?logo=google&logoColor=white&style=flat-square)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white&style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white&style=flat-square)

<details>
<summary><b>Architecture</b></summary>

```mermaid
flowchart LR
  U[Browser] --> V[Vercel<br/>React 19 + edge middleware]
  V -->|crawlers| P[Prerendered HTML<br/>JSON-LD]
  V -->|/api| F[Flask on Railway<br/>rate-limited, compressed]
  P -.->|snapshot via SSRF guard| F
  F --> DB[(PostgreSQL 16 + pgvector<br/>Oracle Cloud VM)]
  GA[GitHub Actions<br/>scheduled] -->|scrapers + precompute| DB
  S[RateMyProfessors · Reddit<br/>NUBanner · catalog] --> GA
```

</details>

<details>
<summary><b>What I built</b></summary>

- *Proxy & session security*: Resolved the real client IP behind the proxy, compared the proxy key in constant time, fixed login CSRF, and shortened session tokens
- *Browser & input hardening*: Added a report-only Content-Security-Policy with a violation-report endpoint, validated paging and search input, and rendered only http(s) links from scraped data
- *Abuse prevention & privacy*: Put CAPTCHA and per-IP limits on the feedback and rating forms, and set a 30-day retention limit on AI query logs
- *Accounts & auth*: Built bookmarks end to end: a backend module, Flask routes, a React context with optimistic updates, and a bookmarks page. Fixed Google sign-in so it only redirects to paths on the site, stays in sync across open tabs, and completes when started in two tabs
- *Compare*: Reworked the side-by-side compare table, adding per-metric best and second-best picks, tie handling, rating-count bars, and clear marking for professors with too few ratings to rank

</details>

<details>
<summary><b>The platform</b></summary>

- *Data pipeline*: Custom Python scrapers for RateMyProfessors, Reddit, the NUBanner course schedule, and the course catalog. They load 43K+ ratings and about 9K Reddit mentions into one PostgreSQL schema, which `precompute` jobs rebuild on a schedule via GitHub Actions
- *Entity resolution*: A layered matcher (calibration, surname stoplists, thread anchoring) keeps false matches out of the Reddit mentions it links to professors, and each mention gets a sentiment score. Automatic face focal-point detection crops about 2,000 professor photos correctly
- *Product*: Professor, course, and department pages, autocomplete search, side-by-side compare, a top-rated leaderboard, rating-history, radar and grade-distribution charts, dark mode, and a moderated student rating form
- *AI search (paused)*: Hybrid retrieval that fuses full-text search with BGE-small embeddings using Reciprocal Rank Fusion, with prompt-injection guards, plus an offline evaluation harness (nDCG@k, recall@k, MRR) built on human-labeled relevance judgments
- *SEO*: Flask-rendered snapshots for crawlers with JSON-LD, edge middleware, behind an SSRF guard, that routes bots to prerendered HTML, a sitemap generated at build time, `llms.txt`, and Bing IndexNow
- *Delivery*: A rate-limited, compressed API and GitHub Actions CI (build, lint, pytest, and a gitleaks secret scan of the full history)

</details>

---

### <picture><source media="(prefers-color-scheme: dark)" srcset="assets/momentum-light.png"><img src="assets/momentum-dark.png" alt="Momentum" height="26"></picture>

[GitHub](https://github.com/Cory585/babson26)

**Babson 2026 Hackathon (Semifinalist)**

AI-powered weightlifting form analysis built in 8 hours. Upload a lift video and get biomechanically validated coaching feedback compared against professional references.

![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white&style=flat-square)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black&style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&style=flat-square)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white&style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white&style=flat-square)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white&style=flat-square)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?logo=googlegemini&logoColor=white&style=flat-square)

<details>
<summary><b>Architecture</b></summary>

**System**

```mermaid
flowchart LR
  U[Browser] --> N[Next.js 16<br/>React 19 + Tailwind]
  N -->|POST /api/analyze<br/>video + lift type| F[FastAPI]
  F --> ML[MediaPipe + OpenCV<br/>pose, phases, scoring]
  F --> AG[Agent pipeline]
  AG <--> G[Google Gemini]
  ML --> D[(Local storage<br/>references + results)]
  AG --> D
  N -->|GET results<br/>+ annotated videos| F
```

**Analysis pipeline**

```mermaid
flowchart LR
  V[Lift video] --> P[MediaPipe pose<br/>33 landmarks/frame]
  P --> PH[Phase detection<br/>setup → lockout]
  PH --> S[Score vs. all<br/>pro references<br/>0–100 per phase]
  S --> C[Coaching generator<br/>Gemini drafts cards]
  C --> HV{Validator<br/>checks claims vs.<br/>angle deltas}
  HV -->|supported| RF[Reference finder<br/>pro clip timestamp]
  HV -->|partial: rewritten| RF
  HV -->|unsupported: flagged| RF
  RF --> R[Results<br/>synced replay +<br/>skeleton overlay]
  S --> R
```

</details>

<details>
<summary><b>How it works</b></summary>

- *MediaPipe*: Extracts pose keypoints frame by frame and detects lift phases (setup → descent → bottom → lockout)
- *Scoring*: Weighted joint angles (knee, hip, back, ankle) produce a 0–100 similarity score across phases
- *Three-agent pipeline*: Gemini generates coaching cards, a hallucination validator fact-checks every claim against raw angle data, and a reference finder links each issue to the exact timestamp in the pro footage
- *UI*: Side-by-side synced video player with skeleton overlay and per-phase score breakdown

</details>

---

### <img src="assets/password-manager.svg" alt="" height="32" align="center"> Password Manager

[GitHub](https://github.com/Cory585/Password-Manager-Project)

A command-line password manager that keeps credentials in a local, encrypted SQLite vault, unlocked by a single master password.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white&style=flat-square)
![AES-256-GCM](https://img.shields.io/badge/AES--256--GCM-555555?style=flat-square)
![Argon2id](https://img.shields.io/badge/Argon2id-555555?style=flat-square)

<details>
<summary><b>Details</b></summary>

- *Master password*: Hashed with Argon2id; the plaintext is never written to disk
- *Per-entry keys*: Each entry has its own random 16-byte salt, and PBKDF2-HMAC-SHA256 (480,000 iterations) derives a separate 32-byte key for it, so no two entries share a key
- *Encryption*: AES-256-GCM with a fresh 12-byte nonce on every write. The authentication tag catches tampering on decrypt
- *CLI*: `init`, `add`, `get`, `list`, `delete`, and a secure random password generator

</details>

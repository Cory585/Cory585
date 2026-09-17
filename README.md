# Hey, I'm Cory Pierson

Cybersecurity @ Northeastern University (2029) | New York

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?logo=linkedin&logoColor=white&style=flat-square)](https://www.linkedin.com/in/cory-pierson-15925a384/)
[![Email](https://img.shields.io/badge/-Email-EA4335?logo=gmail&logoColor=white&style=flat-square)](mailto:pierson.c@northeastern.edu)

----

## Public Projects

${\color{lightblue}\textbf{\huge Momentum}}$

[GitHub](https://github.com/Cory585/babson26)

**Babson 2026 Hackathon (Semi-Finalist)**

AI-powered weightlifting form analysis built in 8 hours; Upload a lift video, get biomechanically-validated coaching feedback compared against professional references.

- *MediaPipe* extracts pose keypoints frame-by-frame and detects lift phases (setup → descent → bottom → lockout)
- Weighted joint-angle scoring (knee, hip, back, ankle) produces a 0–100 similarity score across phases
- Three-agent pipeline: Gemini generates coaching cards, a hallucination validator fact-checks every claim against raw angle data, and a reference finder links each issue to the exact timestamp in pro footage
- Side-by-side synced video player with skeleton overlay and per-phase score breakdown

![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?logo=googlegemini&logoColor=white)

---

${\color{lightblue}\textbf{\huge RateMyHusky}}$

[GitHub](https://github.com/Cory585/RateMyHusky) · [ratemyhusky.com](https://ratemyhusky.com)

**Oasis @ Northeastern**

Professor discovery platform for Northeastern 
students, covering 9,300+ professors. Aggregates RateMyProfessors
ratings, and Reddit discussion into a single profile per professor, then layers search,
filtering, and side-by-side comparison on top. React 19 + TypeScript on Vercel, Flask on
Railway, CockroachDB Serverless. AGPL-3.0.

- *Data pipeline*: Three custom Python scrapers (a resumable term-by-term Bluera
  crawler with parallel report downloads, plus RMP and Reddit) 43K+ ratings, and ~9K Reddit mentions into a unified CockroachDB schema
- *Entity resolution*: Layered professor-mention matcher using calibration, surname
  stoplists, and thread anchoring to suppress Reddit false positives; per-mention sentiment
  scoring; automated facial focal-point detection so 3,700+ scraped photos crop correctly
- *Product surface*: Professor, course, and department hubs; autocomplete search with
  shuffle-based discovery; side-by-side compare with per-metric breakdowns; top-rated
  leaderboard; rating-history, radar, and grade-distribution charts; dark mode
- *SEO / AEO engineering*: Flask-rendered crawler snapshots carrying
  WebSite/ItemList/ProfilePage/Course JSON-LD, prebuild sitemap generation, edge middleware
  that routes bots to prerendered HTML behind an SSRF guard, `llms.txt`, and Bing IndexNow
  push indexing
- *Retrieval evaluation*: Offline harness scoring the retrieval layer against
  human-labeled relevance judgments (nDCG@k, recall@k, MRR, precision@k) with a local
  labeling UI, a curated question set, and run-over-run comparison
- *Platform & delivery*: Google OAuth 2.0 + JWT accounts with bookmarks, rate-limited
  and compressed API, precomputed catalog aggregates, and GitHub Actions CI (build, lint,
  pytest, gitleaks full-history secret scan)

![React](https://img.shields.io/badge/React_19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router_7-CA4245?logo=reactrouter&logoColor=white)
![Recharts](https://img.shields.io/badge/Recharts-FF6384)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![CockroachDB](https://img.shields.io/badge/CockroachDB-6933FF?logo=cockroachlabs&logoColor=white)
![Google OAuth](https://img.shields.io/badge/Google_OAuth_2.0-4285F4?logo=google&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
<!--
**Cory585/Cory585** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

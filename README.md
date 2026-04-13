# Hey, I'm Cory Pierson

---

Cybersecurity @ Northeastern University (2029) | New York

---

## Public Projects

<img width="80" height="80" alt="logo" src="https://github.com/user-attachments/assets/afe83008-b1b7-4a34-b85f-8b11fa29f5fb" />

— Babson 2026 Hackathon

AI-powered weightlifting form analysis built in 8 hours; Upload a lift video, get biomechanically-validated coaching feedback compared against professional references.

- MediaPipe extracts pose keypoints frame-by-frame and detects lift phases (setup → descent → bottom → lockout)
- Weighted joint-angle scoring (knee, hip, back, ankle) produces a 0–100 similarity score across phases
- Three-agent pipeline: Gemini generates coaching cards, a hallucination validator fact-checks every claim against raw angle data, and a reference finder links each issue to the exact timestamp in pro footage
- Side-by-side synced video player with skeleton overlay and per-phase score breakdown

Stack: Next.js · React · TypeScript · TailwindCSS · FastAPI · MediaPipe · OpenCV · Google Gemini

---

**RateMyHusky**

— Oasis @ Northeastern

Comprehensive professor discovery platform for Northeastern students — search, filter, and compare professors using aggregated RateMyProfessors ratings and TRACE course evaluation data.

- Custom scrapers pull RMP ratings, TRACE scores, student comments, and professor photos into a unified CockroachDB database
- Side-by-side professor comparison with per-metric breakdowns to inform course selection decisions
- Smart search with autocomplete across professors and courses, plus shuffle-based discovery
- Google OAuth 2.0 authentication with rate-limited API and compressed responses for fast load times

Stack: React 19 · TypeScript · Vite · React Router 7 · Recharts · Flask · CockroachDB · Google OAuth · Vercel
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

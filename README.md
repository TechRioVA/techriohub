# TechRio Hub

A personal learning dashboard I built to track my own journey into automation and coding — part study tracker, part portfolio, part AI-assisted sandbox project.

<p align="center">
  <img src="./Screenshot_1%20TechRioVAHub.png" width="800" alt="TechRio Hub Preview">
</p>

## About this project

I'm an aspiring learner in automation and coding, and this was one of my first real dives into **vibe coding** — building something functional by describing what I want and iterating with the help of AI (Claude), rather than writing every line from deep prior expertise. TechRio Hub is the result: a full mini web app with user accounts, a personal progress tracker, and an embedded AI chat assistant, all running on a Google Apps Script backend with zero traditional server hosting.

This project also doubles as my own 90-day self-study roadmap for becoming a Tech VA (Virtual Assistant) specializing in automation — so the content inside it (market research, the roadmap itself) reflects research I did into what skills and tools are actually in demand for that path.

## What it does

- **Accounts & auth** — register, log in, forgot username/password recovery via email, all backed by a Google Sheet acting as a lightweight user database
- **90-Day Roadmap** — an interactive, checkbox-driven roadmap broken into 3 phases (Days 1–30, 31–60, 61–90) and 12 weekly blocks, with live progress bars and auto-saving to the backend
- **Profile page** — auto-generated stats (completion %, phase breakdown, recently completed tasks) computed from roadmap progress
- **Market Research page** — a data breakdown of tools and skills in demand for Tech VA roles, based on real job posting research (GoHighLevel, Make.com, Zapier, AI tools, etc.)
- **AI chat widget** — a floating assistant (powered by Groq/Llama 3.3 through a proxy) that can answer questions about the roadmap and tools, available on every page
- **Fully responsive** — custom mobile nav, adaptive layouts, no external UI framework

## Tech stack

- **Frontend:** Vanilla HTML/CSS/JavaScript (single-page app style, no framework)
- **Backend:** Google Apps Script (`doGet`/`doPost` router)
- **Database:** Google Sheets (`Users` and `Progress` sheets, managed via `setupSheets()`)
- **Auth:** SHA-256 client-side password hashing (Web Crypto API) before ever hitting the backend
- **Email:** Google's `MailApp` for password reset links
- **AI Chat:** JSONP call to a Groq-backed Apps Script proxy

## Why I built it this way

Using Google Apps Script + Sheets as a backend was a deliberate choice for a beginner project — no server costs, no database setup, and it let me focus on learning the actual logic (auth flows, session handling, CRUD operations, API routing) without getting stuck on infrastructure. It's not how I'd build a production app at scale, but it was a great way to learn the fundamentals end-to-end.

## Status & learning notes

This is a personal, in-progress learning project — not a polished commercial product. Expect rough edges. I'm sharing it publicly mainly to document my learning process and to have something tangible to show as I keep building.

⚠️ **Note on the code as published:** the Apps Script Web App URLs in this repo point to my live deployment. If you clone this, you'll need to deploy your own Apps Script backend (see `Code.gs`) and swap in your own URLs at the top of the `<script>` section in the HTML.

## Author

Built by **Rio (TechRioVA)** — learning automation, coding, and AI-assisted ("vibe coding") development, one project at a time.

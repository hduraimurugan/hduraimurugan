<!-- ============================== HEADER ============================== -->
<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=230&color=0:A960FF,100:38B2AC&text=Duraimurugan%20H&fontColor=FFFFFF&fontSize=52&fontAlignY=38&desc=Full%20Stack%20%C2%B7%20AI-Powered%20Systems%20%C2%B7%20Mobile&descAlignY=58&descSize=20&animation=fadeIn" alt="Duraimurugan H" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=A960FF&center=true&vCenter=true&width=720&lines=Full+Stack+Developer+%7C+MERN+%2B+React+Native;Building+AI-native+tools+with+MCP+%26+LLMs;Instrumentation+Engineer+turned+Ex-Banker+turned+Dev;Open-sourcing+ChessReview+%E2%99%9F%EF%B8%8F+soon" alt="Typing animation" />
</a>

</div>

---

## 👋 About Me

I'm a full stack developer who moved from **banking** into software, with a background in **Instrumentation Engineering**. That shows in how I build: measure first, instrument everything, and make systems that fail safely.

Today I ship end-to-end products across **web, mobile, backend and AI tooling**, from a payments-grade booking platform to an MCP server that lets AI assistants query it.

| | |
|:--|:--|
| 🔭 **Now building** | **ChessReview** — an engine-powered chess game review app (going open source) · **FD/RD Manager** — an offline-first Android app (pre-release) |
| 🤖 **Exploring** | Model Context Protocol (MCP), agentic workflows with Claude Code, local LLMs with Ollama, ComfyUI |
| ⚡ **Strengths** | MERN · TypeScript · React Native · PostgreSQL · RBAC · payments · background jobs · automated reporting |
| 🎯 **Goal** | High-performance systems that solve real-world problems, with AI as a first-class interface |

---

## 🚀 Featured Projects

### ♟️ ChessReview &nbsp;![Status](https://img.shields.io/badge/status-in%20development-F59E0B?style=flat-square) ![License](https://img.shields.io/badge/license-AGPL--3.0-blue?style=flat-square) ![Open Source](https://img.shields.io/badge/open--sourcing-soon-A960FF?style=flat-square)

> Import your games, run **Stockfish** analysis through a background worker queue, and browse a move-by-move review.

- ⚙️ **Architecture:** Express API + **BullMQ** worker pool + Postgres + Redis, fully containerised with Docker Compose
- 🧠 **Engine:** Stockfish 19, run server-side in workers and in the browser (WASM build) for instant client-side analysis
- 🎨 **Frontend:** React 19, Tailwind CSS 4, shadcn/ui, with Lichess piece sets, board themes and opening (ECO) data
- 🔐 **Backend hardening:** JWT auth, Helmet, Redis-backed rate limiting, Zod validation, structured Pino logging
- 🌍 **Plan:** release under **AGPL-3.0**. The repo is currently private while I get it ready for open source.

`React 19` `Tailwind 4` `Node 20` `Express` `Prisma` `BullMQ` `Redis` `PostgreSQL` `Stockfish` `Docker`

<br/>

### 🎬 CineMax — Full Cinema Booking Platform

A complete, multi-surface product: **customer web app, admin panel, REST API, mobile app, and an AI/MCP server**, all sharing one backend.

```mermaid
flowchart LR
    U["🎟️ Customers<br/>Web (React) · Mobile (React Native)"] --> API
    A["⚙️ Admin Panel<br/>React + shadcn/ui"] --> API
    AI["🤖 AI Assistants<br/>Claude · Cursor · ChatGPT"] --> MCP["🔌 Cinemax MCP Server<br/>57 tools"]
    MCP -->|"per-user API keys + RBAC"| API["🧩 cinema-hall-api<br/>Express 5"]
    MCP -->|"read-only role + RLS"| DB[("🐘 PostgreSQL")]
    API --> DB
    API --> PAY["💳 Razorpay"]
    API --> PUSH["🔔 Firebase Push"]
    API --> Q["⏱️ QStash / Cron"]
```

| Component | What it is | Highlights | Links |
|:--|:--|:--|:--|
| 📱 **CineMax Mobile** | React Native (New Architecture) booking app, Android + iOS | End-to-end flow to a **QR ticket**, Razorpay in WebView, dark/light theme, pinch-zoom seat map, Google Sign-In, mock-first dev | [Repo](https://github.com/hduraimurugan/ciemax-app) |
| 🌐 **Customer Web App** | React 19 + Vite + Tailwind 4 | Location-aware showtimes, live seat grid, **5-min server-side seat hold** with countdown, coupons, QR/PNG tickets, refund tracking | [Repo](https://github.com/hduraimurugan/cinema-hall-users) |
| 🛠️ **Admin Panel** | React 19 + shadcn/ui + Recharts + Leaflet | Multi-hall workspace, **drag-and-design seat layout canvas**, bulk show scheduler, camera **QR ticket validator**, RBAC, notifications, API keys | [Repo](https://github.com/hduraimurugan/cinema-hall-admin) |
| 🧩 **Backend API** | Express 5 + PostgreSQL | Razorpay verification + atomic webhooks + refunds, idempotency, seat-hold TTL release, Sentry, **352 passing tests** (Vitest + Supertest) | [Repo](https://github.com/hduraimurugan/cinema-hall-api) |
| 🤖 **MCP Server** | Model Context Protocol (Node) | **57 tools** across 9 domains, per-person API keys that inherit real permissions, Postgres **Row-Level Security**, confirm-gated write tools, stdio + HTTP transports | 🔒 Private |
| 📚 **Docs** | Architecture & API docs | Endpoint reference, test inventory, flow diagrams | [Repo](https://github.com/hduraimurugan/cinema-app-docs) |

<details>
<summary><b>📸 CineMax mobile screenshots</b></summary>
<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/hduraimurugan/ciemax-app/main/screensnip/home.png" width="19%" alt="Home" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/ciemax-app/main/screensnip/movie_info.png" width="19%" alt="Movie details" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/ciemax-app/main/screensnip/seat_selection.png" width="19%" alt="Seat selection" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/ciemax-app/main/screensnip/checkout.png" width="19%" alt="Checkout" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/ciemax-app/main/screensnip/ticket.png" width="19%" alt="QR ticket" />
</p>
</details>

<details>
<summary><b>🖥️ Admin panel screenshots</b></summary>
<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/hduraimurugan/cinema-hall-admin/main/docs/screenshots/04-dashboard.png" width="48%" alt="Dashboard" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/cinema-hall-admin/main/docs/screenshots/09-shows-management.png" width="48%" alt="Shows management" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/cinema-hall-admin/main/docs/screenshots/23-settings-roles-permissions.png" width="48%" alt="Roles and permissions matrix" />
  <img src="https://raw.githubusercontent.com/hduraimurugan/cinema-hall-admin/main/docs/screenshots/25-settings-api-keys.png" width="48%" alt="API keys for MCP" />
</p>
</details>

<br/>

### 💰 FD/RD Manager &nbsp;![Status](https://img.shields.io/badge/status-pre--release-F59E0B?style=flat-square) ![Platform](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white) ![Offline](https://img.shields.io/badge/100%25-offline-success?style=flat-square)

> Track **Fixed Deposits & Recurring Deposits** with no backend, no ads, no account, and no `INTERNET` permission.

- 📊 Portfolio overview, payout & maturity timeline, and standalone FD/RD calculators
- 🔔 On-device maturity reminders (1/3/7/14 days before)
- 🔐 PIN + biometric app lock (PBKDF2-SHA256) and **AES-256-GCM encrypted backups**
- 🧮 "Derive, don't store" design: maturity values are always recomputed from the real current date
- 📦 **Releasing soon** as a signed open-source APK

`React Native 0.87` `TypeScript` `SQLite (op-sqlite)` `Notifee` `@noble/ciphers`

<details>
<summary><b>🗂️ Earlier work</b></summary>
<br/>

- **Military Assets Management System** — secure defense-inventory tracking with RBAC and a **cron-scheduled** daily audit/sync (React, Node, Express, MongoDB, Tailwind) · [Frontend](https://github.com/hduraimurugan/military-management-FE) · [Backend](https://github.com/hduraimurugan/military-BE)
- **College Placement Portal** — MERN platform with Redux-managed student and recruiter dashboards
- **X (Twitter) Clone** — social app using React Query for server-state management · [Repo](https://github.com/hduraimurugan/twitter-clone-app)

</details>

---

## 🛠️ Tech Stack

<div align="center">

**Frontend & Mobile**<br/>
<img src="https://skillicons.dev/icons?i=react,ts,js,vite,tailwind,redux,html,css&perline=8" alt="Frontend" />
<br/>
<img src="https://img.shields.io/badge/React%20Native-0.84%2B-61DAFB?style=flat-square&logo=react&logoColor=white" />
<img src="https://img.shields.io/badge/Zustand-State-433E38?style=flat-square" />
<img src="https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white" />
<img src="https://img.shields.io/badge/React%20Query-FF4154?style=flat-square&logo=reactquery&logoColor=white" />
<img src="https://img.shields.io/badge/Recharts-22B14C?style=flat-square" />

**Backend & Data**<br/>
<img src="https://skillicons.dev/icons?i=nodejs,express,python,postgres,mongodb,redis,prisma,mysql,supabase&perline=9" alt="Backend" />
<br/>
<img src="https://img.shields.io/badge/BullMQ-Queues-DC382D?style=flat-square&logo=redis&logoColor=white" />
<img src="https://img.shields.io/badge/Razorpay-Payments-002E6E?style=flat-square&logo=razorpay&logoColor=white" />
<img src="https://img.shields.io/badge/Sentry-Monitoring-362D59?style=flat-square&logo=sentry&logoColor=white" />
<img src="https://img.shields.io/badge/Firebase-Push-FFCA28?style=flat-square&logo=firebase&logoColor=black" />
<img src="https://img.shields.io/badge/Zod-Validation-3E67B1?style=flat-square&logo=zod&logoColor=white" />

**DevOps, Testing & Tools**<br/>
<img src="https://skillicons.dev/icons?i=docker,git,github,vercel,postman,vscode,androidstudio,figma&perline=8" alt="Tools" />
<br/>
<img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white" />
<img src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white" />
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" />
<img src="https://img.shields.io/badge/Neon-Serverless%20Postgres-00E599?style=flat-square" />

</div>

### 🤖 AI & Agentic Engineering

| Focus | What I work with |
|:--|:--|
| **Model Context Protocol** | Designing and shipping a production-style **MCP server** (57 tools, RBAC-aware, RLS-backed, stdio + HTTP) so AI assistants can safely query real business data |
| **AI-assisted development** | ![Claude](https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=anthropic&logoColor=white) agentic coding workflows, **Playwright MCP** for browser-driven verification, AI design prototypes turned into shipped UIs |
| **Local & open models** | ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) local LLM experiments · ![ComfyUI](https://img.shields.io/badge/ComfyUI-Image%20Gen-6C4CE0?style=flat-square) node-based image-generation pipelines |
| **AI-safe tool design** | Permission-gated tools, `confirm: true` write guards, read-only DB roles, per-user revocable API keys, and audit logging for agent actions |
| **Engine-driven analysis** | Stockfish (UCI engine) integration, in-browser WASM and server-side worker queues, in ChessReview |

---

## 📊 GitHub Analytics

<div align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=hduraimurugan&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&icon_color=A960FF&text_color=FFFFFF&include_all_commits=true&count_private=true" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=hduraimurugan&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&text_color=FFFFFF&langs_count=8" alt="Top languages" />
</div>

<p align="center">
  <img width="75%" src="https://streak-stats.demolab.com/?user=hduraimurugan&theme=tokyonight&hide_border=true&background=0D1117&stroke=A960FF&ring=A960FF&fire=FF6B6B&currStreakLabel=A960FF" alt="GitHub streak" />
</p>

<!-- Generated by .github/workflows/snake.yml and served from the `output` branch of this repo -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/hduraimurugan/hduraimurugan/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/hduraimurugan/hduraimurugan/output/github-snake.svg" />
    <img width="95%" alt="Contribution graph" src="https://raw.githubusercontent.com/hduraimurugan/hduraimurugan/output/github-snake-dark.svg" />
  </picture>
</p>

#### 📌 Public repositories

<div align="center">
  <a href="https://github.com/hduraimurugan/ciemax-app"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=hduraimurugan&repo=ciemax-app&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&icon_color=A960FF&text_color=FFFFFF" alt="ciemax-app" /></a>
  <a href="https://github.com/hduraimurugan/cinema-hall-api"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=hduraimurugan&repo=cinema-hall-api&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&icon_color=A960FF&text_color=FFFFFF" alt="cinema-hall-api" /></a>
  <a href="https://github.com/hduraimurugan/cinema-hall-users"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=hduraimurugan&repo=cinema-hall-users&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&icon_color=A960FF&text_color=FFFFFF" alt="cinema-hall-users" /></a>
  <a href="https://github.com/hduraimurugan/cinema-hall-admin"><img width="49%" src="https://github-readme-stats.vercel.app/api/pin/?username=hduraimurugan&repo=cinema-hall-admin&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=A960FF&icon_color=A960FF&text_color=FFFFFF" alt="cinema-hall-admin" /></a>
</div>

---

## 🗺️ Roadmap

- [x] CineMax platform: web, admin, API, mobile, MCP server
- [ ] 🚧 Ship **ChessReview** and open-source it under AGPL-3.0
- [ ] 📦 Release **FD/RD Manager** as a signed Android APK
- [ ] 🔌 Extend the Cinemax MCP server with `prepare_` / `confirm_` write workflows

---

## 🌐 Connect with Me

<p align="center">
  <a href="https://linkedin.com/in/duraimurugan16"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/hduraimurugan16"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>
  <a href="https://github.com/hduraimurugan?tab=repositories"><img src="https://img.shields.io/badge/All%20Repositories-181717?style=for-the-badge&logo=github&logoColor=white" alt="Repositories" /></a>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&height=110&color=0:38B2AC,100:A960FF&section=footer" alt="" />

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/AyedAlmudarra/AyedAlmudarra/main/assets/banner-dark.svg">
  <img alt="Ayed Almudarra — Software Engineer & Product Manager · Riyadh, Saudi Arabia" src="https://raw.githubusercontent.com/AyedAlmudarra/AyedAlmudarra/main/assets/banner-light.svg" width="100%">
</picture>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-ayedalmudarra-0A66C2?style=flat)](https://www.linkedin.com/in/ayedalmudarra/)
[![X](https://img.shields.io/badge/X-@liiitb-000000?style=flat&logo=x)](https://x.com/liiitb)
[![Email](https://img.shields.io/badge/Email-AyedAlmudarra%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:AyedAlmudarra@gmail.com)

</div>

## Selected work

### Investor Data Room → multi-tenant SaaS
Secure data rooms for fundraising — every view tracked, every document watermarked, every action audited. Shipped a self-hosted version to production in ~3 weeks, then evolved it into a multi-tenant SaaS.
- Six in-browser viewers (PDF, Excel, Word, PowerPoint, video, images) plus OnlyOffice full-fidelity mode; NDA e-sign gating, per-investor watermarks, anti-screenshot viewing
- Engagement analytics — session-replay timeline, page heatmaps, Hot/Warm/Cold scoring, email digests, CSV export — and real-time comments + online-viewer presence over SSE
- SaaS layer: subdomain-per-tenant and customer custom domains (Caddy on-demand TLS), Stripe subscriptions with plan limits, super-admin console, CI tests that prove cross-tenant isolation

<sub>Next.js 16 · React 19 · TypeScript · Prisma 7 · PostgreSQL · Redis · NextAuth · Stripe · Cloudflare R2 · Docker · Coolify · next-intl (AR/EN)</sub>

### LUBY — curated luxury-residence platform
Guest storefront, owner console and admin back-office for an editor-selected register of residences across Saudi Arabia — "a private register, not a listings platform".
- Availability core where double-booking is impossible at the database level (Postgres exclusion constraints), holds with expiry, iCal channel sync
- Money done properly: integer-halala model, pricing engine, local payment gateways behind one provider interface, idempotent webhooks, refunds, ZATCA e-invoice chain with QR
- Phone-OTP auth with rotating RSA JWTs and reuse detection; 13 cron jobs on a shared harness; CI blocks merges on missing Arabic translations

<sub>Bun · Express 5 · Next.js 16 · React 19 · Prisma 7 · PostgreSQL 17 · Zod · Tailwind 4 · Jest · Playwright + axe · Docker · GitHub Actions</sub>

### Saqer — voice-first AI operator for my codebases
A personal system that drives Claude Code across many projects from an iPhone app and a web cockpit: delegates coding tasks, asks before anything destructive, reports back.
- Event-sourced session store with cross-restart resume; human-in-the-loop approvals enforced via hooks, per-project policies, budget caps and a full audit log
- Durable multi-turn task runs, inbox → auto-triage → PRD-writer → plan-approval queue, morning briefs by push notification
- Native SwiftUI iOS app at feature parity with desktop; ~156 integration tests; 21 ADRs and retros

<sub>TypeScript · Bun · Hono · Drizzle · PostgreSQL · Vite + React 19 · SwiftUI · Claude Code · MCP · Inngest · Tailscale</sub>

### [TerraShield](https://github.com/AyedAlmudarra/terra-shield) — smart-ground vibration security &nbsp;<sub>public</sub>
Defensethon 2026 (Saudi MoD / GADD) hackathon entry: ground vibration sensors → ML classification → context-aware threat scoring → TDOA source localization → bilingual operator dashboard. Full-simulation MVP, team of three.
- **95.8%** human-detection accuracy on the public FootprintID geophone dataset (99.9% on silence); sub-metre TDOA on a 100 × 100 m field; ~2 ms p50 end-to-end latency
- Closed a 3% → 95.8% real-data gap with a documented diagnose-and-recalibrate loop on the synthetic training generator

<sub>Python · Flask · scikit-learn · XGBoost · SciPy · React · Leaflet</sub>

### [RISE](https://github.com/AyedAlmudarra/rise) — startup–investor platform &nbsp;<sub>public · [live](https://rise-red.vercel.app)</sub>
Dual-role platform for the Saudi market: startups get an AI investment-readiness analysis; investors browse, shortlist and track deals.
- Fine-tuned GPT-3.5 model (300-example dataset) that returns structured SWOT, readiness score, KPIs and a 12-month growth plan — rendered as cards and exported to PDF
- Realtime dashboards, messaging, calendar, data rooms, four-language i18n (EN/AR/FR/ZH)

<sub>React · TypeScript · Supabase (Postgres, Realtime, Edge Functions) · OpenAI · Gemini · Vite · Tailwind</sub>

### Glint — career exploration for Saudi youth
Try a career before choosing it: interactive job simulations, an Arabic AI mentor ("Sanad"), and verifiable certificates. Two generations (2025 MVP → 2026 rebuild).
- Eight browser-based simulators — code editor, terminal with a virtual filesystem, spreadsheet with its own formula engine, document editor, product board, design canvas, data dashboard, email client — driven by pure-data task definitions and a validator engine
- Tool-calling AI mentor grounded in the platform's own content; canvas-rendered bilingual certificates with QR verification; admin analytics (DAU/WAU/MAU, funnel, cohorts)

<sub>React 19 · TypeScript · Vite · Supabase (RLS, PL/pgSQL, Edge Functions) · Cohere → OpenAI · CodeMirror 6 · i18next · Netlify</sub>

### GPS-denied UAV navigation &nbsp;<sub>R&D</sub>
ROS-free pipeline that keeps a drone localized without GNSS: optical-flow VIO + map-based visual place recognition fused in a factor graph, streamed to ArduPilot as vision position estimates. Built for PSAU's R&D Center across three iterations.
- Quaternion EKF over pose, velocity and IMU biases with chi-square-gated updates; forward–backward LK flow with RANSAC/MAD gating; SIFT + FLANN place recognition with temporal smoothing
- GTSAM sliding-window optimizer with robust losses, watchdogs and adaptive rates; ~20 FPS HUD in Gazebo + ArduPilot SITL; replay, metrics and self-check tooling

<sub>Python · OpenCV · NumPy · SciPy · GTSAM · pymavlink · GStreamer · Gazebo Harmonic · ArduPilot SITL</sub>

### Also
- **Venture-studio platform** — bilingual, RTL-first B2B platform (marketing site, admin, company portal, investor room) with defense-in-depth auth: route guards → ownership checks → Postgres RLS; spec- and ADR-driven rebuild. <sub>Next.js 16 · Supabase · next-intl · Vitest · Playwright</sub>
- **Team project tracker** — invite-only Kanban with tRPC + REST API keys, AI card generation, @mentions, R2 uploads, PWA; Docker on Coolify. <sub>Next.js 16 · tRPC 11 · Prisma 7 · Better Auth</sub>
- **Fintech wallet investor demo** — Arabic-first RTL simulation of a mobile wallet, built from a pixel-level spec in two days for an investor conference. <sub>Vite · React 19 · Zustand · Framer Motion</sub>

<sub>Unlinked projects live in private repositories — happy to walk through any of them.</sub>

## Background

- **How I work** — I run products end to end: discovery and PRD, roadmap and decision log, then the build, the tests and the deploy. Most of my repos carry their own PRD, roadmap and ADRs, and I ship with spec-driven, AI-assisted workflows — which is how a production data room went live in ~3 weeks and a full booking platform MVP in days.
- **Defaults I ship with** — Arabic/English with RTL from day one · security by design (RLS default-deny, RBAC, rate limiting, audited actions) · Saudi-market integrations (local payment gateways, ZATCA e-invoicing, SMS OTP) · Docker + CI on every project.
- **Before this** — product roadmap owner at Wetaan (+15% platform engagement) · Python/OpenCV reporting pipelines (~20% efficiency gain) · GPS-denied UAV navigation for PSAU's R&D Center · Defensethon 2026 and Gravity Hackathon 2023.
- **Community** — President, PSAU Cyber Security Club · Activities Committee Lead, PSAU Student Council.
- **Interests** — formal methods (Coloured Petri Nets) · autonomy and sensor fusion · agentic developer tooling.

## Stack

**Languages**&nbsp;&nbsp;
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)

**Frontend**&nbsp;&nbsp;
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=flat&logo=reactrouter&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn/ui-000000?style=flat&logo=shadcnui&logoColor=white)
![Radix UI](https://img.shields.io/badge/Radix_UI-161618?style=flat&logo=radixui&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat&logo=framer&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=flat&logo=tanstack&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-443E38?style=flat)
![React Hook Form](https://img.shields.io/badge/React_Hook_Form-EC5990?style=flat&logo=reacthookform&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat&logo=zod&logoColor=white)
![i18next](https://img.shields.io/badge/i18next-26A69A?style=flat&logo=i18next&logoColor=white)
![CodeMirror](https://img.shields.io/badge/CodeMirror-D30707?style=flat&logo=codemirror&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=flat&logo=leaflet&logoColor=white)

**Backend & data**&nbsp;&nbsp;
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat&logo=bun&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat&logo=hono&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=flat&logo=trpc&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat&logo=prisma&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle-C5F74F?style=flat&logo=drizzle&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![Deno](https://img.shields.io/badge/Deno-000000?style=flat&logo=deno&logoColor=white)
![NextAuth](https://img.shields.io/badge/NextAuth-000000?style=flat)
![Better Auth](https://img.shields.io/badge/Better_Auth-000000?style=flat&logo=betterauth&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=flat&logo=resend&logoColor=white)
![OnlyOffice](https://img.shields.io/badge/OnlyOffice-444444?style=flat&logo=onlyoffice&logoColor=white)

**AI / ML**&nbsp;&nbsp;
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat&logo=claude&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat&logo=modelcontextprotocol&logoColor=white)
![Cohere](https://img.shields.io/badge/Cohere-39594D?style=flat)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-1A6FB5?style=flat)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![GTSAM](https://img.shields.io/badge/GTSAM-2F4858?style=flat)

**Robotics & simulation**&nbsp;&nbsp;
![ArduPilot SITL](https://img.shields.io/badge/ArduPilot_SITL-1C3D5A?style=flat)
![Gazebo](https://img.shields.io/badge/Gazebo-F58113?style=flat)
![MAVLink](https://img.shields.io/badge/MAVLink-2B2B2B?style=flat)
![GStreamer](https://img.shields.io/badge/GStreamer-2E2E2E?style=flat&logo=gstreamer&logoColor=white)

**Infra & DevOps**&nbsp;&nbsp;
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Coolify](https://img.shields.io/badge/Coolify-6B16ED?style=flat&logo=coolify&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat&logo=cloudflare&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?style=flat&logo=caddy&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat&logo=sentry&logoColor=white)
![Inngest](https://img.shields.io/badge/Inngest-000000?style=flat)
![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat&logo=tailscale&logoColor=white)

**Testing & quality**&nbsp;&nbsp;
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat&logo=vitest&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat&logo=jest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat)
![Testing Library](https://img.shields.io/badge/Testing_Library-E33332?style=flat&logo=testinglibrary&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-69D3A7?style=flat&logo=cypress&logoColor=black)
![MSW](https://img.shields.io/badge/MSW-FF6A33?style=flat&logo=mockserviceworker&logoColor=white)
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat&logo=eslint&logoColor=white)
![Prettier](https://img.shields.io/badge/Prettier-F7B93E?style=flat&logo=prettier&logoColor=black)
![Biome](https://img.shields.io/badge/Biome-60A5FA?style=flat&logo=biome&logoColor=white)

**Mobile & tools**&nbsp;&nbsp;
![SwiftUI](https://img.shields.io/badge/SwiftUI-F05138?style=flat&logo=swift&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat&logo=pwa&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat&logo=cursor&logoColor=white)

## Activity

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=AyedAlmudarra&hide_border=true&theme=github-dark-blue">
  <img alt="GitHub streak" src="https://streak-stats.demolab.com/?user=AyedAlmudarra&hide_border=true&theme=default">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/AyedAlmudarra/AyedAlmudarra/output/github-snake-dark.svg">
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/AyedAlmudarra/AyedAlmudarra/output/github-snake.svg" width="100%">
</picture>

</div>

<div align="center">

Open to conversations about AI products, product strategy, computer vision, and collaboration — [email me](mailto:AyedAlmudarra@gmail.com).

</div>

<div align="center">

# Stijn Jakobs

**Software Engineer** — distributed systems, developer tooling, full-stack platforms.

[![Website](https://img.shields.io/badge/website-ordnary.com-0a0a0a?style=flat-square&logo=vercel&logoColor=white)](https://ordnary.com)
[![Org](https://img.shields.io/badge/building_at-@ordnary--com-1f6feb?style=flat-square&logo=github&logoColor=white)](https://github.com/ordnary-com)
[![Profile Views](https://komarev.com/ghpvc/?username=7txr&style=flat-square&color=blue&label=profile+views)](https://github.com/7txr)
[![Followers](https://img.shields.io/github/followers/7txr?style=flat-square&label=followers&color=blue)](https://github.com/7txr?tab=followers)

</div>

---

## About

I build production-grade tools and distributed systems across the stack — from low-level Java networking and event-driven backend architecture to TypeScript frontends and mobile applications. Strong interest in open source, performance engineering, and developer tooling.

Currently building at [**@ordnary-com**](https://github.com/ordnary-com).

---

## Featured Projects

### 🔗 [NetworkDataAPI](https://github.com/7txr/NetworkDataAPI)
> **Enterprise-grade shared MongoDB connection layer for distributed server networks** · `Java` · `MongoDB` · `Caffeine` · `REST`

A production-ready data synchronization solution architected for high-concurrency server networks. Instead of each plugin managing its own database connections — causing connection storms at scale — NetworkDataAPI exposes a **shared MongoDB connection pool** consumed by all plugins simultaneously, reducing total connections by 80%+ on a typical 5-server network.

**Architecture highlights:**
- Multi-module Maven project with isolated `core`, `paper`, `bungee`, and `example-plugin` modules — the core is platform-agnostic, platform modules provide thin adapter layers
- **Caffeine-backed in-memory cache** with configurable TTL and max-size, achieving 85–95% cache hit rates in production workloads
- Fully async API built on `CompletableFuture` thread pools (`core-pool-size` / `max-pool-size` configurable) — zero blocking on the main server thread
- Optional **REST API** (Spark Java) exposing `/api/player/{uuid}` CRUD endpoints, secured via `X-API-Key` header, for external service integrations
- CodeQL, Maven CI, and build/release pipelines via **GitHub Actions**
- Benchmarks: `<5ms` for cached reads, `<50ms` for live MongoDB queries, supports `1000+` concurrent operations

---

### ☁️ [cloud-controller](https://github.com/7txr/cloud-controller)
> **Event-driven infrastructure automation for containerized game server orchestration** · `Python` · `RabbitMQ` · `Redis` · `Pterodactyl API` · `Docker`

An automated lifecycle management system for dynamically scaling containerized server instances across Pterodactyl nodes. The controller subscribes to AMQP queues via `pika`, evaluates per-game-mode capacity policies every 30 seconds, and provisions or deprovisions Docker containers through the Pterodactyl REST API — without any manual intervention.

**Architecture highlights:**
- **Event-driven concurrency model**: main thread runs the capacity evaluation loop while a dedicated consumer thread processes RabbitMQ messages, communicating via `threading.Queue` — no shared mutable state, no locks
- **Redis as single source of truth**: all server state stored as persistent hash maps at `minecraft:servers:{type}:{id}`, enabling stateless controller restarts with zero data loss
- Per-game-mode capacity policies: configurable `min_servers`, `max_servers`, `empty_buffer_count`, `spawn_threshold_percent`, and `despawn_empty_after` — scaling algorithm runs in `<100ms` per evaluation cycle across 10 game modes
- Pterodactyl API integration for Docker container provisioning with `~40–90s` total time-to-accepting-connections per new instance
- RabbitMQ queues are durable, messages published with `delivery_mode=2` (persistent) and manual ACK — no message loss on broker restart

---

### 🌐 [front-end.weblance](https://github.com/7txr/front-end.weblance)
> **Next.js frontend for the Weblance platform** · `JavaScript` · `Next.js` · `React` · `SCSS` · `HTML`

The production frontend web application for Weblance, built on the Next.js App Router with a component-driven architecture. Implements `next/font` for automatic font optimization, context-based state management, and a clean separation between page routing (`/app`), reusable UI components (`/components`), and utility functions (`/utils`).

**Stack:** Next.js App Router · SCSS modules (44.9% of codebase) · JavaScript · Static export via `next export` · Yarn workspaces

---

### 📦 [com.ordnary.accounts](https://github.com/7txr/com.ordnary.accounts) · [com.ordnary.developers](https://github.com/7txr/com.ordnary.developers)
> **Core platform services for the Ordnary ecosystem** · `Laravel`, `Vite`, `TailwindCSS`, `Blade` · `@ordnary-com`

Backend services powering the Ordnary platform: `com.ordnary.accounts` handles authentication, identity management, and account lifecycle; `com.ordnary.developers` provides the developer portal, API key management, and tooling for third-party integrations within the Ordnary ecosystem.

---

### 🖼️ [YEETIFF](https://github.com/7txr/YEETIFF)
> **Custom image container format with transcoding pipeline** · `Python`, `Rust`

An experimental image file format specification and transcoding toolchain — *Yet Even Extremely Expressier Transcoded Image File Format*. Built to explore custom binary encoding, metadata schemas, and image pipeline design at a low level.

---

## Tech Stack

### Languages
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)
![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)
![Swift](https://img.shields.io/badge/swift-F54A2A?style=for-the-badge&logo=swift&logoColor=white)
![Lua](https://img.shields.io/badge/lua-%232C2D72.svg?style=for-the-badge&logo=lua&logoColor=white)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

### Frameworks & Libraries
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Webpack](https://img.shields.io/badge/webpack-%238DD6F9.svg?style=for-the-badge&logo=webpack&logoColor=black)
![FFmpeg](https://shields.io/badge/FFmpeg-%23171717.svg?logo=ffmpeg&style=for-the-badge&labelColor=171717&logoColor=5cb85c)

### Infrastructure & Tooling
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/rabbitmq-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)

### DevOps & Version Control
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

---

## GitHub Stats

<div align="center">

<a href="https://github.com/7txr">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=7txr&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&title_color=1f6feb&icon_color=1f6feb&text_color=c9d1d9&bg_color=0d1117" alt="GitHub Stats" />
  <img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=7txr&hide_border=true&background=0d1117&stroke=1f6feb&ring=1f6feb&fire=ff6b35&currStreakLabel=1f6feb&sideLabels=c9d1d9&currStreakNum=c9d1d9&sideNums=c9d1d9&dates=8b949e" alt="GitHub Streak" />
</a>

<br/>

<img width="55%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=7txr&layout=compact&hide_border=true&langs_count=10&title_color=1f6feb&text_color=c9d1d9&bg_color=0d1117" alt="Top Languages" />

<br/><br/>

<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=7txr&bg_color=0d1117&color=c9d1d9&line=1f6feb&point=ff6b35&area=true&hide_border=true" alt="Activity Graph" />

<br/>

<img width="95%" src="https://github-profile-trophy.vercel.app/?username=7txr&theme=onedark&no-frame=true&no-bg=true&margin-w=8&column=7" alt="GitHub Trophies" />

</div>

---

## Get Involved

Open source thrives on collaboration. Feedback, bug reports, and pull requests are always welcome.

- 📂 [Browse my repositories](https://github.com/7txr?tab=repositories)
- ⭐ [See what I'm starring](https://github.com/7txr?tab=stars)
- 🏢 [Check out Ordnary](https://github.com/ordnary-com)

---

<div align="center">

<sub>Built with care · <a href="https://github.com/7txr">@7txr</a></sub>

</div>

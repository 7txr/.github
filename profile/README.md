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
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white)
![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)
![Swift](https://img.shields.io/badge/swift-F54A2A?style=for-the-badge&logo=swift&logoColor=white)
![Ruby](https://img.shields.io/badge/ruby-%23CC342D.svg?style=for-the-badge&logo=ruby&logoColor=white)
![Lua](https://img.shields.io/badge/lua-%232C2D72.svg?style=for-the-badge&logo=lua&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![PowerShell](https://img.shields.io/badge/powershell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![GraphQL](https://img.shields.io/badge/graphql-%23E10098.svg?style=for-the-badge&logo=graphql&logoColor=white)
![SQL](https://img.shields.io/badge/sql-%2300758F.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![Sass](https://img.shields.io/badge/sass-%23CC6699.svg?style=for-the-badge&logo=sass&logoColor=white)
![YAML](https://img.shields.io/badge/yaml-%23CB171E.svg?style=for-the-badge&logo=yaml&logoColor=white)

### Frameworks & Libraries
![Next.js](https://img.shields.io/badge/next.js-%23000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vue.js](https://img.shields.io/badge/vue.js-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white)
![Astro](https://img.shields.io/badge/astro-%232C2052.svg?style=for-the-badge&logo=astro&logoColor=white)
![Expo](https://img.shields.io/badge/expo-1B1F23?style=for-the-badge&logo=expo&logoColor=white)
![Node.js](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Laravel](https://img.shields.io/badge/laravel-%23FF2D20.svg?style=for-the-badge&logo=laravel&logoColor=white)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![FastAPI](https://img.shields.io/badge/fastapi-%23009688.svg?style=for-the-badge&logo=fastapi&logoColor=white)
![Prisma](https://img.shields.io/badge/prisma-%232D3748.svg?style=for-the-badge&logo=prisma&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-%232596BE.svg?style=for-the-badge&logo=trpc&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Webpack](https://img.shields.io/badge/webpack-%238DD6F9.svg?style=for-the-badge&logo=webpack&logoColor=black)
![FFmpeg](https://shields.io/badge/FFmpeg-%23171717.svg?logo=ffmpeg&style=for-the-badge&labelColor=171717&logoColor=5cb85c)

### Databases & Storage
![PostgreSQL](https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/mongodb-%2347A248.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Supabase](https://img.shields.io/badge/supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase&logoColor=white)

### Infrastructure & Cloud
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Cloudflare](https://img.shields.io/badge/cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/rabbitmq-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)

### DevOps & Tooling
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/linux-%23FCC624.svg?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/bash-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Maven](https://img.shields.io/badge/maven-%23C71A36.svg?style=for-the-badge&logo=apachemaven&logoColor=white)
![Gradle](https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)
![pnpm](https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220)
![Postman](https://img.shields.io/badge/postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)

---

## Activity

<div align="center">

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

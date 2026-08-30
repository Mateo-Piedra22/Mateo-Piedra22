<div align="center">

  <!-- Header Animated Wave Banner -->
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=10,14,20&height=240&section=header&text=Mateo%20Piedrabuena&fontSize=54&fontAlignY=36&animation=fadeIn&desc=Computer%20Engineering%20%40%20UNL%20%7C%20Creator%20of%20ArgenPOS%20%26%20ClineMarket&descFontSize=20&descAlignY=62&fontColor=c7ff69" width="100%" alt="Mateo Piedrabuena Header" />

  <!-- Dynamic Typing Subtitle -->
  <p align="center">
    <a href="https://github.com/Mateo-Piedra22">
      <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=21&duration=2600&pause=900&color=C7FF69&background=14141400&center=true&vCenter=true&multiline=false&width=750&lines=Creator+%26+Lead+Architect+of+ArgenPOS+%F0%9F%8F%B7%EF%B8%8F;Computer+Engineering+Student+%40+UNL+%F0%9F%87%A6%F0%9F%87%B7;Full-Stack+%26+Low-Level+Systems+Engineer;Creator+of+ClineMarket+%26+Discord+Archive+Pro;Founder+%26+Tech+Lead+%40+MotionA+Studio" alt="Typing SVG" />
    </a>
  </p>

  <!-- Metric Badges & Status -->
  <p align="center">
    <a href="https://github.com/Mateo-Piedra22"><img src="https://img.shields.io/badge/Location-Santa%20Fe%2C%20Argentina-141414?style=for-the-badge&logo=googlemaps&logoColor=c7ff69&labelColor=1a1a1a" alt="Location" /></a>
    <a href="https://motiona.xyz"><img src="https://img.shields.io/badge/Studio-MotionA-141414?style=for-the-badge&logo=safari&logoColor=7a78ff&labelColor=1a1a1a" alt="MotionA" /></a>
    <a href="mailto:piedrabuena.mateo03@gmail.com"><img src="https://img.shields.io/badge/Email-Contact%20Me-141414?style=for-the-badge&logo=gmail&logoColor=ff6d38&labelColor=1a1a1a" alt="Email" /></a>
    <img src="https://komarev.com/ghpvc/?username=Mateo-Piedra22&label=Profile%20Views&color=c7ff69&style=for-the-badge" alt="Profile Views" />
  </p>

  <!-- GitHub Profile Trophies -->
  <p align="center">
    <img src="https://github-profile-trophy.vercel.app/?username=Mateo-Piedra22&theme=radical&no-frame=true&no-bg=true&margin_w=10&margin_h=10" alt="GitHub Trophies" />
  </p>

</div>

---

## ⚡ Executive Summary & Engineering Focus

I am a **Computer Engineering student** at the *National University of the Littoral (UNL)* in Santa Fe, Argentina, and a **Systems & Full-Stack Architect** with a deep passion for building high-performance, offline-resilient desktop/web software, hardware communication layers, developer tools, and local-first control planes.

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│  🎓 Computer Engineering @ Universidad Nacional del Litoral (UNL), Argentina          │
│  👑 Flagship Systems: ArgenPOS (Enterprise POS & Hardware Bridge) · Cline Marketplace  │
│  💼 Founder & Lead Developer: MotionA Studio (https://motiona.xyz)                     │
│  ⚙️ Core Focus: Systems Programming, Native Hardware Interfacing, Distributed Web, AI  │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

- 🏛️ **Academic Base**: Advanced Computer Engineering curriculum at UNL (computer architecture, operating systems, data structures, concurrency, low-level protocols).
- 🏷️ **Flagship Project**: [**ArgenPOS**](https://github.com/Mateo-Piedra22/ArgenPOS) & [**ArgenPOS Bridge**](https://github.com/Mateo-Piedra22/argenpos-bridge-releases) — high-reliability commercial Point of Sale platform and Windows native hardware bridge.
- ⚡ **Developer Infrastructure**: [**Cline Marketplace**](https://github.com/Mateo-Piedra22/ClineMarket) — local-first browser and execution control plane for Cline primitives.
- 💡 **Architectural Philosophy**: **Local-first sovereignty**, sub-millisecond I/O pipelines, defensive input boundaries, zero-dependency binary distribution, and crafted UI design systems.

---

## 👑 Flagship Engineering Projects

<br />

### 🏷️ 1. [ArgenPOS & ArgenPOS Bridge](https://github.com/Mateo-Piedra22/argenpos-bridge-releases) — *Enterprise Point of Sale & Native Hardware Bridge*

> **ArgenPOS** is a comprehensive, modern retail management and commercial POS platform engineered for maximum uptime, high-speed transaction checkout, and seamless hardware peripheral control.

```
┌───────────────────────────┐         WebSocket Protocol         ┌───────────────────────────────────────┐
│     ArgenPOS Web POS      │ ─────────────────────────────────► │      ArgenPOS Native Bridge           │
│   (Touchscreen Checkout)  │ ◄───────────────────────────────── │    (Windows Background Service .exe)  │
└───────────────────────────┘        Local Auth Token Handshake   └───────────────────┬───────────────────┘
                                                                                      │
                           ┌──────────────────────────┬───────────────────────────────┴───────────────────────────┐
                           ▼                          ▼                               ▼                           ▼
                 ┌───────────────────┐      ┌───────────────────┐           ┌───────────────────┐       ┌───────────────────┐
                 │  Thermal Printer  │      │    Cash Drawer    │           │  Customer Display │       │   Barcode / Scale │
                 │ (ESC/POS via COM) │      │  (Kick Pulse Pin) │           │    (VFD Pole COM) │       │   (Serial RS-232) │
                 └───────────────────┘      └───────────────────┘           └───────────────────┘       └───────────────────┘
```

- **Native Hardware Bridge**: Self-contained Windows background service daemon (`.exe`) that connects modern web apps with physical retail hardware via loopback WebSocket (`ws://127.0.0.1:9876`).
- **Direct ESC/POS & Serial Engine**: Raw bit-level serial and COM port communication with thermal receipt printers, electronic scales, and customer-facing pole displays.
- **Offline Cashier Resiliency**: Local transactional queueing with automatic sync reconciliation to ensure non-stop sales operations during internet outages.
- **Enterprise Security**: Token-based inter-process authentication, zero external open network ports, and localized audit logging.

<p align="left">
  <img src="https://img.shields.io/badge/Architecture-Distributed%20Local--First-c7ff69?style=flat-square&labelColor=141414" alt="Arch" />
  <img src="https://img.shields.io/badge/Hardware-ESC%2FPOS%20%7C%20COM%20Serial%20%7C%20VFD-7a78ff?style=flat-square&labelColor=141414" alt="Hardware" />
  <img src="https://img.shields.io/badge/Release-Windows%20Service%20.exe-ff6d38?style=flat-square&labelColor=141414" alt="Release" />
</p>

---

### ⚡ 2. [Cline Marketplace](https://github.com/Mateo-Piedra22/ClineMarket) — *Local Control Plane for Cline Ecosystem*

> Developer-grade, offline-first local browser, management control plane, and CLI runner for Cline plugins, skills, and Model Context Protocol (MCP) servers.

- **Offline-First Registry**: Caches and indexes 250+ community primitives with live upstream GitHub synchronization.
- **Filesystem Reconciler & Drift Detection**: Probes active VS Code, Claude, and Cline storage directories to detect live vs ghost installations.
- **Context-Aware Heuristics**: Analyzes active project codebases (Node, Python, Rust, Go, Git remotes) to suggest tailored toolchain bundles.
- **Automated CI/CD**: Matrix testing across Linux, Windows, and macOS, CodeQL SAST scanning, and pre-push verification pipelines.

<p align="left">
  <img src="https://img.shields.io/badge/Ecosystem-Cline%20%7C%20MCP%20%7C%20Agents-c7ff69?style=flat-square&labelColor=141414" alt="Ecosystem" />
  <img src="https://img.shields.io/badge/Stack-Node.js%20%7C%20Express%20%7C%20ESM-7a78ff?style=flat-square&labelColor=141414" alt="Stack" />
  <img src="https://img.shields.io/badge/UI%20Design-Dark%20Chalkboard%20Poster-00a652?style=flat-square&labelColor=141414" alt="UI" />
</p>

---

### 📦 3. [Discord Archive Pro](https://github.com/Mateo-Piedra22/Discord-Archive-Pro) & [IronTrain](https://github.com/Mateo-Piedra22/IronTrain)

<table>
  <tr>
    <td width="50%" valign="top">
      <h4 align="center"><a href="https://github.com/Mateo-Piedra22/Discord-Archive-Pro">📦 Discord Archive Pro</a></h4>
      <p>High-fidelity desktop application for complete offline archiving and browsing of Discord servers, forum channels, message threads, voice logs, and media attachments with SQLite indexing and instant full-text search.</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Stack-Electron%20%7C%20Node%20%7C%20SQLite-ff6d38?style=flat-square&labelColor=141414" alt="Stack" />
      </p>
    </td>
    <td width="50%" valign="top">
      <h4 align="center"><a href="https://github.com/Mateo-Piedra22/IronTrain">🏋️ IronTrain & IronHub</a></h4>
      <p>Cross-platform fitness application featuring customizable training progression algorithms, real-time set/rep telemetry, workout history analytics, and community workout sharing.</p>
      <p align="center">
        <img src="https://img.shields.io/badge/Stack-React%20%7C%20TypeScript%20%7C%20Postgres-478bff?style=flat-square&labelColor=141414" alt="Stack" />
      </p>
    </td>
  </tr>
</table>

---

## 🛠️ Complete Technical Skill Matrix

<div align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,py,cpp,nodejs,express,react,nextjs,vite,tailwind&perline=10" alt="Languages and Frontend" />
  <br />
  <img src="https://skillicons.dev/icons?i=postgres,sqlite,redis,docker,cloudflare,git,githubactions,linux,bash,vscode&perline=10" alt="Infrastructure and Tools" />
</div>

<br />

```
  SYSTEMS & LOW-LEVEL     C / C++ · Node.js Native Internals · Windows Service Daemons · Serial Ports / COM
  BACKEND & RUNTIMES      Node.js (v18-22+) · Express.js · Fastify · WebSockets (ws) · REST APIs · Child Process IPC
  FRONTEND & DESKTOP      TypeScript · React · Next.js · Electron · Vite · Tailwind CSS · Vanilla ES Modules
  DATABASES & STORAGE     PostgreSQL · SQLite (WAL Mode) · Redis · Atomic JSON Engines · Local-first Storage
  DEVOPS & WORKFLOWS      Docker · GitHub Actions CI/CD · Cloudflare Workers · Linux Administration · Shell Scripting
  AI AGENTS & PROTOCOLS   Model Context Protocol (MCP) · Cline Ecosystem · Anthropic Claude API · Local LLMs (Ollama)
```

---

## 📊 Live GitHub Analytics & Performance Metrics

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Mateo-Piedra22&show_icons=true&theme=tokyonight&hide_border=true&bg_color=141414&title_color=c7ff69&icon_color=7a78ff&text_color=fdf9f0&rank_icon=github" alt="GitHub Stats" width="49%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mateo-Piedra22&layout=compact&theme=tokyonight&hide_border=true&bg_color=141414&title_color=c7ff69&text_color=fdf9f0" alt="Top Languages" width="49%" />
</div>

<div align="center" style="margin-top: 10px;">
  <img src="https://streak-stats.demolab.com/?user=Mateo-Piedra22&theme=tokyonight&hide_border=true&background=141414&ring=c7ff69&fire=ff6d38&currStreakLabel=c7ff69&sideLabels=fdf9f0&dates=888888" alt="Streak Stats" width="49%" />
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Mateo-Piedra22&theme=github-compact&bg_color=141414&color=c7ff69&line=7a78ff&point=ff6d38&area=true&hide_border=true" alt="Activity Graph" width="49%" />
</div>

---

## 🐍 Interactive Contribution Snake Grid

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake.svg">
  <img alt="Snake Contribution Graph" src="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake-dark.svg" width="100%">
</picture>

---

## 🌐 Connect, Collaborate & Inquire

<div align="center">
  <a href="https://github.com/Mateo-Piedra22">
    <img src="https://img.shields.io/badge/GitHub-Mateo--Piedra22-141414?style=for-the-badge&logo=github&logoColor=c7ff69&labelColor=232323" alt="GitHub" />
  </a>
  &nbsp;
  <a href="https://motiona.xyz">
    <img src="https://img.shields.io/badge/Website-motiona.xyz-141414?style=for-the-badge&logo=safari&logoColor=7a78ff&labelColor=232323" alt="Website" />
  </a>
  &nbsp;
  <a href="mailto:piedrabuena.mateo03@gmail.com">
    <img src="https://img.shields.io/badge/Email-piedrabuena.mateo03@gmail.com-141414?style=for-the-badge&logo=gmail&logoColor=ff6d38&labelColor=232323" alt="Email" />
  </a>
  &nbsp;
  <a href="https://discord.com">
    <img src="https://img.shields.io/badge/Discord-Community-141414?style=for-the-badge&logo=discord&logoColor=478bff&labelColor=232323" alt="Discord" />
  </a>
</div>

<br />

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=20,14,10&height=120&section=footer" width="100%" alt="Footer Banner" />
</div>

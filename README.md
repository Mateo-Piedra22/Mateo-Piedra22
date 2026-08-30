<div align="center">

  <!-- Native SVG Header (Self-Hosted in Repository) -->
  <img src="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/main/assets/header.svg" width="100%" alt="Mateo Piedrabuena Header" />

  <br /><br />

  <!-- Dynamic Animated Typing Subtitle -->
  <p align="center">
    <a href="https://github.com/Mateo-Piedra22">
      <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&duration=2400&pause=900&color=C7FF69&background=14141400&center=true&vCenter=true&multiline=false&width=800&lines=Creator+%26+Lead+Architect+of+ArgenPOS;Computer+Engineering+Student+%40+UNL+(Argentina);Full-Stack+%26+Low-Level+Systems+Engineer;Creator+of+ClineMarket+%26+Discord+Archive+Pro;Founder+%26+Tech+Lead+%40+MotionA+Studio" alt="Typing Subtitle" />
    </a>
  </p>

  <!-- Metric Badges -->
  <p align="center">
    <a href="https://github.com/Mateo-Piedra22"><img src="https://img.shields.io/badge/LOCATION-Santa%20Fe%2C%20Argentina-141414?style=for-the-badge&logo=googlemaps&logoColor=c7ff69&labelColor=1a1a1a" alt="Location" /></a>
    <a href="https://motiona.xyz"><img src="https://img.shields.io/badge/STUDIO-MotionA-141414?style=for-the-badge&logo=safari&logoColor=7a78ff&labelColor=1a1a1a" alt="MotionA" /></a>
    <a href="mailto:piedrabuena.mateo03@gmail.com"><img src="https://img.shields.io/badge/CONTACT-piedrabuena.mateo03%40gmail.com-141414?style=for-the-badge&logo=gmail&logoColor=ff6d38&labelColor=1a1a1a" alt="Email" /></a>
    <img src="https://komarev.com/ghpvc/?username=Mateo-Piedra22&label=PROFILE%20VIEWS&color=c7ff69&style=for-the-badge" alt="Profile Views" />
  </p>

</div>

---

## Executive Profile & Systems Engineering Focus

I am a **Computer Engineering student** at the **National University of the Littoral (UNL)** in Santa Fe, Argentina, and a **Systems & Full-Stack Architect**. My work focuses on high-reliability transactional software, native hardware communication layers, offline-first architectures, developer tooling, and distributed systems.

```
+-----------------------------------------------------------------------------------------------+
|  ACADEMIC DISCIPLINE    : Computer Engineering (Ingenieria en Informatica)                    |
|  INSTITUTION            : Universidad Nacional del Litoral (UNL), Santa Fe, Argentina         |
|  FLAGSHIP SYSTEMS       : ArgenPOS (Enterprise POS & Hardware Bridge) · Cline Marketplace    |
|  VENTURE & STUDIO       : MotionA Studio (https://motiona.xyz)                                |
|  CORE SPECIALIZATION    : Hardware Protocols · IPC · Local-First Engines · AI Control Planes  |
+-----------------------------------------------------------------------------------------------+
```

### Core Architecture & Systems Principles

- **Local-First Sovereignty**: Applications must operate with full fidelity regardless of network availability. Critical sales and state data reside in ACID-compliant local engines with background cloud reconciliation.
- **Hardware-Level Interfacing**: Direct bit-level communication with commercial hardware via serial buses (RS-232, COM), raw USB, and native Windows daemon services.
- **Zero-Friction Distribution**: Standalone self-contained executables and CLI tools requiring zero external runtime pre-installation on client machines.
- **Defensive Engineering**: Sandboxed subprocess execution, memory-safe buffer handling, path traversal barriers, and token-authenticated local loopback protocols.

---

## Flagship Systems & Core Engineering Showcase

<br />

### 1. [ArgenPOS & ArgenPOS Bridge](https://github.com/Mateo-Piedra22/argenpos-bridge-releases) — *Enterprise Point of Sale & Native Hardware Bridge*

**ArgenPOS** is a high-availability Point of Sale and retail transaction platform engineered for commercial retail chains, supermarkets, and hospitality environments requiring continuous transaction processing and millisecond-level hardware execution.

#### Hardware Interfacing & IPC Protocol Topology

```
+------------------------------------+                             +----------------------------------------+
|         ArgenPOS Web Client        |    Local Loopback WebSocket |          ArgenPOS Native Bridge        |
|      (React / TypeScript POS)      | <=========================> |     (Self-Contained Windows Service)   |
|   - Real-time Cashier Terminal     |     ws://127.0.0.1:9876     |   - Token-Authenticated IPC Protocol   |
|   - Offline Queue & Reconciliation |                             |   - Low-Level COM Serial Multiplexer   |
+------------------------------------+                             +-------------------+--------------------+
                                                                                       |
                         +-----------------------------+-------------------------------+------------------------------+
                         |                             |                               |                              |
                         v                             v                               v                              v
             +-----------------------+     +-----------------------+       +-----------------------+      +-----------------------+
             |   Thermal Printers    |     |     Cash Drawers      |       |   Customer Displays   |      |  Barcode & Scales     |
             |   (ESC/POS via COM)   |     |   (Pin 2 Kick Pulse)  |       |   (VFD 2x20 Pole Display)    |  (RS-232 Serial Port) |
             |   - Raw Raster Bitmap |     |   - Automated Solenoid|       |   - Real-time Price Line  |      |  - Continuous Weight  |
             |   - Sub-10ms Cut Fire |     |   - Drawer State Probe|       |   - Scrolling Promotional |      |  - Tare / Zero Events |
             +-----------------------+     +-----------------------+       +-----------------------+      +-----------------------+
```

#### Key Technical Capabilities

| System Layer | Implementation Specification |
| :--- | :--- |
| **Native Daemon** | Windows background service distributed as a standalone `.exe` without Node or runtime dependencies. |
| **Hardware Driver Engine** | Raw bitstream ESC/POS generation with bitmap conversion, codepage mapping, and cut command queuing. |
| **Serial Bus Multiplexer** | Concurrent non-blocking polling across COM1–COM16 serial ports for scanners and digital weighing scales. |
| **Offline Transaction Buffer**| Local transactional append-only log with deterministic conflict resolution upon cloud reconnection. |
| **Security Layer** | Local loopback isolation (`127.0.0.1`), shared cryptographic tokens, and zero outbound telemetry exposure. |

<p align="left">
  <a href="https://github.com/Mateo-Piedra22/argenpos-bridge-releases"><img src="https://img.shields.io/badge/DOWNLOAD-Latest%20Windows%20Release%20(.exe)-c7ff69?style=for-the-badge&logo=windows&logoColor=141414&labelColor=1a1a1a" alt="Download" /></a>
  <img src="https://img.shields.io/badge/STATUS-Production%20Active-7a78ff?style=for-the-badge&labelColor=1a1a1a" alt="Status" />
</p>

---

### 2. [Cline Marketplace](https://github.com/Mateo-Piedra22/ClineMarket) — *Local Control Plane & Primitive Registry for Cline*

**Cline Marketplace** is a developer-grade local control plane, offline-first registry browser, and CLI runner for Cline plugins, skills, and Model Context Protocol (MCP) servers.

```
+--------------------------------------------------------------------------------------------------------------------+
|                                              CLINE MARKETPLACE SYSTEM                                              |
+--------------------------------------------------------------------------------------------------------------------+
|   [ FRONTEND CONTROL PLANE ]            [ RECONCILIATION ENGINE ]              [ WORKSPACE HEURISTICS ]            |
|   - Vanilla ESM Design System           - Multi-root Filesystem Probing        - package.json / pyproject AST      |
|   - Multi-token Inverted Index          - Ghost / Drift Detection Engine       - Curated Toolchain Synthesizer     |
|   - Dynamic Port Auto-Allocation        - Atomic JSON State Persistence        - Project-scoped Installation Scope |
+--------------------------------------------------------------------------------------------------------------------+
```

- **Live Filesystem Reconciliation**: Probes active VS Code, Claude Desktop, and Cline CLI configuration paths to dynamically reconcile live disk state against catalog definitions.
- **Project-Scoped Installation**: Supports scoped primitive execution targeting isolated project workspaces (`--scope workspace`) with persistent workspace history.
- **Automated Verification Pipeline**: Headless Chrome DevTools Protocol (CDP) screenshot capture hook and full cross-platform CI matrix testing on every push.

<p align="left">
  <a href="https://github.com/Mateo-Piedra22/ClineMarket"><img src="https://img.shields.io/badge/REPO-Mateo--Piedra22%2FClineMarket-c7ff69?style=for-the-badge&logo=github&logoColor=141414&labelColor=1a1a1a" alt="Repo" /></a>
  <img src="https://img.shields.io/badge/LICENSE-Apache%202.0-7a78ff?style=for-the-badge&labelColor=1a1a1a" alt="License" />
</p>

---

### 3. [Discord Archive Pro](https://github.com/Mateo-Piedra22/Discord-Archive-Pro) & [IronTrain](https://github.com/Mateo-Piedra22/IronTrain)

<table>
  <tr>
    <td width="50%" valign="top">
      <h3 align="center">Discord Archive Pro</h3>
      <p align="center">
        <img src="https://img.shields.io/badge/RUNTIME-Electron%20%7C%20Node.js-ff6d38?style=flat-square&labelColor=141414" alt="Runtime" />
        <img src="https://img.shields.io/badge/STORAGE-SQLite%20(FTS5)-ffc412?style=flat-square&labelColor=141414" alt="Storage" />
      </p>
      <p>High-fidelity desktop application engineered for cold archival, indexing, and offline browsing of complete Discord communities, voice logs, threads, and multi-gigabyte media attachments with full-text search indexing.</p>
    </td>
    <td width="50%" valign="top">
      <h3 align="center">IronTrain & IronHub</h3>
      <p align="center">
        <img src="https://img.shields.io/badge/STACK-React%20%7C%20TypeScript-00a652?style=flat-square&labelColor=141414" alt="Stack" />
        <img src="https://img.shields.io/badge/DATABASE-PostgreSQL-478bff?style=flat-square&labelColor=141414" alt="Database" />
      </p>
      <p>Cross-platform fitness analytics and training progression system featuring dynamic periodization calculators, set-by-set velocity tracking, and distributed community workout logging.</p>
    </td>
  </tr>
</table>

---

## Technical Skills & Systems Matrix

<div align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,py,cpp,nodejs,express,react,nextjs,vite,tailwind&perline=10" alt="Core Technologies" />
  <br />
  <img src="https://skillicons.dev/icons?i=postgres,sqlite,redis,docker,cloudflare,git,githubactions,linux,bash,vscode&perline=10" alt="Infrastructure and Systems" />
</div>

<br />

| Technical Domain | Technologies, Protocols & Toolchains |
| :--- | :--- |
| **Low-Level & Hardware** | `C / C++` `Serial Ports (RS-232 / COM)` `ESC/POS Thermal Protocol` `Windows Service Daemons` `Child Process IPC` |
| **Runtimes & Backends** | `Node.js (v18–v22+)` `TypeScript` `Express.js` `Fastify` `WebSockets (ws)` `RESTful Architectures` `CDP Protocol` |
| **Frontend & Desktop** | `React` `Next.js` `Electron` `Vite` `Tailwind CSS` `Vanilla ES Modules` `Design Systems` `HTML5 / CSS3 (CSS Grid)` |
| **Databases & Storage** | `PostgreSQL` `SQLite (WAL Mode & FTS5)` `Redis` `Atomic JSON File Engines` `Prisma ORM` |
| **DevOps & Infrastructure** | `Docker` `GitHub Actions (CI/CD Matrices)` `Cloudflare Workers` `Linux (Debian/Ubuntu)` `Git & GitHub CLI` |
| **AI Agents & MCP** | `Model Context Protocol (MCP)` `Cline Agent Ecosystem` `Anthropic Claude API` `Local LLM Integration (Ollama)` |

---

## Live Performance & GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats-sigma-five.vercel.app/api?username=Mateo-Piedra22&show_icons=true&theme=tokyonight&hide_border=true&bg_color=141414&title_color=c7ff69&icon_color=7a78ff&text_color=fdf9f0&rank_icon=github" alt="GitHub Stats" width="49%" />
  <img src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=Mateo-Piedra22&layout=compact&theme=tokyonight&hide_border=true&bg_color=141414&title_color=c7ff69&text_color=fdf9f0" alt="Top Languages" width="49%" />
</div>

<div align="center" style="margin-top: 10px;">
  <img src="https://streak-stats.demolab.com/?user=Mateo-Piedra22&theme=tokyonight&hide_border=true&background=141414&ring=c7ff69&fire=ff6d38&currStreakLabel=c7ff69&sideLabels=fdf9f0&dates=888888" alt="Streak Stats" width="80%" />
</div>

---

## Contribution Graph & Continuous Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake.svg">
  <img alt="Snake Contribution Graph" src="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/output/github-contribution-grid-snake-dark.svg" width="100%">
</picture>

---

## Contact & Professional Inquiries

<div align="center">
  <a href="https://github.com/Mateo-Piedra22">
    <img src="https://img.shields.io/badge/GITHUB-Mateo--Piedra22-141414?style=for-the-badge&logo=github&logoColor=c7ff69&labelColor=232323" alt="GitHub" />
  </a>
  &nbsp;
  <a href="https://motiona.xyz">
    <img src="https://img.shields.io/badge/STUDIO%20PORTFOLIO-motiona.xyz-141414?style=for-the-badge&logo=safari&logoColor=7a78ff&labelColor=232323" alt="Website" />
  </a>
  &nbsp;
  <a href="mailto:piedrabuena.mateo03@gmail.com">
    <img src="https://img.shields.io/badge/DIRECT%20EMAIL-piedrabuena.mateo03%40gmail.com-141414?style=for-the-badge&logo=gmail&logoColor=ff6d38&labelColor=232323" alt="Email" />
  </a>
  &nbsp;
  <a href="https://discord.com">
    <img src="https://img.shields.io/badge/DISCORD-Community-141414?style=for-the-badge&logo=discord&logoColor=478bff&labelColor=232323" alt="Discord" />
  </a>
</div>

<br />

<div align="center">
  <img src="https://raw.githubusercontent.com/Mateo-Piedra22/Mateo-Piedra22/main/assets/footer.svg" width="100%" alt="Footer Banner" />
</div>

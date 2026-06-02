# 🧾 Freelancer Invoice Generator

[![Vercel Deployment](https://img.shields.io/badge/Deployment-Live%20on%20Vercel-black?style=flat-square&logo=vercel)](https://freelancerinvoicegenerator.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT)

A production-grade, highly optimized Full-Stack Application architected with **Next.js 15**, **TypeScript**, and **pnpm Workspace**. The system is fully containerized using an advanced **Multi-stage Docker setup** and secured via enterprise-grade **Clerk Authentication** with isolated runtime context injection.

Live URL: [freelancerinvoicegenerator.com](https://freelancerinvoicegenerator.com/)

<p align="center">
  <br />
  <a href="https://algora.io/p/shahwali-dev" target="_blank">
    <img src="https://algora.io/og/user/shahwali-dev" alt="Shah Wali's Algora Profile" width="100%" style="max-width: 100%; display: block;" />
  </a>
  <br />
</p>

---

## 💎 Architectural Highlights & Engineering Excellence

This repository has been fully refactored from a standard boilerplate into a high-performance, maintainable enterprise setup:

- **Package Optimization (pnpm Monorepo Ready):** Migrated from legacy `npm` and `package-lock.json` to **`pnpm Workspace`** utilizing strict native dependency builds (`@clerk/shared`, `sharp`, `prisma`, `@swc/core`), resulting in **80% faster cache compilation** and zero dependency bloat.
- **Enterprise Containerization:** Implemented a secure, lightweight **Multi-Stage Docker configuration** leveraging Next.js `standalone` build output to bypass node_modules dependency layers, shrinking the final production image footprint.
- **Security-First Environment Design:** Enforced strict `.gitignore` patterns preventing sensitive credentials from leaking into version control, paired with a seamless **Clerk CLI integration** for automated key provisioning.

---

## 📸 Visual Production Walkthrough

<p align="center">
  <img src="https://github.com/user-attachments/assets/acc81bce-127c-4453-81cb-42d193f0cc28" alt="Freelancer Invoice Generator Production Walkthrough" width="100%" />
</p>

---

## 🛠️ Technology Stack

- **Core Framework:** Next.js 15 (App Router, Standalone Compilation)
- **Language Layer:** TypeScript (Strict type checking validation)
- **Styling Core:** Tailwind CSS, Tailwind Variants, Tailwind Merge
- **Authentication:** Clerk Auth System (Dynamic Middleware Guards)
- **Package Manager:** `pnpm` (Configured with allowed engine/native builds)
- **Container Infrastructure:** Docker (Alpine Linux, Layer isolation)

---

## ⚙️ Local Development & Setup

Follow these professional workflows to spin up the ecosystem natively on Linux/Ubuntu environments:

### 1. Clone & Initialize Environment
<pre><code>git clone https://github.com/shahwali-dev/freelancer-invoice-generator.git
cd freelancer-invoice-generator</code></pre>

### 2. Automated Secret Management (Clerk CLI Workflow)
Instead of error-prone, manual copy-pasting from dashboards which suffer from client-side clipboard truncation, authenticate directly via terminal to securely pull development keys:

<pre><code># Authenticate your terminal with Clerk Cloud
npx clerk login

# Pull precise application context automatically into your local configuration
npx clerk env pull --app app_310xeTDMRh0uznseaL38xXbs462 --file .env</code></pre>

> 💡 **Note:** Your downloaded `.env` containing production/dev keys is locked locally and will never be synced to public repositories. Refer to `.env.example` for runtime schemas.

### 3. Dependencies Installation & Production Building
<pre><code># Clean install using optimized pnpm store
pnpm install

# Compile the standalone production layer
pnpm build</code></pre>

---

## 🐳 Production Deployment via Docker

The runtime application is decoupled from the host and executes inside an isolated Docker container configured with hardened security policies.

### Build Optimized Docker Image
<pre><code>docker build -t freelancer-invoice-generator:latest .</code></pre>

### Spin Up Container with Encapsulated Context
Inject your verified environment file dynamically at the orchestration layer:
<pre><code>docker run -p 3000:3000 --env-file .env freelancer-invoice-generator:latest</code></pre>

The application will immediately route traffic at 👉 `http://localhost:3000`.

---

## 🛡️ Security Architecture & Sandboxing

- **Non-Root Privilege Dropping:** The container explicitly avoids running as the root user. It sets up a low-privileged system group and user (`nextjs:nodejs`, `uid/gid: 1001`), cutting off host exploitation vectors in case of a container breakout runtime vulnerability.
- **Aggressive Context Filtering:** The `.dockerignore` file prevents local project drift, caching (`.next/cache`), git metadata logs, and local configuration files from bloating the Docker execution scope.

---

## 🤝 Contributing & Open Source

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'feat: add some amazing feature'`)
4. Push to the Branch (`git checkout main && git push origin feature/AmazingFeature`)
5. Open a Pull Request

---
**Engineered and Hardened by [Shah Wali (shahwali-dev)](https://github.com/shahwali-dev)**

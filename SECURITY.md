# 🛡️ Security Policy

The management tracking and automated dependency verification policies for the **Freelancer Invoice Generator** ecosystem.

---

## 📈 Supported Versions

Security patches, automated dependency rollouts (Next.js framework updates, Clerk middleware adjustments, and Alpine Linux Docker base layer patches) are strictly applied directly to the primary production environment.

| Version | Supported | Security Rollouts |
| :--- | :---: | :--- |
| **1.0.x** (Current / `main`) | ✅ | Active Maintenance & Automated Dependency Patches |
| **< 1.0.0** (Legacy Build) | ❌ | Unsupported (Immediate upgrade recommended) |

---

## 🚨 Reporting a Vulnerability

We take the security of this infrastructure extremely seriously. If you discover any active security vulnerabilities, dynamic credential leaks, or potential Docker container breakout vectors, please **do not open a public GitHub Issue**. 

Instead, please initiate a private remediation workflow through the following secure channels:

### 1. GitHub Private Vulnerability Reporting
1. Navigate directly to the **Security** tab of this repository.
2. Select **Advisories** under the vulnerability management pane.
3. Click the **"Report a vulnerability"** button to open a secure disclosure context directly with the core maintainer.

### 2. Direct Maintainer Escalation
If you prefer direct communication, please securely coordinate an isolated patch deployment via the verified profile contact options.

---

## ⏳ Operational SLA & What to Expect

> 💡 **Security Commitment:** Every verified vulnerability is treated with the highest priority to ensure the integrity of the containerized production stack.

* **Initial Verification:** Within 48 hours of secure vulnerability submission.
* **Active Status Updates:** Transparent progress tracking as we validate, reproduce, and engineer the targeted security patch.
* **Resolution & Release:** Once a production-grade patch is verified, a compiled release layer will be safely merged, and your contribution will be formally credited within the release logs (if explicitly desired).

---
**Engineered and Hardened by [Shah Wali (shahwali-dev)](https://github.com/shahwali-dev)**

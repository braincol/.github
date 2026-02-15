<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-light.svg">
    <img alt="Braincol" src="https://raw.githubusercontent.com/braincol/.github/main/profile/braincol-banner-dark.svg" width="700">
  </picture>
</p>

<h3 align="center">Building the infrastructure for AI-native enterprises.</h3>

<p align="center">
  <a href="https://braincol.com">Website</a> &middot;
  <a href="https://github.com/braincol/braincol-vault">Vault</a> &middot;
  <a href="https://github.com/braincol/braincol-sentry">Sentry</a> &middot;
  <a href="https://github.com/braincol/never-leak-protocol">NL Protocol</a>
</p>

---

<div align="center">

**What happens when your AI agent reads a secret?**

It enters the LLM context window. It leaves your machine. It's gone.

**We built the protocol that makes this impossible.**

</div>

---

### What we build

Three products. One mission: make AI agents enterprise-ready.

<table>
  <tr>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/braincol/braincol-vault">Braincol Vault</a></h4>
      <strong>The Secret Manager for AI Agents</strong><br/><br/>
      AI agents use your secrets without ever seeing them. 5 layers of defense. Zero secrets in LLM context windows. The first &mdash; and only &mdash; secret manager designed for this threat model.<br/><br/>
      <a href="https://github.com/braincol/braincol-vault"><img src="https://img.shields.io/badge/v1.0-Stable-22C55E?style=flat-square" alt="Stable"/></a>
      <a href="https://github.com/braincol/braincol-vault"><img src="https://img.shields.io/badge/Open_Core-AGPL--v3-blue?style=flat-square" alt="Open Core"/></a>
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/braincol/braincol-sentry">Braincol Sentry</a></h4>
      <strong>Data Intelligence Platform</strong><br/><br/>
      Source-agnostic anomaly detection powered by AI agents. Connect any data source, detect anomalies, and get explanations &mdash; not just alerts. Enterprise security and compliance built in.<br/><br/>
      <a href="https://github.com/braincol/braincol-sentry"><img src="https://img.shields.io/badge/status-Active_Development-3B82F6?style=flat-square" alt="Active Development"/></a>
    </td>
    <td width="33%" valign="top">
      <h4><a href="https://github.com/braincol/never-leak-protocol">Never Leak Protocol</a></h4>
      <strong>The Open Standard for Agent Security</strong><br/><br/>
      The security standard for the AI agent era. 7 defense levels. Defines how agents interact with credentials. Open source. Vendor-neutral. Built for the community.<br/><br/>
      <a href="https://github.com/braincol/never-leak-protocol"><img src="https://img.shields.io/badge/spec-v1.0-8B5CF6?style=flat-square" alt="v1.0 Spec"/></a>
      <a href="https://github.com/braincol/never-leak-protocol"><img src="https://img.shields.io/badge/license-Apache_2.0-blue?style=flat-square" alt="Apache 2.0"/></a>
    </td>
  </tr>
</table>

---

### How Vault works

Traditional secret managers expose values. Braincol Vault never does.

```
❌ Traditional    Agent reads secret → secret in LLM context → leaked
✅ Braincol Vault Agent requests action → vault executes → only result returned
```

The agent says *"run this with my API key"*. Vault injects the secret into a subprocess as an environment variable. The agent never sees the value. The LLM provider never sees the value. Nobody does.

**Works with every major AI coding agent:** Claude Code &middot; Cursor &middot; Copilot &middot; Codex &middot; Windsurf &middot; Aider &middot; Any MCP client

```bash
# One command to start
curl -fsSL https://raw.githubusercontent.com/braincol/braincol-vault/main/install.sh | bash
```

---

### The NL Protocol &mdash; an open standard we created

We didn't just build a product. We wrote the specification.

The [Never Leak Protocol](https://github.com/braincol/never-leak-protocol) is an open standard (Apache 2.0) that defines how AI agents must interact with secrets. Any tool can implement it. Braincol Vault is the reference implementation.

| Level | Defense | What it does |
|:-----:|---------|-------------|
| **L1** | Agent Identity | Cryptographic identity and trust tiers |
| **L2** | Action-Based Access | Agents request actions, never see values |
| **L3** | Execution Isolation | Subprocess sandboxing and memory wipe |
| **L4** | Pre-Execution Defense | Command interception and injection detection |
| **L5** | Audit &amp; Integrity | SHA-256 hash-chained tamper-evident records |
| **L6** | Attack Detection | Behavioral anomaly detection and circuit breakers |
| **L7** | Cross-Agent Trust | Delegation tokens with scope attenuation |

**Conformance tiers:** Basic (L1-L3) for startups &middot; Standard (L1-L5) for SaaS teams &middot; Advanced (L1-L7) for enterprise

---

### Why Braincol

<table>
  <tr>
    <td width="25%" align="center" valign="top">
      <h4>Security First</h4>
      Defense-in-depth by default. Zero-knowledge encryption. X25519 + ChaCha20-Poly1305. No custom crypto &mdash; built on <a href="https://age-encryption.org">age</a>.
    </td>
    <td width="25%" align="center" valign="top">
      <h4>Enterprise Grade</h4>
      Multi-tenant isolation. RBAC with per-project scoping. Immutable audit logs. SOX, HIPAA, GDPR, PCI-DSS ready.
    </td>
    <td width="25%" align="center" valign="top">
      <h4>AI Native</h4>
      Purpose-built for autonomous agents. Native MCP integration. 23 opaque proxy tools. 7 agent config generators.
    </td>
    <td width="25%" align="center" valign="top">
      <h4>Open Standards</h4>
      We created the NL Protocol. Open source core. No vendor lock-in. Free forever for individuals.
    </td>
  </tr>
</table>

---

### By the numbers

<div align="center">

**2,655** tests passing &middot; **7** AI agents supported &middot; **5** security layers &middot; **23** MCP tools &middot; **0** secrets leaked

</div>

---

### Tech stack

`TypeScript` `Python` `NestJS` `FastAPI` `Next.js` `React 19` `LangGraph` `MongoDB` `Redis` `Turborepo` `Polars` `Zod` `Pydantic`

---

<div align="center">

**[Get started with Braincol Vault](https://github.com/braincol/braincol-vault)** &mdash; it's free and open source.

<br/>

<a href="https://braincol.com">braincol.com</a>

<br/>

<sub>Built in Colombia. Open source at heart.</sub>

</div>

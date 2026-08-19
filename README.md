# Awesome Agent Orchestrators with stars

A curated list of tools and frameworks for orchestrating agents.

Everything here decides what an agent works on, when it runs, where it runs, or what happens to its output, and takes whatever task you point it at. Single-purpose bots, and things an agent merely consumes — memory backends, MCP servers, sandbox providers, skill libraries — are out of scope.

## How to choose

* **Run several agents at once and review each diff.** [Terminal](#parallel-coding-agents--terminal-tuicli) if you live in tmux, [Desktop & Web](#parallel-coding-agents--desktop--web) if you want a GUI or phone access.
* **Keep an agent working while you're away.** [Autonomous Loop Runners](#autonomous-loop-runners) drive one goal until it verifies. [Autonomous Task Runners](#autonomous-task-runners) pull work from an issue tracker, board, or schedule.
* **Have agents split a large job between themselves.** [Multi-Agent Swarms](#multi-agent-swarms).
* **Message an agent instead of opening a tool.** [Personal Assistants](#personal-assistants) stay running, remember across sessions, and pick up work from a chat thread — general tasks, not only code.
* **Build your own orchestrator.** [Agent Infrastructure & Primitives](#agent-infrastructure--primitives) — control planes, coordination protocols, harness adapters, and runtimes.

## Parallel Coding Agents — Terminal (TUI/CLI)

Run and supervise several agent sessions side by side from a terminal — tmux panes, git worktrees, and TUI dashboards.

* [herdr](https://github.com/ogulcancelik/herdr) ⭐ 30,436 | 🐛 200 | 🌐 Rust | 📅 2026-08-19 - Agent-aware multiplexer with persistent workspaces, tabs, panes, and status detection for CLI coding agents.
* [cmux](https://github.com/manaflow-ai/cmux) ⭐ 26,216 | 🐛 4,357 | 🌐 Swift | 📅 2026-08-19 - Ghostty-based macOS terminal with vertical tabs and per-agent notifications, built for keeping many concurrent sessions legible.
* [claude-squad](https://github.com/smtg-ai/claude-squad) ⭐ 8,336 | 🐛 55 | 🌐 Go | 📅 2026-07-30 - Runs each agent as a detached background session with its own worktree, so work continues after you close the pane. Claude Code, Codex, OpenCode, Amp.
* [agent-of-empires](https://github.com/agent-of-empires/agent-of-empires) ⭐ 3,099 | 🐛 133 | 🌐 Rust | 📅 2026-08-19 - Pairs a TUI with a matching web view, so the same sessions stay reachable from a phone. Claude Code, Codex, OpenCode, Gemini, Mistral Vibe.
* [dmux](https://github.com/standardagents/dmux) ⭐ 1,743 | 🐛 30 | 🌐 HTML | 📅 2026-08-16 - Dev agent multiplexer pairing coding agents with git worktrees over tmux.
* [agent-deck](https://github.com/asheshgoplani/agent-deck) ⭐ 751 | 🐛 46 | 🌐 Go | 📅 2026-08-17 - One TUI covering sessions across Claude Code, Codex, Gemini, and OpenCode, with live status and resume for each.
* [tmux-ide](https://github.com/wavyrai/tmux-ide) ⭐ 539 | 🐛 8 | 🌐 TypeScript | 📅 2026-08-18 - Turns any project into a tmux IDE from a checked-in `ide.yml`, including preset agent-team layouts.
* [agterm](https://github.com/umputun/agterm) ⭐ 478 | 🐛 6 | 🌐 Swift | 📅 2026-08-18 - Native macOS terminal with named workspaces, a live dashboard, attention states, and a scriptable control API.
* [agentbox](https://github.com/madarco/agentbox) ⭐ 365 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-03 - Gives each agent its own sandboxed VM — local Docker or cloud via Hetzner, Daytona, Vercel, or E2B — with sub-second checkpoint starts.
* [agent-manager](https://github.com/YoanWai/agent-manager) ⭐ 337 | 🐛 21 | 🌐 Go | 📅 2026-08-19 - tmux TUI with live status, a prompt that lands in the pane without attaching, and in-terminal diff review that sends line comments back to the agent. Claude Code, Codex, OpenCode, Grok, Gemini CLI, Pi, Hermes.
* [amux](https://github.com/andyrewlee/amux) ⭐ 148 | 🐛 5 | 🌐 Go | 📅 2026-08-17 - Minimal TUI for spawning parallel coding agents in git worktrees.
* [openkanban](https://github.com/TechDufus/openkanban) ⭐ 138 | 🐛 6 | 🌐 Go | 📅 2026-06-12 - Kanban board for orchestrating coding agents, rendered entirely in the terminal.
* [thurbox](https://github.com/Thurbeen/thurbox) ⭐ 46 | 🐛 6 | 🌐 Rust | 📅 2026-08-18 - TUI orchestrator with remote SSH sessions, inter-session messaging, and a native code-review view. Works with any CLI agent you define.
* [agent-console](https://github.com/buhuipao/agent-console) ⭐ 15 | 🐛 0 | 🌐 Rust | 📅 2026-08-19 - Rust TUI that finds Codex and Claude Code sessions from the providers' own transcripts, including ones started elsewhere, and resumes their native UI rather than replacing it. No tmux or worktrees.
* [repomon](https://github.com/AliHamzaAzam/repomon) ⭐ 13 | 🐛 5 | 🌐 Rust | 📅 2026-08-18 - Rust TUI that supervises a fleet across many repositories at once, in durable tmux sessions you can approve from your phone.

## Parallel Coding Agents — Desktop & Web

The same parallel-sessions workflow as a desktop app or browser/mobile dashboard, with diff review and merge.

* [Orca](https://github.com/stablyai/orca) ⭐ 48,540 | 🐛 4,137 | 🌐 TypeScript | 📅 2026-08-19 - Agentic development environment for running a fleet on your own subscription, available on desktop and mobile.
* [t3code](https://github.com/pingdotgg/t3code) ⭐ 19,414 | 🐛 1,573 | 🌐 TypeScript | 📅 2026-08-19 - Harness control surface available as web, mobile, and desktop app. Claude Code, Codex, Cursor, Grok Build, OpenCode.
* [Aperant](https://github.com/AndyMik90/Aperant) ⭐ 14,534 | 🐛 74 | 🌐 TypeScript | 📅 2026-06-14 - Runs up to 12 agent terminals with a self-validating QA loop and automatic conflict resolution when merging back to main.
* [qm](https://github.com/yc-software/qm) ⭐ 13,912 | 🐛 270 | 🌐 TypeScript | 📅 2026-08-19 - Multiplayer harness where each teammate gets an isolated workspace to run agents independently, driven from Slack or the web.
* [superset](https://github.com/superset-sh/superset) ⭐ 13,062 | 🐛 585 | 🌐 TypeScript | 📅 2026-08-19 - Code editor built around running many agents on your machine at once.
* [humanlayer](https://github.com/humanlayer/humanlayer) ⭐ 11,295 | 🐛 69 | 🌐 TypeScript | 📅 2026-06-19 - Human-in-the-loop control for coding agents on hard problems; the repo notes its code is now largely deprecated in favor of a rebuild.
* [agent-orchestrator](https://github.com/Untrivial-ai/agent-orchestrator) ⭐ 9,626 | 🐛 717 | 🌐 Go | 📅 2026-08-19 - Agent IDE for fleets that plans the work, spawns the agents, then fixes CI failures and merge conflicts without being asked.
* [OpenChamber](https://github.com/openchamber/openchamber) ⭐ 8,947 | 🐛 889 | 🌐 TypeScript | 📅 2026-08-19 - Open-source workspace for running, supervising, and reviewing AI coding work across desktop, browser, editor, and mobile, with parallel model runs and per-run worktrees.
* [Emdash](https://github.com/generalaction/emdash) ⭐ 5,440 | 🐛 206 | 🌐 TypeScript | 📅 2026-08-18 - Agentic development environment running parallel agents against any model provider.
* [automaker](https://github.com/AutoMaker-Org/automaker) ⭐ 3,215 | 🐛 11 | 🌐 TypeScript | 📅 2026-05-22 - Describe features on a Kanban board and agents implement them in isolated worktrees, running tests and committing as they go.
* [collaborator](https://github.com/collabs-inc/collab-public) ⭐ 2,910 | 🐛 80 | 🌐 TypeScript | 📅 2026-08-08 - Arranges terminals, editors, and files as tiles on an infinite pan-and-zoom canvas instead of tabs.
* [CodeNomad](https://github.com/NeuralNomadsAI/CodeNomad) ⭐ 2,483 | 🐛 29 | 🌐 TypeScript | 📅 2026-08-19 - Desktop and web workspace around the OpenCode CLI whose SideCars embed local tools like VS Code and terminals as tabs.
* [bb](https://github.com/get-bb/bb) ⭐ 2,340 | 🐛 200 | 🌐 TypeScript | 📅 2026-08-19 - Self-controlling agentic IDE that orchestrates multiple coding agents in live threads you can follow, steer, or hand off, driven from a desktop app, web app, CLI, or HTTP API.
* [supacode](https://github.com/supabitapp/supacode) ⭐ 2,282 | 🐛 57 | 🌐 Swift | 📅 2026-08-13 - Native macOS command center for worktree-per-agent development.
* [mux](https://github.com/coder/mux) ⭐ 1,976 | 🐛 270 | 🌐 TypeScript | 📅 2026-08-19 - Desktop app for isolated, parallel agentic development.
* [synara](https://github.com/Emanuele-web04/synara) ⭐ 1,565 | 🐛 186 | 🌐 TypeScript | 📅 2026-08-18 - GUI desktop workspace for running and managing agents across local projects.
* [nimbalyst](https://github.com/nimbalyst/nimbalyst) ⭐ 1,514 | 🐛 543 | 🌐 TypeScript | 📅 2026-08-19 - Visual workspace pairing parallel worktree sessions with kanban and direct visual editing. Claude Code, Codex, OpenCode.
* [Traycer](https://github.com/traycerai/traycer) ⭐ 1,199 | 🐛 144 | 🌐 TypeScript | 📅 2026-08-19 - Bring-your-own-agent workspace running many sessions in parallel with context shared across models and providers, plus agent-to-agent messaging, shareable boards, and cross-device sync.
* [jean](https://github.com/coollabsio/jean) ⭐ 1,186 | 🐛 124 | 🌐 TypeScript | 📅 2026-08-18 - Desktop and web app for orchestrating agents across multiple projects and their git worktrees. Claude, Codex, OpenCode.
* [takopi](https://github.com/banteg/takopi) ⭐ 1,045 | 🐛 47 | 🌐 Python | 📅 2026-05-25 - Telegram bridge that puts Codex, Claude Code, OpenCode, and Pi sessions in a chat thread.
* [Waku](https://github.com/egoist/waku) ⭐ 1,018 | 🐛 83 | 🌐 Rust | 📅 2026-08-18 - Native macOS desktop app for working with local coding agents, keeping projects, sessions, and transcripts on your machine. Supports Amp, Claude Code, Codex CLI, Cursor CLI, Grok Build, OpenCode, and Pi.
* [Comet](https://github.com/zeronsh/comet) ⭐ 1,001 | 🐛 68 | 🌐 Rust | 📅 2026-08-19 - Cross-device control plane for coding agents, syncing sessions across machines and keeping agents running on an always-on daemon. Claude Code, Codex, Cursor, Grok, Hermes, Pi.
* [parallel-code](https://github.com/johannesjo/parallel-code) ⭐ 979 | 🐛 52 | 🌐 TypeScript | 📅 2026-08-18 - Desktop app running Claude Code, Codex, and Gemini CLI side by side in isolated worktrees, with a built-in diff viewer and one-click merge.
* [IM.codes](https://github.com/im4codes/imcodes) ⭐ 963 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-19 - Mobile and web control layer built for away-from-desk continuation, with terminal access, git views, localhost preview, and scheduled tasks. Claude Code, Codex, Gemini CLI.
* [ai-maestro](https://github.com/23blocks-OS/ai-maestro) ⭐ 748 | 🐛 12 | 🌐 TypeScript | 📅 2026-08-19 - Dashboard spanning multiple machines, adding memory search, code-graph queries, and agent-to-agent messaging. Claude, Aider, Cursor.
* [kandev](https://github.com/kdlbs/kandev) ⭐ 663 | 🐛 58 | 🌐 Go | 📅 2026-08-19 - Kanban workbench whose multi-step workflows assign a different agent per step behind human gates, running locally, in Docker, over SSH, or in cloud executors.
* [Alethe](https://github.com/Kc1t/alethe-agents) ⭐ 356 | 🐛 53 | 🌐 TypeScript | 📅 2026-08-18 - Local-first desktop workspace where agents and shells run as real PTYs in split panes and custom grids across projects, surviving pane close and app restart. Suspend idle groups to reclaim memory and resume with scrollback intact. Claude Code, Codex, OpenCode.
* [dorothy](https://github.com/Charlie85270/Dorothy) ⭐ 338 | 🐛 11 | 🌐 TypeScript | 📅 2026-07-07 - Desktop app combining agent orchestration with automations, Kanban management, and MCP servers.
* [aizen](https://github.com/vivy-company/aizen) ⭐ 299 | 🐛 3 | 🌐 Swift | 📅 2026-08-01 - macOS workspace that organizes worktrees, environments, and agent sessions per project.
* [vibe-tree](https://github.com/sahithvibudhi/vibe-tree) ⭐ 266 | 🐛 12 | 🌐 TypeScript | 📅 2026-07-25 - One git worktree per agent, delivered as desktop, web, and CLI.
* [diri](https://github.com/cristicretu/diri) ⭐ 264 | 🐛 21 | 🌐 Rust | 📅 2026-08-17 - Native macOS app running Claude Code, Codex, Cursor, Gemini, and shells in parallel across git worktrees or remote hosts, with live status, session persistence across restarts, a menu-bar rollup, and an MCP server for agents to spawn others.
* [jat](https://github.com/joewinke/jat) ⭐ 251 | 🐛 1 | 🌐 Svelte | 📅 2026-08-13 - Visual dashboard combining live sessions, task management, code editor, and terminal, with parallel swarm workflows.
* [constellagent](https://github.com/owengretzinger/constellagent) ⭐ 214 | 🐛 6 | 🌐 TypeScript | 📅 2026-05-05 - macOS app giving each agent its own terminal, editor, and git worktree in a single window.
* [Proliferate](https://github.com/proliferate-ai/proliferate) ⭐ 172 | 🐛 51 | 🌐 TypeScript | 📅 2026-08-19 - Agent IDE that runs sessions locally or in the cloud and lets you build reusable workflows from them.
* [ivy-tendril](https://github.com/Ivy-Interactive/Ivy-Tendril) ⭐ 170 | 🐛 166 | 🌐 C# | 📅 2026-08-18 - Drives agents through a plan-based lifecycle with verification gates, self-improving memory, and human checkpoints. Claude Code, Codex, Antigravity, Copilot, OpenCode.
* [Ouijit](https://github.com/ouijit/ouijit) ⭐ 154 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-19 - Kanban board and terminals wired together by lifecycle hooks, scripts, and a session-aware CLI, so a task runs by hand, on a script, or delegated to the agent. Per-task worktrees, optional VM sandboxing. Claude Code, Codex, Pi, OpenCode.
* [clideck](https://github.com/rustykuntz/clideck) ⭐ 151 | 🐛 3 | 🌐 JavaScript | 📅 2026-08-19 - Chat-app-style dashboard with autopilot routing between agents and full control from a phone. Claude Code, Codex, Gemini CLI, OpenCode.
* [Claude Command Center (CCC)](https://github.com/amirfish1/claude-command-center) ⭐ 125 | 🐛 18 | 🌐 Python | 📅 2026-08-19 - Local dashboard for spawning, monitoring, and resuming sessions across Claude Code, Codex, Cursor, Antigravity, and Kilo Code.
* [Tempest](https://github.com/tempestai-dev/tempest) ⭐ 124 | 🐛 4 | 🌐 TypeScript | 📅 2026-08-18 - Tauri desktop ADE running CLI agents in parallel isolated worktrees, with a shared local code-knowledge graph that cuts token use across sessions, plus live status and built-in diff/PR review.
* [tlbx](https://github.com/tlbx-ai/tlbx) ⭐ 101 | 🐛 11 | 🌐 C# | 📅 2026-08-18 - Self-hosted browser workspace holding persistent real PTY sessions on your own machines, reachable from any browser or phone.
* [Garcon](https://github.com/cfal/garcon) ⭐ 57 | 🐛 37 | 🌐 TypeScript | 📅 2026-08-18 - Self-hosted browser and mobile workspace with diff review, Git/PR workflows, mobile approvals, scheduling, and cross-agent transfers. Seven CLI agents.
* [Better Agent](https://github.com/ofekron/better-agent) ⭐ 56 | 🐛 1 | 🌐 Python | 📅 2026-08-19 - Local web workspace with persistent state, approvals, and restart recovery for native Claude, Codex, and Gemini sessions.
* [clave](https://github.com/codika-io/clave) ⭐ 47 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-19 - Native macOS app with split and grid layouts, session groups, SSH remote sessions, and usage analytics for Claude Code.
* [GraphCode](https://github.com/scgopi/GraphCode) ⭐ 43 | 🐛 6 | 🌐 Swift | 📅 2026-08-18 - macOS app that wires agent sessions into a graph: each node is a live terminal you can attach to mid-run, each edge a hand-off, message, or spawn that fires while you're away. Claude Code, Copilot CLI, Codex.
* [vibecraft](https://github.com/rayzhudev/vibecraft) ⭐ 35 | 🐛 2 | 🌐 TypeScript | 📅 2026-07-19 - RTS-style workspace for commanding coding agents.
* [AGX](https://github.com/ramarlina/agx) ⭐ 27 | 🐛 1 | 🌐 TypeScript | 📅 2026-05-06 - Wake-work-sleep checkpointing keeps a persistent agent team on long objectives, with human gates between cycles.
* [octomux](https://github.com/ShreyPaharia/octomux) ⭐ 21 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-17 - Local dashboard with a kanban fleet view, one unified permission inbox across agents, and in-app diff review.
* [Fletch](https://github.com/fwdai/fletch) ⭐ 20 | 🐛 0 | 🌐 Rust | 📅 2026-08-14 - Native macOS IDE that seals each agent in its own repo clone under Seatbelt or Docker, serves each a shared symbol and call-graph index over MCP, and gates every step on tests or your approval. Claude Code, Codex, Cursor, OpenCode.
* [intentic](https://github.com/intentic/intentic) ⭐ 16 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-19 - Browser and mobile workspace where every agent gets a persistent Docker sandbox on a machine you own plus a git worktree of its own, reached over an outbound-only Cloudflare tunnel, so runs keep going after you close the tab. Plan mode, per-hunk diff review, an environment Dockerfile the agent proposes and you approve, credential capabilities injected per turn, and schedule, webhook or event triggers. Claude Code, Codex, Grok, Kimi Code, Gemini. MIT.
* [agent-squid](https://github.com/agent-squid/squid) ⭐ 13 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-19 - Browser UI organized into named lanes (`#topic@agent`), with context shared across agents and a realtime quota gauge.

## Multi-Agent Swarms

Systems where multiple specialized agents actively coordinate, communicate, and delegate toward a shared goal.

* [paperclip](https://github.com/paperclipai/paperclip) ⭐ 78,832 | 🐛 5,159 | 🌐 TypeScript | 📅 2026-08-19 - Self-hosted platform where agents wake on heartbeats to claim tickets, governed by org charts, budgets, and approval gates.
* [ruflo](https://github.com/ruvnet/ruflo) ⭐ 68,257 | 🐛 844 | 🌐 TypeScript | 📅 2026-08-19 - Meta-harness for deploying coordinated swarms and conversational multi-agent workflows. Formerly claude-flow.
* [buzz](https://github.com/block/buzz) ⭐ 28,459 | 🐛 2,861 | 🌐 Rust | 📅 2026-08-19 - Agents are first-class members of shared channels on a Nostr relay you own, with their own keys and audit trails. Claude Code, Codex, Goose.
* [gastown](https://github.com/gastownhall/gastown) ⭐ 17,668 | 🐛 393 | 🌐 Go | 📅 2026-08-19 - Scales to 20-30 agents with a coordinator, git-backed issue tracking, health watchdogs, and a Bors-style merge queue.
* [ClawTeam](https://github.com/HKUDS/ClawTeam) ⭐ 5,497 | 🐛 37 | 🌐 Python | 📅 2026-05-09 - Agents spawn and manage their own teammates from one command, coordinating through file-based or P2P inboxes across tmux worktrees.
* [claude\_codex\_bridge](https://github.com/SeemSeam/claude_codex_bridge) ⭐ 3,426 | 🐛 100 | 🌐 Python | 📅 2026-08-18 - Workspace for mixing different vendors' CLI agents in one visible collaboration session.
* [agentsmesh](https://github.com/AgentsMesh/AgentsMesh) ⭐ 2,322 | 🐛 20 | 🌐 Go | 📅 2026-08-03 - Remote AI workstations with PTY sandboxes and worktree isolation, coordinating across channels and pod bindings. Claude Code, Codex, Gemini CLI, Aider, OpenCode.
* [Agent Teams](https://github.com/777genius/agent-teams-ai) ⭐ 1,948 | 🐛 23 | 🌐 TypeScript | 📅 2026-08-17 - Desktop app where you give high-level commands to autonomous coding-agent teams across Claude Code, Codex, OpenCode, Cursor, Grok, GitHub Copilot, Kiro, Z.AI, MiniMax, Kimi, 200+ models, and 75+ LLM providers. Agents coordinate through inter-agent messaging, Kanban tasks, and built-in code review.
* [scion](https://github.com/GoogleCloudPlatform/scion) ⭐ 1,675 | 🐛 50 | 🌐 Go | 📅 2026-08-18 - Orchestration testbed running agents in parallel isolated containers with dynamic coordination and normalized telemetry.
* [multi-agent-shogun](https://github.com/yohey-w/multi-agent-shogun) ⭐ 1,415 | 🐛 7 | 🌐 Shell | 📅 2026-08-06 - Shogun to karo to ashigaru hierarchy running up to 10 agents over tmux with no coordination API cost.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 1,334 | 🐛 15 | 🌐 TypeScript | 📅 2026-08-16 - A commander agent decomposes goals and dispatches specialists with isolated skills and memory. Claude Code, Codex, OpenCode, Cline.
* [Fusion](https://github.com/Runfusion/Fusion) ⭐ 1,135 | 🐛 71 | 🌐 TypeScript | 📅 2026-08-19 - Multi-node orchestrator with a kanban board, plan-review-execute gates, per-task worktrees, and hierarchical missions.
* [loki-mode](https://github.com/asklokesh/loki-mode) ⭐ 1,046 | 🐛 7 | 🌐 Shell | 📅 2026-08-18 - PRD-to-deployed-product SDLC with 41 agents in 8 swarms, nine quality gates, and blind three-reviewer code review. Source-available under BUSL-1.1.
* [hcom](https://github.com/aannoo/hcom) ⭐ 455 | 🐛 26 | 🌐 Rust | 📅 2026-08-09 - Lets agents message, watch, and spawn each other across terminals. Claude Code, Codex, Antigravity, Cursor, OpenCode, Kilo, and more.
* [agent-kanban](https://github.com/saltbo/agent-kanban) ⭐ 448 | 🐛 20 | 🌐 TypeScript | 📅 2026-07-28 - Leader-worker task board with cryptographic agent identity. Claude Code, Codex, Gemini CLI.
* [NXTG-Forge Orchestrator](https://github.com/nxtg-ai/forge-orchestrator) ⭐ 155 | 🐛 6 | 🌐 Rust | 📅 2026-08-09 - Coordinates Claude Code, Codex, and Gemini CLI on one shared repo through a research-plan-delegate-adversarial-verify-deploy pipeline, with file locking, knowledge capture, and drift detection. Single Rust binary.
* [ORCH](https://github.com/oxgeneral/ORCH) ⭐ 144 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-01 - CLI runtime managing agents as typed teams with an explicit state machine and goals. Claude Code, Codex, Cursor.
* [kodo](https://github.com/ikamensh/kodo) ⭐ 128 | 🐛 3 | 🌐 Python | 📅 2026-07-18 - Directs agents through work cycles where a separate agent independently verifies each result. Claude Code, Codex, Gemini CLI.
* [tutti](https://github.com/nutthouse/tutti) ⭐ 112 | 🐛 19 | 🌐 Rust | 📅 2026-07-28 - Config-driven workflows passing typed artifacts between agents, each in its own worktree.
* [CompanyHelm](https://github.com/CompanyHelm/companyhelm) ⭐ 73 | 🐛 0 | 🌐 TypeScript | 📅 2026-06-29 - Distributed orchestrator with task management and direct agent-to-agent conversations.
* [5dive](https://github.com/5dive-ai/5dive) ⭐ 52 | 🐛 12 | 🌐 Shell | 📅 2026-08-19 - Named agents on a shared org chart and backlog hand work to each other and escalate to a human over Telegram. Claude Code, Codex, Grok, Antigravity, OpenCode.
* [Agon](https://github.com/AutoResearch-Factory/Agon) ⭐ 41 | 🐛 1 | 🌐 Python | 📅 2026-08-18 - Orchestrates scientist, coder, and auditor loops from research topic through proposal to experiment.
* [shire](https://github.com/victor36max/shire) ⭐ 37 | 🐛 2 | 🌐 TypeScript | 📅 2026-05-03 - Persistent team workspaces with inter-agent mailboxes and a shared drive. Claude Code, OpenCode, Pi.
* [corellis](https://github.com/CorellisOrg/corellis) ⭐ 27 | 🐛 4 | 🌐 Shell | 📅 2026-04-13 - Multi-agent governance framework for OpenClaw — goal decomposition, fleet-wide memory, correction propagation, and approval workflows for 20+ agent fleets.
* [orc](https://github.com/spencermarx/orc) ⭐ 23 | 🐛 0 | 🌐 Shell | 📅 2026-06-21 - Lightweight framework that piggybacks your existing CLI setup for planning, task decomposition, worktrees, and review.

## Autonomous Loop Runners

The "keep running until done" pattern — a single goal driven through a retry-until-verified loop.

* [Loop Engineering](https://github.com/cobusgreyling/loop-engineering) ⭐ 10,467 | 🐛 16 | 🌐 JavaScript | 📅 2026-08-19 - Designs repeatable coding-agent loops around automation, worktrees, skills, state, and verification, with starters and a Loop Ready score for Grok, Claude Code, Codex, and OpenCode.
* [ralph-claude-code](https://github.com/frankbria/ralph-claude-code) ⭐ 9,604 | 🐛 33 | 🌐 Shell | 📅 2026-07-18 - Development loop for Claude Code with exit detection that recognizes when the work is actually finished.
* [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) ⭐ 3,101 | 🐛 8 | 🌐 Rust | 📅 2026-08-16 - Hat-based orchestration that keeps agents looping until done, as a fuller implementation of the Ralph Wiggum technique.
* [ralph-tui](https://github.com/subsy/ralph-tui) ⭐ 2,425 | 🐛 49 | 🌐 TypeScript | 📅 2026-05-13 - Drives an agent through a task list autonomously, with a TUI for watching the loop.
* [ralphex](https://github.com/umputun/ralphex) ⭐ 1,438 | 🐛 5 | 🌐 Go | 📅 2026-08-17 - Executes an implementation plan autonomously with a fresh session per task, plus validation, retries, multi-phase review, and automatic commits. Claude Code, Codex.
* [bernstein](https://github.com/sipyourdrink-ltd/bernstein) ⭐ 929 | 🐛 213 | 🌐 Python | 📅 2026-08-19 - Keeps no model in the coordination loop, so orchestration costs zero tokens. Verifies with tests and auto-commits across 40+ CLI agents.
* [fractal](https://github.com/plasma-ai/fractal) ⭐ 693 | 🐛 7 | 🌐 Python | 📅 2026-08-18 - Loops that recursively delegate separable subtasks to child agents, bounded by configurable depth, cost, and time limits.
* [LoopTroop](https://github.com/looptroop-ai/LoopTroop) ⭐ 122 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-18 - An LLM council plans the work, then Ralph-style loops retry failed units with fresh context. Executes via OpenCode worktrees.
* [MartinLoop](https://github.com/Keesan12/martin-loop) ⭐ 44 | 🐛 3 | 🌐 TypeScript | 📅 2026-08-19 - Caps spend, enforces policy, verifies output, and rolls back failures, leaving inspectable run receipts.
* [Dex](https://github.com/francescoalemanno/dex) ⭐ 21 | 🐛 0 | 🌐 Rust | 📅 2026-06-11 - Human-gated planning, multi-reviewer code review, and dead-end-aware research loops, shipped as cross-platform binaries for 7 CLI backends.
* [toryo](https://github.com/JesseRWeigel/toryo) ⭐ 12 | 🐛 3 | 🌐 TypeScript | 📅 2026-05-23 - Trust-based delegation with quality ratcheting that commits improvements and reverts regressions. Chains Claude Code, Aider, Gemini CLI, Ollama.

## Autonomous Task Runners

Unattended agents driven by an external source — an issue queue, a work board, or a schedule — that run and sync state back without side-by-side supervision.

* [OpenHands](https://github.com/OpenHands/OpenHands) ⭐ 84,446 | 🐛 493 | 🌐 TypeScript | 📅 2026-08-19 - Self-hostable control center running its own agent or driving Claude Code, Codex, and any Agent Client Protocol agent, on schedules or webhooks.
* [multica](https://github.com/multica-ai/multica) ⭐ 46,748 | 🐛 1,385 | 🌐 Go | 📅 2026-08-19 - Managed agents platform where you assign tasks, track progress, and let agents compound skills between runs.
* [symphony](https://github.com/openai/symphony) ⭐ 26,749 | 🐛 9 | 🌐 Elixir | 📅 2026-08-12 - Turns project work into isolated autonomous runs, so teams manage the work rather than supervise the agent.
* [open-swe](https://github.com/langchain-ai/open-swe) ⭐ 10,575 | 🐛 27 | 🌐 Python | 📅 2026-08-19 - Invoked from Slack, Linear, or GitHub comments; each task runs in its own cloud sandbox and ends in a draft PR linked to the ticket.
* [claude-code-action](https://github.com/anthropics/claude-code-action) ⭐ 8,663 | 🐛 695 | 🌐 TypeScript | 📅 2026-08-19 - Anthropic's official GitHub Action, detecting from context whether to answer, review, or implement. Auth via Anthropic API, Bedrock, Vertex, or Foundry.
* [gh-aw](https://github.com/github/gh-aw) ⭐ 4,954 | 🐛 387 | 🌐 Go | 📅 2026-08-19 - Compiles agentic workflows written in Markdown into GitHub Actions YAML. Read-only by default, with writes only through sanitized safe-outputs. Copilot, Claude, Codex, Gemini.
* [background-agents](https://github.com/ColeMurray/background-agents) ⭐ 2,664 | 🐛 84 | 🌐 TypeScript | 📅 2026-08-19 - Sessions trigger from a web UI, Slack, GitHub, Linear, webhooks, or cron, run in Modal, Daytona, Vercel, E2B, or OpenComputer sandboxes, and open attributed PRs.
* [run-gemini-cli](https://github.com/google-github-actions/run-gemini-cli) ⭐ 2,054 | 🐛 83 | 🌐 TypeScript | 📅 2026-07-06 - Google's official GitHub Action, running on event or schedule triggers or on demand via `@gemini-cli /review` and `/triage`.
* [codex-action](https://github.com/openai/codex-action) ⭐ 1,195 | 🐛 50 | 🌐 TypeScript | 📅 2026-08-18 - OpenAI's official GitHub Action, running Codex CLI headlessly under drop-sudo, unprivileged-user, or fully read-only sandboxes.
* [centaur](https://github.com/paradigmxyz/centaur) ⭐ 1,149 | 🐛 46 | 🌐 Python | 📅 2026-08-19 - Multiplayer self-hosted agents with Slack-native conversations, Kubernetes sandboxes, shared tools, and durable workflows.
* [cyrus](https://github.com/cyrusagents/cyrus) ⭐ 773 | 🐛 95 | 🌐 TypeScript | 📅 2026-08-14 - Watches Linear, GitHub, GitLab, and Slack issues assigned to it, spinning up an isolated worktree per issue. Claude Code, Codex, Cursor, Gemini.
* [aeon](https://github.com/aeonfun/aeon) ⭐ 673 | 🐛 1 | 🌐 TypeScript | 📅 2026-08-18 - Runs unattended on GitHub Actions; dispatches skills to six coding-agent harnesses behind one contract (Claude Code, Grok, Codex, Pi, Vibe, Kimi), with quality scoring, git-persisted memory, a self-healing loop, and reactive triggers.
* [remote-swe-agents](https://github.com/aws-samples/remote-swe-agents) ⭐ 241 | 🐛 23 | 🌐 TypeScript | 📅 2026-08-04 - Serverless control plane on Lambda with a dedicated EC2 worker per session, triggered by issue comments, assignments, and PR reviews.
* [Contrabass](https://github.com/junhoyeo/contrabass) ⭐ 214 | 🐛 2 | 🌐 Go | 📅 2026-07-17 - Terminal-first orchestrator for issue-driven agent runs, pulling work from Linear, GitHub Issues, or a local board into git worktrees with TUI, headless, and dashboard modes.
* [Factory](https://github.com/owainlewis/factory) ⭐ 188 | 🐛 45 | 🌐 Go | 📅 2026-08-18 - Keeps coding agents working on a repository without making a human orchestrate every step from a terminal, pulling tasks from trusted ticket queues into isolated Codex workspaces.
* [lalph](https://github.com/tim-smart/lalph) ⭐ 130 | 🐛 2 | 🌐 TypeScript | 📅 2026-07-08 - Orchestrator driven by whichever source of issues you point it at.
* [sortie](https://github.com/sortie-ai/sortie) ⭐ 127 | 🐛 52 | 🌐 Go | 📅 2026-08-19 - Turns tracker tickets into agent sessions. Agent-agnostic and tracker-agnostic, as a single Go binary with SQLite persistence.

## Agent Infrastructure & Primitives

Control planes, coordination protocols, harness adapters, and runtimes — the layer beneath your agents rather than the surface you work in.

* [Archon](https://github.com/coleam00/Archon) ⭐ 23,225 | 🐛 281 | 🌐 TypeScript | 📅 2026-08-19 - Harness builder for deterministic AI coding workflows, combining agent steps with scripts, validation gates, approvals, and isolated git worktrees. Claude Code, Codex, and more.
* [NemoClaw](https://github.com/NVIDIA/NemoClaw) ⭐ 22,197 | 🐛 326 | 🌐 TypeScript | 📅 2026-08-19 - Runs Hermes, LangChain Deep Agents, and OpenClaw inside NVIDIA OpenShell with managed inference.
* [openfang](https://github.com/RightNow-AI/openfang) ⭐ 18,121 | 🐛 115 | 🌐 Rust | 📅 2026-07-02 - Open-source agent operating system.
* [omnigent](https://github.com/omnigent-ai/omnigent) ⭐ 9,038 | 🐛 1,071 | 🌐 Python | 📅 2026-08-19 - Meta-harness running Claude Code, Codex, Cursor, OpenCode, Hermes, Pi, or custom YAML agents against swappable sandbox backends, with policy enforcement.
* [Open Multi-Agent](https://github.com/open-multi-agent/open-multi-agent) ⭐ 6,792 | 🐛 11 | 🌐 TypeScript | 📅 2026-08-19 - TypeScript-native runtime where a coordinator turns a goal into a task DAG and a deterministic scheduler runs specialized agents, with approvals, traces, evaluation, checkpoints, and resume support.
* [sandbox-agent](https://github.com/rivet-dev/sandbox-agent) ⭐ 1,539 | 🐛 79 | 🌐 TypeScript | 📅 2026-06-19 - Daemon, HTTP/SSE API, and TypeScript SDK for driving six coding agents inside E2B, Daytona, Modal, Cloudflare Containers, or Docker.
* [Agentlas OS](https://github.com/agentlas-ai/Agentlas-OS) ⭐ 1,158 | 🐛 0 | 🌐 Python | 📅 2026-08-19 - Keeps specialist agents in a hub and spins up a temporary orchestrator per task, with A2A routing and governed memory gates. Formerly Hephaestus.
* [Claudexor](https://github.com/razzant/claudexor) ⭐ 416 | 🐛 45 | 🌐 TypeScript | 📅 2026-08-18 - Routes one coding thread across harnesses with quota-aware rotation between subscription profiles, Best-of-N runs, and cross-family review.
* [guild](https://github.com/mathomhaus/guild) ⭐ 312 | 🐛 21 | 🌐 Go | 📅 2026-08-18 - Shared context, memory, and task coordination as a single Go binary over local SQLite with hybrid keyword and semantic search.
* [handoff](https://github.com/dazuiba/handoff) ⭐ 84 | 🐛 1 | 🌐 Python | 📅 2026-08-02 - Delegates a task to DeepSeek, Codex, or Claude from inside your current Claude Code or Codex session, returning the result automatically.
* [sub-agents-skills](https://github.com/shinpr/sub-agents-skills) ⭐ 79 | 🐛 2 | 🌐 Python | 📅 2026-08-14 - Portable Markdown definitions that route a task to a chosen backend, model, effort level, and permission set.
* [agenttier](https://github.com/agenttier/agenttier) ⭐ 72 | 🐛 18 | 🌐 Go | 📅 2026-08-19 - Kubernetes runtime giving each agent its own Pod and PVC sandbox behind a default-deny NetworkPolicy, with a streaming SSE invoke API.
* [neuralyzer](https://github.com/gintasz/neuralyzer) ⭐ 38 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-07 - Lets an agent wipe its own session context and re-run the first message, making Ralph loops easier to engineer.
* [Crewplane](https://github.com/crewplaneai/crewplane) ⭐ 33 | 🐛 2 | 🌐 Python | 📅 2026-08-18 - CLI-first control plane that turns one-off coding-agent calls into reviewable Markdown workflows spanning Claude Code, Codex, Gemini CLI, or Copilot CLI. Explicit artifact handoffs keep execution inspectable on disk, while validated completed nodes let failed workflows resume instead of starting over.
* [codecast](https://github.com/codecast-sh/codecast) ⭐ 26 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-19 - Watches your real local sessions and surfaces them in a live triage inbox, keeping a searchable record with line-level agent attribution. Claude Code, Codex, Cursor, Gemini.
* [agent-runbook](https://github.com/KnoxOps/agent-runbook) ⭐ 17 | 🐛 0 | 🌐 Python | 📅 2026-07-15 - Compiles YAML runbooks with loops, branching, and parallelism into SKILL.md files for Claude Code and Codex.
* [LionClaw](https://github.com/moshthepitt/lionclaw) ⭐ 14 | 🐛 12 | 🌐 Rust | 📅 2026-08-06 - Local control plane running coding agents as durable, auditable workers with explicit state, skills, and checkpoints.
* [skillfold](https://github.com/byronxlg/skillfold) ⭐ 12 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-03 - Declares skills in YAML and pins exact revisions in a lockfile so installs are reproducible across Claude Code and Codex.

## Personal Assistants

Always-on agents you reach over chat or a desktop app. They remember across sessions, run on their own schedule, and hand work off to tools and other agents — coding agents included, though the work isn't limited to code.

* [openclaw](https://github.com/openclaw/openclaw) ⭐ 386,704 | 🐛 5,761 | 🌐 TypeScript | 📅 2026-08-19 - Your own personal AI assistant, on any OS and any platform.
* [hermes-agent](https://github.com/NousResearch/hermes-agent) ⭐ 232,696 | 🐛 33,373 | 🌐 Python | 📅 2026-08-19 - Self-improving harness with persistent cross-session memory and auto-generated skill documents.
* [nanobot](https://github.com/HKUDS/nanobot) ⭐ 47,162 | 🐛 720 | 🌐 Python | 📅 2026-08-19 - Ultra-lightweight self-hosted assistant in Python with WebUI, tools, memory, MCP, and multi-agent workflows.
* [QwenPaw](https://github.com/agentscope-ai/QwenPaw) ⭐ 34,022 | 🐛 997 | 🌐 Python | 📅 2026-08-19 - Personal assistant that deploys to your own machine or the cloud and plugs into multiple chat apps. Formerly CoPaw.
* [zeroclaw](https://github.com/zeroclaw-labs/zeroclaw) ⭐ 32,613 | 🐛 733 | 🌐 Rust | 📅 2026-08-19 - Fast, small, fully autonomous assistant infrastructure in Rust, deployable anywhere.
* [nanoclaw](https://github.com/nanocoai/nanoclaw) ⭐ 30,546 | 🐛 914 | 🌐 TypeScript | 📅 2026-08-19 - Lightweight OpenClaw alternative running in containers, connecting to WhatsApp, Telegram, Slack, Discord, and Gmail.
* [picoclaw](https://github.com/sipeed/picoclaw) ⭐ 29,877 | 🐛 48 | 🌐 Go | 📅 2026-08-14 - Tiny and fast assistant deployable anywhere.
* [leon](https://github.com/leon-ai/leon) ⭐ 17,442 | 🐛 110 | 🌐 TypeScript | 📅 2026-08-16 - Long-running open-source personal assistant with voice and text interfaces.
* [rowboat](https://github.com/rowboatlabs/rowboat) ⭐ 17,321 | 🐛 155 | 🌐 TypeScript | 📅 2026-08-18 - Open-source AI coworker with memory.
* [ironclaw](https://github.com/nearai/ironclaw) ⭐ 12,604 | 🐛 1,511 | 🌐 Rust | 📅 2026-08-19 - Agent OS in Rust focused on privacy, security, and extensibility.
* [Coworker](https://github.com/accomplish-ai/coworker) ⭐ 10,947 | 🐛 13 | 📅 2026-08-13 - Open source AI coworker that lives on your desktop. Formerly accomplish.
* [Cloudflare OS](https://github.com/cloudflare/cloudflare-os) ⭐ 8,576 | 🐛 82 | 🌐 TypeScript | 📅 2026-08-19 - Self-hostable "company OS" on Cloudflare Workers: a chat UI where agents preloaded with your company context do tasks, build sandboxed apps, and stay inside a Gatekeepers guardrail framework.
* [nullclaw](https://github.com/nullclaw/nullclaw) ⭐ 8,031 | 🐛 86 | 🌐 Zig | 📅 2026-07-19 - Fully autonomous assistant infrastructure written in Zig.
* [lobsterai](https://github.com/netease-youdao/LobsterAI) ⭐ 5,920 | 🐛 686 | 🌐 TypeScript | 📅 2026-08-18 - Desktop-grade agent for data analysis, slides, docs, and web research.
* [MetaClaw](https://github.com/aiming-lab/MetaClaw) ⭐ 3,485 | 🐛 17 | 🌐 Python | 📅 2026-06-07 - Assistant that learns and evolves from conversation alone.
* [zclaw](https://github.com/tnm/zclaw) ⭐ 2,218 | 🐛 12 | 🌐 C | 📅 2026-05-17 - Complete personal assistant in 888 KiB, running on an ESP32 with GPIO, cron, and custom tools.
* [denchclaw](https://github.com/DenchHQ/DenchClaw) ⭐ 1,643 | 🐛 96 | 🌐 TypeScript | 📅 2026-06-11 - Managed OpenClaw framework aimed at CRM, sales automation, and outreach.
* [Ouroboros](https://github.com/razzant/ouroboros) ⭐ 1,187 | 🐛 95 | 🌐 Python | 📅 2026-08-19 - General-purpose agent with durable identity and memory, reviewed self-modification, multi-agent coordination, and desktop and headless interfaces.
* [rho](https://github.com/mikeyobrien/rho) ⭐ 369 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-26 - Stays running, remembers across sessions, and checks in on its own. macOS, Linux, Android.
* [iva](https://github.com/smixs/iva) ⭐ 174 | 🐛 6 | 🌐 TypeScript | 📅 2026-08-19 - Telegram assistant that turns your messages, voice notes and photos into an Obsidian-compatible markdown vault it remembers across sessions. Crons, skills, MCP and Google Workspace from an in-chat menu. Self-hosted in one command, MIT.
* [lemon](https://github.com/z80dev/lemon) ⭐ 129 | 🐛 1 | 🌐 Elixir | 📅 2026-08-19 - Local-first assistant and coding agent runtime.
* [automata](https://github.com/sentientwave/automata) ⭐ 111 | 🐛 0 | 🌐 Elixir | 📅 2026-05-05 - Matrix-native workspace where Temporal-backed durable workflows survive restarts and keep long tasks moving.
* [assistant](https://github.com/kcosr/assistant) ⭐ 90 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-03 - Panel-based assistant whose plugins share one workspace of notes, lists, and objects.
* [ghostclaw](https://github.com/b1rdmania/ghostclaw) ⭐ 90 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-03 - An AI that lives on your computer and does things for you.
* [Hivekeep](https://github.com/MarlBurroW/hivekeep) ⭐ 45 | 🐛 25 | 🌐 TypeScript | 📅 2026-08-18 - Self-hosted team of specialized agents with persistent memory that delegate and build their own tools and mini-apps. Telegram, Slack, Discord, Matrix. Single container, MIT.
* [lucinate](https://github.com/lucinate-ai/lucinate) ⭐ 11 | 🐛 18 | 🌐 Go | 📅 2026-08-16 - Terminal-native chat client for OpenClaw, Hermes, Ollama, and OpenAI-compatible providers, with cron management and session browsing.

## Resting

A watchlist of projects without a push in the last few months (checked 2026-07-28). They stay here until they're active again, then move back up.

* [vibe-kanban](https://github.com/BloopAI/vibe-kanban) ⭐ 27,846 | 🐛 534 | 🌐 Rust | 📅 2026-04-24 - Kanban board for managing AI coding agents. *(last commit 2026-04)*
* [1code](https://github.com/21st-dev/1code) ⚠️ Archived - Orchestration layer for Claude Code and Codex. *(last commit 2026-03; archived)*
* [CodexMonitor](https://github.com/Dimillian/CodexMonitor) ⭐ 4,239 | 🐛 93 | 🌐 TypeScript | 📅 2026-03-26 - Orchestrate multiple Codex agents across local workspaces. *(last commit 2026-03)*
* [ralphy](https://github.com/michaelshimeles/ralphy) ⭐ 2,957 | 🐛 43 | 🌐 TypeScript | 📅 2026-02-05 - Bash script that loops Claude Code, Codex, OpenCode, Cursor, Qwen, or Droid until the task is done. *(last commit 2026-02)*
* [antfarm](https://github.com/snarktank/antfarm) ⭐ 2,496 | 🐛 117 | 🌐 TypeScript | 📅 2026-02-26 - Build your agent team in OpenClaw with one command. *(last commit 2026-02)*
* [cashclaw](https://github.com/moltlaunch/cashclaw) ⭐ 1,095 | 🐛 54 | 🌐 TypeScript | 📅 2026-03-14 - An autonomous agent that takes work, does work, gets paid, and gets better at it. *(last commit 2026-03)*
* [clawe](https://github.com/getclawe/clawe) ⭐ 747 | 🐛 6 | 🌐 TypeScript | 📅 2026-02-23 - Multi-agent coordination system: think Trello for OpenClaw agents. *(last commit 2026-02)*
* [opengoat](https://github.com/marian2js/opengoat) ⭐ 393 | 🐛 6 | 🌐 TypeScript | 📅 2026-04-12 - Build organizations of OpenClaw agents coordinating across Codex, Claude Code, Cursor, and OpenCode. *(last commit 2026-04)*
* [subtask](https://github.com/zippoxer/subtask) ⭐ 339 | 🐛 5 | 🌐 Go | 📅 2026-04-27 - Claude Skill that runs your tasks through subagents in git worktrees. *(last commit 2026-04)*
* [lettabot](https://github.com/letta-ai/lettabot) ⚠️ Archived - Personal assistant that remembers everything. *(last commit 2026-05; archived, replaced by Letta Code)*
* [mercury](https://github.com/Michaelliv/mercury) ⚠️ Archived - Personal AI assistant that lives where you chat. *(last commit 2026-03; archived)*
* [babyagi3](https://github.com/yoheinakajima/babyagi3) ⭐ 129 | 🐛 2 | 🌐 Python | 📅 2026-03-07 - A minimal AI agent you configure once, then run through natural language. *(last commit 2026-03)*
* [wreckit](https://github.com/mikehostetler/wreckit) ⭐ 129 | 🐛 18 | 🌐 Elixir | 📅 2026-04-14 - Run the Ralph Wiggum loop over your roadmap. *(last commit 2026-04)*
* [gnap](https://github.com/farol-team/gnap) ⭐ 81 | 🐛 2 | 📅 2026-03-17 - Git-native agent protocol coordinating agents through a shared repo as a task board, with no orchestrator process. *(last commit 2026-03)*
* [swarm-protocol](https://github.com/phuryn/swarm-protocol) ⭐ 53 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-15 - Headless coordination over MCP: claim work, detect file conflicts, heartbeat, and hand off across sessions. *(last commit 2026-03)*
* [wit](https://github.com/amaar-mc/wit) ⭐ 46 | 🐛 10 | 🌐 TypeScript | 📅 2026-03-27 - Locks individual functions rather than files via Tree-sitter, warning agents of conflicts before they write. *(last commit 2026-03)*
* [ariana](https://github.com/ariana-dot-dev/ariana) - The IDE of the future. *(last commit 2026-03)*

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-19._

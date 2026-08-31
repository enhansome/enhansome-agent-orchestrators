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

* [herdr](https://github.com/herdrdev/herdr) ⭐ 33,906 | 🐛 272 | 🌐 Rust | 📅 2026-08-31 - Background runtime that owns your agents' terminals: sessions survive reboot and reattach from any terminal or SSH, panes are marked working/blocked/idle, and agents themselves spawn panes and prompt each other over a CLI and socket API. One Rust binary.
* [cmux](https://github.com/manaflow-ai/cmux) ⭐ 26,620 | 🐛 4,659 | 🌐 Swift | 📅 2026-08-31 - Ghostty-based macOS terminal with vertical tabs and per-agent notifications, built for keeping many concurrent sessions legible.
* [claude-squad](https://github.com/smtg-ai/claude-squad) ⭐ 8,401 | 🐛 56 | 🌐 Go | 📅 2026-08-20 - Runs each agent as a detached background session with its own worktree, so work continues after you close the pane. Claude Code, Codex, OpenCode, Amp.
* [agent-of-empires](https://github.com/agent-of-empires/agent-of-empires) ⭐ 3,165 | 🐛 134 | 🌐 Rust | 📅 2026-08-31 - Pairs a TUI with a matching web view, so the same sessions stay reachable from a phone. Claude Code, Codex, OpenCode, Gemini, Mistral Vibe.
* [dmux](https://github.com/standardagents/dmux) ⭐ 1,759 | 🐛 32 | 🌐 HTML | 📅 2026-08-16 - Dev agent multiplexer pairing coding agents with git worktrees over tmux.
* [agent-deck](https://github.com/asheshgoplani/agent-deck) ⭐ 818 | 🐛 45 | 🌐 Go | 📅 2026-08-24 - One TUI covering sessions across Claude Code, Codex, Gemini, and OpenCode, with live status and resume for each.
* [agterm](https://github.com/umputun/agterm) ⭐ 549 | 🐛 9 | 🌐 Swift | 📅 2026-08-31 - Native macOS terminal with named workspaces, a live dashboard, attention states, and a scriptable control API.
* [tmux-ide](https://github.com/wavyrai/tmux-ide) ⭐ 540 | 🐛 9 | 🌐 TypeScript | 📅 2026-08-31 - Turns any project into a tmux IDE from a checked-in `ide.yml`, including preset agent-team layouts.
* [agentbox](https://github.com/madarco/agentbox) ⭐ 380 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-31 - Gives each agent its own sandboxed VM — local Docker or cloud via Hetzner, Daytona, Vercel, or E2B — with sub-second checkpoint starts.
* [agent-manager](https://github.com/YoanWai/agent-manager) ⭐ 378 | 🐛 16 | 🌐 Go | 📅 2026-08-30 - tmux TUI with live status, a prompt that lands in the pane without attaching, and in-terminal diff review that sends line comments back to the agent. Claude Code, Codex, OpenCode, Grok, Gemini CLI, Pi, Hermes.
* [amux](https://github.com/andyrewlee/amux) ⭐ 154 | 🐛 6 | 🌐 Go | 📅 2026-08-27 - Minimal TUI for spawning parallel coding agents in git worktrees.
* [openkanban](https://github.com/TechDufus/openkanban) ⭐ 142 | 🐛 6 | 🌐 Go | 📅 2026-06-12 - Kanban board for orchestrating coding agents, rendered entirely in the terminal.
* [thurbox](https://github.com/Thurbeen/thurbox) ⭐ 57 | 🐛 2 | 🌐 Rust | 📅 2026-08-30 - TUI orchestrator with remote SSH sessions, inter-session messaging, and a native code-review view. Works with any CLI agent you define.
* [repomon](https://github.com/AliHamzaAzam/repomon) ⭐ 17 | 🐛 3 | 🌐 Rust | 📅 2026-08-29 - Rust TUI that supervises a fleet across many repositories at once, in durable tmux sessions you can approve from your phone.
* [agent-console](https://github.com/buhuipao/agent-console) ⭐ 16 | 🐛 0 | 🌐 Rust | 📅 2026-08-31 - Rust TUI that finds Codex and Claude Code sessions from the providers' own transcripts, including ones started elsewhere, and resumes their native UI rather than replacing it. No tmux or worktrees.

## Parallel Coding Agents — Desktop & Web

The same parallel-sessions workflow as a desktop app or browser/mobile dashboard, with diff review and merge.

* [Orca](https://github.com/stablyai/orca) ⭐ 57,997 | 🐛 4,885 | 🌐 TypeScript | 📅 2026-08-31 - Agentic development environment for running a fleet on your own subscription, available on desktop and mobile.
* [t3code](https://github.com/pingdotgg/t3code) ⭐ 21,134 | 🐛 1,418 | 🌐 TypeScript | 📅 2026-08-31 - Harness control surface available as web, mobile, and desktop app. Claude Code, Codex, Cursor, Grok Build, OpenCode.
* [Paseo](https://github.com/getpaseo/paseo) ⭐ 15,604 | 🐛 1,171 | 🌐 TypeScript | 📅 2026-08-31 - Self-hosted daemon running agents in parallel on your own machines, driven from desktop, iOS/Android, web, or CLI, with voice control, diff review, and no telemetry or forced log-ins. Claude Code, Codex, Copilot, OpenCode, Pi.
* [Aperant](https://github.com/AndyMik90/Aperant) ⭐ 14,546 | 🐛 63 | 🌐 TypeScript | 📅 2026-06-14 - Runs up to 12 agent terminals with a self-validating QA loop and automatic conflict resolution when merging back to main.
* [qm](https://github.com/yc-software/qm) ⭐ 14,387 | 🐛 362 | 🌐 TypeScript | 📅 2026-08-30 - Multiplayer harness where each teammate gets an isolated workspace to run agents independently, driven from Slack or the web.
* [superset](https://github.com/superset-sh/superset) ⭐ 13,561 | 🐛 584 | 🌐 TypeScript | 📅 2026-08-31 - Code editor built around running many agents on your machine at once.
* [humanlayer](https://github.com/humanlayer/humanlayer) ⭐ 11,355 | 🐛 72 | 🌐 TypeScript | 📅 2026-06-19 - Human-in-the-loop control for coding agents on hard problems; the repo notes its code is now largely deprecated in favor of a rebuild.
* [agent-orchestrator](https://github.com/Untrivial-ai/agent-orchestrator) ⭐ 10,757 | 🐛 858 | 🌐 Go | 📅 2026-08-31 - Agent IDE for fleets that plans the work, spawns the agents, then fixes CI failures and merge conflicts without being asked.
* [OpenChamber](https://github.com/openchamber/openchamber) ⭐ 9,411 | 🐛 651 | 🌐 TypeScript | 📅 2026-08-30 - Open-source workspace for running, supervising, and reviewing AI coding work across desktop, browser, editor, and mobile, with parallel model runs and per-run worktrees.
* [Emdash](https://github.com/generalaction/emdash) ⭐ 5,553 | 🐛 209 | 🌐 TypeScript | 📅 2026-08-31 - Agentic development environment running parallel agents against any model provider.
* [automaker](https://github.com/AutoMaker-Org/automaker) ⭐ 3,212 | 🐛 11 | 🌐 TypeScript | 📅 2026-05-22 - Describe features on a Kanban board and agents implement them in isolated worktrees, running tests and committing as they go.
* [collaborator](https://github.com/collabs-inc/collab-public) ⭐ 2,933 | 🐛 81 | 🌐 TypeScript | 📅 2026-08-08 - Arranges terminals, editors, and files as tiles on an infinite pan-and-zoom canvas instead of tabs.
* [bb](https://github.com/get-bb/bb) ⭐ 2,775 | 🐛 365 | 🌐 TypeScript | 📅 2026-08-31 - Self-controlling agentic IDE that orchestrates multiple coding agents in live threads you can follow, steer, or hand off, driven from a desktop app, web app, CLI, or HTTP API.
* [CodeNomad](https://github.com/NeuralNomadsAI/CodeNomad) ⭐ 2,530 | 🐛 28 | 🌐 TypeScript | 📅 2026-08-31 - Desktop and web workspace around the OpenCode CLI whose SideCars embed local tools like VS Code and terminals as tabs.
* [supacode](https://github.com/supabitapp/supacode) ⭐ 2,321 | 🐛 56 | 🌐 Swift | 📅 2026-08-26 - Native macOS command center for worktree-per-agent development.
* [mux](https://github.com/coder/mux) ⭐ 1,998 | 🐛 238 | 🌐 TypeScript | 📅 2026-08-31 - Desktop app for isolated, parallel agentic development.
* [synara](https://github.com/Emanuele-web04/synara) ⭐ 1,627 | 🐛 200 | 🌐 TypeScript | 📅 2026-08-31 - GUI desktop workspace for running and managing agents across local projects.
* [nimbalyst](https://github.com/nimbalyst/nimbalyst) ⭐ 1,615 | 🐛 592 | 🌐 TypeScript | 📅 2026-08-28 - Visual workspace pairing parallel worktree sessions with kanban and direct visual editing. Claude Code, Codex, OpenCode.
* [Traycer](https://github.com/traycerai/traycer) ⭐ 1,367 | 🐛 186 | 🌐 TypeScript | 📅 2026-08-31 - Bring-your-own-agent workspace running many sessions in parallel with context shared across models and providers, plus agent-to-agent messaging, shareable boards, and cross-device sync.
* [Waku](https://github.com/egoist/waku) ⭐ 1,297 | 🐛 132 | 🌐 Rust | 📅 2026-08-31 - Native macOS desktop app for working with local coding agents, keeping projects, sessions, and transcripts on your machine. Supports Amp, Claude Code, Codex CLI, Cursor CLI, Grok Build, OpenCode, and Pi.
* [jean](https://github.com/coollabsio/jean) ⭐ 1,242 | 🐛 139 | 🌐 TypeScript | 📅 2026-08-25 - Desktop and web app for orchestrating agents across multiple projects and their git worktrees. Claude, Codex, OpenCode.
* [Comet](https://github.com/zeronsh/comet) ⭐ 1,146 | 🐛 64 | 🌐 Rust | 📅 2026-08-25 - Cross-device control plane for coding agents, syncing sessions across machines and keeping agents running on an always-on daemon. Claude Code, Codex, Cursor, Grok, Hermes, Pi.
* [takopi](https://github.com/banteg/takopi) ⭐ 1,048 | 🐛 46 | 🌐 Python | 📅 2026-05-25 - Telegram bridge that puts Codex, Claude Code, OpenCode, and Pi sessions in a chat thread.
* [parallel-code](https://github.com/johannesjo/parallel-code) ⭐ 997 | 🐛 49 | 🌐 TypeScript | 📅 2026-08-29 - Desktop app running Claude Code, Codex, and Gemini CLI side by side in isolated worktrees, with a built-in diff viewer and one-click merge.
* [IM.codes](https://github.com/im4codes/imcodes) ⭐ 973 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-31 - Mobile and web control layer built for away-from-desk continuation, with terminal access, git views, localhost preview, and scheduled tasks. Claude Code, Codex, Gemini CLI.
* [Berd](https://github.com/block/berd) ⭐ 836 | 🐛 84 | 🌐 TypeScript | 📅 2026-08-30 - Block's open-source desktop app for working with AI agents: project chats with per-folder worktree behavior over the Goose backend, with agents, skills, connections, and agent sharing in one place.
* [ai-maestro](https://github.com/23blocks-OS/ai-maestro) ⭐ 760 | 🐛 13 | 🌐 TypeScript | 📅 2026-08-29 - Dashboard spanning multiple machines, adding memory search, code-graph queries, and agent-to-agent messaging. Claude, Aider, Cursor.
* [kandev](https://github.com/kdlbs/kandev) ⭐ 713 | 🐛 83 | 🌐 Go | 📅 2026-08-31 - Kanban workbench whose multi-step workflows assign a different agent per step behind human gates, running locally, in Docker, over SSH, or in cloud executors.
* [omg.dev](https://github.com/BennyKok/omg.dev) ⭐ 506 | 🐛 5 | 🌐 TypeScript | 📅 2026-08-31 - Open-source parallel-agent harness: run coding agents on your own computer or a hosted one, controlled from a single web UI with a mobile client. Claude Code, Codex, Grok, Cursor, OpenCode, Copilot, Pi.
* [Alethe](https://github.com/Kc1t/alethe-agents) ⭐ 499 | 🐛 58 | 🌐 TypeScript | 📅 2026-08-31 - Local-first desktop workspace where agents and shells run as real PTYs in split panes and custom grids across projects, surviving pane close and app restart. Suspend idle groups to reclaim memory and resume with scrollback intact. Claude Code, Codex, OpenCode.
* [Proliferate](https://github.com/proliferate-ai/proliferate) ⭐ 447 | 🐛 99 | 🌐 TypeScript | 📅 2026-08-31 - Agent IDE that runs sessions locally or in the cloud and lets you build reusable workflows from them.
* [dorothy](https://github.com/Charlie85270/Dorothy) ⭐ 341 | 🐛 10 | 🌐 TypeScript | 📅 2026-07-07 - Desktop app combining agent orchestration with automations, Kanban management, and MCP servers.
* [Open Session](https://github.com/tellahq/opensession) ⭐ 333 | 🐛 18 | 🌐 TypeScript | 📅 2026-08-31 - Self-hosted server driving coding sessions in git worktrees on your own box or in isolated sandboxes, with a web UI, Slack/Linear/Plain/GitHub intake, diff and PR review, and multiple Codex and Claude subscriptions.
* [aizen](https://github.com/vivy-company/aizen) ⭐ 302 | 🐛 3 | 🌐 Swift | 📅 2026-08-01 - macOS workspace that organizes worktrees, environments, and agent sessions per project.
* [diri](https://github.com/cristicretu/diri) ⭐ 277 | 🐛 23 | 🌐 Rust | 📅 2026-08-31 - Native macOS app running Claude Code, Codex, Cursor, Gemini, and shells in parallel across git worktrees or remote hosts, with live status, session persistence across restarts, a menu-bar rollup, and an MCP server for agents to spawn others.
* [vibe-tree](https://github.com/sahithvibudhi/vibe-tree) ⭐ 267 | 🐛 12 | 🌐 TypeScript | 📅 2026-07-25 - One git worktree per agent, delivered as desktop, web, and CLI.
* [constellagent](https://github.com/owengretzinger/constellagent) ⭐ 214 | 🐛 6 | 🌐 TypeScript | 📅 2026-05-05 - macOS app giving each agent its own terminal, editor, and git worktree in a single window.
* [ivy-tendril](https://github.com/Ivy-Interactive/Ivy-Tendril) ⭐ 174 | 🐛 142 | 🌐 C# | 📅 2026-08-31 - Drives agents through a plan-based lifecycle with verification gates, self-improving memory, and human checkpoints. Claude Code, Codex, Antigravity, Copilot, OpenCode.
* [Tempest](https://github.com/tempestai-dev/tempest) ⭐ 162 | 🐛 11 | 🌐 TypeScript | 📅 2026-08-30 - Tauri desktop ADE running CLI agents in parallel isolated worktrees, with a shared local code-knowledge graph that cuts token use across sessions, plus live status and built-in diff/PR review.
* [Ouijit](https://github.com/ouijit/ouijit) ⭐ 161 | 🐛 3 | 🌐 TypeScript | 📅 2026-08-28 - Kanban board and terminals wired together by lifecycle hooks, scripts, and a session-aware CLI, so a task runs by hand, on a script, or delegated to the agent. Per-task worktrees, optional VM sandboxing. Claude Code, Codex, Pi, OpenCode.
* [clideck](https://github.com/rustykuntz/clideck) ⭐ 153 | 🐛 3 | 🌐 JavaScript | 📅 2026-08-19 - Chat-app-style dashboard with autopilot routing between agents and full control from a phone. Claude Code, Codex, Gemini CLI, OpenCode.
* [Claude Command Center (CCC)](https://github.com/amirfish1/claude-command-center) ⭐ 132 | 🐛 14 | 🌐 Python | 📅 2026-08-31 - Local dashboard for spawning, monitoring, and resuming sessions across Claude Code, Codex, Cursor, Antigravity, and Kilo Code.
* [tlbx](https://github.com/tlbx-ai/tlbx) ⭐ 105 | 🐛 12 | 🌐 C# | 📅 2026-08-31 - Self-hosted browser workspace holding persistent real PTY sessions on your own machines, reachable from any browser or phone.
* [Garcon](https://github.com/cfal/garcon) ⭐ 65 | 🐛 41 | 🌐 TypeScript | 📅 2026-08-31 - Self-hosted browser and mobile workspace with diff review, Git/PR workflows, mobile approvals, scheduling, and cross-agent transfers. Seven CLI agents.
* [GraphCode](https://github.com/scgopi/GraphCode) ⭐ 57 | 🐛 7 | 🌐 Swift | 📅 2026-08-31 - macOS app that wires agent sessions into a graph: each node is a live terminal you can attach to mid-run, each edge a hand-off, message, or spawn that fires while you're away. Claude Code, Copilot CLI, Codex.
* [clave](https://github.com/codika-io/clave) ⭐ 47 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-31 - Native macOS app with split and grid layouts, session groups, SSH remote sessions, and usage analytics for Claude Code.
* [Tortie](https://github.com/gregce/tortie) ⭐ 41 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-31 - Native macOS agent multiplexer with familiar IDE features: all projects in one window, agents that survive restarts, and organized terminal sessions without tmux.
* [vibecraft](https://github.com/rayzhudev/vibecraft) ⭐ 35 | 🐛 2 | 🌐 TypeScript | 📅 2026-07-19 - RTS-style workspace for commanding coding agents.
* [intentic](https://github.com/intentic/intentic) ⭐ 30 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-31 - Browser and mobile workspace where every agent gets a persistent Docker sandbox on a machine you own plus a git worktree of its own, reached over an outbound-only Cloudflare tunnel, so runs keep going after you close the tab. Plan mode, per-hunk diff review, an environment Dockerfile the agent proposes and you approve, credential capabilities injected per turn, and schedule, webhook or event triggers. Claude Code, Codex, Grok, Kimi Code, Gemini. MIT.
* [AGX](https://github.com/ramarlina/agx) ⭐ 27 | 🐛 1 | 🌐 TypeScript | 📅 2026-05-06 - Wake-work-sleep checkpointing keeps a persistent agent team on long objectives, with human gates between cycles.
* [Fletch](https://github.com/fwdai/fletch) ⭐ 24 | 🐛 1 | 🌐 Rust | 📅 2026-08-26 - Native macOS IDE that seals each agent in its own repo clone under Seatbelt or Docker, serves each a shared symbol and call-graph index over MCP, and gates every step on tests or your approval. Claude Code, Codex, Cursor, OpenCode.
* [octomux](https://github.com/ShreyPaharia/octomux) ⭐ 22 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-27 - Local dashboard with a kanban fleet view, one unified permission inbox across agents, and in-app diff review.
* [agent-squid](https://github.com/agent-squid/squid) ⭐ 15 | 🐛 0 | 🌐 JavaScript | 📅 2026-08-28 - Browser UI organized into named lanes (`#topic@agent`), with context shared across agents and a realtime quota gauge.
* [Zaivern Code](https://github.com/tacyan/zaivern-code) ⭐ 8 | 🐛 0 | 🌐 Rust | 📅 2026-08-31 - Cross-platform Rust desktop cockpit for running Claude Code, Codex, Gemini CLI, and 30+ coding agents in parallel, with fleet monitoring, mobile control, and line-level ownership to prevent merge conflicts.
* [Better Agent](https://github.com/ofekron/better-agent) - Local web workspace with persistent state, approvals, and restart recovery for native Claude, Codex, and Gemini sessions.
* [jat](https://github.com/joewinke/jat) - Visual dashboard combining live sessions, task management, code editor, and terminal, with parallel swarm workflows.

## Multi-Agent Swarms

Systems where multiple specialized agents actively coordinate, communicate, and delegate toward a shared goal.

* [paperclip](https://github.com/paperclipai/paperclip) ⭐ 79,738 | 🐛 5,423 | 🌐 TypeScript | 📅 2026-08-31 - Self-hosted platform where agents wake on heartbeats to claim tickets, governed by org charts, budgets, and approval gates.
* [ruflo](https://github.com/ruvnet/ruflo) ⭐ 69,929 | 🐛 877 | 🌐 TypeScript | 📅 2026-08-31 - Meta-harness for deploying coordinated swarms and conversational multi-agent workflows. Formerly claude-flow.
* [buzz](https://github.com/block/buzz) ⭐ 31,611 | 🐛 3,279 | 🌐 Rust | 📅 2026-08-31 - Agents are first-class members of shared channels on a Nostr relay you own, with their own keys and audit trails. Claude Code, Codex, Goose.
* [gastown](https://github.com/gastownhall/gastown) ⭐ 17,866 | 🐛 442 | 🌐 Go | 📅 2026-08-19 - Scales to 20-30 agents with a coordinator, git-backed issue tracking, health watchdogs, and a Bors-style merge queue.
* [ClawTeam](https://github.com/HKUDS/ClawTeam) ⭐ 5,518 | 🐛 36 | 🌐 Python | 📅 2026-05-09 - Agents spawn and manage their own teammates from one command, coordinating through file-based or P2P inboxes across tmux worktrees.
* [claude\_codex\_bridge](https://github.com/SeemSeam/claude_codex_bridge) ⭐ 3,462 | 🐛 100 | 🌐 Python | 📅 2026-08-31 - Workspace for mixing different vendors' CLI agents in one visible collaboration session.
* [agentsmesh](https://github.com/AgentsMesh/AgentsMesh) ⭐ 2,333 | 🐛 20 | 🌐 Go | 📅 2026-08-03 - Remote AI workstations with PTY sandboxes and worktree isolation, coordinating across channels and pod bindings. Claude Code, Codex, Gemini CLI, Aider, OpenCode.
* [Agent Teams](https://github.com/777genius/agent-teams-ai) ⭐ 2,004 | 🐛 24 | 🌐 TypeScript | 📅 2026-08-31 - Desktop app where you give high-level commands to autonomous coding-agent teams across Claude Code, Codex, OpenCode, Cursor, Grok, GitHub Copilot, Kiro, Z.AI, MiniMax, Kimi, 200+ models, and 75+ LLM providers. Agents coordinate through inter-agent messaging, Kanban tasks, and built-in code review.
* [scion](https://github.com/GoogleCloudPlatform/scion) ⭐ 1,684 | 🐛 55 | 🌐 Go | 📅 2026-08-31 - Orchestration testbed running agents in parallel isolated containers with dynamic coordination and normalized telemetry.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 1,575 | 🐛 12 | 🌐 TypeScript | 📅 2026-08-31 - A commander agent decomposes goals and dispatches specialists with isolated skills and memory. Claude Code, Codex, OpenCode, Cline.
* [multi-agent-shogun](https://github.com/yohey-w/multi-agent-shogun) ⭐ 1,419 | 🐛 7 | 🌐 Shell | 📅 2026-08-06 - Shogun to karo to ashigaru hierarchy running up to 10 agents over tmux with no coordination API cost.
* [Fusion](https://github.com/Runfusion/Fusion) ⭐ 1,176 | 🐛 96 | 🌐 TypeScript | 📅 2026-08-31 - Multi-node orchestrator with a kanban board, plan-review-execute gates, per-task worktrees, and hierarchical missions.
* [loki-mode](https://github.com/asklokesh/loki-mode) ⭐ 1,052 | 🐛 9 | 🌐 Shell | 📅 2026-08-31 - PRD-to-deployed-product SDLC with 41 agents in 8 swarms, nine quality gates, and blind three-reviewer code review. Source-available under BUSL-1.1.
* [hcom](https://github.com/aannoo/hcom) ⭐ 469 | 🐛 34 | 🌐 Rust | 📅 2026-08-09 - Lets agents message, watch, and spawn each other across terminals. Claude Code, Codex, Antigravity, Cursor, OpenCode, Kilo, and more.
* [agent-kanban](https://github.com/saltbo/agent-kanban) ⭐ 459 | 🐛 23 | 🌐 TypeScript | 📅 2026-08-31 - Leader-worker task board with cryptographic agent identity. Claude Code, Codex, Gemini CLI.
* [NXTG-Forge Orchestrator](https://github.com/nxtg-ai/forge-orchestrator) ⭐ 158 | 🐛 6 | 🌐 Rust | 📅 2026-08-20 - Coordinates Claude Code, Codex, and Gemini CLI on one shared repo through a research-plan-delegate-adversarial-verify-deploy pipeline, with file locking, knowledge capture, and drift detection. Single Rust binary.
* [ORCH](https://github.com/oxgeneral/ORCH) ⭐ 155 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-01 - CLI runtime managing agents as typed teams with an explicit state machine and goals. Claude Code, Codex, Cursor.
* [kodo](https://github.com/ikamensh/kodo) ⭐ 130 | 🐛 2 | 🌐 Python | 📅 2026-07-18 - Directs agents through work cycles where a separate agent independently verifies each result. Claude Code, Codex, Gemini CLI.
* [tutti](https://github.com/nutthouse/tutti) ⭐ 116 | 🐛 19 | 🌐 Rust | 📅 2026-07-28 - Config-driven workflows passing typed artifacts between agents, each in its own worktree.
* [CompanyHelm](https://github.com/CompanyHelm/companyhelm) ⭐ 74 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-28 - Distributed orchestrator with task management and direct agent-to-agent conversations.
* [5dive](https://github.com/5dive-ai/5dive) ⭐ 54 | 🐛 9 | 🌐 Shell | 📅 2026-08-31 - Named agents on a shared org chart and backlog hand work to each other and escalate to a human over Telegram. Claude Code, Codex, Grok, Antigravity, OpenCode.
* [Agon](https://github.com/AutoResearch-Factory/Agon) ⭐ 44 | 🐛 1 | 🌐 Python | 📅 2026-08-24 - Orchestrates scientist, coder, and auditor loops from research topic through proposal to experiment.
* [shire](https://github.com/victor36max/shire) ⭐ 39 | 🐛 2 | 🌐 TypeScript | 📅 2026-05-03 - Persistent team workspaces with inter-agent mailboxes and a shared drive. Claude Code, OpenCode, Pi.
* [corellis](https://github.com/CorellisOrg/corellis) ⭐ 28 | 🐛 4 | 🌐 Shell | 📅 2026-04-13 - Multi-agent governance framework for OpenClaw — goal decomposition, fleet-wide memory, correction propagation, and approval workflows for 20+ agent fleets.
* [orc](https://github.com/spencermarx/orc) ⭐ 23 | 🐛 0 | 🌐 Shell | 📅 2026-06-21 - Lightweight framework that piggybacks your existing CLI setup for planning, task decomposition, worktrees, and review.

## Autonomous Loop Runners

The "keep running until done" pattern — a single goal driven through a retry-until-verified loop.

* [Loop Engineering](https://github.com/cobusgreyling/loop-engineering) ⭐ 10,766 | 🐛 11 | 🌐 TypeScript | 📅 2026-08-31 - Designs repeatable coding-agent loops around automation, worktrees, skills, state, and verification, with starters and a Loop Ready score for Grok, Claude Code, Codex, and OpenCode.
* [ralph-claude-code](https://github.com/frankbria/ralph-claude-code) ⭐ 9,611 | 🐛 35 | 🌐 Shell | 📅 2026-07-18 - Development loop for Claude Code with exit detection that recognizes when the work is actually finished.
* [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) ⭐ 3,117 | 🐛 1 | 🌐 Rust | 📅 2026-08-29 - Hat-based orchestration that keeps agents looping until done, as a fuller implementation of the Ralph Wiggum technique.
* [ralph-tui](https://github.com/subsy/ralph-tui) ⭐ 2,433 | 🐛 37 | 🌐 TypeScript | 📅 2026-08-28 - Drives an agent through a task list autonomously, with a TUI for watching the loop.
* [ralphex](https://github.com/umputun/ralphex) ⭐ 1,464 | 🐛 7 | 🌐 Go | 📅 2026-08-28 - Executes an implementation plan autonomously with a fresh session per task, plus validation, retries, multi-phase review, and automatic commits. Claude Code, Codex.
* [bernstein](https://github.com/sipyourdrink-ltd/bernstein) ⭐ 1,038 | 🐛 137 | 🌐 Python | 📅 2026-08-31 - Keeps no model in the coordination loop, so orchestration costs zero tokens. Verifies with tests and auto-commits across 40+ CLI agents.
* [fractal](https://github.com/plasma-ai/fractal) ⭐ 705 | 🐛 3 | 🌐 Python | 📅 2026-08-29 - Loops that recursively delegate separable subtasks to child agents, bounded by configurable depth, cost, and time limits.
* [LoopTroop](https://github.com/looptroop-ai/LoopTroop) ⭐ 129 | 🐛 3 | 🌐 TypeScript | 📅 2026-08-31 - An LLM council plans the work, then Ralph-style loops retry failed units with fresh context. Executes via OpenCode worktrees.
* [MartinLoop](https://github.com/Keesan12/martin-loop) ⭐ 47 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-31 - Caps spend, enforces policy, verifies output, and rolls back failures, leaving inspectable run receipts.
* [Dex](https://github.com/francescoalemanno/dex) ⭐ 21 | 🐛 0 | 🌐 Rust | 📅 2026-06-11 - Human-gated planning, multi-reviewer code review, and dead-end-aware research loops, shipped as cross-platform binaries for 7 CLI backends.
* [toryo](https://github.com/JesseRWeigel/toryo) ⭐ 12 | 🐛 3 | 🌐 TypeScript | 📅 2026-05-23 - Trust-based delegation with quality ratcheting that commits improvements and reverts regressions. Chains Claude Code, Aider, Gemini CLI, Ollama.

## Autonomous Task Runners

Unattended agents driven by an external source — an issue queue, a work board, or a schedule — that run and sync state back without side-by-side supervision.

* [OpenHands](https://github.com/OpenHands/OpenHands) ⭐ 85,739 | 🐛 608 | 🌐 TypeScript | 📅 2026-08-31 - Self-hostable control center running its own agent or driving Claude Code, Codex, and any Agent Client Protocol agent, on schedules or webhooks.
* [multica](https://github.com/multica-ai/multica) ⭐ 48,380 | 🐛 1,414 | 🌐 Go | 📅 2026-08-31 - Managed agents platform where you assign tasks, track progress, and let agents compound skills between runs.
* [symphony](https://github.com/openai/symphony) ⭐ 26,959 | 🐛 8 | 🌐 Elixir | 📅 2026-08-19 - Turns project work into isolated autonomous runs, so teams manage the work rather than supervise the agent.
* [open-swe](https://github.com/langchain-ai/open-swe) ⭐ 10,638 | 🐛 67 | 🌐 Python | 📅 2026-08-31 - Invoked from Slack, Linear, or GitHub comments; each task runs in its own cloud sandbox and ends in a draft PR linked to the ticket.
* [claude-code-action](https://github.com/anthropics/claude-code-action) ⭐ 8,765 | 🐛 726 | 🌐 TypeScript | 📅 2026-08-28 - Anthropic's official GitHub Action, detecting from context whether to answer, review, or implement. Auth via Anthropic API, Bedrock, Vertex, or Foundry.
* [gh-aw](https://github.com/github/gh-aw) ⭐ 5,065 | 🐛 362 | 🌐 Go | 📅 2026-08-31 - Compiles agentic workflows written in Markdown into GitHub Actions YAML. Read-only by default, with writes only through sanitized safe-outputs. Copilot, Claude, Codex, Gemini.
* [background-agents](https://github.com/ColeMurray/background-agents) ⭐ 2,703 | 🐛 88 | 🌐 TypeScript | 📅 2026-08-31 - Sessions trigger from a web UI, Slack, GitHub, Linear, webhooks, or cron, run in Modal, Daytona, Vercel, E2B, or OpenComputer sandboxes, and open attributed PRs.
* [run-gemini-cli](https://github.com/google-github-actions/run-gemini-cli) ⭐ 2,066 | 🐛 84 | 🌐 TypeScript | 📅 2026-08-21 - Google's official GitHub Action, running on event or schedule triggers or on demand via `@gemini-cli /review` and `/triage`.
* [codex-action](https://github.com/openai/codex-action) ⭐ 1,217 | 🐛 69 | 🌐 TypeScript | 📅 2026-08-26 - OpenAI's official GitHub Action, running Codex CLI headlessly under drop-sudo, unprivileged-user, or fully read-only sandboxes.
* [centaur](https://github.com/paradigmxyz/centaur) ⭐ 1,207 | 🐛 119 | 🌐 Python | 📅 2026-08-31 - Multiplayer self-hosted agents with Slack-native conversations, Kubernetes sandboxes, shared tools, and durable workflows.
* [cyrus](https://github.com/cyrusagents/cyrus) ⭐ 792 | 🐛 105 | 🌐 TypeScript | 📅 2026-08-29 - Watches Linear, GitHub, GitLab, and Slack issues assigned to it, spinning up an isolated worktree per issue. Claude Code, Codex, Cursor, Gemini.
* [aeon](https://github.com/aeonfun/aeon) ⭐ 707 | 🐛 2 | 🌐 TypeScript | 📅 2026-08-30 - Runs unattended on GitHub Actions; dispatches skills to six coding-agent harnesses behind one contract (Claude Code, Grok, Codex, Pi, Vibe, Kimi), with quality scoring, git-persisted memory, a self-healing loop, and reactive triggers.
* [remote-swe-agents](https://github.com/aws-samples/remote-swe-agents) ⭐ 243 | 🐛 23 | 🌐 TypeScript | 📅 2026-08-25 - Serverless control plane on Lambda with a dedicated EC2 worker per session, triggered by issue comments, assignments, and PR reviews.
* [Factory](https://github.com/owainlewis/factory) ⭐ 220 | 🐛 26 | 🌐 Go | 📅 2026-08-31 - Keeps coding agents working on a repository without making a human orchestrate every step from a terminal, pulling tasks from trusted ticket queues into isolated Codex workspaces.
* [Contrabass](https://github.com/junhoyeo/contrabass) ⭐ 219 | 🐛 2 | 🌐 Go | 📅 2026-07-17 - Terminal-first orchestrator for issue-driven agent runs, pulling work from Linear, GitHub Issues, or a local board into git worktrees with TUI, headless, and dashboard modes.
* [sortie](https://github.com/sortie-ai/sortie) ⭐ 135 | 🐛 30 | 🌐 Go | 📅 2026-08-31 - Turns tracker tickets into agent sessions. Agent-agnostic and tracker-agnostic, as a single Go binary with SQLite persistence.
* [lalph](https://github.com/tim-smart/lalph) ⭐ 130 | 🐛 2 | 🌐 TypeScript | 📅 2026-07-08 - Orchestrator driven by whichever source of issues you point it at.
* [Taskuary](https://github.com/ldbumble/taskuary) ⭐ 43 | 🐛 11 | 🌐 Python | 📅 2026-08-31 - Local-first work inbox that triages email, chat, issue trackers, and scheduled reports into supervised Claude Code, Codex, Gemini, Cursor, or Copilot CLI runs, with conflict-aware queuing, live terminals, and approval-gated replies.
* [NEEDLE](https://github.com/jedarden/NEEDLE) ⭐ 18 | 🐛 3 | 🌐 Rust | 📅 2026-08-31 - Runs unattended against a shared bead queue (SQLite, atomic claims), dispatching each bead to a headless CLI — Claude Code, Codex, OpenCode, Aider — with every outcome routed through an explicit state machine; no inter-agent channel, coordination is done at decomposition time.

## Agent Infrastructure & Primitives

Control planes, coordination protocols, harness adapters, and runtimes — the layer beneath your agents rather than the surface you work in.

* [Archon](https://github.com/coleam00/Archon) ⭐ 23,318 | 🐛 278 | 🌐 TypeScript | 📅 2026-08-31 - Harness builder for deterministic AI coding workflows, combining agent steps with scripts, validation gates, approvals, and isolated git worktrees. Claude Code, Codex, and more.
* [NemoClaw](https://github.com/NVIDIA/NemoClaw) ⭐ 22,324 | 🐛 521 | 🌐 TypeScript | 📅 2026-08-31 - Runs Hermes, LangChain Deep Agents, and OpenClaw inside NVIDIA OpenShell with managed inference.
* [openfang](https://github.com/RightNow-AI/openfang) ⭐ 18,151 | 🐛 115 | 🌐 Rust | 📅 2026-07-02 - Open-source agent operating system.
* [omnigent](https://github.com/omnigent-ai/omnigent) ⭐ 9,540 | 🐛 1,196 | 🌐 Python | 📅 2026-08-31 - Meta-harness running Claude Code, Codex, Cursor, OpenCode, Hermes, Pi, or custom YAML agents against swappable sandbox backends, with policy enforcement.
* [Open Multi-Agent](https://github.com/open-multi-agent/open-multi-agent) ⭐ 6,850 | 🐛 12 | 🌐 TypeScript | 📅 2026-08-31 - TypeScript-native runtime where a coordinator turns a goal into a task DAG and a deterministic scheduler runs specialized agents, with approvals, traces, evaluation, checkpoints, and resume support.
* [sandbox-agent](https://github.com/rivet-dev/sandbox-agent) ⭐ 1,554 | 🐛 82 | 🌐 TypeScript | 📅 2026-06-19 - Daemon, HTTP/SSE API, and TypeScript SDK for driving six coding agents inside E2B, Daytona, Modal, Cloudflare Containers, or Docker.
* [Agentlas OS](https://github.com/agentlas-ai/Agentlas-OS) ⭐ 1,101 | 🐛 0 | 🌐 Python | 📅 2026-08-30 - Keeps specialist agents in a hub and spins up a temporary orchestrator per task, with A2A routing and governed memory gates. Formerly Hephaestus.
* [Claudexor](https://github.com/razzant/claudexor) ⭐ 425 | 🐛 64 | 🌐 TypeScript | 📅 2026-08-31 - Routes one coding thread across harnesses with quota-aware rotation between subscription profiles, Best-of-N runs, and cross-family review.
* [guild](https://github.com/mathomhaus/guild) ⭐ 305 | 🐛 26 | 🌐 Go | 📅 2026-08-26 - Shared context, memory, and task coordination as a single Go binary over local SQLite with hybrid keyword and semantic search.
* [handoff](https://github.com/dazuiba/handoff) ⭐ 88 | 🐛 1 | 🌐 Python | 📅 2026-08-02 - Delegates a task to DeepSeek, Codex, or Claude from inside your current Claude Code or Codex session, returning the result automatically.
* [sub-agents-skills](https://github.com/shinpr/sub-agents-skills) ⭐ 81 | 🐛 1 | 🌐 Python | 📅 2026-08-30 - Portable Markdown definitions that route a task to a chosen backend, model, effort level, and permission set.
* [agenttier](https://github.com/agenttier/agenttier) ⭐ 60 | 🐛 18 | 🌐 Go | 📅 2026-08-24 - Kubernetes runtime giving each agent its own Pod and PVC sandbox behind a default-deny NetworkPolicy, with a streaming SSE invoke API.
* [neuralyzer](https://github.com/gintasz/neuralyzer) ⭐ 39 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-07 - Lets an agent wipe its own session context and re-run the first message, making Ralph loops easier to engineer.
* [Crewplane](https://github.com/crewplaneai/crewplane) ⭐ 35 | 🐛 1 | 🌐 Python | 📅 2026-08-29 - CLI-first control plane that turns one-off coding-agent calls into reviewable Markdown workflows spanning Claude Code, Codex, Gemini CLI, or Copilot CLI. Explicit artifact handoffs keep execution inspectable on disk, while validated completed nodes let failed workflows resume instead of starting over.
* [codecast](https://github.com/codecast-sh/codecast) ⭐ 30 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-31 - Watches your real local sessions and surfaces them in a live triage inbox, keeping a searchable record with line-level agent attribution. Claude Code, Codex, Cursor, Gemini.
* [agent-runbook](https://github.com/KnoxOps/agent-runbook) ⭐ 17 | 🐛 0 | 🌐 Python | 📅 2026-07-15 - Compiles YAML runbooks with loops, branching, and parallelism into SKILL.md files for Claude Code and Codex.
* [aGiTrack](https://github.com/core-aix/agitrack) ⭐ 17 | 🐛 3 | 🌐 Python | 📅 2026-08-31 - Takes what a coding agent produces and commits each turn to git, recording the prompt, model, and that turn's token cost in the commit message, with the agent confined to its own worktree. Claude Code, Codex, and OpenCode.
* [LionClaw](https://github.com/moshthepitt/lionclaw) ⭐ 16 | 🐛 12 | 🌐 Rust | 📅 2026-08-06 - Local control plane running coding agents as durable, auditable workers with explicit state, skills, and checkpoints.
* [skillfold](https://github.com/byronxlg/skillfold) ⭐ 12 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-24 - Declares skills in YAML and pins exact revisions in a lockfile so installs are reproducible across Claude Code and Codex.

## Personal Assistants

Always-on agents you reach over chat or a desktop app. They remember across sessions, run on their own schedule, and hand work off to tools and other agents — coding agents included, though the work isn't limited to code.

* [openclaw](https://github.com/openclaw/openclaw) ⭐ 388,196 | 🐛 5,836 | 🌐 TypeScript | 📅 2026-08-31 - Your own personal AI assistant, on any OS and any platform.
* [hermes-agent](https://github.com/NousResearch/hermes-agent) ⭐ 238,768 | 🐛 38,228 | 🌐 Python | 📅 2026-08-31 - Self-improving harness with persistent cross-session memory and auto-generated skill documents.
* [nanobot](https://github.com/HKUDS/nanobot) ⭐ 47,569 | 🐛 757 | 🌐 Python | 📅 2026-08-31 - Ultra-lightweight self-hosted assistant in Python with WebUI, tools, memory, MCP, and multi-agent workflows.
* [QwenPaw](https://github.com/agentscope-ai/QwenPaw) ⭐ 34,735 | 🐛 889 | 🌐 Python | 📅 2026-08-31 - Personal assistant that deploys to your own machine or the cloud and plugs into multiple chat apps. Formerly CoPaw.
* [zeroclaw](https://github.com/zeroclaw-labs/zeroclaw) ⭐ 32,683 | 🐛 814 | 🌐 Rust | 📅 2026-08-31 - Fast, small, fully autonomous assistant infrastructure in Rust, deployable anywhere.
* [nanoclaw](https://github.com/nanocoai/nanoclaw) ⭐ 30,653 | 🐛 1,078 | 🌐 TypeScript | 📅 2026-08-31 - Lightweight OpenClaw alternative running in containers, connecting to WhatsApp, Telegram, Slack, Discord, and Gmail.
* [picoclaw](https://github.com/sipeed/picoclaw) ⭐ 29,916 | 🐛 37 | 🌐 Go | 📅 2026-08-27 - Tiny and fast assistant deployable anywhere.
* [leon](https://github.com/leon-ai/leon) ⭐ 17,476 | 🐛 111 | 🌐 TypeScript | 📅 2026-08-26 - Long-running open-source personal assistant with voice and text interfaces.
* [rowboat](https://github.com/rowboatlabs/rowboat) ⭐ 17,444 | 🐛 167 | 🌐 TypeScript | 📅 2026-08-31 - Open-source AI coworker with memory.
* [OpenWorker](https://github.com/andrewyng/openworker) ⭐ 17,098 | 🐛 450 | 🌐 Python | 📅 2026-08-31 - Open-source desktop AI coworker that delivers finished work — security review with re-scanned fixes, cloud posture audits, triaged inboxes — from specialist coworkers, with every action governed and logged. BYO model key or fully local via Ollama.
* [ironclaw](https://github.com/nearai/ironclaw) ⭐ 12,601 | 🐛 1,488 | 🌐 Rust | 📅 2026-08-31 - Agent OS in Rust focused on privacy, security, and extensibility.
* [Coworker](https://github.com/accomplish-ai/coworker) ⭐ 10,926 | 🐛 13 | 📅 2026-08-13 - Open source AI coworker that lives on your desktop. Formerly accomplish.
* [Cloudflare OS](https://github.com/cloudflare/cloudflare-os) ⭐ 9,419 | 🐛 112 | 🌐 TypeScript | 📅 2026-08-31 - Self-hostable "company OS" on Cloudflare Workers: a chat UI where agents preloaded with your company context do tasks, build sandboxed apps, and stay inside a Gatekeepers guardrail framework.
* [nullclaw](https://github.com/nullclaw/nullclaw) ⭐ 8,055 | 🐛 93 | 🌐 Zig | 📅 2026-07-19 - Fully autonomous assistant infrastructure written in Zig.
* [lobsterai](https://github.com/netease-youdao/LobsterAI) ⭐ 5,968 | 🐛 626 | 🌐 TypeScript | 📅 2026-08-31 - Desktop-grade agent for data analysis, slides, docs, and web research.
* [MetaClaw](https://github.com/aiming-lab/MetaClaw) ⭐ 3,495 | 🐛 17 | 🌐 Python | 📅 2026-06-07 - Assistant that learns and evolves from conversation alone.
* [zclaw](https://github.com/tnm/zclaw) ⭐ 2,222 | 🐛 12 | 🌐 C | 📅 2026-05-17 - Complete personal assistant in 888 KiB, running on an ESP32 with GPIO, cron, and custom tools.
* [OpenMausBot](https://github.com/milind-soni/OpenMausBot) ⭐ 1,925 | 🐛 86 | 🌐 TypeScript | 📅 2026-08-31 - Open-source Grok Bot-style team of bots in a chat-app sidebar, where every bot is a real local agent — Claude or Codex — with its own personality, model, cloud computer, and connected apps, behind approval gates. Local-first, bring-your-own-agent.
* [denchclaw](https://github.com/DenchHQ/DenchClaw) ⭐ 1,649 | 🐛 96 | 🌐 TypeScript | 📅 2026-06-11 - Managed OpenClaw framework aimed at CRM, sales automation, and outreach.
* [Rakazo](https://github.com/elie222/rakazo) ⭐ 1,617 | 🐛 17 | 🌐 TypeScript | 📅 2026-08-31 - Self-hosted platform for persistent AI teammates with their own conversations, memory, and routines, running on shared team computers or isolated private ones, reachable from web, desktop, and mobile with voice mode. Bots delegate to peer bots or short-lived subagents. BYO model and sandbox.
* [row-bot](https://github.com/siddsachar/row-bot) ⭐ 1,475 | 🐛 29 | 🌐 Python | 📅 2026-08-28 - Local-first desktop assistant that reasons through messy context, orchestrates tools and providers, and works inside your files, repos, and channels — durable memory, scheduled tasks, voice, visible browser automation, and parent-led child agents for research, review, and implementation. Runs on Ollama or opt-in cloud models. Formerly Thoth.
* [Ouroboros](https://github.com/razzant/ouroboros) ⭐ 1,243 | 🐛 133 | 🌐 Python | 📅 2026-08-31 - General-purpose agent with durable identity and memory, reviewed self-modification, multi-agent coordination, and desktop and headless interfaces.
* [rho](https://github.com/mikeyobrien/rho) ⭐ 371 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-26 - Stays running, remembers across sessions, and checks in on its own. macOS, Linux, Android.
* [OpenInstinct](https://github.com/Merit-Systems/OpenInstinct) ⭐ 219 | 🐛 15 | 🌐 TypeScript | 📅 2026-08-28 - iMessage assistant that drives a real browser to do chores, book tickets, and handle groceries, keeping your passwords and cards in an encrypted vault it unlocks per action. Self-hosted on your own Vercel, any model.
* [iva](https://github.com/smixs/iva) ⭐ 189 | 🐛 3 | 🌐 TypeScript | 📅 2026-08-31 - Telegram assistant that turns your messages, voice notes and photos into an Obsidian-compatible markdown vault it remembers across sessions. Crons, skills, MCP and Google Workspace from an in-chat menu. Self-hosted in one command, MIT.
* [Overlay](https://github.com/LayerNorm/overlay-web) ⭐ 131 | 🐛 10 | 🌐 TypeScript | 📅 2026-08-31 - Open-source workspace where humans and agents share context — knowledge, files, memory, connected apps — so you delegate repeatable work to agents, review what they produce, and take action through tools, provider-neutral.
* [lemon](https://github.com/z80dev/lemon) ⭐ 129 | 🐛 2 | 🌐 Elixir | 📅 2026-08-31 - Local-first assistant and coding agent runtime.
* [automata](https://github.com/sentientwave/automata) ⭐ 111 | 🐛 0 | 🌐 Elixir | 📅 2026-05-05 - Matrix-native workspace where Temporal-backed durable workflows survive restarts and keep long tasks moving.
* [ghostclaw](https://github.com/b1rdmania/ghostclaw) ⭐ 91 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-03 - An AI that lives on your computer and does things for you.
* [assistant](https://github.com/kcosr/assistant) ⭐ 90 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-30 - Panel-based assistant whose plugins share one workspace of notes, lists, and objects.
* [Hivekeep](https://github.com/MarlBurroW/hivekeep) ⭐ 51 | 🐛 31 | 🌐 TypeScript | 📅 2026-08-30 - Self-hosted team of specialized agents with persistent memory that delegate and build their own tools and mini-apps. Telegram, Slack, Discord, Matrix. Single container, MIT.
* [lucinate](https://github.com/lucinate-ai/lucinate) ⭐ 11 | 🐛 18 | 🌐 Go | 📅 2026-08-30 - Terminal-native chat client for OpenClaw, Hermes, Ollama, and OpenAI-compatible providers, with cron management and session browsing.

## Resting

A watchlist of projects without a push in the last few months (checked 2026-07-28). They stay here until they're active again, then move back up.

* [vibe-kanban](https://github.com/BloopAI/vibe-kanban) ⭐ 27,965 | 🐛 533 | 🌐 Rust | 📅 2026-04-24 - Kanban board for managing AI coding agents. *(last commit 2026-04)*
* [1code](https://github.com/21st-dev/1code) ⚠️ Archived - Orchestration layer for Claude Code and Codex. *(last commit 2026-03; archived)*
* [CodexMonitor](https://github.com/Dimillian/CodexMonitor) ⭐ 4,260 | 🐛 93 | 🌐 TypeScript | 📅 2026-03-26 - Orchestrate multiple Codex agents across local workspaces. *(last commit 2026-03)*
* [ralphy](https://github.com/michaelshimeles/ralphy) ⭐ 2,965 | 🐛 43 | 🌐 TypeScript | 📅 2026-02-05 - Bash script that loops Claude Code, Codex, OpenCode, Cursor, Qwen, or Droid until the task is done. *(last commit 2026-02)*
* [antfarm](https://github.com/snarktank/antfarm) ⭐ 2,495 | 🐛 113 | 🌐 TypeScript | 📅 2026-02-26 - Build your agent team in OpenClaw with one command. *(last commit 2026-02)*
* [cashclaw](https://github.com/moltlaunch/cashclaw) ⭐ 1,199 | 🐛 54 | 🌐 TypeScript | 📅 2026-03-14 - An autonomous agent that takes work, does work, gets paid, and gets better at it. *(last commit 2026-03)*
* [clawe](https://github.com/getclawe/clawe) ⭐ 749 | 🐛 6 | 🌐 TypeScript | 📅 2026-02-23 - Multi-agent coordination system: think Trello for OpenClaw agents. *(last commit 2026-02)*
* [opengoat](https://github.com/marian2js/opengoat) ⭐ 426 | 🐛 6 | 🌐 TypeScript | 📅 2026-04-12 - Build organizations of OpenClaw agents coordinating across Codex, Claude Code, Cursor, and OpenCode. *(last commit 2026-04)*
* [subtask](https://github.com/zippoxer/subtask) ⭐ 340 | 🐛 5 | 🌐 Go | 📅 2026-04-27 - Claude Skill that runs your tasks through subagents in git worktrees. *(last commit 2026-04)*
* [lettabot](https://github.com/letta-ai/lettabot) ⚠️ Archived - Personal assistant that remembers everything. *(last commit 2026-05; archived, replaced by Letta Code)*
* [mercury](https://github.com/Michaelliv/mercury) ⚠️ Archived - Personal AI assistant that lives where you chat. *(last commit 2026-03; archived)*
* [wreckit](https://github.com/mikehostetler/wreckit) ⭐ 130 | 🐛 18 | 🌐 Elixir | 📅 2026-04-14 - Run the Ralph Wiggum loop over your roadmap. *(last commit 2026-04)*
* [babyagi3](https://github.com/yoheinakajima/babyagi3) ⭐ 129 | 🐛 2 | 🌐 Python | 📅 2026-03-07 - A minimal AI agent you configure once, then run through natural language. *(last commit 2026-03)*
* [gnap](https://github.com/farol-team/gnap) ⭐ 83 | 🐛 2 | 📅 2026-03-17 - Git-native agent protocol coordinating agents through a shared repo as a task board, with no orchestrator process. *(last commit 2026-03)*
* [swarm-protocol](https://github.com/phuryn/swarm-protocol) ⭐ 53 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-15 - Headless coordination over MCP: claim work, detect file conflicts, heartbeat, and hand off across sessions. *(last commit 2026-03)*
* [wit](https://github.com/amaar-mc/wit) ⭐ 46 | 🐛 10 | 🌐 TypeScript | 📅 2026-03-27 - Locks individual functions rather than files via Tree-sitter, warning agents of conflicts before they write. *(last commit 2026-03)*
* [ariana](https://github.com/ariana-dot-dev/ariana) - The IDE of the future. *(last commit 2026-03)*

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-31._

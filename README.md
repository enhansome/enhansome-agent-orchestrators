# Awesome Agent Orchestrators with stars

A curated list of open source and source available tools for orchestrating agents.

Prefer a web version? Visit [agent-orchestrators.com](https://agent-orchestrators.com) for more information on each tool.

**Run several agents at once and review each diff.** Parallel Coding Agents — Terminal (TUI/CLI) if you live in tmux; Desktop & Web if you want a GUI or phone access.

**Keep an agent working while you're away.** Autonomous Loop Runners drive one goal until it verifies; Autonomous Task Runners pull work from an issue tracker, board, or schedule.

**Have agents split a large job between themselves.** Multi-Agent Swarms.

**Message an agent instead of opening a tool.** Personal Assistants stay running, remember across sessions, and pick up work from a chat thread — general tasks, not only code.

**Build your own orchestrator.** Agent Infrastructure & Primitives — control planes, coordination protocols, harness adapters, and runtimes.

## Contents

* [Parallel Coding Agents — Terminal (TUI/CLI)](#parallel-coding-agents--terminal-tuicli)
* [Parallel Coding Agents — Desktop & Web](#parallel-coding-agents--desktop--web)
* [Multi-Agent Swarms](#multi-agent-swarms)
* [Autonomous Loop Runners](#autonomous-loop-runners)
* [Autonomous Task Runners](#autonomous-task-runners)
* [Agent Infrastructure & Primitives](#agent-infrastructure--primitives)
* [Personal Assistants](#personal-assistants)
* [Resting](#resting)

## Parallel Coding Agents — Terminal (TUI/CLI)

Run and supervise several agent sessions side by side from a terminal — tmux panes, git worktrees, and TUI dashboards.

* [herdr](https://github.com/herdrdev/herdr) ⭐ 40,145 | 🐛 346 | 🌐 Rust | 📅 2026-09-21 - Background runtime that owns your agents' terminals: sessions survive reboot and reattach from any terminal or SSH, panes are marked working/blocked/idle, and agents themselves spawn panes and prompt each other over a CLI and socket API. One Rust binary.
* [cmux](https://github.com/manaflow-ai/cmux) ⭐ 27,321 | 🐛 5,291 | 🌐 Swift | 📅 2026-09-22 - Ghostty-based macOS terminal with vertical tabs and per-agent notifications, built for keeping many concurrent sessions legible.
* [claude-squad](https://github.com/smtg-ai/claude-squad) ⭐ 8,517 | 🐛 58 | 🌐 Go | 📅 2026-08-20 - Runs each agent as a detached background session with its own worktree, so work continues after you close the pane. Claude Code, Codex, OpenCode, Amp.
* [agent-of-empires](https://github.com/agent-of-empires/agent-of-empires) ⭐ 3,281 | 🐛 109 | 🌐 Rust | 📅 2026-09-22 - Pairs a TUI with a matching web view, so the same sessions stay reachable from a phone. Claude Code, Codex, OpenCode, Gemini, Mistral Vibe.
* [dmux](https://github.com/standardagents/dmux) ⭐ 1,776 | 🐛 39 | 🌐 HTML | 📅 2026-08-16 - Dev agent multiplexer pairing coding agents with git worktrees over tmux.
* [ai-devkit](https://github.com/codeaholicguy/ai-devkit) ⭐ 1,632 | 🐛 20 | 🌐 TypeScript | 📅 2026-09-20 - CLI control plane that runs agent sessions in managed tmux, sends prompts and logs to running agents from the terminal or a TUI console, and gives every agent one setup with shared local memory, verification skills, and lifecycle workflows. Claude Code, Codex, Pi, and more.
* [agent-deck](https://github.com/asheshgoplani/agent-deck) ⭐ 936 | 🐛 16 | 🌐 Go | 📅 2026-09-21 - One TUI covering sessions across Claude Code, Codex, Gemini, and OpenCode, with live status and resume for each.
* [Prowl](https://github.com/onevcat/Prowl) ⭐ 621 | 🐛 52 | 🌐 Swift | 📅 2026-09-21 - Native macOS command center for running coding agents in parallel, with vertical tabs, a live canvas view of every running session, and a command palette. Claude Code, Codex, and more.
* [agterm](https://github.com/umputun/agterm) ⭐ 619 | 🐛 7 | 🌐 Swift | 📅 2026-09-21 - Native macOS terminal with named workspaces, a live dashboard, attention states, and a scriptable control API.
* [tmux-ide](https://github.com/wavyrai/tmux-ide) ⭐ 550 | 🐛 7 | 🌐 TypeScript | 📅 2026-09-21 - Turns any project into a tmux IDE from a checked-in `ide.yml`, including preset agent-team layouts.
* [agent-manager](https://github.com/YoanWai/agent-manager) ⭐ 491 | 🐛 55 | 🌐 Go | 📅 2026-09-21 - Live-status tmux TUI with a prompt that lands in the pane without attaching, and in-terminal diff review that sends line comments back to the agent. Claude Code, Codex, OpenCode, Grok, Gemini CLI, Pi, Hermes.
* [agentbox](https://github.com/madarco/agentbox) ⭐ 486 | 🐛 1 | 🌐 TypeScript | 📅 2026-09-21 - Gives each agent its own sandboxed VM — local Docker or cloud via Hetzner, Daytona, Vercel, or E2B — with sub-second checkpoint starts.
* [termany](https://github.com/thinkany-ai/termany) ⭐ 433 | 🐛 30 | 🌐 TypeScript | 📅 2026-09-16 - Terminal that keeps many agent sessions in one window, tagging each pane working/done/needs-attention from the running job rather than the shell prompt, with diffs, worktrees, port handling, remote hosts, and token cost in the same place. Claude, Codex, Gemini, Grok Build, OpenClaw, Hermes, OpenCode, Cursor, Kimi, OMP.
* [Calyx](https://github.com/yuuichieguchi/Calyx) ⭐ 327 | 🐛 0 | 🌐 Swift | 📅 2026-09-14 - Native macOS terminal built on libghostty with an approval inbox for permission prompts, a working/blocked/idle sidebar, and in-terminal diff review.
* [amux](https://github.com/andyrewlee/amux) ⭐ 161 | 🐛 6 | 🌐 Go | 📅 2026-09-21 - Minimal TUI for spawning parallel coding agents in git worktrees.
* [openkanban](https://github.com/TechDufus/openkanban) ⭐ 146 | 🐛 6 | 🌐 Go | 📅 2026-06-12 - Kanban board for orchestrating coding agents, rendered entirely in the terminal.
* [thurbox](https://github.com/Thurbeen/thurbox) ⭐ 74 | 🐛 8 | 🌐 Rust | 📅 2026-09-22 - TUI orchestrator with remote SSH sessions, inter-session messaging, and a native code-review view. Works with any CLI agent you define.
* [YYLO](https://github.com/yylo-dev/yylo) ⭐ 60 | 🐛 10 | 🌐 Python | 📅 2026-09-21 - Command-line orchestrator for coding agents with typed task, validation, merge, and release-readiness boundaries: each task runs in a dedicated branch and worktree, and a risk-based merge queue reviews the result with receipt-backed changes. Pi and Codex subagents.
* [Vigil](https://github.com/butterlatte-zhang/vigil) ⭐ 28 | 🐛 0 | 🌐 Swift | 📅 2026-09-07 - Native macOS terminal where a manager agent runs the tree — spawning workers and sub-managers, detail flowing down, summaries rolling up — while every node stays the CLI's own TUI you can take over. Claude Code, Codex, OpenCode.
* [agent-console](https://github.com/buhuipao/agent-console) ⭐ 22 | 🐛 0 | 🌐 Rust | 📅 2026-09-20 - Rust TUI that finds Codex and Claude Code sessions from the providers' own transcripts, including ones started elsewhere, and resumes their native UI rather than replacing it. No tmux or worktrees.
* [repomon](https://github.com/AliHamzaAzam/repomon) ⭐ 21 | 🐛 6 | 🌐 Rust | 📅 2026-09-14 - Rust TUI that supervises a fleet across many repositories at once, in durable tmux sessions you can approve from your phone.
* [pappardelle](https://github.com/chardigio/pappardelle) ⭐ 17 | 🐛 1 | 🌐 TypeScript | 📅 2026-09-20 - TUI that turns a description into a Linear, Jira, or beads issue, a git worktree, a PR, and a Claude Code session beside a companion pane, wired together in a 3-pane tmux layout.
* [agent-session-manager](https://github.com/izll/agent-session-manager) ⭐ 13 | 🐛 0 | 🌐 Go | 📅 2026-09-05 - Live tmux TUI with session groups, resume and fork, diff review, and mobile push when an agent needs an answer. Claude Code, Codex, Gemini, Aider, Amazon Q, OpenCode.
* [Cyclops](https://github.com/cyclops-team/cyclops) ⭐ 12 | 🐛 1 | 🌐 Rust | 📅 2026-09-08 - Coordinates coding agents running in tmux through a durable mailbox with guarded terminal notifications, FIFO delivery per recipient, and fail-closed human-composer protection, with an optional workspace UI for overseeing the team. Codex CLI, Claude Code, Antigravity, Cursor Agent.

## Parallel Coding Agents — Desktop & Web

The same parallel-sessions workflow as a desktop app or browser/mobile dashboard, with diff review and merge.

* [Orca](https://github.com/stablyai/orca) ⭐ 75,116 | 🐛 6,484 | 🌐 TypeScript | 📅 2026-09-22 - Agentic development environment for running a fleet on your own subscription, available on desktop and mobile.
* [t3code](https://github.com/pingdotgg/t3code) ⭐ 23,280 | 🐛 2,057 | 🌐 TypeScript | 📅 2026-09-22 - Harness control surface available as web, mobile, and desktop app. Claude Code, Codex, Cursor, Grok Build, OpenCode.
* [Paseo](https://github.com/getpaseo/paseo) ⭐ 18,054 | 🐛 888 | 🌐 TypeScript | 📅 2026-09-22 - Self-hosted daemon running agents in parallel on your own machines, driven from desktop, iOS/Android, web, or CLI, with voice control, diff review, and no telemetry or forced log-ins. Claude Code, Codex, Copilot, OpenCode, Pi.
* [qm](https://github.com/yc-software/qm) ⭐ 15,198 | 🐛 551 | 🌐 TypeScript | 📅 2026-09-22 - Multiplayer harness where each teammate gets an isolated workspace to run agents independently, driven from Slack or the web.
* [Aperant](https://github.com/AndyMik90/Aperant) ⭐ 14,565 | 🐛 48 | 🌐 TypeScript | 📅 2026-06-14 - Runs up to 12 agent terminals with a self-validating QA loop and automatic conflict resolution when merging back to main.
* [superset](https://github.com/superset-sh/superset) ⭐ 14,477 | 🐛 746 | 🌐 TypeScript | 📅 2026-09-22 - Code editor built around running many agents on your machine at once.
* [agent-orchestrator](https://github.com/Untrivial-ai/agent-orchestrator) ⭐ 12,255 | 🐛 783 | 🌐 Go | 📅 2026-09-22 - Agent IDE for fleets that plans the work, spawns the agents, then fixes CI failures and merge conflicts without being asked.
* [humanlayer](https://github.com/humanlayer/humanlayer) ⭐ 11,597 | 🐛 46 | 🌐 TypeScript | 📅 2026-06-19 - Human-in-the-loop control for coding agents on hard problems; the repo notes its code is now largely deprecated in favor of a rebuild.
* [OpenChamber](https://github.com/openchamber/openchamber) ⭐ 10,276 | 🐛 645 | 🌐 TypeScript | 📅 2026-09-22 - Open-source workspace for running, supervising, and reviewing AI coding work across desktop, browser, editor, and mobile, with parallel model runs and per-run worktrees.
* [Emdash](https://github.com/generalaction/emdash) ⭐ 5,800 | 🐛 93 | 🌐 TypeScript | 📅 2026-09-21 - Agentic development environment running parallel agents against any model provider.
* [bb](https://github.com/get-bb/bb) ⭐ 3,842 | 🐛 409 | 🌐 TypeScript | 📅 2026-09-22 - Self-controlling agentic IDE that orchestrates multiple coding agents in live threads you can follow, steer, or hand off, driven from a desktop app, web app, CLI, or HTTP API.
* [automaker](https://github.com/AutoMaker-Org/automaker) ⭐ 3,219 | 🐛 11 | 🌐 TypeScript | 📅 2026-05-22 - Describe features on a Kanban board and agents implement them in isolated worktrees, running tests and committing as they go.
* [collaborator](https://github.com/collabs-inc/collab-public) ⭐ 2,946 | 🐛 81 | 🌐 TypeScript | 📅 2026-08-08 - Arranges terminals, editors, and files as tiles on an infinite pan-and-zoom canvas instead of tabs.
* [CodeNomad](https://github.com/NeuralNomadsAI/CodeNomad) ⭐ 2,585 | 🐛 23 | 🌐 TypeScript | 📅 2026-09-22 - Desktop and web workspace around the OpenCode CLI whose SideCars embed local tools like VS Code and terminals as tabs.
* [supacode](https://github.com/supabitapp/supacode) ⭐ 2,383 | 🐛 77 | 🌐 Swift | 📅 2026-09-05 - Native macOS command center for worktree-per-agent development.
* [xum](https://github.com/coder/xum) ⭐ 2,034 | 🐛 255 | 🌐 TypeScript | 📅 2026-09-22 - Desktop app for isolated, parallel agentic development.
* [synara](https://github.com/Emanuele-web04/synara) ⭐ 1,859 | 🐛 324 | 🌐 TypeScript | 📅 2026-09-22 - GUI desktop workspace for running and managing agents across local projects.
* [Zeron](https://github.com/zeronsh/zeron) ⭐ 1,846 | 🐛 120 | 🌐 Rust | 📅 2026-09-22 - Cross-device control plane for coding agents, syncing sessions across machines and keeping agents running on an always-on daemon. Claude Code, Codex, Cursor, Grok, Hermes, Pi.
* [nimbalyst](https://github.com/nimbalyst/nimbalyst) ⭐ 1,758 | 🐛 658 | 🌐 TypeScript | 📅 2026-09-21 - Visual workspace pairing parallel worktree sessions with kanban and direct visual editing. Claude Code, Codex, OpenCode.
* [Waku](https://github.com/egoist/waku) ⭐ 1,517 | 🐛 159 | 🌐 Rust | 📅 2026-09-17 - Native macOS desktop app for working with local coding agents, keeping projects, sessions, and transcripts on your machine. Supports Amp, Claude Code, Codex CLI, Cursor CLI, Grok Build, OpenCode, and Pi.
* [Traycer](https://github.com/traycerai/traycer) ⭐ 1,508 | 🐛 210 | 🌐 TypeScript | 📅 2026-09-22 - Bring-your-own-agent workspace running many sessions in parallel with context shared across models and providers, plus agent-to-agent messaging, shareable boards, and cross-device sync.
* [jean](https://github.com/coollabsio/jean) ⭐ 1,289 | 🐛 116 | 🌐 TypeScript | 📅 2026-09-22 - Desktop and web app for orchestrating agents across multiple projects and their git worktrees. Claude, Codex, OpenCode.
* [MonoCode](https://github.com/hardbeat920/monocode) ⭐ 1,106 | 🐛 85 | 🌐 TypeScript | 📅 2026-09-22 - Tauri desktop UI where tabs are agent sessions, running Claude Code, Codex, Cursor, Grok Build, OpenCode, Pi, omp, and fx on your existing subscriptions. macOS, Linux, and Windows.
* [takopi](https://github.com/banteg/takopi) ⭐ 1,054 | 🐛 49 | 🌐 Python | 📅 2026-05-25 - Telegram bridge that puts Codex, Claude Code, OpenCode, and Pi sessions in a chat thread.
* [parallel-code](https://github.com/johannesjo/parallel-code) ⭐ 1,017 | 🐛 58 | 🌐 TypeScript | 📅 2026-09-21 - Desktop app running Claude Code, Codex, and Gemini CLI side by side in isolated worktrees, with a built-in diff viewer and one-click merge.
* [IM.codes](https://github.com/im4codes/imcodes) ⭐ 973 | 🐛 2 | 🌐 TypeScript | 📅 2026-09-22 - Mobile and web control layer built for away-from-desk continuation, with terminal access, git views, localhost preview, and scheduled tasks. Claude Code, Codex, Gemini CLI.
* [Berd](https://github.com/block/berd) ⭐ 928 | 🐛 101 | 🌐 TypeScript | 📅 2026-09-17 - Block's open-source desktop app for working with AI agents: project chats with per-folder worktree behavior over the Goose backend, with agents, skills, connections, and agent sharing in one place.
* [Ghostex](https://github.com/maddada/Ghostex) ⭐ 834 | 🐛 9 | 🌐 Rust | 📅 2026-09-22 - Native macOS workspace (Rust/GPUI) running CLI agents side by side in low-RAM Ghostty terminals, with embedded browser and editor panes, a Kanban board, and iOS/Android session access. Claude Code, Codex, OpenCode.
* [kandev](https://github.com/kdlbs/kandev) ⭐ 824 | 🐛 129 | 🌐 Go | 📅 2026-09-22 - Kanban workbench whose multi-step workflows assign a different agent per step behind human gates, running locally, in Docker, over SSH, or in cloud executors.
* [ai-maestro](https://github.com/23blocks-OS/ai-maestro) ⭐ 790 | 🐛 10 | 🌐 TypeScript | 📅 2026-09-21 - Dashboard spanning multiple machines, adding memory search, code-graph queries, and agent-to-agent messaging. Claude, Aider, Cursor.
* [Alethe](https://github.com/Kc1t/alethe-agents) ⭐ 691 | 🐛 74 | 🌐 TypeScript | 📅 2026-09-22 - Local-first desktop workspace where agents and shells run as real PTYs in split panes and custom grids across projects, surviving pane close and app restart. Suspend idle groups to reclaim memory and resume with scrollback intact. Claude Code, Codex, OpenCode.
* [omg.dev](https://github.com/BennyKok/omg.dev) ⭐ 535 | 🐛 6 | 🌐 TypeScript | 📅 2026-09-22 - Open-source parallel-agent harness: run coding agents on your own computer or a hosted one, controlled from a single web UI with a mobile client. Claude Code, Codex, Grok, Cursor, OpenCode, Copilot, Pi.
* [Proliferate](https://github.com/proliferate-ai/proliferate) ⭐ 505 | 🐛 104 | 🌐 TypeScript | 📅 2026-09-22 - Agent IDE that runs sessions locally or in the cloud and lets you build reusable workflows from them.
* [Open Session](https://github.com/tellahq/opensession) ⭐ 383 | 🐛 64 | 🌐 TypeScript | 📅 2026-09-22 - Self-hosted server driving coding sessions in git worktrees on your own box or in isolated sandboxes, with a web UI, Slack/Linear/Plain/GitHub intake, diff and PR review, and multiple Codex and Claude subscriptions.
* [dorothy](https://github.com/Charlie85270/Dorothy) ⭐ 346 | 🐛 10 | 🌐 TypeScript | 📅 2026-07-07 - Desktop app combining agent orchestration with automations, Kanban management, and MCP servers.
* [diri](https://github.com/cristicretu/diri) ⭐ 333 | 🐛 45 | 🌐 Rust | 📅 2026-09-21 - Native macOS app running Claude Code, Codex, Cursor, Gemini, and shells in parallel across git worktrees or remote hosts, with live status, session persistence across restarts, a menu-bar rollup, and an MCP server for agents to spawn others.
* [aizen](https://github.com/vivy-company/aizen) ⭐ 306 | 🐛 3 | 🌐 Swift | 📅 2026-08-01 - macOS workspace that organizes worktrees, environments, and agent sessions per project.
* [Vicoa](https://github.com/vicoa-ai/vicoa) ⭐ 273 | 🐛 3 | 🌐 Python | 📅 2026-09-22 - Agentic IDE and AI orchestrator for running a team of coding agents from desktop, web, or mobile, with real-time sync, parallel git worktrees, and push notifications. Claude Code, Codex, OpenCode, Gemini, Cursor, GitHub Copilot, Kimi, Hermes.
* [vibe-tree](https://github.com/sahithvibudhi/vibe-tree) ⭐ 267 | 🐛 12 | 🌐 TypeScript | 📅 2026-07-25 - One git worktree per agent, delivered as desktop, web, and CLI.
* [MulmoTerminal](https://github.com/receptron/mulmoterminal) ⭐ 224 | 🐛 53 | 🌐 TypeScript | 📅 2026-09-22 - Browser grid of live Claude Code / Codex sessions started with one `npx` command. Each cell is a real PTY with a colour-coded status, tmux-backed persistence, and a git worktree per cell. For Claude Code, needs-you is shown separately from done, read from the CLI's own hooks.
* [constellagent](https://github.com/owengretzinger/constellagent) ⭐ 215 | 🐛 6 | 🌐 TypeScript | 📅 2026-05-05 - macOS app giving each agent its own terminal, editor, and git worktree in a single window.
* [ivy-tendril](https://github.com/Ivy-Interactive/Ivy-Tendril) ⭐ 198 | 🐛 174 | 🌐 C# | 📅 2026-09-15 - Drives agents through a plan-based lifecycle with verification gates, self-improving memory, and human checkpoints. Claude Code, Codex, Antigravity, Copilot, OpenCode.
* [Tempest](https://github.com/tempestai-dev/tempest) ⭐ 178 | 🐛 9 | 🌐 TypeScript | 📅 2026-09-21 - Tauri desktop ADE running CLI agents in parallel isolated worktrees, with a shared local code-knowledge graph that cuts token use across sessions, plus live status and built-in diff/PR review.
* [Ouijit](https://github.com/ouijit/ouijit) ⭐ 171 | 🐛 5 | 🌐 TypeScript | 📅 2026-09-08 - Kanban board and terminals wired together by lifecycle hooks, scripts, and a session-aware CLI, so a task runs by hand, on a script, or delegated to the agent. Per-task worktrees, optional VM sandboxing. Claude Code, Codex, Pi, OpenCode.
* [Claude Command Center (CCC)](https://github.com/amirfish1/claude-command-center) ⭐ 170 | 🐛 3 | 🌐 Python | 📅 2026-09-22 - Local dashboard for spawning, monitoring, and resuming sessions across Claude Code, Codex, Cursor, Antigravity, and Kilo Code.
* [clideck](https://github.com/rustykuntz/clideck) ⭐ 158 | 🐛 2 | 🌐 JavaScript | 📅 2026-09-22 - Chat-app-style dashboard with autopilot routing between agents and full control from a phone. Claude Code, Codex, Gemini CLI, OpenCode.
* [GraphCode](https://github.com/scgopi/GraphCode) ⭐ 125 | 🐛 23 | 🌐 Swift | 📅 2026-09-22 - macOS app that wires agent sessions into a graph: each node is a live terminal you can attach to mid-run, each edge a hand-off, message, or spawn that fires while you're away. Claude Code, Copilot CLI, Codex.
* [tlbx](https://github.com/tlbx-ai/tlbx) ⭐ 111 | 🐛 12 | 🌐 C# | 📅 2026-09-15 - Self-hosted browser workspace holding persistent real PTY sessions on your own machines, reachable from any browser or phone.
* [Garcon](https://github.com/cfal/garcon) ⭐ 86 | 🐛 40 | 🌐 TypeScript | 📅 2026-09-22 - Self-hosted browser and mobile workspace with diff review, Git/PR workflows, mobile approvals, scheduling, and cross-agent transfers. Seven CLI agents.
* [Tortie](https://github.com/gregce/tortie) ⭐ 85 | 🐛 5 | 🌐 TypeScript | 📅 2026-09-22 - Native macOS agent multiplexer with familiar IDE features: all projects in one window, agents that survive restarts, and organized terminal sessions without tmux.
* [clave](https://github.com/antasphere/clave) ⭐ 50 | 🐛 3 | 🌐 TypeScript | 📅 2026-09-22 - Native macOS app with split and grid layouts, session groups, SSH remote sessions, and usage analytics for Claude Code.
* [Zaivern Code](https://github.com/tacyan/zaivern-code) ⭐ 50 | 🐛 5 | 🌐 Rust | 📅 2026-09-22 - Cross-platform Rust desktop cockpit for running Claude Code, Codex, Gemini CLI, and 30+ coding agents in parallel, with fleet monitoring, mobile control, and line-level ownership to prevent merge conflicts.
* [intentic](https://github.com/intentic/intentic) ⭐ 44 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-22 - Browser and mobile workspace where every agent gets a persistent Docker sandbox on a machine you own plus a git worktree of its own, reached over an outbound-only Cloudflare tunnel, so runs keep going after you close the tab. Plan mode, per-hunk diff review, an environment Dockerfile the agent proposes and you approve, credential capabilities injected per turn, and schedule, webhook or event triggers. Claude Code, Codex, Grok, Kimi Code, Gemini. MIT.
* [AI4Kanban](https://github.com/ai4kanban/ai4kanban) ⭐ 35 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-21 - AI project manager that turns rough ideas into actionable tasks, coordinates coding agents through planning and implementation, and builds shared project memory from decisions. Humans steer priorities and make key decisions through a desktop and web interface.
* [vibecraft](https://github.com/rayzhudev/vibecraft) ⭐ 35 | 🐛 2 | 🌐 TypeScript | 📅 2026-07-19 - RTS-style workspace for commanding coding agents.
* [AGX](https://github.com/ramarlina/agx) ⭐ 29 | 🐛 1 | 🌐 TypeScript | 📅 2026-05-06 - Wake-work-sleep checkpointing keeps a persistent agent team on long objectives, with human gates between cycles.
* [Superagent](https://github.com/pungme/superagent-desktop) ⭐ 26 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-22 - macOS desktop app giving Claude Code and Codex a real browser to drive, an iOS Simulator to install and screenshot apps in, and a phone companion app for remote monitoring.
* [Fletch](https://github.com/fwdai/fletch) ⭐ 25 | 🐛 0 | 🌐 Rust | 📅 2026-09-22 - Native macOS IDE that seals each agent in its own repo clone under Seatbelt or Docker, serves each a shared symbol and call-graph index over MCP, and gates every step on tests or your approval. Claude Code, Codex, Cursor, OpenCode.
* [octomux](https://github.com/ShreyPaharia/octomux) ⭐ 22 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-18 - Local dashboard with a kanban fleet view, one unified permission inbox across agents, and in-app diff review.
* [muxel](https://github.com/ProjectHax/muxel) ⭐ 20 | 🐛 1 | 🌐 Rust | 📅 2026-09-22 - GPU-accelerated native desktop multiplexer (not a TUI) where every pane embeds a real terminal running a coding agent, with first-class git worktrees, live agent status, scheduled runs, and notifications.
* [agent-session-manager-desktop](https://github.com/izll/agent-session-manager-desktop) ⭐ 18 | 🐛 0 | 🌐 Go | 📅 2026-09-22 - Desktop GUI over tmux where each session holds agent and shell tabs with per-tab working directories; waiting agents raise a header counter you can answer without switching tabs, and ntfy push carries it to your phone. Linux, macOS, Windows. Claude Code, Codex, Gemini, Aider.
* [agent-squid](https://github.com/agent-squid/squid) ⭐ 18 | 🐛 0 | 🌐 Python | 📅 2026-09-16 - Browser UI organized into named lanes (`#topic@agent`), with context shared across agents and a realtime quota gauge.
* [alas](https://github.com/mrmans0n/alas) ⭐ 18 | 🐛 11 | 🌐 Swift | 📅 2026-09-22 - Native macOS workspace for the whole agent loop: libghostty terminals or native chat panes across every worktree, on your Mac or over SSH, with comment-based review, in-app merge, and pickup from your phone.
* [ateam](https://github.com/clawnify/ateam) ⭐ 12 | 🐛 19 | 🌐 TypeScript | 📅 2026-09-15 - macOS and iPhone app orchestrating Claude Code, OpenCode, and Codex crews, each isolated in its own git worktree.

## Multi-Agent Swarms

Systems where multiple specialized agents actively coordinate, communicate, and delegate toward a shared goal.

* [paperclip](https://github.com/paperclipai/paperclip) ⭐ 81,249 | 🐛 5,542 | 🌐 TypeScript | 📅 2026-09-22 - Self-hosted platform where agents wake on heartbeats to claim tickets, governed by org charts, budgets, and approval gates.
* [ruflo](https://github.com/ruvnet/ruflo) ⭐ 73,040 | 🐛 1,013 | 🌐 TypeScript | 📅 2026-09-22 - Meta-harness for deploying coordinated swarms and conversational multi-agent workflows. Formerly claude-flow.
* [crewAI](https://github.com/crewAIInc/crewAI) ⭐ 58,894 | 🐛 454 | 🌐 Python | 📅 2026-09-22 - Framework for orchestrating role-playing, autonomous AI agents that collaborate through defined roles, tools, and task delegation.
* [buzz](https://github.com/block/buzz) ⭐ 33,884 | 🐛 3,639 | 🌐 Rust | 📅 2026-09-22 - Agents are first-class members of shared channels on a Nostr relay you own, with their own keys and audit trails. Claude Code, Codex, Goose.
* [gastown](https://github.com/gastownhall/gastown) ⭐ 18,150 | 🐛 475 | 🌐 Go | 📅 2026-09-18 - Scales to 20-30 agents with a coordinator, git-backed issue tracking, health watchdogs, and a Bors-style merge queue.
* [ClawTeam](https://github.com/HKUDS/ClawTeam) ⭐ 5,541 | 🐛 34 | 🌐 Python | 📅 2026-05-09 - Agents spawn and manage their own teammates from one command, coordinating through file-based or P2P inboxes across tmux worktrees.
* [claude\_codex\_bridge](https://github.com/SeemSeam/claude_codex_bridge) ⭐ 3,517 | 🐛 101 | 🌐 Python | 📅 2026-09-21 - Workspace for mixing different vendors' CLI agents in one visible collaboration session.
* [agentsmesh](https://github.com/AgentsMesh/AgentsMesh) ⭐ 2,355 | 🐛 22 | 🌐 Go | 📅 2026-08-03 - Remote AI workstations with PTY sandboxes and worktree isolation, coordinating across channels and pod bindings. Claude Code, Codex, Gemini CLI, Aider, OpenCode.
* [Agent Teams](https://github.com/777genius/agent-teams-ai) ⭐ 2,157 | 🐛 26 | 🌐 TypeScript | 📅 2026-09-22 - Desktop app where you give high-level commands to autonomous coding-agent teams across Claude Code, Codex, OpenCode, Cursor, Grok, GitHub Copilot, Kiro, Z.AI, MiniMax, Kimi, 200+ models, and 75+ LLM providers. Agents coordinate through inter-agent messaging, Kanban tasks, and built-in code review.
* [Orkas](https://github.com/Orkas-AI/Orkas) ⭐ 2,106 | 🐛 12 | 🌐 TypeScript | 📅 2026-09-22 - A commander agent decomposes goals and dispatches specialists with isolated skills and memory. Claude Code, Codex, OpenCode, OpenClaw, Hermes.
* [scion](https://github.com/GoogleCloudPlatform/scion) ⭐ 1,716 | 🐛 43 | 🌐 Go | 📅 2026-09-22 - Orchestration testbed running agents in parallel isolated containers with dynamic coordination and normalized telemetry.
* [multi-agent-shogun](https://github.com/yohey-w/multi-agent-shogun) ⭐ 1,423 | 🐛 7 | 🌐 Shell | 📅 2026-08-06 - Shogun to karo to ashigaru hierarchy running up to 10 agents over tmux with no coordination API cost.
* [Fusion](https://github.com/Runfusion/Fusion) ⭐ 1,242 | 🐛 76 | 🌐 TypeScript | 📅 2026-09-22 - Multi-node orchestrator with a kanban board, plan-review-execute gates, per-task worktrees, and hierarchical missions.
* [loki-mode](https://github.com/asklokesh/loki-mode) ⭐ 1,067 | 🐛 13 | 🌐 Shell | 📅 2026-09-21 - PRD-to-deployed-product SDLC with 41 agents in 8 swarms, nine quality gates, and blind three-reviewer code review. Source-available under BUSL-1.1.
* [hcom](https://github.com/aannoo/hcom) ⭐ 511 | 🐛 36 | 🌐 Rust | 📅 2026-09-13 - Lets agents message, watch, and spawn each other across terminals. Claude Code, Codex, Antigravity, Cursor, OpenCode, Kilo, and more.
* [agent-kanban](https://github.com/saltbo/agent-kanban) ⭐ 478 | 🐛 13 | 🌐 TypeScript | 📅 2026-09-13 - Leader-worker task board with cryptographic agent identity. Claude Code, Codex, Gemini CLI.
* [AgentBridge](https://github.com/raysonmeng/agent-bridge) ⭐ 353 | 🐛 47 | 🌐 TypeScript | 📅 2026-09-21 - Local MIT CLI that keeps Claude Code and Codex as live peers in one session for mid-turn review, task split, and quota-boundary handoff.
* [OtoDock](https://github.com/OtoDock/oto-dock) ⭐ 184 | 🐛 0 | 🌐 Python | 📅 2026-09-15 - Self-hosted "company OS" where agents work in departments, delegate to each other, and keep working unwatched on your Anthropic/OpenAI subscriptions — company map, per-agent dashboards, artifacts, meetings, and terminals. Source-available under FSL-1.1.
* [ORCH](https://github.com/oxgeneral/ORCH) ⭐ 164 | 🐛 7 | 🌐 TypeScript | 📅 2026-08-01 - CLI runtime managing agents as typed teams with an explicit state machine and goals. Claude Code, Codex, Cursor.
* [NXTG-Forge Orchestrator](https://github.com/nxtg-ai/forge-orchestrator) ⭐ 161 | 🐛 3 | 🌐 Rust | 📅 2026-08-20 - Coordinates Claude Code, Codex, and Gemini CLI on one shared repo through a research-plan-delegate-adversarial-verify-deploy pipeline, with file locking, knowledge capture, and drift detection. Single Rust binary.
* [kodo](https://github.com/ikamensh/kodo) ⭐ 133 | 🐛 2 | 🌐 Python | 📅 2026-09-06 - Directs agents through work cycles where a separate agent independently verifies each result. Claude Code, Codex, Gemini CLI.
* [tutti](https://github.com/nutthouse/tutti) ⭐ 127 | 🐛 19 | 🌐 Rust | 📅 2026-07-28 - Config-driven workflows passing typed artifacts between agents, each in its own worktree.
* [CompanyHelm](https://github.com/CompanyHelm/companyhelm) ⭐ 76 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-28 - Distributed orchestrator with task management and direct agent-to-agent conversations.
* [5dive](https://github.com/5dive-ai/5dive) ⭐ 60 | 🐛 14 | 🌐 Shell | 📅 2026-09-22 - Named agents on a shared org chart and backlog hand work to each other and escalate to a human over Telegram. Claude Code, Codex, Grok, Antigravity, OpenCode.
* [Agon](https://github.com/AutoResearch-Factory/Agon) ⭐ 49 | 🐛 1 | 🌐 Python | 📅 2026-09-05 - Orchestrates scientist, coder, and auditor loops from research topic through proposal to experiment.
* [shire](https://github.com/victor36max/shire) ⭐ 39 | 🐛 2 | 🌐 TypeScript | 📅 2026-05-03 - Persistent team workspaces with inter-agent mailboxes and a shared drive. Claude Code, OpenCode, Pi.
* [corellis](https://github.com/CorellisOrg/Corellis) ⭐ 29 | 🐛 4 | 🌐 Shell | 📅 2026-04-13 - Multi-agent governance framework for OpenClaw — goal decomposition, fleet-wide memory, correction propagation, and approval workflows for 20+ agent fleets.
* [orc](https://github.com/spencermarx/orc) ⭐ 26 | 🐛 0 | 🌐 Shell | 📅 2026-06-21 - Lightweight framework that piggybacks your existing CLI setup for planning, task decomposition, worktrees, and review.

## Autonomous Loop Runners

The "keep running until done" pattern — a single goal driven through a retry-until-verified loop.

* [Loop Engineering](https://github.com/cobusgreyling/loop-engineering) ⭐ 11,279 | 🐛 10 | 🌐 TypeScript | 📅 2026-09-22 - Designs repeatable coding-agent loops around automation, worktrees, skills, state, and verification, with starters and a Loop Ready score for Grok, Claude Code, Codex, and OpenCode.
* [ralph-claude-code](https://github.com/frankbria/ralph-claude-code) ⭐ 9,642 | 🐛 37 | 🌐 Shell | 📅 2026-09-19 - Development loop for Claude Code with exit detection that recognizes when the work is actually finished.
* [ralph-orchestrator](https://github.com/mikeyobrien/ralph-orchestrator) ⭐ 3,152 | 🐛 6 | 🌐 Rust | 📅 2026-09-10 - Hat-based orchestration that keeps agents looping until done, as a fuller implementation of the Ralph Wiggum technique.
* [ralph-tui](https://github.com/subsy/ralph-tui) ⭐ 2,448 | 🐛 39 | 🌐 TypeScript | 📅 2026-09-04 - Drives an agent through a task list autonomously, with a TUI for watching the loop.
* [LongHorizon-Harness](https://github.com/AMAP-ML/LongHorizon-Harness) ⭐ 1,616 | 🐛 40 | 🌐 Python | 📅 2026-08-20 - Long-running computer-use harness with fresh-context execution, independent auditing, and verified checkpoints across desktop apps and CLI workflows. Claude Code, Codex, OpenCode, DeepSeek Harness.
* [ralphex](https://github.com/umputun/ralphex) ⭐ 1,487 | 🐛 4 | 🌐 Go | 📅 2026-09-14 - Executes an implementation plan autonomously with a fresh session per task, plus validation, retries, multi-phase review, and automatic commits. Claude Code, Codex.
* [bernstein](https://github.com/sipyourdrink-ltd/bernstein) ⭐ 1,241 | 🐛 419 | 🌐 Python | 📅 2026-09-22 - Keeps no model in the coordination loop, so orchestration costs zero tokens. Verifies with tests and auto-commits across 40+ CLI agents.
* [fractal](https://github.com/plasma-ai/fractal) ⭐ 732 | 🐛 5 | 🌐 Python | 📅 2026-09-21 - Loops that recursively delegate separable subtasks to child agents, bounded by configurable depth, cost, and time limits.
* [MartinLoop](https://github.com/Keesan12/martin-loop) ⭐ 190 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-19 - Caps spend, enforces policy, verifies output, and rolls back failures, leaving inspectable run receipts.
* [LoopTroop](https://github.com/looptroop-ai/LoopTroop) ⭐ 152 | 🐛 2 | 🌐 TypeScript | 📅 2026-09-22 - An LLM council plans the work, then Ralph-style loops retry failed units with fresh context. Executes via OpenCode worktrees.
* [ordewell](https://github.com/ordewell/ordewell) ⭐ 136 | 🐛 7 | 🌐 TypeScript | 📅 2026-09-22 - Turns one goal into an editable plan of tasks, each carrying its own runner, model and mode, then runs each task as its own agent session and passes it only when evidence of completion shows up in that session's output. Claude Code, Codex, OpenCode.
* [future-os](https://github.com/futuregene/future-os) ⭐ 95 | 🐛 0 | 🌐 Rust | 📅 2026-09-22 - One agent everywhere (terminal, desktop, mobile, CLI, IM bots) with a built-in loop control plane: durable goals, event-sourced state, and verification gates for 24h+ runs.
* [Dex](https://github.com/francescoalemanno/dex) ⭐ 21 | 🐛 0 | 🌐 Rust | 📅 2026-06-11 - Human-gated planning, multi-reviewer code review, and dead-end-aware research loops, shipped as cross-platform binaries for 7 CLI backends.
* [toryo](https://github.com/JesseRWeigel/toryo) ⭐ 12 | 🐛 3 | 🌐 TypeScript | 📅 2026-09-09 - Trust-based delegation with quality ratcheting that commits improvements and reverts regressions. Chains Claude Code, Aider, Gemini CLI, Ollama.

## Autonomous Task Runners

Unattended agents driven by an external source — an issue queue, a work board, or a schedule — that run and sync state back without side-by-side supervision.

* [OpenHands](https://github.com/OpenHands/OpenHands) ⭐ 88,798 | 🐛 881 | 🌐 TypeScript | 📅 2026-09-22 - Self-hostable control center running its own agent or driving Claude Code, Codex, and any Agent Client Protocol agent, on schedules or webhooks.
* [multica](https://github.com/multica-ai/multica) ⭐ 51,084 | 🐛 1,635 | 🌐 Go | 📅 2026-09-22 - Managed agents platform where you assign tasks, track progress, and let agents compound skills between runs.
* [symphony](https://github.com/openai/symphony) ⭐ 27,349 | 🐛 8 | 🌐 Elixir | 📅 2026-09-15 - Turns project work into isolated autonomous runs, so teams manage the work rather than supervise the agent.
* [open-swe](https://github.com/langchain-ai/open-swe) ⭐ 10,747 | 🐛 176 | 🌐 Python | 📅 2026-09-22 - Invoked from Slack, Linear, or GitHub comments; each task runs in its own cloud sandbox and ends in a draft PR linked to the ticket.
* [claude-code-action](https://github.com/anthropics/claude-code-action) ⭐ 8,923 | 🐛 797 | 🌐 TypeScript | 📅 2026-09-19 - Anthropic's official GitHub Action, detecting from context whether to answer, review, or implement. Auth via Anthropic API, Bedrock, Vertex, or Foundry.
* [gh-aw](https://github.com/github/gh-aw) ⭐ 5,168 | 🐛 410 | 🌐 Go | 📅 2026-09-22 - Compiles agentic workflows written in Markdown into GitHub Actions YAML. Read-only by default, with writes only through sanitized safe-outputs. Copilot, Claude, Codex, Gemini.
* [background-agents](https://github.com/ColeMurray/background-agents) ⭐ 3,269 | 🐛 112 | 🌐 TypeScript | 📅 2026-09-22 - Sessions trigger from a web UI, Slack, GitHub, Linear, webhooks, or cron, run in Modal, Daytona, Vercel, E2B, or OpenComputer sandboxes, and open attributed PRs.
* [run-gemini-cli](https://github.com/google-github-actions/run-gemini-cli) ⭐ 2,084 | 🐛 84 | 🌐 TypeScript | 📅 2026-08-21 - Google's official GitHub Action, running on event or schedule triggers or on demand via `@gemini-cli /review` and `/triage`.
* [centaur](https://github.com/paradigmxyz/centaur) ⭐ 1,322 | 🐛 114 | 🌐 Python | 📅 2026-09-21 - Multiplayer self-hosted agents with Slack-native conversations, Kubernetes sandboxes, shared tools, and durable workflows.
* [codex-action](https://github.com/openai/codex-action) ⭐ 1,242 | 🐛 81 | 🌐 TypeScript | 📅 2026-09-19 - OpenAI's official GitHub Action, running Codex CLI headlessly under drop-sudo, unprivileged-user, or fully read-only sandboxes.
* [agent-qa](https://github.com/vostride/agent-qa) ⭐ 887 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-03 - Runs natural-language web and mobile test suites through a self-healing execution loop, persists memory between runs, and exposes a dashboard, CLI, MCP server, and coding-agent skills.
* [cyrus](https://github.com/cyrusagents/cyrus) ⭐ 820 | 🐛 115 | 🌐 TypeScript | 📅 2026-09-22 - Watches Linear, GitHub, GitLab, and Slack issues assigned to it, spinning up an isolated worktree per issue. Claude Code, Codex, Cursor, Gemini.
* [aeon](https://github.com/aeonfun/aeon) ⭐ 751 | 🐛 2 | 🌐 Shell | 📅 2026-09-21 - Runs unattended on GitHub Actions; dispatches skills to six coding-agent harnesses behind one contract (Claude Code, Grok, Codex, Pi, Vibe, Kimi), with quality scoring, git-persisted memory, a self-healing loop, and reactive triggers.
* [Machinist](https://github.com/owainlewis/machinist) ⭐ 452 | 🐛 17 | 🌐 Go | 📅 2026-09-22 - Keeps coding agents working on a repository without making a human orchestrate every step from a terminal, pulling tasks from trusted ticket queues into isolated Codex workspaces.
* [no\_human](https://github.com/no-human-ai/no_human) ⭐ 320 | 🐛 108 | 🌐 Python | 📅 2026-09-22 - Takes a ticket (Jira, Linear, monday.com, GitHub/GitLab issues) to a reviewed pull request on your own machine: a second model in a fresh session reviews each diff and is told to refute "done", a tamper guard blocks net test reductions before that review, and merging stays human. Claude Code as the coder; Codex and local backends optional. MIT.
* [remote-swe-agents](https://github.com/aws-samples/remote-swe-agents) ⭐ 243 | 🐛 24 | 🌐 TypeScript | 📅 2026-09-22 - Serverless control plane on Lambda with a dedicated EC2 worker per session, triggered by issue comments, assignments, and PR reviews.
* [Contrabass](https://github.com/junhoyeo/contrabass) ⭐ 222 | 🐛 3 | 🌐 Go | 📅 2026-07-17 - Terminal-first orchestrator for issue-driven agent runs, pulling work from Linear, GitHub Issues, or a local board into git worktrees with TUI, headless, and dashboard modes.
* [sortie](https://github.com/sortie-ai/sortie) ⭐ 189 | 🐛 51 | 🌐 Go | 📅 2026-09-21 - Turns tracker tickets into agent sessions. Agent-agnostic and tracker-agnostic, as a single Go binary with SQLite persistence.
* [lalph](https://github.com/tim-smart/lalph) ⭐ 130 | 🐛 1 | 🌐 TypeScript | 📅 2026-07-08 - Orchestrator driven by whichever source of issues you point it at.
* [Taskuary](https://github.com/ldbumble/taskuary) ⭐ 117 | 🐛 9 | 🌐 Python | 📅 2026-09-22 - Local-first work inbox that triages email, chat, issue trackers, and scheduled reports into supervised Claude Code, Codex, Gemini, Cursor, or Copilot CLI runs, with conflict-aware queuing, live terminals, and approval-gated replies.
* [NEEDLE](https://github.com/jedarden/NEEDLE) ⭐ 26 | 🐛 6 | 🌐 Rust | 📅 2026-09-22 - Runs unattended against a shared bead queue (SQLite, atomic claims), dispatching each bead to a headless CLI — Claude Code, Codex, OpenCode, Aider — with every outcome routed through an explicit state machine; no inter-agent channel, coordination is done at decomposition time.

## Agent Infrastructure & Primitives

Control planes, coordination protocols, harness adapters, and runtimes — the layer beneath your agents rather than the surface you work in.

* [oh-my-codex](https://github.com/Yeachan-Heo/oh-my-codex) ⭐ 33,312 | 🐛 1 | 🌐 TypeScript | 📅 2026-09-22 - Workflow layer for OpenAI Codex CLI: stronger default sessions, reusable skills, native hooks, HUD/status surfaces, project guidance, and team-style execution commands.
* [Archon](https://github.com/coleam00/Archon) ⭐ 23,525 | 🐛 315 | 🌐 TypeScript | 📅 2026-09-22 - Harness builder for deterministic AI coding workflows, combining agent steps with scripts, validation gates, approvals, and isolated git worktrees. Claude Code, Codex, and more.
* [NemoClaw](https://github.com/NVIDIA/NemoClaw) ⭐ 22,516 | 🐛 728 | 🌐 TypeScript | 📅 2026-09-22 - Runs Hermes, LangChain Deep Agents, and OpenClaw inside NVIDIA OpenShell with managed inference.
* [openfang](https://github.com/RightNow-AI/openfang) ⭐ 18,210 | 🐛 120 | 🌐 Rust | 📅 2026-07-02 - Open-source agent operating system.
* [omnigent](https://github.com/omnigent-ai/omnigent) ⭐ 10,146 | 🐛 1,420 | 🌐 Python | 📅 2026-09-22 - Meta-harness running Claude Code, Codex, Cursor, OpenCode, Hermes, Pi, or custom YAML agents against swappable sandbox backends, with policy enforcement.
* [Open Multi-Agent](https://github.com/open-multi-agent/open-multi-agent) ⭐ 6,948 | 🐛 4 | 🌐 TypeScript | 📅 2026-09-18 - TypeScript-native runtime where a coordinator turns a goal into a task DAG and a deterministic scheduler runs specialized agents, with approvals, traces, evaluation, checkpoints, and resume support.
* [sandbox-agent](https://github.com/rivet-dev/sandbox-agent) ⭐ 1,571 | 🐛 82 | 🌐 TypeScript | 📅 2026-06-19 - Daemon, HTTP/SSE API, and TypeScript SDK for driving six coding agents inside E2B, Daytona, Modal, Cloudflare Containers, or Docker.
* [Agentlas OS](https://github.com/agentlas-ai/Agentlas-OS) ⭐ 1,086 | 🐛 2 | 🌐 Python | 📅 2026-09-18 - Keeps specialist agents in a hub and spins up a temporary orchestrator per task, with A2A routing and governed memory gates. Formerly Hephaestus.
* [foremerge](https://github.com/naw103/foremerge) ⭐ 492 | 🐛 3 | 🌐 Rust | 📅 2026-09-20 - Coordination protocol above Git: agents declare intent, semantic scope, and operation before writing code, deterministic rules raise findings when plans collide, and acceptance is gated on a verification run it executes itself. One Rust binary over local SQLite, with MCP for Claude Code, Codex, and Cursor.
* [Claudexor](https://github.com/razzant/claudexor) ⭐ 479 | 🐛 78 | 🌐 TypeScript | 📅 2026-09-22 - Routes one coding thread across harnesses with quota-aware rotation between subscription profiles, Best-of-N runs, and cross-family review.
* [Concord MCP](https://github.com/Get-Concord-AI/concord-mcp) ⭐ 323 | 🐛 16 | 🌐 TypeScript | 📅 2026-09-18 - Shared coordination protocol for Claude Code, Codex, Cursor, Gemini CLI, and Grok Build agents to claim work, detect edit collisions, exchange durable messages, transfer ownership, and hand off review evidence without replacing their existing harnesses.
* [guild](https://github.com/mathomhaus/guild) ⭐ 302 | 🐛 27 | 🌐 Go | 📅 2026-09-14 - Shared context, memory, and task coordination as a single Go binary over local SQLite with hybrid keyword and semantic search.
* [OrcaReplay](https://github.com/Continuum-AI-Corp/OrcaReplay) ⭐ 260 | 🐛 6 | 🌐 TypeScript | 📅 2026-09-22 - Records a coding agent at the process and socket boundary so model traffic, shell exit codes, per-turn file changes and MCP JSON-RPC share one timeline, then replays the run offline with the network off or forks it from a checkpoint onto a different model.
* [AIWG](https://github.com/jmagly/aiwg) ⭐ 211 | 🐛 27 | 🌐 TypeScript | 📅 2026-09-21 - Deploys versioned agents, skills, rules, and governed workflows into the native project paths used by Claude Code, Codex, Copilot, Cursor, and other coding agents.
* [handoff](https://github.com/dazuiba/handoff) ⭐ 90 | 🐛 1 | 🌐 Python | 📅 2026-08-02 - Delegates a task to DeepSeek, Codex, or Claude from inside your current Claude Code or Codex session, returning the result automatically.
* [sub-agents-skills](https://github.com/shinpr/sub-agents-skills) ⭐ 88 | 🐛 1 | 🌐 Python | 📅 2026-09-06 - Portable Markdown definitions that route a task to a chosen backend, model, effort level, and permission set.
* [ox](https://github.com/sageox/ox) ⭐ 59 | 🐛 67 | 🌐 Go | 📅 2026-09-22 - The team hivemind: persistent context recorded once and recalled across agents, machines, and teammates, as a Go CLI.
* [agenttier](https://github.com/agenttier/agenttier) ⭐ 55 | 🐛 25 | 🌐 Go | 📅 2026-09-21 - Kubernetes runtime giving each agent its own Pod and PVC sandbox behind a default-deny NetworkPolicy, with a streaming SSE invoke API.
* [Crewplane](https://github.com/crewplaneai/crewplane) ⭐ 38 | 🐛 1 | 🌐 Python | 📅 2026-09-22 - CLI-first control plane that turns one-off coding-agent calls into reviewable Markdown workflows spanning Claude Code, Codex, Gemini CLI, or Copilot CLI. Explicit artifact handoffs keep execution inspectable on disk, while validated completed nodes let failed workflows resume instead of starting over.
* [neuralyzer](https://github.com/gintasz/neuralyzer) ⭐ 38 | 🐛 0 | 🌐 TypeScript | 📅 2026-08-07 - Lets an agent wipe its own session context and re-run the first message, making Ralph loops easier to engineer.
* [Agent Messaging Protocol](https://github.com/agentmessaging/protocol) ⭐ 36 | 🐛 3 | 📅 2026-08-03 - Open standard for agent-to-agent messaging with Ed25519-signed envelopes, federation across providers, and delivery that must be proven rather than assumed. Reference server, TypeScript SDK, and a Claude Code plugin.
* [codecast](https://github.com/codecast-sh/codecast) ⭐ 33 | 🐛 1 | 🌐 TypeScript | 📅 2026-09-22 - Watches your real local sessions and surfaces them in a live triage inbox, keeping a searchable record with line-level agent attribution. Claude Code, Codex, Cursor, Gemini.
* [Mnemoverse](https://github.com/mnemoverse/mcp-memory-server) ⭐ 21 | 🐛 14 | 🌐 TypeScript | 📅 2026-09-22 - Hosted memory engine over MCP: decisions, preferences, and lessons follow an agent between sessions and tools, and recall re-ranks from reported outcomes rather than similarity alone. Remote endpoint with sign-in, or `npx -y @mnemoverse/mcp-memory-server@latest` with an API key. Claude Code, Cursor, Gemini CLI, VS Code, Windsurf, ChatGPT. MIT server, free tier.
* [LionClaw](https://github.com/moshthepitt/lionclaw) ⭐ 18 | 🐛 12 | 🌐 Rust | 📅 2026-09-01 - Local control plane running coding agents as durable, auditable workers with explicit state, skills, and checkpoints.
* [aGiTrack](https://github.com/core-aix/agitrack) ⭐ 17 | 🐛 4 | 🌐 Python | 📅 2026-09-21 - Takes what a coding agent produces and commits each turn to git, recording the prompt, model, and that turn's token cost in the commit message, with the agent confined to its own worktree. Claude Code, Codex, and OpenCode.
* [agent-runbook](https://github.com/KnoxOps/agent-runbook) ⭐ 13 | 🐛 0 | 🌐 Python | 📅 2026-07-15 - Compiles YAML runbooks with loops, branching, and parallelism into SKILL.md files for Claude Code and Codex.
* [skillfold](https://github.com/byronxlg/skillfold) ⭐ 13 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-21 - Declares skills in YAML and pins exact revisions in a lockfile so installs are reproducible across Claude Code and Codex.

## Personal Assistants

Always-on agents you reach over chat or a desktop app. They remember across sessions, run on their own schedule, and hand work off to tools and other agents — coding agents included, though the work isn't limited to code.

* [openclaw](https://github.com/openclaw/openclaw) ⭐ 390,240 | 🐛 8,333 | 🌐 TypeScript | 📅 2026-09-22 - Your own personal AI assistant, on any OS and any platform.
* [hermes-agent](https://github.com/NousResearch/hermes-agent) ⭐ 247,943 | 🐛 43,544 | 🌐 Python | 📅 2026-09-22 - Self-improving harness with persistent cross-session memory and auto-generated skill documents.
* [nanobot](https://github.com/HKUDS/nanobot) ⭐ 48,477 | 🐛 803 | 🌐 Python | 📅 2026-09-22 - Ultra-lightweight self-hosted assistant in Python with WebUI, tools, memory, MCP, and multi-agent workflows.
* [QwenPaw](https://github.com/agentscope-ai/QwenPaw) ⭐ 35,204 | 🐛 966 | 🌐 TypeScript | 📅 2026-09-22 - Personal assistant that deploys to your own machine or the cloud and plugs into multiple chat apps. Formerly CoPaw.
* [zeroclaw](https://github.com/zeroclaw-labs/zeroclaw) ⭐ 32,858 | 🐛 749 | 🌐 Rust | 📅 2026-09-22 - Fast, small, fully autonomous assistant infrastructure in Rust, deployable anywhere.
* [nanoclaw](https://github.com/nanocoai/nanoclaw) ⭐ 30,824 | 🐛 1,067 | 🌐 TypeScript | 📅 2026-09-22 - Lightweight OpenClaw alternative running in containers, connecting to WhatsApp, Telegram, Slack, Discord, and Gmail.
* [picoclaw](https://github.com/sipeed/picoclaw) ⭐ 30,009 | 🐛 37 | 🌐 Go | 📅 2026-09-17 - Tiny and fast assistant deployable anywhere.
* [OpenWorker](https://github.com/andrewyng/openworker) ⭐ 18,127 | 🐛 503 | 🌐 Python | 📅 2026-09-22 - Open-source desktop AI coworker that delivers finished work — security review with re-scanned fixes, cloud posture audits, triaged inboxes — from specialist coworkers, with every action governed and logged. BYO model key or fully local via Ollama.
* [rowboat](https://github.com/rowboatlabs/rowboat) ⭐ 17,942 | 🐛 180 | 🌐 TypeScript | 📅 2026-09-22 - Open-source AI coworker with memory.
* [leon](https://github.com/leon-ai/leon) ⭐ 17,537 | 🐛 112 | 🌐 TypeScript | 📅 2026-09-22 - Long-running open-source personal assistant with voice and text interfaces.
* [ironclaw](https://github.com/nearai/ironclaw) ⭐ 12,627 | 🐛 1,526 | 🌐 Rust | 📅 2026-09-21 - Agent OS in Rust focused on privacy, security, and extensibility.
* [Coworker](https://github.com/accomplish-ai/coworker) ⭐ 10,890 | 🐛 13 | 📅 2026-08-13 - Open source AI coworker that lives on your desktop. Formerly accomplish.
* [Cloudflare OS](https://github.com/cloudflare/cloudflare-os) ⭐ 10,040 | 🐛 127 | 🌐 TypeScript | 📅 2026-09-22 - Self-hostable "company OS" on Cloudflare Workers: a chat UI where agents preloaded with your company context do tasks, build sandboxed apps, and stay inside a Gatekeepers guardrail framework.
* [nullclaw](https://github.com/nullclaw/nullclaw) ⭐ 8,103 | 🐛 96 | 🌐 Zig | 📅 2026-07-19 - Fully autonomous assistant infrastructure written in Zig.
* [lobsterai](https://github.com/netease-youdao/LobsterAI) ⭐ 6,062 | 🐛 577 | 🌐 TypeScript | 📅 2026-09-22 - Desktop-grade agent for data analysis, slides, docs, and web research.
* [MetaClaw](https://github.com/aiming-lab/MetaClaw) ⭐ 3,493 | 🐛 17 | 🌐 Python | 📅 2026-06-07 - Assistant that learns and evolves from conversation alone.
* [OpenMausBot](https://github.com/milind-soni/OpenMausBot) ⭐ 3,227 | 🐛 274 | 🌐 TypeScript | 📅 2026-09-22 - Open-source Grok Bot-style team of bots in a chat-app sidebar, where every bot is a real local agent — Claude or Codex — with its own personality, model, cloud computer, and connected apps, behind approval gates. Local-first, bring-your-own-agent.
* [Rakazo](https://github.com/elie222/rakazo) ⭐ 2,838 | 🐛 35 | 🌐 TypeScript | 📅 2026-09-22 - Self-hosted platform for persistent AI teammates with their own conversations, memory, and routines, running on shared team computers or isolated private ones, reachable from web, desktop, and mobile with voice mode. Bots delegate to peer bots or short-lived subagents. BYO model and sandbox.
* [zclaw](https://github.com/tnm/zclaw) ⭐ 2,229 | 🐛 11 | 🌐 C | 📅 2026-05-17 - Complete personal assistant in 888 KiB, running on an ESP32 with GPIO, cron, and custom tools.
* [denchclaw](https://github.com/DenchHQ/DenchClaw) ⭐ 1,658 | 🐛 96 | 🌐 TypeScript | 📅 2026-06-11 - Managed OpenClaw framework aimed at CRM, sales automation, and outreach.
* [row-bot](https://github.com/siddsachar/row-bot) ⭐ 1,512 | 🐛 30 | 🌐 Python | 📅 2026-09-21 - Local-first desktop assistant that reasons through messy context, orchestrates tools and providers, and works inside your files, repos, and channels — durable memory, scheduled tasks, voice, visible browser automation, and parent-led child agents for research, review, and implementation. Runs on Ollama or opt-in cloud models. Formerly Thoth.
* [Ouroboros](https://github.com/razzant/ouroboros) ⭐ 1,367 | 🐛 228 | 🌐 Python | 📅 2026-09-22 - General-purpose agent with durable identity and memory, reviewed self-modification, multi-agent coordination, and desktop and headless interfaces.
* [taOS](https://github.com/jaylfc/taOS) ⭐ 544 | 🐛 300 | 🌐 Python | 📅 2026-09-22 - Self-hosted AI agent OS where memory, conversations, agents, and files live on hardware you own, offline by default with cloud by choice, including multi-framework group chat and a desktop GUI.
* [rho](https://github.com/mikeyobrien/rho) ⭐ 373 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-26 - Stays running, remembers across sessions, and checks in on its own. macOS, Linux, Android.
* [OpenInstinct](https://github.com/Merit-Systems/OpenInstinct) ⭐ 352 | 🐛 14 | 🌐 TypeScript | 📅 2026-09-15 - iMessage assistant that drives a real browser to do chores, book tickets, and handle groceries, keeping your passwords and cards in an encrypted vault it unlocks per action. Self-hosted on your own Vercel, any model.
* [iva](https://github.com/smixs/iva-agent) ⭐ 215 | 🐛 14 | 🌐 TypeScript | 📅 2026-09-22 - Telegram assistant that turns your messages, voice notes and photos into an Obsidian-compatible markdown vault it remembers across sessions. Crons, skills, MCP and Google Workspace from an in-chat menu. Self-hosted in one command, MIT.
* [Overlay](https://github.com/LayerNorm/overlay-web) ⭐ 142 | 🐛 8 | 🌐 TypeScript | 📅 2026-09-22 - Open-source workspace where humans and agents share context — knowledge, files, memory, connected apps — so you delegate repeatable work to agents, review what they produce, and take action through tools, provider-neutral.
* [lemon](https://github.com/z80dev/lemon) ⭐ 130 | 🐛 34 | 🌐 Elixir | 📅 2026-09-16 - Local-first assistant and coding agent runtime.
* [automata](https://github.com/sentientwave/automata) ⭐ 113 | 🐛 0 | 🌐 Elixir | 📅 2026-05-05 - Matrix-native workspace where Temporal-backed durable workflows survive restarts and keep long tasks moving.
* [ghostclaw](https://github.com/b1rdmania/ghostclaw) ⭐ 93 | 🐛 0 | 🌐 TypeScript | 📅 2026-05-03 - An AI that lives on your computer and does things for you.
* [assistant](https://github.com/kcosr/assistant) ⭐ 90 | 🐛 0 | 🌐 TypeScript | 📅 2026-09-20 - Panel-based assistant whose plugins share one workspace of notes, lists, and objects.
* [Hivekeep](https://github.com/MarlBurroW/hivekeep) ⭐ 63 | 🐛 23 | 🌐 TypeScript | 📅 2026-09-21 - Self-hosted team of specialized agents with persistent memory that delegate and build their own tools and mini-apps. Telegram, Slack, Discord, Matrix. Single container, MIT.
* [lucinate](https://github.com/lucinate-ai/lucinate) ⭐ 11 | 🐛 18 | 🌐 Go | 📅 2026-09-20 - Terminal-native chat client for OpenClaw, Hermes, Ollama, and OpenAI-compatible providers, with cron management and session browsing.

## Resting

A watchlist of projects without a push in the last few months (checked 2026-07-28). They stay here until they're active again, then move back up.

* [vibe-kanban](https://github.com/BloopAI/vibe-kanban) ⭐ 28,159 | 🐛 538 | 🌐 Rust | 📅 2026-09-19 - Kanban board for managing AI coding agents. *(last commit 2026-04)*
* [1code](https://github.com/21st-dev/1code) ⚠️ Archived - Orchestration layer for Claude Code and Codex. *(last commit 2026-03; archived)*
* [CodexMonitor](https://github.com/Dimillian/CodexMonitor) ⭐ 4,329 | 🐛 94 | 🌐 TypeScript | 📅 2026-03-26 - Orchestrate multiple Codex agents across local workspaces. *(last commit 2026-03)*
* [ralphy](https://github.com/michaelshimeles/ralphy) ⭐ 2,973 | 🐛 43 | 🌐 TypeScript | 📅 2026-02-05 - Bash script that loops Claude Code, Codex, OpenCode, Cursor, Qwen, or Droid until the task is done. *(last commit 2026-02)*
* [antfarm](https://github.com/snarktank/antfarm) ⭐ 2,499 | 🐛 112 | 🌐 TypeScript | 📅 2026-02-26 - Build your agent team in OpenClaw with one command. *(last commit 2026-02)*
* [cashclaw](https://github.com/moltlaunch/cashclaw) ⭐ 1,220 | 🐛 54 | 🌐 TypeScript | 📅 2026-03-14 - An autonomous agent that takes work, does work, gets paid, and gets better at it. *(last commit 2026-03)*
* [clawe](https://github.com/getclawe/clawe) ⭐ 752 | 🐛 6 | 🌐 TypeScript | 📅 2026-02-23 - Multi-agent coordination system: think Trello for OpenClaw agents. *(last commit 2026-02)*
* [opengoat](https://github.com/marian2js/opengoat) ⭐ 429 | 🐛 6 | 🌐 TypeScript | 📅 2026-04-12 - Build organizations of OpenClaw agents coordinating across Codex, Claude Code, Cursor, and OpenCode. *(last commit 2026-04)*
* [subtask](https://github.com/zippoxer/subtask) ⭐ 341 | 🐛 5 | 🌐 Go | 📅 2026-04-27 - Claude Skill that runs your tasks through subagents in git worktrees. *(last commit 2026-04)*
* [lettabot](https://github.com/letta-ai/lettabot) ⚠️ Archived - Personal assistant that remembers everything. *(last commit 2026-05; archived, replaced by Letta Code)*
* [mercury](https://github.com/Michaelliv/mercury) ⚠️ Archived - Personal AI assistant that lives where you chat. *(last commit 2026-03; archived)*
* [babyagi3](https://github.com/yoheinakajima/babyagi3) ⭐ 130 | 🐛 2 | 🌐 Python | 📅 2026-03-07 - A minimal AI agent you configure once, then run through natural language. *(last commit 2026-03)*
* [wreckit](https://github.com/mikehostetler/wreckit) ⭐ 130 | 🐛 18 | 🌐 Elixir | 📅 2026-04-14 - Run the Ralph Wiggum loop over your roadmap. *(last commit 2026-04)*
* [gnap](https://github.com/farol-team/gnap) ⭐ 86 | 🐛 2 | 📅 2026-03-17 - Git-native agent protocol coordinating agents through a shared repo as a task board, with no orchestrator process. *(last commit 2026-03)*
* [swarm-protocol](https://github.com/phuryn/swarm-protocol) ⭐ 54 | 🐛 6 | 🌐 TypeScript | 📅 2026-03-15 - Headless coordination over MCP: claim work, detect file conflicts, heartbeat, and hand off across sessions. *(last commit 2026-03)*
* [wit](https://github.com/amaar-mc/wit) ⭐ 46 | 🐛 10 | 🌐 TypeScript | 📅 2026-03-27 - Locks individual functions rather than files via Tree-sitter, warning agents of conflicts before they write. *(last commit 2026-03)*

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-09-22._

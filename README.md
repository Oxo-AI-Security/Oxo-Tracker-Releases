# Oxo Tracker Releases

Official binary distribution channel for **Oxo Tracker**, a Windows desktop application for testing model agents, prompt safety, connector behavior, and red-team resilience.

> **The source code is private.** This repository publishes the product overview and downloadable release builds only. It contains no application source code.

![Red-team comparison workspace](images/red-team-workspace.png)

## What is Oxo Tracker

Oxo Tracker combines a Tauri desktop host, a FastAPI backend, and a Vue 3 workspace so AI security teams can:

- run cookbook and recipe benchmark suites against model endpoints, inspect live progress, prompt traces, judge results, errors, and downloadable reports;
- keep adversarial red-team sessions with payload templates, attack modules, context strategies, and clean comparison conversations;
- browse and curate payload assets: cookbooks, recipes, datasets, prompt templates, and attack modules;
- create model agents and configurable HTTP / SSE / WebSocket connectors;
- turn design documents, diagrams, prompts, tool specs, and screenshots into an application functionality and risk map;
- keep benchmark jobs, red-team sessions, settings, and evidence in a local-first, identifier-scoped data store.

![Benchmark run details](images/benchmark-run-details.png)

### 简介（中文）

Oxo Tracker 是一个面向 AI 安全评估的 Windows 桌面应用，用于对模型 Agent、提示词安全、连接器行为和红队韧性进行可重复测试与证据留档。它集成了基准评测编排、红队会话工作区、Payload 资产库、Agent 与连接器管理、Agent 安全审查画布，以及本地优先的证据存储。源码仓库为私有，本仓库仅提供产品简介与可下载的安装包。

![Evaluation suites](images/cookbooks.png)

## Downloads

Download installers from the [Releases](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases) page. Large binaries are stored as GitHub Release assets and are not committed to Git history.

| Version | Status | Installer |
|---|---|---|
| **v0.3.0** | Preview | [Oxo-Tracker_0.3.0_x64-setup.exe](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/download/v0.3.0/Oxo-Tracker_0.3.0_x64-setup.exe) |
| v0.2.4 and earlier | Preview | see the [Releases](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases) page |

### Latest: v0.3.0 (Preview)

- Adaptive desktop window: sized and centered to the current monitor work area, remembers size/position/maximized state, and restores back to the last normal size instead of jumping to full screen.
- Stable UI scale (80/90/100/110) across navigation, refresh, and restarts; deterministic section landing pages.
- Concise AI settings, with single-line connection results, collapsed advanced options, and synchronized English/Chinese UI.
- Resilient benchmark scanning: pause anytime, partial results survive pause/crash/restart, live progress, and resume only the remaining prompts.
- Includes the red-team workspace, agent security review canvas, and Azure AI Foundry connector.

See the [v0.3.0 release notes](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/tag/v0.3.0) for details and SHA-256.

## Install

1. Download `Oxo-Tracker_0.3.0_x64-setup.exe` from the latest release.
2. Run the NSIS installer (current-user install; no administrator account required).
3. On first launch Oxo Tracker creates its local data directory at `%LOCALAPPDATA%\com.oxoai.oxo-tracker`.

This is an **unsigned Preview build**. Windows SmartScreen may show a first-run warning; choose **More info → Run anyway**. The installer bundles the offline WebView2 bootstrapper, local Moonshot assets, and NLTK resources, so it is large (about 422 MB).

## Verify a download

```powershell
Get-FileHash .\Oxo-Tracker_0.3.0_x64-setup.exe -Algorithm SHA256
Get-Content .\Oxo-Tracker_0.3.0_x64-setup.exe.sha256
```

The two SHA-256 values must match. Each release also publishes an SPDX SBOM, third-party notices, a dataset manifest, and release notes.

Preview builds are marked as **Pre-release**. A build should only be marked stable after Windows Authenticode signing and full release validation are configured. The v0.3.0 local preview does not include a Tauri updater signature or updater metadata; install by downloading the installer directly.

## Source code and security

The Oxo Tracker source repository is private and is intentionally not linked from this public distribution repository. Please do not open public issues containing sensitive details; report security concerns through the project maintainers' private channel.

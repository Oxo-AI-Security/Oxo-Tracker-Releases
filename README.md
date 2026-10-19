<div align="center">

<img src="images/logo.png" alt="Oxo Tracker logo" width="112" />

# 🛡️ Oxo Tracker

### 🧪 Test AI models & agents for safety, prompt-injection resilience and policy compliance — on your own Windows PC

Turn **“I think the model is safe”** into **repeatable evidence**: benchmark suites, red-team sessions, live prompt traces and exportable reports — in one friendly desktop app.

[![Latest release](https://img.shields.io/github/v/release/Oxo-AI-Security/Oxo-Tracker-Releases?label=latest&style=flat-square&color=7c3aed)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows%20x64-0078D4?style=flat-square&logo=windows)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)
[![Status](https://img.shields.io/badge/status-Preview-orange?style=flat-square)](#-preview-notice)
[![Downloads](https://img.shields.io/github/downloads/Oxo-AI-Security/Oxo-Tracker-Releases/total?label=downloads&style=flat-square)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)
[![Source](https://img.shields.io/badge/source-private-lightgrey?style=flat-square)](#-privacy-data--security)

**English** · [🇨🇳 中文](README.zh-CN.md)

[⬇️ Download latest](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest) &nbsp;•&nbsp; [🚀 Quick start](#-quick-start-5-minutes) &nbsp;•&nbsp; [🤖 Supported models](#-supported-models--api-keys) &nbsp;•&nbsp; [🖼️ Screenshots](#-screenshots) &nbsp;•&nbsp; [❓ FAQ](#-faq--troubleshooting)

</div>

---

## 👋 What is Oxo Tracker?

**Oxo Tracker is an AI security testing desktop app.** It helps you answer questions like:

- 🤔 *Does this model refuse harmful requests — or does it comply?*
- 🪄 *Can it be tricked by prompt injection, role-play or character-spacing bypasses?*
- 📊 *How does it compare with another model or another system prompt?*
- 🧾 *Can I produce evidence and a report my team can review?*

You connect a model or your own AI application with an API key, choose an evaluation suite, press **Run**, and watch every prompt and response in real time. No coding required, and **no local models or GPU needed** — the app calls the model APIs you already use.

> 💡 **New to AI testing?** Start with the [5-minute quick start](#-quick-start-5-minutes). The app ships with ready-made benchmark suites, so you do not have to write any test cases.

![Oxo Tracker dashboard](images/dashboard.png)

---

## ✨ What you can do

| | Feature | What it means for you |
|---|---|---|
| 🧪 | **Benchmark scans** | Run 19 ready-made cookbooks / 120 recipes (hallucination, data disclosure, adversarial prompts, undesirable content, …) against one or more endpoints. |
| ⏯️ | **Pause & resume** | Pause a long scan whenever you want. Results are saved as they arrive; resume later — even after restarting the app. |
| 🥷 | **Red-team sessions** | Chat with a target manually, apply Payload templates and attack modules, and keep a clean comparison conversation side by side. |
| 📚 | **Payload library** | Browse and reuse 221 datasets, 31 prompt templates, 15 attack modules and the recipes that combine them. |
| 🔌 | **Any model or app** | Connect Qwen, Kimi, DeepSeek, ChatGPT, Gemini, Azure AI Foundry — or any custom HTTP / SSE / WebSocket AI application. |
| 🧭 | **Agent security review** | Upload design docs, prompts, tool specs and screenshots to build a function map and a risk map of an AI application. |
| 📈 | **Evidence & reports** | Live prompt traces, judge results, errors, ETA, downloadable HTML reports and local history. |
| 🔐 | **Local-first** | Everything stays on your PC in a local data folder. API keys are encrypted with Windows DPAPI. |

---

## 📸 Screenshots

<div align="center">

### 🧭 Dashboard — one look at your testing inventory
<img src="images/dashboard.png" alt="Dashboard" width="100%" />

### 🧪 Benchmark in three steps: choose endpoints → choose tests → run
<img src="images/benchmark-endpoint-selection.png" alt="Select endpoints" width="100%" />
<img src="images/benchmark-cookbooks.png" alt="Select cookbooks" width="100%" />

### 📊 Live run details with prompt traces and downloadable reports
<img src="images/run-details.png" alt="Run details" width="100%" />

### 🥷 Red-team sessions with Payloads, attack modules and comparison chat
<img src="images/red-team-workspace.png" alt="Red-team workspace" width="100%" />

### 🤖 Connect providers like DeepSeek or Azure AI Foundry in Settings
<img src="images/ai-settings-providers.png" alt="AI settings" width="100%" />
<img src="images/ai-settings-azure.png" alt="Azure AI Foundry settings" width="100%" />

</div>

<details>
<summary>🖼️ More screenshots (Agents, Payload library, History, connector setup) — click to expand</summary>

<br />

<img src="images/agents-workbench.png" alt="Agents workbench" width="100%" />
<img src="images/red-team-sessions.png" alt="Red-team session list" width="100%" />
<img src="images/payload-library.png" alt="Payload library" width="100%" />
<img src="images/cookbooks.png" alt="Cookbooks" width="100%" />
<img src="images/history.png" alt="History" width="100%" />
<img src="images/connector-endpoint.png" alt="New connector endpoint" width="100%" />
<img src="images/security-review.png" alt="Agent security review" width="100%" />
<img src="images/settings.png" alt="Settings" width="100%" />

</details>

---

## 🚀 Quick start (5 minutes)

### 1️⃣ 💾 Download and install

1. Open the [latest release](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest).
2. Download **`Oxo-Tracker_0.3.0_x64-setup.exe`**.
3. Run the installer. It installs for the current Windows user — no administrator account needed.
4. If Windows SmartScreen appears, click **More info → Run anyway**. This is expected for an unsigned Preview build.

> 💬 First launch creates your local data folder at `%LOCALAPPDATA%\com.oxoai.oxo-tracker`. Nothing is uploaded automatically.

### 2️⃣ 🪄 Connect your first AI model

1. Open **Settings → AI settings** (bottom-left ⚙️).
2. Pick a provider card: **Qwen / Kimi / DeepSeek / ChatGPT / Gemini / Azure AI Foundry**.
3. Choose a **model** from the suggestions (or type any model ID your account can use).
4. Keep the pre-filled **Base URL**, or replace it with your own compatible endpoint.
5. Paste your **API key** from the provider console.
6. Click **Test connection** — you should see a green one-line result.
7. Click **Save & activate**.

> 🔐 Your key is stored locally and encrypted with Windows DPAPI. It is only sent to the AI provider you configured.

📷 *See the screenshots above — `Settings → AI settings` with DeepSeek and Azure AI Foundry.*

### 3️⃣ 🎯 Add the entity you want to test

A model you test is called a **target**. There are two ways to create one:

- **Model endpoint** — a provider model plus its API key, ready for benchmark scans.
- **Application connector** — map your own AI app with an HTTP, SSE or WebSocket request template (great for testing chatbots, agents and internal applications).

Steps: **Agents → Connectors → ➕ New Endpoint** → fill in name, request URL, model/deployment name, headers or API key → save.

<img src="images/connector-endpoint.png" alt="Create a connector endpoint" width="100%" />

> 🌐 Custom connector help: choose **HTTP / SSE / WebSocket template**, define the request body with `{{ prompt }}`, and tell Oxo Tracker how to extract the answer from the response (for example a JSON path).

### 4️⃣ 🧪 Run your first benchmark scan

1. Open **Benchmark** (left sidebar).
2. **Connect Endpoint** — tick one or more targets, then click **Next**.
3. **Select Tests** — pick one or more cookbooks (start with a small one), then click **Next**.
4. **Run** — give the scan a name, choose concurrency, and start it.
5. Watch progress, prompt traces and errors live. You can **pause** at any time.

<div align="center">
<img src="images/benchmark-endpoint-selection.png" alt="Select endpoints" width="49%" />
<img src="images/benchmark-cookbooks.png" alt="Select cookbooks" width="49%" />
</div>

### 5️⃣ 📊 Review results and export evidence

Open **History**, select your run and click **Details**. You can inspect every prompt / response, filter traces, and use **Preview report** / **Download** to get a self-contained HTML report.

<img src="images/run-details.png" alt="Run details" width="100%" />

### 6️⃣ 🥷 (Optional) Start a red-team conversation

1. Open **Agents → Open testing workspace** (Red Team Sessions).
2. Click **New session**, choose the target.
3. Chat manually, attach a **Payload template**, toggle an **Attack module**, and use **Compare** to keep a clean control conversation.

<div align="center">
<img src="images/red-team-sessions.png" alt="Red-team sessions" width="49%" />
<img src="images/red-team-workspace.png" alt="Red-team workspace" width="49%" />
</div>

---

## 🤖 Supported models & API keys

Oxo Tracker speaks the **OpenAI-compatible chat API** for the major providers, and can run any chat model your provider exposes. These providers are built in as one-click suggestions:

| Provider | Default Base URL | Example model IDs | 💡 Where to get your API key |
|---|---|---|---|
| 🟣 **Qwen** (Alibaba Cloud) | `https://dashscope.aliyuncs.com/compatible-mode/v1` | `qwen3.7-max`, `qwen3.7-plus`, `qwen3.6-flash` | [Alibaba Cloud Model Studio console](https://bailian.console.aliyun.com/) → API-KEY |
| ⚫ **Kimi** (Moonshot AI) | `https://api.moonshot.cn/v1` | `kimi-k3`, `kimi-k2.7-code`, `kimi-k2.6` | [Moonshot open platform](https://platform.moonshot.cn/console/api-keys) |
| 🐋 **DeepSeek** | `https://api.deepseek.com` | `deepseek-v4-flash`, `deepseek-v4-pro` | [DeepSeek platform](https://platform.deepseek.com/api_keys) |
| 🟢 **ChatGPT** (OpenAI) | `https://api.openai.com/v1` | `gpt-5.6-sol`, `gpt-5.6`, `gpt-4.1`, `gpt-4o` | [OpenAI platform](https://platform.openai.com/api-keys) |
| 🔵 **Gemini** (Google) | `https://generativelanguage.googleapis.com/v1beta/openai` | `gemini-3.6-flash`, `gemini-3.5-flash`, `gemini-2.5-pro` | [Google AI Studio](https://aistudio.google.com/apikey) |
| 🔷 **Azure AI Foundry** (Microsoft) | `https://<your-resource>.openai.azure.com/openai/v1` *or* `https://<your-resource>.services.ai.azure.com/openai/v1` | your **deployment name**, e.g. `gpt-5.6-sol`, `DeepSeek-V4.1-Flash` | [Azure AI Foundry](https://ai.azure.com/) → your project / deployment → Keys |

> 🪄 The model list is a convenience catalogue — **you can type any model ID** your provider supports. New models usually work as soon as the provider exposes them.
>
> 🧩 **OpenAI-compatible services** (self-hosted gateways, proxies, vLLM, Ollama with the OpenAI endpoint, etc.) work too: pick the closest provider, replace the base URL, and enter the model ID.

<details>
<summary>🔷 <strong>Azure AI Foundry — which URL should I paste?</strong> (click to expand)</summary>

Azure has several ways to reach the same deployment. From easiest to most advanced:

| Your situation | Base URL to use | Deployment name |
|---|---|---|
| 🟢 Resource-level OpenAI v1 endpoint *(recommended)* | `https://<resource>.services.ai.azure.com/openai/v1` or `https://<resource>.openai.azure.com/openai/v1` | the deployment name from the Foundry portal *(not the model market ID)* |
| 🟡 Project endpoint with an Entra ID token | `https://<resource>.services.ai.azure.com/api/projects/<project>` | the deployment name |
| 🟠 Full Responses URL | `https://<resource>.services.ai.azure.com/openai/v1/responses` | the deployment name |
| 🟠 Full Claude Messages URL | `https://<resource>.services.ai.azure.com/anthropic` (complete URL may end `/v1/messages`) | your Claude deployment name |
| ⚪️ Legacy deployment URL | `https://<resource>.openai.azure.com/openai/deployments/<deployment>/chat/completions` | must match the URL |

- 🔑 **API key** works for the recommended resource-level endpoint. Full endpoint URLs in the deployment's "code sample" are the safest copy-paste source.
- 🎫 **Entra ID access token** works for project routes; paste it as the "API key" with authentication set to **Microsoft Entra access token**. Tokens expire and must be refreshed manually.
- 📌 A **project endpoint + resource API key** combination is usually rejected by Azure — use a resource-level OpenAI v1 URL instead.
- ⚙️ Leave **API version** empty for v1 URLs. Only legacy endpoints need an `api-version` (put it in the Advanced section).

</details>

### 🔑 How API keys are handled

- 🔒 Keys are encrypted with **Windows DPAPI** and stored in your local app-data folder — never in the repository, never in plain text.
- 🔁 You can **reveal / copy / replace** a key in the UI after saving.
- 🚫 Oxo Tracker does not proxy or collect your traffic; requests go directly from your PC to the provider you configured.

---

## 🧰 Workspaces at a glance

| Workspace | What it is for |
|---|---|
| 🧭 **Dashboard** | Inventory and readiness overview: targets, recipes, cookbooks, attack modules and recent evidence. |
| 🧪 **Benchmark** | The guided scan wizard: select endpoints → select cookbooks/recipes → run and monitor. |
| 🤖 **Agents** | Targets and connectors, red-team sessions and the agent security review canvas. |
| 📚 **Payload** | Datasets, prompt templates, recipes, cookbooks and attack modules — the building blocks of every test. |
| 🕘 **History** | Every benchmark run, with details, prompt traces, reports and downloads. |
| ⚙️ **Settings** | AI providers, theme, interface size and language. |

<img src="images/payload-library.png" alt="Payload library" width="100%" />

---

## 🧪 Ready-made evaluation content

Oxo Tracker ships with a local copy of the Moonshot asset library, so you can start immediately without downloading datasets:

- 📚 **19 cookbooks** (IMDA Starter Kit, Capability, Trust & Safety, Others)
- 🧾 **120 recipes** covering hallucination, data disclosure, adversarial prompts, undesirable content and more
- 🗂️ **221 datasets** with expected answers and policy labels
- 🧬 **31 prompt templates** + **15 attack modules** for prompt transformation and red-teaming

You can also create your own datasets, prompt templates, recipes and cookbooks from the **Payload** workspace. Everything is stored locally.

---

## 💻 System requirements

| ✅ Required | Notes |
|---|---|
| 🪟 Windows 10 or Windows 11, **x64** | The packaged desktop app is Windows-only today. |
| 🌐 Microsoft Edge WebView2 Runtime | Already included on modern Windows; the installer can bootstrap it offline. |
| 💾 ~600 MB free disk space | The installer bundles offline WebView2, local datasets and NLTK resources. |
| 🔑 An API key from at least one model provider | Required to call a model. Some providers offer free trial quotas. |
| 🌍 Internet access | Needed for the model APIs you test and for online AI settings. |

> 🚫 No GPU, no local model weights, no Python installation, no Node.js — the installer is self-contained.

---

## 🔐 Privacy, data & security

- 🏠 **Local-first**: benchmark jobs, red-team sessions, settings, reports and evidence live in `%LOCALAPPDATA%\com.oxoai.oxo-tracker`.
- 🔒 **Encrypted credentials**: provider API keys are sealed with Windows DPAPI for the current Windows user.
- 🛰️ **No telemetry, no cloud account**: the app does not collect analytics. Network traffic is limited to the model/application endpoints you configure and update checks.
- 📂 **Your data stays yours**: uninstalling the app does not delete your local data folder; you can back it up or remove it yourself.
- 🧑‍💻 **Source code is private**: this public repository only carries product information and downloadable builds. Security reports are handled privately.

---

## ❓ FAQ & troubleshooting

<details>
<summary><strong>🛡️ Windows says “Windows protected your PC” — is this safe?</strong></summary>

Yes — the Preview installer is simply **not code-signed yet**, so SmartScreen shows a warning. Click **More info → Run anyway**. A signed build will replace this once certificate signing is configured.
</details>

<details>
<summary><strong>🔑 I got “401 / 403 / authentication failed” in Test connection</strong></summary>

- Check that you copied the whole key (no spaces or line breaks).
- Make sure the key belongs to the same provider and region as the Base URL.
- Some models require access to be requested first, or are only available in certain regions.
- For Azure, confirm you're using the right resource URL **and** deployment name, and that the deployment permits API-key auth.
</details>

<details>
<summary><strong>🔷 My Azure URL works in the browser code sample but not in the app</strong></summary>

Use the **resource-level OpenAI v1 endpoint** (`https://<resource>.services.ai.azure.com/openai/v1`) with the API key, and enter the **deployment name** as the model. Avoid pasting the “project endpoint” together with a resource key — Azure normally rejects that combination. See the [Azure section](#-supported-models--api-keys) above.
</details>

<details>
<summary><strong>🧪 The benchmark finished but I see no results / errors</strong></summary>

- Open **History → Details** and inspect the prompt trace and error column — target errors (wrong URL, timeout, blocked request) are shown per prompt.
- Confirm the endpoint works with **Test connection** in **Agents → Connectors** first.
- Rate limits (429) or content filters are reported by the provider and usually appear as errors rather than responses.
</details>

<details>
<summary><strong>⏸️ Can I pause a long scan and continue tomorrow?</strong></summary>

Yes. Click **Pause**; completed results are already saved. You can close the app and resume the scan later from **History → Details → Resume**. Already-completed prompts are not repeated.
</details>

<details>
<summary><strong>🔄 How do I update the app?</strong></summary>

Preview builds are installed by downloading a newer installer from the [Releases](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases) page. Automatic updates are not enabled for unsigned Preview builds yet.
</details>

<details>
<summary><strong>🗑️ How do I fully remove local data?</strong></summary>

1. Uninstall Oxo Tracker from **Windows Settings → Apps**.
2. Delete `%LOCALAPPDATA%\com.oxoai.oxo-tracker` to remove settings, sessions and job data.
</details>

---

## 🔗 Links

- ⬇️ **[All releases / download](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)** — every Windows build with checksums, SBOM and release notes.
- 📖 **[Release notes](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)** — what changed in each Preview.
- 🔐 **Source code:** maintained in a **private repository**; this public repository intentionally contains no source code.
- 🛡️ **Security reports:** please contact the project maintainers privately rather than opening a public issue with sensitive details.

---

<div align="center">

### 🚀 Ready? [Download the latest build](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest) and run your first safety scan in 5 minutes.

Made with 💜 for AI security, red teams and responsible evaluation.

<a id="-preview-notice"></a>
<sub>⚠️ <strong>Preview notice:</strong> Windows x64 unsigned build, published as a Pre-release. Windows SmartScreen may warn on first install. Automatic updates and code signing are not available for this Preview yet.</sub>

</div>

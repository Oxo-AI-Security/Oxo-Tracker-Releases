<div align="center">

<img src="images/logo.png" alt="Oxo Tracker logo" width="112" />

# 🛡️ Oxo Tracker

### 🧪 在你自己电脑上测试 AI 模型 / Agent 的安全性、提示词注入韧性与合规表现

把 **“我觉得这个模型挺安全”** 变成 **可复现、可留档的证据**：基准评测、红队会话、实时 Prompt 轨迹、可下载报告，全在一个友好的 Windows 桌面应用里完成。

[![最新版本](https://img.shields.io/github/v/release/Oxo-AI-Security/Oxo-Tracker-Releases?label=latest&style=flat-square&color=7c3aed)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)
[![平台](https://img.shields.io/badge/platform-Windows%20x64-0078D4?style=flat-square&logo=windows)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)
[![状态](https://img.shields.io/badge/status-Preview-orange?style=flat-square)](#-预览版说明)
[![下载次数](https://img.shields.io/github/downloads/Oxo-AI-Security/Oxo-Tracker-Releases/total?label=downloads&style=flat-square)](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)
[![源码](https://img.shields.io/badge/source-private-lightgrey?style=flat-square)](#-隐私数据与安全)

[🇬🇧 English](README.md) · **🇨🇳 中文**

[⬇️ 下载最新版](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest) &nbsp;•&nbsp; [🚀 快速上手](#-五分钟快速上手) &nbsp;•&nbsp; [🤖 支持的模型](#-支持的模型与-api-key) &nbsp;•&nbsp; [🖼️ 截图](#-界面截图) &nbsp;•&nbsp; [❓ 常见问题](#-常见问题与排障)

</div>

---

## 👋 Oxo Tracker 是做什么的？

**Oxo Tracker 是一个 AI 安全测试桌面应用。** 它能帮你回答这些问题：

- 🤔 *这个模型面对有害请求时会拒绝，还是会照做？*
- 🪄 *它能不能被提示词注入、角色扮演、字符间隔绕过等手法攻破？*
- 📊 *它和另一个模型、另一套系统提示词相比，表现差多少？*
- 🧾 *我能不能拿出可复核的证据和报告？*

你只需要用 API Key 连上模型（或你自己的 AI 应用），选一套评测套件，点 **Run**，就能实时看到每一条 Prompt 和回复。**不需要写代码，也不需要本地显卡或本地模型** —— 应用调用的是你已经在用的模型 API。

> 💡 **第一次接触 AI 安全测试？** 直接从下面的 [5 分钟快速上手](#-五分钟快速上手) 开始即可。应用内置了现成的评测套件，不需要你自己写测试用例。

![Oxo Tracker 仪表盘](images/dashboard.png)

---

## ✨ 它能做什么？

| | 功能 | 对你意味着什么 |
|---|---|---|
| 🧪 | **基准评测扫描** | 用 19 个现成 Cookbook / 120 个 Recipe（幻觉、数据泄露、对抗性提示词、不良内容……）测试一个或多个目标。 |
| ⏯️ | **随时暂停、下次继续** | 长扫描可以随时暂停，已完成的结果实时落盘；关闭应用、隔天再续扫也不会重复跑已完成的部分。 |
| 🥷 | **红队会话** | 手动和被测目标对话，叠加 Payload 模板与攻击模块，并保留干净的对照会话做对比。 |
| 📚 | **Payload 资产库** | 浏览复用 221 个数据集、31 个 Prompt 模板、15 个攻击模块，以及组合它们的 Recipe。 |
| 🔌 | **任何模型 / 应用** | 支持 Qwen、Kimi、DeepSeek、ChatGPT、Gemini、Azure AI Foundry，也支持任意 HTTP / SSE / WebSocket AI 应用。 |
| 🧭 | **Agent 安全审查** | 上传设计文档、提示词、工具说明和截图，生成功能地图与风险地图。 |
| 📈 | **证据与报告** | 实时 Prompt 轨迹、判定结果、错误、预计剩余时间，以及可下载的 HTML 报告和本地历史。 |
| 🔐 | **本地优先** | 所有数据都保存在你自己电脑的本地目录；API Key 用 Windows DPAPI 加密。 |

---

## 🖼️ 界面截图

<div align="center">

### 🧭 仪表盘 —— 一眼掌握测试资产与准备度
<img src="images/dashboard.png" alt="仪表盘" width="100%" />

### 🧪 三步完成基准评测：选目标 → 选测试 → 运行
<img src="images/benchmark-endpoint-selection.png" alt="选择目标" width="100%" />
<img src="images/benchmark-cookbooks.png" alt="选择评测套件" width="100%" />

### 📊 实时运行详情：Prompt 轨迹 + 可下载报告
<img src="images/run-details.png" alt="运行详情" width="100%" />

### 🥷 红队会话：Payload、攻击模块、对照组对比
<img src="images/red-team-workspace.png" alt="红队工作区" width="100%" />

### 🤖 在设置里连接 DeepSeek、Azure AI Foundry 等模型
<img src="images/ai-settings-providers.png" alt="AI 设置" width="100%" />
<img src="images/ai-settings-azure.png" alt="Azure AI Foundry 设置" width="100%" />

</div>

<details>
<summary>🖼️ 更多截图（Agent 工作台、Payload 资产库、历史记录、连接器配置）—— 点击展开</summary>

<br />

<img src="images/agents-workbench.png" alt="Agent 工作台" width="100%" />
<img src="images/red-team-sessions.png" alt="红队会话列表" width="100%" />
<img src="images/payload-library.png" alt="Payload 资产库" width="100%" />
<img src="images/cookbooks.png" alt="Cookbooks" width="100%" />
<img src="images/history.png" alt="历史记录" width="100%" />
<img src="images/connector-endpoint.png" alt="新建连接器端点" width="100%" />
<img src="images/security-review.png" alt="Agent 安全审查" width="100%" />
<img src="images/settings.png" alt="设置" width="100%" />

</details>

---

## 🚀 五分钟快速上手

### 1️⃣ 💾 下载并安装

1. 打开 [最新版本页面](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)。
2. 下载 **`Oxo-Tracker_0.3.0_x64-setup.exe`**。
3. 双击运行安装包。安装到当前 Windows 用户，**不需要管理员权限**。
4. 如果出现 Windows SmartScreen 提示，点 **更多信息 → 仍要运行**。这是未签名预览版的正常现象。

> 💬 首次启动会在 `%LOCALAPPDATA%\com.oxoai.oxo-tracker` 创建本地数据目录，不会自动上传任何内容。

### 2️⃣ 🪄 连接第一个 AI 模型

1. 点左下角 ⚙️ 打开 **Settings → AI settings**。
2. 在 **Select provider** 里选一个提供商：**Qwen / Kimi / DeepSeek / ChatGPT / Gemini / Azure AI Foundry**。
3. 在 **Model** 里选一个建议模型（也可以直接输入你账号支持的任何模型 ID）。
4. **Base URL** 已自动填好，一般不用改；如果你用的是自建/代理服务，替换成你的兼容接口地址。
5. 粘贴你在提供商控制台申请的 **API Key**。
6. 点 **Test connection**，看到绿色的单行成功提示就说明连通了。
7. 点 **Save & activate** 保存。

> 🔐 Key 会保存在本地并用 Windows DPAPI 加密，只会发送给**你自己配置的那个模型服务**。

📷 *可以直接对照上面的截图：`Settings → AI settings` 的 DeepSeek 和 Azure AI Foundry 页面。*

### 3️⃣ 🎯 添加要测试的目标

被测试的模型或应用在应用里叫 **Target（目标）**，有两种方式：

- **模型目标**：一个提供商模型 + API Key，可直接用于基准评测。
- **应用连接器**：用 HTTP / SSE / WebSocket 请求模板接入你自己的 AI 应用（适合测试聊天机器人、Agent、内部系统）。

操作路径：**Agents → Connectors → ➕ New Endpoint** → 填写名称、请求 URL、模型/部署名、请求头或 Key → 保存。

<img src="images/connector-endpoint.png" alt="创建连接器端点" width="100%" />

> 🌐 自定义连接器小贴士：选择 **HTTP / SSE / WebSocket 模板**，在请求体里用 `{{ prompt }}` 占位，并告诉 Oxo Tracker 如何从响应中提取回答（例如一个 JSON 路径）。

### 4️⃣ 🧪 跑第一次基准评测

1. 点左侧 **Benchmark**。
2. **Connect Endpoint**：勾选一个或多个目标，点 **Next**。
3. **Select Tests**：选择一个或多个 Cookbook（第一次建议先选小一点的），点 **Next**。
4. **Run**：给这次扫描起个名字，选择并发数，开始运行。
5. 实时查看进度、Prompt 轨迹和错误；任何时候都可以点 **Pause（暂停）**。

<div align="center">
<img src="images/benchmark-endpoint-selection.png" alt="选择目标" width="49%" />
<img src="images/benchmark-cookbooks.png" alt="选择评测套件" width="49%" />
</div>

### 5️⃣ 📊 查看结果、导出证据

打开 **History**，选中这次运行，点 **Details**。你可以逐条查看 Prompt / 回复、筛选轨迹，并用 **Preview report / Download** 导出完整的 HTML 报告。

<img src="images/run-details.png" alt="运行详情" width="100%" />

### 6️⃣ 🥷（可选）开始红队对话

1. 打开 **Agents → Open testing workspace（Red Team Sessions）**。
2. 点 **New session**，选择目标。
3. 手动输入攻击性/敏感性 Prompt，可叠加 **Payload 模板**、开启 **Attack module**，并用 **Compare** 同时保留一份干净的对照会话。

<div align="center">
<img src="images/red-team-sessions.png" alt="红队会话列表" width="49%" />
<img src="images/red-team-workspace.png" alt="红队工作区" width="49%" />
</div>

---

## 🤖 支持的模型与 API Key

Oxo Tracker 对主流提供商走 **OpenAI 兼容的 Chat API**，并支持你账户下可用的任意聊天模型。以下提供商已内置为一键选项：

| 提供商 | 默认 Base URL | 示例模型 ID | 💡 在哪里获取 API Key |
|---|---|---|---|
| 🟣 **通义千问 Qwen**（阿里云） | `https://dashscope.aliyuncs.com/compatible-mode/v1` | `qwen3.7-max`、`qwen3.7-plus`、`qwen3.6-flash` | [阿里云百炼控制台](https://bailian.console.aliyun.com/) → API-KEY |
| ⚫ **Kimi（月之暗面）** | `https://api.moonshot.cn/v1` | `kimi-k3`、`kimi-k2.7-code`、`kimi-k2.6` | [Moonshot 开放平台](https://platform.moonshot.cn/console/api-keys) |
| 🐋 **DeepSeek** | `https://api.deepseek.com` | `deepseek-v4-flash`、`deepseek-v4-pro` | [DeepSeek 开放平台](https://platform.deepseek.com/api_keys) |
| 🟢 **ChatGPT（OpenAI）** | `https://api.openai.com/v1` | `gpt-5.6-sol`、`gpt-5.6`、`gpt-4.1`、`gpt-4o` | [OpenAI 平台](https://platform.openai.com/api-keys) |
| 🔵 **Gemini（Google）** | `https://generativelanguage.googleapis.com/v1beta/openai` | `gemini-3.6-flash`、`gemini-3.5-flash`、`gemini-2.5-pro` | [Google AI Studio](https://aistudio.google.com/apikey) |
| 🔷 **Azure AI Foundry（微软）** | `https://<你的资源名>.openai.azure.com/openai/v1` 或 `https://<你的资源名>.services.ai.azure.com/openai/v1` | 填你的**部署名称**，例如 `gpt-5.6-sol`、`DeepSeek-V4.1-Flash` | [Azure AI Foundry](https://ai.azure.com/) → 项目 / 部署 → 密钥 |

> 🪄 模型列表只是**输入建议**，你可以直接输入提供商支持的任何模型 ID；模型上线后通常无需等待应用更新。
>
> 🧩 **OpenAI 兼容的自建服务**（vLLM、Ollama 的 OpenAI 接口、网关、代理等）也能用：选一个最接近的提供商，改 Base URL，填模型 ID 即可。

<details>
<summary>🔷 <strong>Azure AI Foundry —— 到底该填哪个 URL？</strong>（点击展开）</summary>

同一个部署，Azure 可能给你多种地址。按简单到进阶排列：

| 你的情况 | 填什么 Base URL | Deployment name 填什么 |
|---|---|---|
| 🟢 资源级 OpenAI v1 端点（**推荐**） | `https://<资源名>.services.ai.azure.com/openai/v1` 或 `https://<资源名>.openai.azure.com/openai/v1` | 在 Foundry 里看到的**部署名称**（不是模型市场里的模型 ID） |
| 🟡 项目端点 + Entra ID 令牌 | `https://<资源名>.services.ai.azure.com/api/projects/<项目名>` | 部署名称 |
| 🟠 完整 Responses 地址 | `https://<资源名>.services.ai.azure.com/openai/v1/responses` | 部署名称 |
| 🟠 完整 Claude Messages 地址 | `https://<资源名>.services.ai.azure.com/anthropic`（完整地址可能以 `/v1/messages` 结尾） | 你的 Claude 部署名称 |
| ⚪️ 旧版 deployment 地址 | `https://<资源名>.openai.azure.com/openai/deployments/<部署名>/chat/completions` | 必须和 URL 里的部署名一致 |

- 🔑 **API Key** 适用于推荐的资源级端点；最稳妥的做法是直接复制部署页“代码示例”里的 URL。
- 🎫 **Entra ID 访问令牌**适用于项目路由；在应用里把身份验证选为 **Microsoft Entra access token**，把令牌粘贴到密钥框。令牌会过期，需要手动更新。
- 📌 **项目端点 + 资源 API Key** 的组合通常会被 Azure 拒绝 —— 请改用资源级 `/openai/v1` 地址。
- ⚙️ 使用 v1 地址时 **API version 留空**；只有旧版端点才需要填 `api-version`（在 Advanced 里填）。

</details>

### 🔑 API Key 是怎么保存的？

- 🔒 Key 用 **Windows DPAPI** 加密，保存在本地数据目录，不会进 Git，也不会明文保存。
- 🔁 保存后仍可在界面上 **复制 / 替换**。
- 🚫 Oxo Tracker 不会中转或收集你的请求；请求直接从你的电脑发往你配置的模型服务。

---

## 🧰 各个工作区是干什么的？

| 工作区 | 用途 |
|---|---|
| 🧭 **Dashboard** | 资产与准备度总览：目标、Recipe、Cookbook、攻击模块、近期证据。 |
| 🧪 **Benchmark** | 向导式评测流程：选择目标 → 选择 Cookbook/Recipe → 运行并监控。 |
| 🤖 **Agents** | 目标与连接器、红队会话、Agent 安全审查画布。 |
| 📚 **Payload** | 数据集、Prompt 模板、Recipe、Cookbook、攻击模块 —— 所有测试的积木。 |
| 🕘 **History** | 所有基准评测运行记录：详情、Prompt 轨迹、报告与下载。 |
| ⚙️ **Settings** | AI 提供商、主题、界面大小、语言。 |

<img src="images/payload-library.png" alt="Payload 资产库" width="100%" />

---

## 🧪 内置评测内容（开箱即用）

Oxo Tracker 内置了本地化的 Moonshot 资产库，无需联网下载数据集即可开始：

- 📚 **19 个 Cookbook**（IMDA Starter Kit、Capability、Trust & Safety、Others）
- 🧾 **120 个 Recipe**，覆盖幻觉、数据泄露、对抗性提示词、不良内容等
- 🗂️ **221 个数据集**（含标准答案与策略标签）
- 🧬 **31 个 Prompt 模板** + **15 个攻击模块**，用于提示词变形与红队测试

你也可以在 **Payload** 工作区创建自己的数据集、Prompt 模板、Recipe 和 Cookbook，全部保存在本地。

---

## 💻 系统要求

| ✅ 需要 | 说明 |
|---|---|
| 🪟 Windows 10 / Windows 11，**x64** | 目前只提供 Windows 桌面版。 |
| 🌐 Microsoft Edge WebView2 运行时 | 现代 Windows 已内置；安装包内含离线安装能力。 |
| 💾 约 600 MB 可用磁盘空间 | 安装包内置离线 WebView2、本地数据集与 NLTK 资源。 |
| 🔑 至少一个模型提供商的 API Key | 调用模型必需；部分提供商有免费试用额度。 |
| 🌍 可访问互联网 | 访问被测模型 API 和在线 AI 设置时需要。 |

> 🚫 不需要显卡、本地模型权重、Python 或 Node.js —— 安装包是自包含的。

---

## 🔐 隐私、数据与安全

- 🏠 **本地优先**：评测任务、红队会话、设置、报告与证据都保存在 `%LOCALAPPDATA%\com.oxoai.oxo-tracker`。
- 🔒 **凭据加密**：模型 API Key 使用 Windows DPAPI 绑定当前 Windows 用户加密保存。
- 🛰️ **无遥测、无云端账号**：应用不做行为统计，网络请求只发往你配置的模型/应用端点及更新检查。
- 📂 **数据属于你**：卸载应用不会删除本地数据目录，可以自行备份或清理。
- 🧑‍💻 **源码私有**：本公开仓库只提供产品介绍与可下载安装包；安全问题请私下联系维护者。

---

## ❓ 常见问题与排障

<details>
<summary><strong>🛡️ Windows 提示“Windows 已保护你的电脑”，安全吗？</strong></summary>

安全。预览版安装包**尚未做代码签名**，SmartScreen 因此会提示。点 **更多信息 → 仍要运行** 即可。后续配置证书签名后会替换为签名版本。
</details>

<details>
<summary><strong>🔑 Test connection 报 “401 / 403 / authentication failed”</strong></summary>

- 确认完整复制了 Key（没有空格或换行）。
- 确认 Key 与 Base URL 属于同一提供商、同一区域。
- 有些模型需要先申请开通，或仅在特定区域可用。
- Azure 场景请确认资源 URL、部署名称都正确，并且该部署允许 API Key 认证。
</details>

<details>
<summary><strong>🔷 Azure 的 URL 在代码示例里能用，但应用里连不上</strong></summary>

请使用**资源级 OpenAI v1 端点**（`https://<资源名>.services.ai.azure.com/openai/v1`）+ API Key，并在 Model 里填**部署名称**。不要把“项目端点”和资源 Key 混用，Azure 通常会拒绝。详见上方的 [Azure 说明](#-支持的模型与-api-key)。
</details>

<details>
<summary><strong>🧪 评测跑完了，但没有结果 / 都是错误？</strong></summary>

- 打开 **History → Details**，查看 Prompt 轨迹和错误列 —— 目标错误（URL 错、超时、请求被拦截）会逐条显示。
- 先在 **Agents → Connectors** 里用 **Test connection** 确认目标本身可用。
- 速率限制（429）或内容过滤通常以错误形式返回，而不是正常回复。
</details>

<details>
<summary><strong>⏸️ 长扫描能暂停、第二天接着跑吗？</strong></summary>

可以。点 **Pause** 后已完成的结果会保存；可以关闭应用，之后在 **History → Details → Resume** 继续。已完成的 Prompt 不会重复请求。
</details>

<details>
<summary><strong>🔄 怎么更新应用？</strong></summary>

预览版通过 [Releases](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases) 页面下载更新安装包覆盖安装。未签名的预览版暂不启用自动更新。
</details>

<details>
<summary><strong>🗑️ 怎么彻底删除本地数据？</strong></summary>

1. 在 **Windows 设置 → 应用** 中卸载 Oxo Tracker。
2. 删除 `%LOCALAPPDATA%\com.oxoai.oxo-tracker`，即可清除设置、会话与任务数据。
</details>

---

## 🔗 相关链接

- ⬇️ **[全部版本 / 下载](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)** —— 每个 Windows 构建都附带校验和、SBOM 与发布说明。
- 📖 **[发布说明](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases)** —— 每个预览版更新了什么。
- 🔐 **源码**：维护在**私有仓库**中，本公开仓库不包含任何源码。
- 🛡️ **安全问题**：请私下联系项目维护者，不要公开提交包含敏感细节的 issue。

---

<div align="center">

### 🚀 准备好了吗？[下载最新版](https://github.com/Oxo-AI-Security/Oxo-Tracker-Releases/releases/latest)，5 分钟完成第一次安全评测。

用 💜 为 AI 安全、红队与负责任的模型评估而做。

<a id="-预览版说明"></a>
<sub>⚠️ <strong>预览版说明：</strong>Windows x64 未签名构建，以 Pre-release 形式发布。首次安装时 Windows SmartScreen 可能提示。当前预览版暂不提供自动更新与代码签名。</sub>

</div>

---
epoch: 1787296323170
mode: agent
backendId: opencode
sessionId: "ses_fdcd915dcffepJtKonTvHmy64p"
agentLabel: "Obsidian Copilot 接入 DeepSeek 使用指南"
usage: '{"usedTokens":39963,"contextWindow":1000000,"updatedAt":1787296619349}'
tags:
  - copilot-conversation
---

**user**: 请你根据我提供的内容替我完成这篇文档的编写：
1.在DeepSeek平台获取API Key
2.在Obsidian插件市场下载Copilot插件
3.通过BYOK输入自定义模型（DeepSeek）的API Key
4.下载OpenCode
5.开始使用
每一点都要以3级标题开头
[Timestamp: 2026/08/21 15:12:03]

**ai**: 我先加载 Obsidian 语法技能并核实 OpenCode 与 Copilot 插件的最新安装/配置细节，然后为你完成这篇文档。已获取到 OpenCode 官方文档和 Copilot 插件最新信息。我再核实一下 Copilot 的 BYOK 与 DeepSeek 具体配置步骤。已核实完毕（OpenCode 官方文档 + Copilot 插件 V4 的最新文档）。现在完成这篇文档：文档已完成。我快速检查一下最终内容：文档已完成，共 101 行，五个章节均按要求以三级标题开头。写作前我核实了 OpenCode 官方文档和 Copilot 插件 V4 的最新说明，确保步骤与当前版本一致。

内容结构如下：

- **### 1. 在 DeepSeek 平台获取 API Key** — 注册平台、创建密钥的步骤，附密钥安全警告（callout）、计费说明，以及后续会用到的 API 地址和模型 ID 速查表
- **### 2. 在 Obsidian 插件市场下载 Copilot 插件** — 关闭限制模式、浏览安装、启用，并链到了你的 [[05 Obsidian 插件]] 笔记
- **### 3. 通过 BYOK 输入自定义模型（DeepSeek）的 API Key** — Add a provider 流程、自定义供应商的 Base URL / 模型填写方式，以及密钥存储在 Obsidian Keychain（不会随 vault 同步）的说明
- **### 4. 下载 OpenCode** — 两种方式：Copilot 托管下载（推荐）+ 独立安装（Windows 的 Scoop/Chocolatey/npm 命令、macOS/Linux 脚本），含 WSL 提示
- **### 5. 开始使用** — 分「Obsidian 中的 Copilot」（Agent 图标、Quick Chat、Quick Ask）和「终端中的 opencode」（`/connect`、`/init`、Tab 切换 Plan/Build 模式等）两部分

几个要点说明：

1. 核实中发现 Copilot V4 的 Agent 模式正是由 opencode 驱动的，所以整篇文档按「同一个 DeepSeek Key 服务两处」的逻辑组织，开头引言也点明了这个关系。
2. 模型名使用了 DeepSeek API 的稳定 ID：`deepseek-chat`（通用对话）和 `deepseek-reasoner`（深度推理）。
3. 计费与赠送额度这类会变动的信息，我都用了「以平台页面为准」的措辞，避免写死。

如果你想在开头加 frontmatter（比如 `tags`、创建日期），或者需要补充截图占位符，告诉我即可。
[Timestamp: 2026/08/21 15:12:03]
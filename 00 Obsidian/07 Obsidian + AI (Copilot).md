
---

本文记录在 Obsidian 中接入 AI 的完整流程：安装 **Copilot** 插件，通过 **BYOK 方式**接入 DeepSeek 大模型，并**安装 opencode 作为 Agent 后端**<u>（Copilot V4 的 Agent 模式由 opencode 驱动）</u>。两者共用一个 DeepSeek API Key，按实际调用量计费。

---

### 在 DeepSeek 平台获取 API Key

1. 打开 DeepSeek 开放平台：<https://platform.deepseek.com>，使用手机号或邮箱注册并登录。
2. 在左侧菜单进入 **API Keys** 页面，点击 **创建 API Key**。
3. 为密钥命名（例如 `Obsidian`），点击创建。
4. **立即复制并妥善保存**——密钥只在创建时完整显示一次，之后无法再次查看。

> [!warning] 密钥安全
> API Key 相当于账户密码，请勿截图分享、发送给他人或提交到公开的 Git 仓库。一旦泄露，应立即在平台删除该密钥并重新创建。

- 后续步骤会用到以下信息：

| 项目     | 值                                               |
| ------ | ----------------------------------------------- |
| API 地址 | `https://api.deepseek.com`                      |
| 模型 ID  | `deepseek-chat`（通用对话）、`deepseek-reasoner`（深度推理） |

### 在 Obsidian 插件市场下载 Copilot 插件

1. 打开 **设置 → 第三方插件**。
2. 首次使用需要先关闭「限制模式」（旧版本称为安全模式），Obsidian 会弹出风险提示，点击确认即可。关于插件与安全模式的更多介绍见 [[05 Obsidian 插件]]。
3. 在搜索框中输入 `Copilot`。
4. 找到由 **Logan Yang** 开发的 Copilot 插件，点击 **安装（Install）**，完成后点击 **启用（Enable）**。
5. 启用成功后，左侧边栏会出现 Copilot 的 **Agent** 图标。

### 通过 BYOK 输入自定义模型（DeepSeek）的 API Key

**BYOK（Bring Your Own Key）即「自带密钥」**，让 Copilot 直接使用你自己购买的模型服务，费用与用量都归属于 DeepSeek 平台，无需购买 Copilot 套餐。

1. 打开 **设置 → Copilot → BYOK**。
2. 点击 **Add a provider**。
3. 在供应商列表中选择 **DeepSeek**；若列表中没有 DeepSeek，则选择 **Add a custom provider**（添加自定义供应商），按 OpenAI 兼容接口填写：
   - **Base URL：** `https://api.deepseek.com`
   - **API Key：** 粘贴第 1 步保存的密钥
   - **Model：** 输入 `deepseek-chat`（或 `deepseek-reasoner`）
4. 点击 **Test** 验证连接，显示成功后再点击 **Save** 保存。
5. 回到 **设置 → Copilot → Basic → Agents**，确认刚添加的模型已在 **Quick Chat** 与 **opencode** 中启用，并将其设为默认模型。

> API Key 保存在本机的 Obsidian Keychain 中，不会写入 vault 的 `data.json`；因此同步 vault 不会把密钥带到其他设备。

### 下载 OpenCode

opencode 是一款开源的 AI Agent 终端应用，Copilot V4 的 Agent 模式正是由它驱动。安装方式有两种：

1. 打开 **设置 → Copilot → Basic → Agents**，选择 **opencode** 标签。
2. 点击 **Download opencode**，插件会自动下载程序并托管管理，无需手动配置。
3. 如果已经自行安装过 opencode，点击 **I already have it** 手动指定程序路径即可。

### 开始使用

#### 在 Obsidian 中使用 Copilot

1. 点击左侧边栏的 **Agent** 图标。
2. 若弹出「Select your agent」，选择已安装的 **opencode** 并点击 **Start chat**。
3. 在输入框旁选择模型（如 `deepseek-chat`）与运行模式，然后描述你的需求。适合初次尝试的请求：

> 「检查 vault 中未完成的任务，并制定一个简短的执行计划。」

- **Quick Chat：** 打开 Copilot 聊天面板，适合不需要 Agent 的短对话。
- **Quick Ask：** 在 **设置 → 快捷键** 中为其设置热键，可以在不离开当前笔记的情况下，针对选中文字就地提问、改写或翻译。

> Copilot 与 opencode 共用同一个 DeepSeek API Key，费用按实际调用量计费，可在 DeepSeek 平台的「用量信息」页面查看。

### 自定义命令

> 选中文段后 右键 → Copilot → **默认命令 + 自定义命令**

打开 **设置 → Copilot → Command**，点击 **Generate Default**，生成默认的自定义命令 (预设提示词) ，支持**自定义**。

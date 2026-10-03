# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 60 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

> **Requirements** | **要求**  
> Claude Code 2.1.287 or higher | Claude Code 2.1.287 或更高版本

---

## 🚀 Quick Start | 快速开始

### Add This Marketplace | 添加此市场

Run in Claude Code | 在 Claude Code 中运行：

```
/plugin marketplace add shuizhengqi1/cc-mod-hub
```

### Install a Mod | 安装 mod

Install any mod from this marketplace | 从此市场安装任意 mod：

```
/plugin install <mod-name>@cc-mod-hub
```

**⚠️ Important | 重要提示**: Mods run with the same access as Claude Code. Only install mods from sources you trust. | Mod 以与 Claude Code 相同的访问权限运行，请仅从您信任的来源安装 mod。

---

## 📖 English

### What is cc-mod-hub?

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 60 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (Chinese descriptions with source links)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 60 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 60 个精选 Claude Code mods：


### 内置 Mod

这些 mod 来自 Claude Code 核心仓库。

#### diff
在面板中显示未提交的更改。  
**来源**：https://github.com/anthropics/claude-code/tree/main/mods/diff

#### agents-md
通过 prompt.context 和 Read 工具调用加载 AGENTS.md 文件。  
**来源**：https://github.com/anthropics/claude-code/tree/main/mods/agents-md

#### sec-default
安全防护，防止用户 mod 覆盖托管钩子。  
**来源**：https://github.com/anthropics/claude-code/tree/main/mods/sec-default

#### telemetry
分析助手，当分析功能关闭时不发送任何数据。  
**来源**：https://github.com/anthropics/claude-code/tree/main/mods/telemetry

### 官方示例 Mod

这些 mod 来自 Anthropic 的官方示例仓库。

#### token-weather
在提示框上方显示上下文预报。  
**许可证**：Apache-2.0  
**来源**：https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/token-weather

#### blast-radius
为风险 Bash 命令提供继续/取消提示。  
**许可证**：Apache-2.0  
**来源**：https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/blast-radius

#### replay-theater
逐步回放上一轮的文件编辑。  
**许可证**：Apache-2.0  
**来源**：https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/replay-theater

### 社区 Mod

这些 mod 由社区开发者贡献。

#### cache-tax
提供 /keepwarm 命令，阻止一次冷启动发送。  
**来源**：https://github.com/karanb192/cache-tax

#### claude-council
并行运行多个编码代理，可并排查看。  
**来源**：https://github.com/hex/claude-council

#### winnow
精简大型未使用的工具结果。  
**来源**：https://github.com/GhalebDweikat/winnow

#### flowpane
实时显示工作流程图。  
**来源**：https://github.com/mpolatcan/flowpane

#### pixelband
在提示框上方显示像素艺术。  
**来源**：https://github.com/furqan-khan07/pixelband

#### cc-side
提供 /side 命令开启第二个对话。  
**来源**：https://github.com/Ahmad8864/cc-side

#### ContextSaver
标记浪费会话习惯。  
**许可证**：MIT  
**来源**：https://github.com/AlmogBaku/ContextSaver

#### cc-arcade
在提示框上方显示游戏，点击不会调用模型。  
**来源**：https://github.com/sezaakgun/cc-arcade

#### mindful-claude
显示呼吸带。  
**来源**：https://github.com/halluton/Mindful-Claude

#### 12ui-plugin
提供设计面板。  
**来源**：https://github.com/just-every/12ui-plugin

#### cueloop
tool.call mod。  
**许可证**：Apache-2.0  
**来源**：https://github.com/mmurakaru/cueloop

#### lcm
tool.call / prompt.submit mod。  
**许可证**：MIT  
**来源**：https://github.com/lossless-claude/lcm

#### taskcut
turn.step mod。  
**许可证**：MIT  
**来源**：https://github.com/wasd96040501/taskcut

#### Katharsis
prompt.submit mod。  
**许可证**：MIT  
**来源**：https://github.com/OpenScribbler/Katharsis

#### fast-jev-compaction
session.compact mod。  
**来源**：https://github.com/tamaratran/fast-jev-compaction

#### claude-image-generation
通过 tool.call 生成图像。  
**来源**：https://github.com/hex/claude-image-generation

#### constellation-claude
注册导出 mod。  
**许可证**：AGPL-3.0  
**来源**：https://github.com/ShiftinBits/constellation-claude

#### usage-band
在提示框上方显示 5 小时/7 天限额、上下文窗口与缓存命中率。  
**许可证**：MIT  
**来源**：https://github.com/JetsonChan/CC-Usage-Band

#### glass
给终端 transcript 换桌面级外观：着色命令、工具树、回合页脚等。  
**许可证**：MIT  
**来源**：https://github.com/rashedInt32/glass

#### trek-band
提示框上方星际迷航风格用量环与像素动画场景。  
**许可证**：MIT  
**来源**：https://github.com/rb17080/trek-band

#### clawd
思考行旁的像素 Clawd 吉祥物，按工具/命令表演动作。  
**来源**：https://github.com/raresmun/claude-mods/tree/main/plugins/clawd

#### cctop
btop 风格侧栏面板，展示上下文、tokens、成本、工具延迟等。  
**来源**：https://github.com/tomstagl/cctop

#### terminal-browser
在会话旁嵌入终端浏览器，预览网页/本地 HTML/PR。  
**许可证**：MIT  
**来源**：https://github.com/zenbu-labs/terminal-browser

#### effort-cycle
Alt+E / Alt+Shift+E 切换 effort，页脚显示模型与档位。  
**许可证**：MIT  
**来源**：https://github.com/Anerco/claude-code-effort-cycle

#### claude-mermaid
把助手回复里的 mermaid 块画成彩色 box art。  
**来源**：https://github.com/galElmalah/claude-mods/tree/main/claude-mermaid

#### claude-queue
/q 在回合进行中排队提示，回合结束后自动发出。  
**来源**：https://github.com/galElmalah/claude-mods/tree/main/claude-queue

#### statuspane
提示框上方浮动状态卡：模型、effort、上下文、5 小时/周限额、费用与分支，另有可供脚本/其他 mod 写入的进度条 API。  
**许可证**：MIT  
**来源**：https://github.com/xuanji86/claude-statuspane

#### effort-guard
上下文/token 条带、升级信号与每回合 effort 日志。  
**许可证**：MIT  
**来源**：https://github.com/stefanochieli/claude-effort-guard

#### gsd-status-mod
面向 GSD 项目：在提示框上方显示阶段/进度与 STATE.md 漂移警告，并把下一步动作放进提示行。  
**许可证**：MIT  
**来源**：https://github.com/helenkwok/gsd-status-mod

#### skins
给 transcript 换肤：主题化工具行、回复边栏与 spinner 文案；桌面端把表格/代码/diff/shell 画成动画卡片。  
**许可证**：MIT  
**来源**：https://github.com/hellosverre/claude-skins

#### cc-pr-tracker
在提示框上方盯着 GitHub PR 的合并状态、评审与必需检查，有变化时 toast。  
**许可证**：MIT  
**来源**：https://github.com/sezaakgun/cc-pr-tracker

#### intermission
Claude 工作时在 Ghostty/kitty 窗格里开 Doom 死斗，回合结束或需要输入时自动切回。  
**许可证**：MIT  
**来源**：https://github.com/jarrodwatts/intermission

#### editor-context
在桌面端提示框上方显示 Cursor/VS Code 当前文件与选区，并在每次提交时把你正在看的内容悄悄告诉 Claude。  
**许可证**：MIT  
**来源**：https://github.com/talbarina/claude-editor-context

#### prompter
边聊边整理需求：把零散想法变成干净 brief，并填入本仓库上下文。  
**来源**：https://github.com/niijoey/prompter-mod

#### next-steps
回合结束后在提示框上方建议最多 3 条下一步 prompt（可按 1/2/3 填入草稿，0 关闭）。  
**许可证**：MIT  
**来源**：https://github.com/anthropics/claude-plugins-community/tree/main/next-steps

#### pet
侧栏/状态行里的毒舌 ASCII 火烈鸟：替 Claude 说话、吐槽你的代码，还可喂养换装。  
**许可证**：MIT  
**来源**：https://github.com/graugart/flingo

#### pets
像素宠物住在 Claude Code 面板里，随工具调用/回合反应并跨会话升级。  
**许可证**：MIT  
**来源**：https://github.com/uppinote20/claude-pets

#### dev-dash
开发者仪表盘面板：会话/子代理、用量限额、git 与 PR 等注意力信息。  
**许可证**：MIT  
**来源**：https://github.com/RanaRauff/claude-dev-dashboard/tree/main/plugins/dev-dash

#### avatar7
可切换人设的机器脸，围观 tool.call 并用角色语气点评。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/avatar7

#### usage-bell
接近上下文/5 小时/7 天限额或自动记忆索引上限时响铃并显示状态行。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/usage-bell

#### mesh7-pane
只读面板展示 mesh7 治理决策（ALLOW/DENY/HUMAN）与待审批（需本机 mesh7）。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/mesh7-pane

#### jukebox7
用自然语言点播 YouTube 音频（本地播放），带小型控制面板。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/jukebox7

#### atelier-bell
atelier/flux7-studio 渲染完成时 toast 与状态行提醒。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/atelier-bell

#### fable-pin
把每个 subagent 的 model 钉到 Fable（/fable-pin on|off|status）。  
**来源**：https://github.com/karanb192/claude-code-mods/tree/main/plugins/fable-pin

#### image-peek
macOS 粘贴图片时在标记旁预览（本地剪贴板，零模型）。  
**来源**：https://github.com/karanb192/claude-code-mods/tree/main/plugins/image-peek

#### git-gates
拦截 git commit/push/merge，需用户授权并校验 Conventional Commits。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/git-gates

#### lean-comments
限制注释过多的 Edit/Write，超预算跟进精简。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-comments

#### lean-docs
文档卫生：拦重复叙述代码的文档。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-docs

#### lean-scripts
新脚本写入后判断是否值得保留。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-scripts

#### claude-games
提示框上方四款街机小游戏，随测试/提交反应，零 token。  
**许可证**：MIT  
**来源**：https://github.com/mohi-devhub/claude-games

#### segmem
本地 SQLite 长期记忆，按 prompt/Bash 召回。  
**来源**：https://github.com/mahuebel/segmem

#### tw-stock-mod
提示框上方台股/美股/加密货币看板与持仓盈亏（Yahoo，零模型）。  
**许可证**：MIT  
**来源**：https://github.com/darrell-tw/darrelltw-mods/tree/main/mods/tw-stock-mod

#### agent-router
按角色为 subagent 指定模型/effort（需兼容网关），带活动面板。  
**许可证**：MIT  
**来源**：https://github.com/alexandernicholson/agent-router/tree/main/agent-router

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

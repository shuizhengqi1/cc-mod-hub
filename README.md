# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 56 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

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

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 56 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (Chinese descriptions with source links)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 56 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 56 个精选 Claude Code mods：


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

#### overalls
提示框上方状态条：上下文预报、用量限额，以及 Ponytail/Caveman 档位（可配置）。  
**许可证**：MIT  
**来源**：https://github.com/Troepster/overalls

#### clawd-spinner
Clawd 按 spinner 词表演动画（本地绘制，零 token）。  
**许可证**：MIT  
**来源**：https://github.com/saiharsha03/clawd-spinner

#### env
在面板里编辑 .env；Claude 管理键名但看不到真实密钥值。  
**许可证**：MIT  
**来源**：https://github.com/davekiss/env

#### ctx-handoff
上下文达阈值时自动生成 handoff 并 /clear；空闲时还能续热缓存。  
**来源**：https://github.com/cablate/ctx-handoff-mod

#### eta
在 spinner 行显示本轮剩余时间（按任务节奏或历史回合学习，零 token）。  
**来源**：https://github.com/hamza-siddiq/claude-eta/tree/main/eta

#### md-prompt
输入时把 prompt 框画成 Markdown（代码块高亮等，不改原文）。  
**许可证**：MIT  
**来源**：https://github.com/nogu66/md-prompt/tree/main/plugins/md-prompt

#### plushie
提示框上方的毛绒 Clawd，会随工具/上下文做出反应。  
**许可证**：MIT  
**来源**：https://github.com/xyc/plushie

#### micro-compaction
提供 `/compact micro`：精简 Read 结果并去掉 thinking，保留对话结构。  
**许可证**：Unlicense  
**来源**：https://github.com/ruihe774/cc-micro-compaction

#### aside
`/aside` 只读侧聊：基于会话 transcript fork 问答，不写回主线程。  
**许可证**：MIT  
**来源**：https://github.com/JayDoubleu/aside

#### lightbox
粘贴图片时在提示框上方大预览，并带说明缩略图。  
**许可证**：MIT  
**来源**：https://github.com/arihantbansal/claude-lightbox

#### gfm-render
在 transcript 里渲染 GFM：alerts、任务列表、删除线与 Mermaid。  
**许可证**：MIT  
**来源**：https://github.com/briangtn/claude-gfm-render

#### session-brief
提示框上方保持会话简报；`/brief` 补充已做决定与下一步。  
**来源**：https://github.com/skanehira/claude-session-brief

#### rtl-text
用 fribidi 把波斯语/阿拉伯语/希伯来语在 transcript 里按 RTL 整形对齐。  
**来源**：https://github.com/aliir74/claude-code-rtl

#### catch-me-up
侧栏实时 catch-up 摘要：为何开始、做了什么、卡在哪里。  
**许可证**：MIT  
**来源**：https://github.com/oliverow/catch-me-up

#### linear-claude-mod
Linear 指派工单面板；点击可加载详情、评论或改状态。  
**许可证**：MIT  
**来源**：https://github.com/rjohnt/linear-claude-mod

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

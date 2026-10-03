# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 102 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

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

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 102 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (Chinese descriptions with source links)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 102 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 102 个精选 Claude Code mods：


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

#### secret-redactor
在模型看到前把密钥/邮箱/IP 换成占位符，工具输入时再还原。  
**来源**：https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/secret-redactor

#### vercel-deploy-status
提示框上方显示 Vercel 部署队列（零 token）。  
**来源**：https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/vercel-deploy-status

#### pii-guard
台湾 PII 可逆脱敏（经本地 hookd）；需 Python/uv。  
**来源**：https://github.com/danyuchn/pii-guard/tree/main/examples/claude-code-mod

#### prompt-rail
提示条/侧栏：悬停读、点击跳回历史 prompt。  
**来源**：https://github.com/oikon48/prompt-rail/tree/main/plugins/prompt-rail

#### agent-flow
/flow 侧栏实时显示 subagent 树（零 token）。  
**来源**：https://github.com/Charlie0113-T/claude-agent-flow

#### plan-progress
计划进度条 + 子代理条带。  
**来源**：https://github.com/zycck/claude-mods/tree/main/plugins/plan-progress

#### context-lens
固定显示上下文占用、增长与距 compaction 的回合数。  
**来源**：https://github.com/Arunjay4213/claude-mods/tree/main/plugins/context-lens

#### budget-guard
费用与 5 小时/7 天限额：接近上限警告，超额拒绝工具调用。  
**来源**：https://github.com/Arunjay4213/claude-mods/tree/main/plugins/budget-guard

#### quota-meter
计划限额条与重置倒计时。  
**来源**：https://github.com/Arunjay4213/claude-mods/tree/main/plugins/quota-meter

#### token-ledger
会话成本与上轮 tokens；面板查看近期回合。  
**来源**：https://github.com/Arunjay4213/claude-mods/tree/main/plugins/token-ledger

#### gh-ci-status
提示框上方钉住 GitHub Actions 状态。  
**来源**：https://github.com/diegorv/claude-functions-hook/tree/main/plugins/gh-ci-status

#### time
每条用户消息上方显示发送时间。  
**来源**：https://github.com/diegorv/claude-functions-hook/tree/main/plugins/time

#### firstmate-calm
/calm 隐藏工具行并换成帆船 spinner；需开启 function hooks。  
**来源**：https://github.com/kunchenguid/firstmate/tree/main/.claude/mods/firstmate-calm

#### multi-core
把 ChatGPT/Cursor/Zen 等接入 /model（需 claude-multi launcher）。  
**来源**：https://github.com/greenpolo/cc-multi-cli-plugin/tree/main/plugins/multi-core

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
提供 /compact micro：精简 Read 结果并去掉 thinking，保留对话结构。  
**许可证**：Unlicense  
**来源**：https://github.com/ruihe774/cc-micro-compaction

#### aside
/aside 只读侧聊：基于会话 transcript fork 问答，不写回主线程。  
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
提示框上方保持会话简报；/brief 补充已做决定与下一步。  
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

#### darkroom
把 Claude 读/写/生成以及你粘贴的图片做成聊天里的胶片条预览。  
**许可证**：MIT  
**来源**：https://github.com/govlog/claude-darkroom

#### paste-view
在提示框上方预览粘贴的图片缩略图与长文本，不再只显示 `[Image #n]`。  
**许可证**：MIT  
**来源**：https://github.com/Amorfx/claude-paste-view

#### compass
实时会话地图：流程图、任务板与异步提问窗格。  
**许可证**：MIT  
**来源**：https://github.com/gil2abir/claude-compass

#### conversation-atlas
长会话侧栏地图：目标、路径、决策、未决问题与证据轨。  
**许可证**：MIT  
**来源**：https://github.com/NeelAPatel/Claude-Mod-ConversationAtlas

#### pult
提示框上方快捷回复与状态带，侧栏卡片显示用量、缓存、截止日期与服务器。  
**许可证**：MIT  
**来源**：https://github.com/Egor062020/claude-code-pult

#### claude-stats
提示框上方显示 5h/7d 限额与 ccusage 花费条。  
**来源**：https://github.com/estruyf/claude-stats-mod

#### typing-speed
提示框上方打字速度计，提交后显示 WPM/准确率与个人最佳。  
**许可证**：MIT  
**来源**：https://github.com/borabiricik/claude-mods/tree/main/plugins/typing-speed

#### context-dungeon
把真实会话做成肉鸽：上下文是 HP，报错出怪，绿测击杀，提交开宝箱（只观察 tool.call）。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/context-dungeon

#### speedrun-splits
LiveSplit 风格计时条，在侦察/首次编辑/测试/提交等节点自动分段。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/speedrun-splits

#### departure-board
Solari 翻牌式出发板，把代理当前任务翻成车站到发显示。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/departure-board

#### netrunner-hud
赛博朋克会话仪表盘：上下文条、token 示波与实时状态窗格。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/netrunner-hud

#### boot-sequence
会话开始时 BIOS 风格开机检查（git/工具链等）。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/boot-sequence

#### transit-map
把 git 历史画成维涅利风格地铁图（分支为线、提交为站）。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/transit-map

#### codebase-galaxy
仓库文件力导向星空（盲文点阵），跟随 Claude 触达的文件。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/codebase-galaxy

#### fault-lacquer
失败操作在漆片上裂开，修复后金缮愈合的会话视觉。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/fault-lacquer

#### minefield
Claude 工作时在窗格里玩经典扫雷。  
**许可证**：MIT  
**来源**：https://github.com/reporails/arcade/tree/main/minefield

#### prayer-times
提示框下方显示下次礼拜时间，到时轻提醒。  
**许可证**：MIT  
**来源**：https://github.com/mkbuilds4/mods/tree/main/plugins/prayer-times

#### limit-bars
提示框下四个动画盲文环：上下文、会话、周限额等。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/limit-bars

#### transcript-fx
给 transcript 上色：工具块、提示面板、动画 spinner 与彩虹回合脚。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/transcript-fx

#### reply-highlight
用彩虹边与紫色底突出 Claude 回复。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/reply-highlight

#### backlog-pane
侧栏展示 git 状态与 Backlog.md 任务，可开始/完成/新建。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/backlog-pane

#### plan-progress-fx
plan-progress 分支：终端下动画彩虹像素进度条。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/plan-progress-fx

#### pro-hud
Pro 计划 HUD：精确 5h/7d 表盘、上下文与回合回执。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/pro-hud

#### cache-clock
显示提示缓存还热多久，过期后下一句会重送多少 tokens。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/cache-clock

#### context-xray
窗格拆解上下文占用：系统提示、工具、记忆、skills、消息。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/context-xray

#### session-receipt
`/receipt` 窗格列出每回合精确 token 花费。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/session-receipt

#### cache-timer
倒计时提示缓存何时过期，方便赶在冷启动前发下一句。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/cache-timer

#### session-meter
`/ctx` 实时窗格：上下文分解、限额节奏、工具与模型请求。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/session-meter

#### turn-timeline
`/timeline` 把当前回合画成时间线（请求/工具/耗时）。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/turn-timeline

#### turn-footer
把每条回答下方改成回合摘要（工具、请求、tokens、缓存命中）。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/turn-footer

#### pin-board
`/pin` 钉住常驻说明，compact/clear 后仍保留并显示在提示框上方。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/pin-board

#### show-me
`/show-me` 把回答里的 mermaid 画成窗格图片（需 mmdc/kitty）。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/show-me

#### change-ledger
`/changes` 列出本会话编辑过的文件与行数，对照 git 工作树。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/change-ledger

#### ci-watch
push/开 PR 后在提示框上方盯着 GitHub Actions 进度条。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/ci-watch

#### plan-bar
提示框上方多计划进度条（阶段、百分比、等待/失败色）。  
**许可证**：MIT  
**来源**：https://github.com/homieyangg/claude-code-mods/tree/main/plan-bar

#### leftovers
记账 Claude 留在本机/服务器上的后台进程与残留。  
**许可证**：MIT  
**来源**：https://github.com/homieyangg/claude-code-mods/tree/main/leftovers

#### deadlines
状态行截止日期倒计时；`/ddl` 增删列表。  
**来源**：https://github.com/richardcsuwandi/claude-mods/tree/main/plugins/deadlines

#### bdt-status
提示框上方显示当前分支 PR/关联 issue 与构建状态（`bdt pr info`）。  
**来源**：https://github.com/bmsuisse/skills/tree/main/mods/bdt-status

#### cc-idle
挂在 Claude 旁边的放置游戏，只吃 Claude 实际工作产出。  
**许可证**：MIT  
**来源**：https://github.com/RichardAtCT/cc-idle/tree/main/plugins/cc-idle

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

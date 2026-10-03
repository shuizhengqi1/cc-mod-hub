# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 299 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

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

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 299 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (Chinese descriptions with source links)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 299 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 299 个精选 Claude Code mods：


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

#### next-steps
每轮结束后在输入框上方建议最多三个下一步提示，可按数字键快速填入；fork 会话向模型问询并共享提示缓存，成本低廉。  
**来源**：https://github.com/anthropics/claude-plugins-community/tree/main/next-steps

#### pet
一只嘴碎的火烈鸟吉祥物 Flingo，在侧栏或状态行陪伴你码字，代 Claude 说话、吐槽代码、喂养玩耍、换装（皇冠、礼帽、蝴蝶结、墨镜），用 /flingo 聊天。  
**许可证**：MIT  
**来源**：https://github.com/graugart/flingo

#### pets
像素宠物窗格：闲逛、记笔记、完成回合时跳跃、限额 80% 流泪、闲置两分钟午睡；八种动物（猫、小鸡、狗、史莱姆、兔子、仓鼠、企鹅、青蛙），可命名、喂食、升级，跨会话记忆。  
**许可证**：MIT  
**来源**：https://github.com/uppinote20/claude-pets

#### dev-dash
开发者仪表板窗格，集中显示会话状态与项目信息。  
**来源**：https://github.com/RanaRauff/claude-dev-dashboard/tree/main/plugins/dev-dash

#### avatar7
机器脸随工具调用作评论，可选声线（SHODAN、HAL、GLaDOS 风格实验室 AI、Ada、duck7、Pod 042、Kaneda、Commis），在人类决策时陪伴等待并朗读通知。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/avatar7

#### usage-bell
接近限额时响铃：上下文占用（70/85/95%）、5 小时/7 天限额（80/95%）、自动记忆索引达 200 行或 25 kB；状态栏显示当前百分比，/usage7 查看详情。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/usage-bell

#### mesh7-pane
从 localhost:9090 每 1.5 秒轮询 mesh7 决策：每次调用的 ALLOW/DENY/HUMAN 及规则参数、待批准请求、紧急停止横幅、状态行计数、每个新拒绝或批准请求时 toast；只读。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/mesh7-pane

#### jukebox7
白话点播音乐（"放点环境音"）：YouTube 音频通过隐藏 VLC 播放，无需浏览器也不抢焦点；窗格带流派按钮（每个是艺人电台）和当值头像的精选。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/jukebox7

#### atelier-bell
告知 atelier 完成时机：flux7-studio 渲染进度显示为 toast 和状态行（studio: rendering、studio: last …），/bell 查看状态。  
**许可证**：MIT  
**来源**：https://github.com/KTCrisis/flux7-mods/tree/main/atelier-bell

#### fable-pin
每个子代理运行你选的模型，不是提示要的那个：在 agent.spawn 时将 model 改写为 fable（除非是 fork 继承父级），/fable-pin on/off 切换，/fable-pin status 查看。  
**来源**：https://github.com/karanb192/claude-code-mods/tree/main/plugins/fable-pin

#### image-peek
文本光标移到粘贴的 [Image #1] 标记上时显示图像，移开隐藏；宽窗口用大预览窗格（深色画布居中），窄窗口用提示框上方区域；键盘焦点保持在提示框。  
**来源**：https://github.com/karanb192/claude-code-mods/tree/main/plugins/image-peek

#### git-gates
Git 工作授权与整洁：追踪用户提示，拦截未授权的 commit/push/merge；检查提交消息（Conventional Commits、issue 引用）和 PR/MR 描述；Haiku 审查。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/git-gates

#### lean-comments
限制注释膨胀：Edit/Write 时标记多注释编辑，回合结束时检查 diff 的新注释行；Haiku 审查不值得保留的注释（复述代码或叙述改动）。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-comments

#### lean-docs
文档值得保留：Haiku 审查 git checkout 中增长的文档（runbook、设置页、叙述）、标记代码重复标识符的文档行、回合结束时检查 diff 的新文档。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-docs

#### lean-scripts
脚本值得保留：Haiku 审查在 git checkout 中写入或增长的脚本，标记那些你需要时直接打出来更快的脚本。  
**来源**：https://github.com/bahaospanov/claude-mods/tree/main/lean-scripts

#### claude-games
提示框上方的街机游戏（/racer、/breakout、/dino、/shooter），在 Claude 工作时玩；游戏对 Claude 的行为作出反应：通过的测试清理道路、失败的测试扔障碍、提交给护盾或炸弹；回合结束时游戏暂停。  
**许可证**：MIT  
**来源**：https://github.com/mohi-devhub/claude-games

#### segmem
长期记忆：区分身份（你是谁）、过程（仓库如何工作）、情节（周二发生了什么）与人物档案；按衰减窗口加载，项目级作用域，压缩历史为摘要，无需服务器或守护进程。  
**来源**：https://github.com/mahuebel/segmem

#### tw-stock-mod
提示框上方的台股/美股观察清单带状栏，台股交易时段显示台股（红涨绿跌）、美股交易时段显示美股（绿涨红跌）；支持 Yahoo 延迟报价或券商即时行情（永豐 shioaji、群益 capital）；显示持仓损益。  
**来源**：https://github.com/darrell-tw/darrelltw-mods/tree/main/mods/tw-stock-mod

#### agent-router
代理路由器，管理子代理调用。  
**来源**：https://github.com/alexandernicholson/agent-router/tree/main/agent-router

#### human-in-the-loop
把只有用户能做的事挂在 My tasks 窗格里，完成后再回给 Claude。  
**许可证**：MIT  
**来源**：https://github.com/tzafrir/human-in-the-loop

#### file-explorer
VS Code 风格文件树/变更/历史/diff 窗格。  
**来源**：https://github.com/tak-kam/claude-mods/tree/main/file-explorer

#### radio
/radio 在会话里听网络电台，状态行与提示框上方控制。  
**来源**：https://github.com/sivori/claude-mods/tree/main/plugins/radio

#### spend-meter
状态行显示会话费用、上下文与 5 小时限额。  
**来源**：https://github.com/sivori/claude-mods/tree/main/plugins/spend-meter

#### commit-drift
状态行未提交文件数与距上次提交时间，久未提交会提醒。  
**来源**：https://github.com/sivori/claude-mods/tree/main/plugins/commit-drift

#### backlog-band
提示框上方显示 BACKLOG.md 的 Now 项。  
**来源**：https://github.com/sivori/claude-mods/tree/main/plugins/backlog-band

#### commonplace-pane
侧边窗格展示芝加哥艺术学院公版画，随仓库状态变「天气」。  
**来源**：https://github.com/sivori/claude-mods/tree/main/plugins/commonplace-pane

#### mize-coworker
像素 Claude 吉祥物，随 spinner 词表演场景，空闲时在状态行呼吸走动。  
**许可证**：MIT  
**来源**：https://github.com/TheMizeGuy/clawdagotchi/tree/main/plugins/mize-coworker

#### usage-meter
提示框上方常显上下文与 5 小时/周限额。  
**来源**：https://github.com/HolyGrail/claude-mods/tree/main/plugins/usage-meter

#### notice-board
同仓库各会话共享通知板。  
**来源**：https://github.com/HolyGrail/claude-mods/tree/main/plugins/notice-board

#### pr-relay
监视会话 PR，合并或 Codex 评论时唤醒。  
**来源**：https://github.com/HolyGrail/claude-mods/tree/main/plugins/pr-relay

#### zsh-safe
把 bash 写法的 Bash 命令改写成 macOS zsh 可跑。  
**来源**：https://github.com/HolyGrail/claude-mods/tree/main/plugins/zsh-safe

#### compact-tools
压缩工具输出显示（含 MCP/Bash 错误）。  
**来源**：https://github.com/AJclemendor/my-mods/tree/main/plugins/compact-tools

#### live-thinking
对话里流式显示 thinking 摘要。  
**来源**：https://github.com/AJclemendor/my-mods/tree/main/plugins/live-thinking

#### sidebar-controls
把 compact-tools/live-thinking 开关放进右上侧栏。  
**来源**：https://github.com/AJclemendor/my-mods/tree/main/plugins/sidebar-controls

#### pr-pane
/prs 提示框上方列出你的 GitHub PR 并可打开。  
**许可证**：MIT  
**来源**：https://github.com/ASRagab/asragab-claude-marketplace/tree/main/plugins/pr-pane

#### hyday-pet
提示框上方虚拟宠物，随 Claude 工作成长、可小游戏/商店。  
**许可证**：MIT  
**来源**：https://github.com/mukiwu/muki-ai-plugins/tree/main/plugins/hyday-pet

#### flash-veille
提示框上方轮播开发者资讯（Human Coders、Anthropic 博客等）。  
**许可证**：MIT  
**来源**：https://github.com/camilleroux/flash-veille/tree/main/plugins/flash-veille

#### pulse-cc
提示框上方显示股票报价（Yahoo 或 Pulse Mac 自选）。  
**许可证**：MIT  
**来源**：https://github.com/fatwang2/Pulse/tree/main/plugins/claude-code

#### action-pin
把常用动作钉在提示框上方。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/action-pin

#### ask-autopick
自动采纳或拒绝提问。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ask-autopick

#### bg-tasks
后台任务管理器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bg-tasks

#### bughunt
追踪与报告 bug。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bughunt

#### cache-warm
缓存预热工具。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/cache-warm

#### commit-cadence
提交节奏提醒。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/commit-cadence

#### config-parse
配置文件解析器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/config-parse

#### context-restore
恢复上下文状态。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/context-restore

#### contract-watch
监视合约变更。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/contract-watch

#### council
代理协商决策。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/council

#### dep-sentinel
依赖变更哨兵。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/dep-sentinel

#### desk-notify
桌面通知提醒。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/desk-notify

#### diagram-render
图表实时渲染。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/diagram-render

#### disk-janitor
清理临时文件。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/disk-janitor

#### doc-drift-watch
监视文档漂移。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/doc-drift-watch

#### edit-loop
编辑循环检测。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/edit-loop

#### effort-auto
自动切换 effort。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/effort-auto

#### env-sync
环境变量同步。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/env-sync

#### error-poke
错误提醒助手。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/error-poke

#### flaky-memory
不稳定记忆诊断。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/flaky-memory

#### gemini-advisor
Gemini 顾问模式。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-advisor

#### gemini-compact
Gemini 压缩助手。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-compact

#### gemini-core
Gemini 核心集成。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-core

#### gemini-plan-review
Gemini 计划审查。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-plan-review

#### gemini-review
Gemini 代码审查。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-review

#### git-commit
Git 提交助手。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/git-commit

#### i18n-watch
国际化监视器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/i18n-watch

#### idle-art
空闲时显示艺术。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/idle-art

#### limit-watch
限额监视器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/limit-watch

#### lockfile-sync
锁文件同步检查。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/lockfile-sync

#### mcp-doctor
MCP 健康诊断。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/mcp-doctor

#### memory-save
记忆保存助手。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/memory-save

#### mod-doctor
Mod 健康检查。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/mod-doctor

#### orphan-server
孤儿进程检测。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/orphan-server

#### output-flood
输出洪水控制。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/output-flood

#### pin-note
固定便签功能。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/pin-note

#### probe-runner
探针运行器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/probe-runner

#### prompt-deck
提示卡片管理。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-deck

#### prompt-offload
提示卸载优化。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-offload

#### prompt-time
提示时间标记。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-time

#### sage-memory
智慧记忆系统。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sage-memory

#### self-command
自定义命令系统。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/self-command

#### session-watch
会话监视器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/session-watch

#### shot-inline
内联截图功能。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/shot-inline

#### sidebar
侧栏扩展面板。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sidebar

#### slash-chain
斜杠命令链。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/slash-chain

#### sql-concat-watch
SQL 拼接监视。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sql-concat-watch

#### storage-guard
存储保护器。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/storage-guard

#### subagent-ledger
子代理账本。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/subagent-ledger

#### task-poke
任务提醒助手。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/task-poke

#### tool-coach
工具使用教练。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/tool-coach

#### ua-fallback
用户代理降级。  
**来源**：https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ua-fallback

#### spx-chart
在侧栏查看 PHP SPX 性能火焰图（需 php-spx-mcp）。  
**来源**：https://github.com/zviryatko/claude-spx

#### cockpit
计划/todo 进度条，并按 quick/normal/hard 路由模型与 effort。  
**来源**：https://github.com/Brxerq/claude-cockpit/tree/main/plugins/cockpit

#### workface
长任务工作笔记，compaction 时保住 workface 状态。  
**来源**：https://github.com/scodge-24/workface

#### handoff-compact
用固定大纲的 handoff 替换默认摘要，少丢决策与否决项。  
**来源**：https://github.com/trytofly94/handoff-compact

#### context-view
提示框上方一行上下文占用与距 auto-compact 余量。  
**来源**：https://github.com/kongyo2/context-view

#### filetree
侧栏文件树，跟住 Claude 正在读/写的文件并可点选带入提示。  
**来源**：https://github.com/data-goblin/claude-code-filetree

#### flightdeck
只读观测面板，集中看权限裁决与子代理进度。  
**来源**：https://github.com/scasella/claude-flightdeck

#### mdview
侧栏渲染对话里的 Markdown，可点选让 Claude 改。  
**来源**：https://github.com/xuanji86/claude-mdview

#### image-view
粘贴图片后在提示框上方显示像素缩略图。  
**来源**：https://github.com/jarrodwatts/claude-image-view

#### burn-meter
提示框上方会话花费「火焰」条与限额，/burn 看每回合费用。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/burn-meter

#### darkroom
把 Claude 读/写/生成以及你粘贴的图片做成聊天里的胶片条预览。  
**许可证**：MIT  
**来源**：https://github.com/govlog/claude-darkroom

#### paste-view
在提示框上方预览粘贴的图片缩略图与长文本。  
**许可证**：MIT  
**来源**：https://github.com/Amorfx/claude-paste-view

#### typing-speed
提示框上方打字速度计，提交后显示 WPM、准确率与个人最佳。  
**许可证**：MIT  
**来源**：https://github.com/borabiricik/claude-mods/tree/main/plugins/typing-speed

#### context-dungeon
把会话做成肉鸽：上下文是 HP，报错出怪，绿测击杀，只观察 tool.call，不改调用。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/context-dungeon

#### departure-board
翻牌式出发板，把当前任务翻成车站到发显示。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/departure-board

#### netrunner-hud
会话仪表盘：上下文条、token 示波与状态窗格。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/netrunner-hud

#### boot-sequence
会话开始时做一次本机开机检查（git、工具链）。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/boot-sequence

#### transit-map
把 git 历史画成地铁图，分支是线，提交是站。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/transit-map

#### codebase-galaxy
用盲文点阵把仓库文件画成星空，跟着 Claude 碰过的文件。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/codebase-galaxy

#### fault-lacquer
失败的操作在漆片上裂开，修好后愈合。  
**许可证**：MIT  
**来源**：https://github.com/ccdwyer/fault-lacquer

#### minefield
Claude 工作时在窗格里玩扫雷。  
**许可证**：MIT  
**来源**：https://github.com/reporails/arcade/tree/main/minefield

#### prayer-times
提示框下方显示下次礼拜时间。  
**许可证**：MIT, except hooks/times.ts is LGPL-3.0.  
**来源**：https://github.com/mkbuilds4/mods/tree/main/plugins/prayer-times

#### limit-bars
提示框下四个动画环，显示上下文、会话和周限额。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/limit-bars

#### transcript-fx
给 transcript 上色：工具块、提示面板和 spinner。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/transcript-fx

#### reply-highlight
用彩虹边和紫色底突出 Claude 的回复。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/reply-highlight

#### backlog-pane
侧栏看 git 状态和 Backlog.md 任务。  
**许可证**：MIT  
**来源**：https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/backlog-pane

#### pro-hud
Pro 计划用量表盘：5 小时、7 天限额、上下文和回合回执。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/pro-hud

#### cache-clock
显示提示缓存还热多久。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/cache-clock

#### context-xray
窗格拆开上下文占用：系统提示、工具、记忆、skills、消息。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/context-xray

#### session-receipt
/receipt 窗格列出每回合的 token 花费。  
**许可证**：MIT  
**来源**：https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/session-receipt

#### cache-timer
倒计时提示缓存何时过期。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/cache-timer

#### turn-timeline
/timeline 把当前回合画成时间线。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/turn-timeline

#### turn-footer
每条回答下方改成回合摘要（工具、请求、tokens、缓存命中）。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/turn-footer

#### change-ledger
/changes 列出本会话改过的文件和行数。  
**许可证**：MIT  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/change-ledger

#### leftovers
记下 Claude 留在本机或服务器上的后台进程。  
**许可证**：MIT  
**来源**：https://github.com/homieyangg/claude-code-mods/tree/main/leftovers

#### deadlines
状态行的截止日期倒计时，/ddl 增删。  
**来源**：https://github.com/richardcsuwandi/claude-mods/tree/main/plugins/deadlines

#### cc-idle
挂在 Claude 旁边的放置游戏，只用本机会话进度。  
**许可证**：MIT  
**来源**：https://github.com/RichardAtCT/cc-idle/tree/main/plugins/cc-idle

#### prompt-stash
本地 /stash 提示词栈：存、列、弹出到输入框，不进模型上下文。  
**来源**：https://github.com/gonzaloserrano/cc-prompt-stash

#### pomodoro
番茄钟状态条与配置面板，纯本地计时与提醒。  
**许可证**：MIT  
**来源**：https://github.com/sneycampos/claude-pomodoro

#### bash-guardrails
用本地规则拒绝危险或畸形的 Bash 与 Monitor 调用（只读命令字符串做判定，不改写命令）。  
**来源**：https://github.com/ruihe774/cc-bash-guardrails

#### notify
桌面通知：Claude 回合完成或等待决策时发系统原生通知，后台时召回焦点。  
**许可证**：MIT  
**来源**：https://github.com/XD3an/cc-notify

#### usage-bar
用量条：可调用 Anthropic 的 OAuth 用量 API（使用当前登录凭证，请求体为空）查看 5 小时与 7 天限额、上下文与缓存命中率。  
**许可证**：MIT  
**来源**：https://github.com/muratkaragozgil/claude-code-usage-bar

#### netsignal
网络探针：向 api.anthropic.com 发延迟探测和带宽采样（不上传会话内容），在状态行显示往返时间。  
**许可证**：MIT  
**来源**：https://github.com/avazibra/claude-statusbar

#### usage-bars
上下文迷你图：把本会话的上下文占用画成字符级走势条，随回合增长刷新。  
**许可证**：MIT  
**来源**：https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/usage-bars

#### agent-watch
子代理侧栏：在窗格里列出活跃子代理、状态与简报，点击可查看 transcript。  
**许可证**：MIT  
**来源**：https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/agent-watch

#### touch-map
文件活动热力图：把 Claude 本会话读过、写过的文件画成文件树热力图，按访问频率着色。  
**许可证**：MIT  
**来源**：https://github.com/y-hirakaw/claude-code-mods/tree/main/touch-map

#### think-meter
桌面端回合计时器：等待/思考/写出/工具分段与 tok/s，附 /think-stats。  
**许可证**：MIT  
**来源**：https://github.com/Huuuuung/think-meter

#### chameleon
在 /rename 与 /branch 时给会话随机上色（/color），便于区分窗口。  
**许可证**：MIT  
**来源**：https://github.com/aksh1618/claude-mods/tree/main/chameleon

#### skill-session-mods
按本地 SKILL.md 元数据给 /skill 会话命名与上色（只读本地技能文件）。  
**许可证**：MIT  
**来源**：https://github.com/aksh1618/claude-mods/tree/main/skill-session-mods

#### paste-peek
粘贴图片实时像素预览（⌥←/→ 切换，⌥↑ 放大，⌥↓ 侧栏）；需支持图片的终端。  
**许可证**：MIT  
**来源**：https://github.com/nokiy/claude-code-mods/tree/main/plugins/paste-peek

#### agent-monitor
子代理监视带与 /sub 历史窗格：冲突/卡住提醒与费用估计（本地事件，不改写工具）。  
**许可证**：MIT  
**来源**：https://github.com/nokiy/claude-code-mods/tree/main/plugins/agent-monitor

#### garde-du-corps
本地拒绝访问 .env 与危险 Bash（rm -rf、force push、hard reset、DROP TABLE）；只读路径/命令字符串做 deny，不改写命令。  
**许可证**：MIT  
**来源**：https://github.com/Para-FR/claude-code-mods-fr/tree/main/garde-du-corps

#### maomao
提示框上方 8-bit 毛毛（垂耳兔）随工作状态跑跳；/maomao 收起或叫出。  
**来源**：https://github.com/jessetsai1024/claude-mods/tree/main/maomao

#### ctx-panel
侧栏 context 用量面板（分类、每轮成长、前几名）；/ctx full 会走精确计费 API。  
**来源**：https://github.com/jessetsai1024/claude-mods/tree/main/ctx-panel

#### files
侧栏本会话新建/修改/删除的文件清单与行数（只观察工具，不改写）。  
**来源**：https://github.com/jessetsai1024/claude-mods/tree/main/files

#### timeline
侧栏时间轴：本回合时间花在等待/思考/写出/工具/等帮手等。  
**来源**：https://github.com/jessetsai1024/claude-mods/tree/main/timeline

#### tokens
侧栏 token 往来：每次请求送出/等待/收到与合计。  
**来源**：https://github.com/jessetsai1024/claude-mods/tree/main/tokens

#### ai-usage-band
提示框上方用量带：上下文占用、限额窗口与会话费用（$.session.usage）。  
**来源**：https://github.com/arvakme/claude-code-butler/tree/main/ai-usage-band

#### no-attribution
去掉或替换 Co-Authored-By 提交尾注与 "Generated with Claude Code" PR 页脚。  
**许可证**：MIT  
**来源**：https://github.com/claudemodz/mods/tree/main/plugins/no-attribution

#### standup
跨会话记录你的提问与改动文件，/standup 用模型写成日报摘要。  
**许可证**：MIT  
**来源**：https://github.com/claudemodz/mods/tree/main/plugins/standup

#### ding
长回合结束 toast+可选音效提醒。  
**来源**：https://github.com/lucenity0/claude-code-mods/tree/main/ding

#### seatbelt
本地规则拦截危险 Bash/写文件（只拒绝不改写命令）。备注：会 deny 匹配的工具调用。  
**来源**：https://github.com/lucenity0/claude-code-mods/tree/main/seatbelt

#### session-dash
会话仪表盘窗格：用量与回合概览。  
**来源**：https://github.com/lucenity0/claude-code-mods/tree/main/session-dash

#### turn-meter
状态行显示当前回合耗时与 token。  
**来源**：https://github.com/lucenity0/claude-code-mods/tree/main/turn-meter

#### collapse-answers
折叠过长回复，界面更干净。  
**来源**：https://github.com/adriancoman/claude-code-mods/tree/main/collapse-answers

#### prompt-highlight
高亮用户消息气泡背景，便于扫读。  
**来源**：https://github.com/adriancoman/claude-code-mods/tree/main/prompt-highlight

#### usage-status
状态行显示 5h/周限额占用。  
**来源**：https://github.com/adriancoman/claude-code-mods/tree/main/usage-status

#### cache-watch
提示缓存重建时 toast 告警并估算回合费用。  
**来源**：https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cache-watch

#### context-guard
上下文占用状态行，越过阈值 toast 提醒 /compact。  
**来源**：https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/context-guard

#### cost-pane
费用窗格：本会话与按日花费汇总。  
**来源**：https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cost-pane

#### turn-timer
轻量回合计时状态。  
**来源**：https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/turn-timer

#### quiet-spinner
弱化/安静化等待 spinner。  
**来源**：https://github.com/schreibse/claude-code-mods/tree/main/quiet-spinner

#### mr-banner
MR/PR 相关横幅提示。  
**来源**：https://github.com/schreibse/claude-code-mods/tree/main/mr-banner

#### reminder-log
本地提醒日志窗格。  
**来源**：https://github.com/schreibse/claude-code-mods/tree/main/reminder-log

#### quiet-bash
精简 Bash 行展示，可选本地 magick 缩略图。备注：会本地调用 magick/identify 生成缩略图。  
**来源**：https://github.com/schreibse/claude-code-mods/tree/main/quiet-bash

#### cache-meter
提示框上方提示缓存剩余 TTL 条。  
**来源**：https://github.com/DarioFontanel/claude-code-mods/tree/main/cache-meter

#### quick-buttons
侧栏快捷按钮启动已选 slash 命令。备注：点击会 $.command.run。  
**来源**：https://github.com/DarioFontanel/claude-code-mods/tree/main/quick-buttons

#### snake
Claude 工作时可玩的贪吃蛇窗格（/snake）。  
**来源**：https://github.com/hamzafer/claude-code-mods/tree/main/mods/snake

#### where-am-i
提示上方只读回顾：目标/正在做/等你什么（观察工具调用，不改写）。  
**来源**：https://github.com/hamzafer/claude-code-mods/tree/main/mods/where-am-i

#### agent-radar
每个运行中子代理一行实时状态。  
**来源**：https://github.com/hamzafer/claude-code-mods/tree/main/mods/agent-radar

#### search-meter
统计模型搜索（Bash grep/find、WebSearch、ToolSearch）命中着色。  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/search-meter

#### compact-keeper
压缩后把摘要与编辑文件清单存到本地 ~/.claude/handoffs/。备注：只写本地 handoff 文件。  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/compact-keeper

#### guardrails
本地拒绝 Cloudflare 写命令、带归因行的 commit、claude/ 分支前缀。备注：只读 Bash 命令字符串做 deny，不改写。  
**来源**：https://github.com/arasovic/claude-code-mods/tree/main/guardrails

#### code-pet
像素宠物窗格，随 Claude 活动反应。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/code-pet

#### session-wrapped
会话「年终总结」式统计动画。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/session-wrapped

#### boss-fight
失败测试变 boss，通过测试打血条的像素小游戏。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/boss-fight

#### sportscaster
会话实况解说（本地 $.audio.speak，不上传会话）。备注：使用本机 TTS。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/sportscaster

#### swarm
子代理/团队任务控制室窗格。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/swarm

#### agent-race
多会话任务赛跑分屏。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/agent-race

#### inner-monologue
会话旁白式内心独白窗格。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/inner-monologue

#### launch-codes
危险 Bash 需解锁码才放行。备注：会 deny 危险命令直至用户解锁。  
**来源**：https://github.com/OneWave-AI/claude-code-mods/tree/main/launch-codes

#### md-view
点击回复里的 Markdown 文件渲染预览。  
**来源**：https://github.com/scoobynko/claude-code-mods/tree/main/plugins/md-view

#### image-preview
会话图片窗格预览。备注：本地 sips/magick 转 PNG，不外传。  
**来源**：https://github.com/scoobynko/claude-code-mods/tree/main/plugins/image-preview

#### little-harvest
随回合生长的自动小花园。  
**来源**：https://github.com/theonly1me/claude-code-mods/tree/main/plugins/little-harvest

#### pocket-familiar
伴随工作的养成伙伴窗格。  
**来源**：https://github.com/theonly1me/claude-code-mods/tree/main/plugins/pocket-familiar

#### night-feast
Claude 工作时的像素小游戏。  
**来源**：https://github.com/theonly1me/claude-code-mods/tree/main/plugins/night-feast

#### change-journal
编辑变更的即时说明窗格。  
**来源**：https://github.com/theonly1me/claude-code-mods/tree/main/plugins/change-journal

#### behavior-map
改动前后行为流图。  
**来源**：https://github.com/theonly1me/claude-code-mods/tree/main/plugins/behavior-map

#### check-ledger
记录跑过哪些检查、之后又有哪些编辑（/evidence）。  
**来源**：https://github.com/LeeHigma0201/claude-code-mods/tree/main/mods/check-ledger

#### collision-guard
另一会话刚改过同一文件时先询问再编辑。备注：可 deny 编辑并询问用户。  
**来源**：https://github.com/nateherkai/claude-code-mods/tree/main/collision-guard

#### adhkar
在 Claude Code 中显示赞念/记主内容。  
**来源**：https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/adhkar

#### daily-ayah
每日经文展示。  
**来源**：https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/daily-ayah

#### secret-mask
在工具输出写入对话前遮罩疑似密钥。备注：会改写展示给模型的工具结果文本（本地遮罩，不外传）。  
**来源**：https://github.com/homieyangg/claude-code-mods/tree/main/secret-mask

#### pong
在提示框上方玩 Pong 游戏，Claude 工作时可打发时间。  
**许可证**：MIT  
**来源**：https://github.com/ambareeshav/claude-pong-mod

#### fortune-cookie
提示框上方随机显示程序员幸运饼干语录。  
**许可证**：Apache-2.0  
**来源**：https://github.com/tobinsouth/fortune-cookie-mod

#### claude-maru-run
Claude 工作时在窗格里看方块跑酷小游戏。  
**来源**：https://github.com/lemonlatte/claude-maru-run

#### cc-dino
Chrome 恐龙跑酷游戏，Claude 忙时可玩。  
**许可证**：MIT  
**来源**：https://github.com/manfye/cc-dino

#### cc-pokedex
在侧栏查看宝可梦图鉴，按名字或编号搜索。  
**来源**：https://github.com/deonmenezes/claude-mods-pokedex

#### statusbar
状态栏显示当前 git 分支与仓库状态，仅本地 git rev-parse 查询。  
**许可证**：MIT  
**来源**：https://github.com/sgmonda/statusbar

#### loose-ends
追踪会话中未完成的待办事项，回合结束用 $.model.complete 总结剩余任务。  
**许可证**：MIT  
**来源**：https://github.com/fernandomoraes/loose-ends

#### gamba
在提示框上方玩老虎机小游戏。  
**来源**：https://github.com/salatmaster/claude-gamba

#### claude-slots
老虎机游戏，等待时可玩。  
**许可证**：MIT  
**来源**：https://github.com/WorldInnovationsDepartment/claude_slots

#### music-mod
通过 osascript 控制 macOS Music.app 播放音乐。  
**许可证**：MIT  
**来源**：https://github.com/zyx1121/music-mod

#### holdtime
显示 Claude 工作耗时，回合结束时用 $.model.complete 生成总结（可能替换默认 turn.complete 文本）。  
**许可证**：MIT  
**来源**：https://github.com/ItsRohith-A/holdtime

#### korkmaz-trail
俄勒冈小径风格像素游戏。  
**许可证**：MIT  
**来源**：https://github.com/BersanKayraKorkmaz/korkmaz-trail

#### clawdgotchi
电子宠物 Clawd，在侧栏养成与互动。  
**许可证**：MIT  
**来源**：https://github.com/arthurseredaa/clawdgotchi

#### usage-report
显示会话用量与费用报告。  
**许可证**：MIT  
**来源**：https://github.com/Schweem/usage-report

#### idle-compact
检测会话闲置时自动调用 $.session.compact 压缩上下文。  
**许可证**：MIT  
**来源**：https://github.com/davidar/claude-idle-compact

#### tps-report
TPS 风格工作报告窗格。  
**许可证**：MIT  
**来源**：https://github.com/vgnshiyer/tps-report

#### cache-ttl-timer
提示缓存 TTL 倒计时，并 tail 本地 transcript 文件。  
**许可证**：MIT  
**来源**：https://github.com/WQGGSEY/cache-ttl-timer

#### wavy-usage
波浪动画风格的用量显示条。  
**许可证**：MIT  
**来源**：https://github.com/BatuhanCakmakk/wavy-usage

#### nowloading
显示加载动画与进度提示。  
**许可证**：MIT  
**来源**：https://github.com/vgnshiyer/nowloading

#### essential-conversation
精简对话显示，只保留核心内容。  
**来源**：https://github.com/SuzumiyaAoba/claude-essential-conversation-mod

#### repo-pulse
显示仓库活动脉搏，仅本地 git status 查询。  
**许可证**：MIT  
**来源**：https://github.com/5d0tal1gat0r/repo-pulse

#### stepscope
步骤追踪与可视化窗格。  
**许可证**：MIT  
**来源**：https://github.com/5d0tal1gat0r/stepscope

#### drift
漂移动画效果窗格。  
**许可证**：MIT  
**来源**：https://github.com/azkhh/drift

#### amp-inbox-band
在提示框上方显示未读 AMP 消息，可 toast / 状态栏提示；可选 autoWake 在空闲时自动提交读信提示。备注：依赖本机 `~/.local/bin/amp-inbox.sh`；autoWake 默认关闭。  
**许可证**：MIT  
**来源**：https://github.com/23blocks-OS/ai-maestro/tree/main/mods/amp-inbox-band

#### reflect-mod
用模型检查短提示是否含可复用规则，上方条带一键写入 CLAUDE.md。备注：调用 $.model.complete（用户自己的 Claude）；会写本地 CLAUDE.md；prompt.compose 注入本会话已保存规则。  
**许可证**：MIT  
**来源**：https://github.com/BayramAnnakov/claude-reflect/tree/main/mod

#### emotion-statusline
状态条/提示框上显示本回合工具成败弧与 Haiku 分类的「情绪」缓存。备注：读本地 `~/.claude/cache/claude-emotion-*.json`；另有 command hook 跑 classify-emotion.sh。  
**来源**：https://github.com/bencium/bencium-marketplace/tree/main/emotion-statusline

#### followthrough-band
提示框上方列出本仓库到期的 followthrough 检查（Run/Snooze/Close），并在无检查就发版时提醒。备注：依赖本机 followthrough CLI；仅观察 Bash 结果，不改写命令。  
**许可证**：MIT  
**来源**：https://github.com/BayramAnnakov/followthrough/tree/main/mod

#### oneform-line
提示框上方显示 OneForm 当日睡眠/蛋白/训练与下周计划；/oneform 查看全日。备注：用用户配置的 OneForm URL + API key 经 $.http.fetch 拉取（仅 https 或 localhost）。  
**来源**：https://github.com/hamzafer/claude-code-mods/tree/main/mods/oneform-line

#### inbox-pane
侧栏窗格展示 claude-inbox 各分区会话，支持快捷键操作。备注：读写本机 `~/.config/claude-inbox/`；可在无写入时拉起 `claude-inbox --headless`。  
**来源**：https://github.com/jordanbyron/claude-inbox/tree/main/mod

#### draft-pane
侧栏展示模型 ```draft 块，支持划选批注后一次提交反馈。备注：仅读会话 transcript / 本地 draft 文件；按钮触发 $.prompt.submit。  
**来源**：https://github.com/meganemura/draft-pane/tree/main/plugin

#### context-bar
提示下方（可改上方）显示上下文窗口进度条与 prompt-cache TTL 倒计时。备注：可 tail 本地 transcript；仅本地读。  
**来源**：https://github.com/k-wolfe99/claude-context-bar/tree/main/mod

#### wake
订阅 PR/CI/devbox 等状态，条件达成时唤醒空闲会话。备注：经本机 unix socket 调 vybava watch 守护进程；会 $.prompt.submit 唤醒。  
**来源**：https://github.com/henderson-tech/vybava/tree/main/mods/wake

#### ruview-live
/ruview 打开 CSI/雷达传感只读窗格（瀑布图与雷达视图）。备注：运行插件旁的 @ruvnet/ruview CLI（node）；只读设备数据。  
**许可证**：MIT  
**来源**：https://github.com/ruvnet/RuView/tree/main/harness/ruview/mod

#### on-me
提示框上条带：Claude 正在做什么，以及轮到你处理的事项。  
**许可证**：MIT  
**来源**：https://github.com/abhibansal60/claude-mods/tree/main/on-me

#### browser-guard
把 cswap 账号与 Chrome 配置配对，防止用错浏览器画像。备注：可 deny 不匹配的 Chrome 工具调用；依赖本机 `cswap status`。  
**来源**：https://github.com/abhibansal60/claude-mods/tree/main/browser-guard

#### resume-on-stop
检测「说了要动手却停住」的意外停轮，经 decision 模型确认后自动续一轮。备注：依赖 decision-model；会自动 $.prompt.submit 续跑（每提示最多一次）。  
**来源**：https://github.com/kzarzycki/claude-mods/tree/main/plugins/resume-on-stop

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

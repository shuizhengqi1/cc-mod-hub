# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 365 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

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

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 365 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (organized by category)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 365 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 365 个精选 Claude Code mods，按类别组织：


### 内置核心 Built-in Core

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| agents-md | 通过 prompt.context 和 Read 工具调用加载 AGENTS.md 文件。 |  | [链接](https://github.com/anthropics/claude-code/tree/main/mods/agents-md) |
| diff | 在面板中显示未提交的更改。 |  | [链接](https://github.com/anthropics/claude-code/tree/main/mods/diff) |
| sec-default | 安全防护，防止用户 mod 覆盖托管钩子。 |  | [链接](https://github.com/anthropics/claude-code/tree/main/mods/sec-default) |
| telemetry | 分析助手，当分析功能关闭时不发送任何数据。 |  | [链接](https://github.com/anthropics/claude-code/tree/main/mods/telemetry) |

### 官方示例 Official Examples

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| blast-radius | 为风险 Bash 命令提供继续/取消提示。 | Apache-2.0 | [链接](https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/blast-radius) |
| next-steps | 每轮结束后在输入框上方建议最多三个下一步提示，可按数字键快速填入；fork 会话向模型问询并共享提示缓存，成本低廉。 |  | [链接](https://github.com/anthropics/claude-plugins-community/tree/main/next-steps) |
| replay-theater | 逐步回放上一轮的文件编辑。 | Apache-2.0 | [链接](https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/replay-theater) |
| token-weather | 在提示框上方显示上下文预报。 | Apache-2.0 | [链接](https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/token-weather) |

### 用量与费用 Usage & Cost

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| agent-flow | /flow 侧栏实时显示 subagent 树（零 token）。 |  | [链接](https://github.com/Charlie0113-T/claude-agent-flow) |
| agent-monitor | 子代理监视带与 /sub 历史窗格：冲突/卡住提醒与费用估计（本地事件，不改写工具）。 | MIT | [链接](https://github.com/nokiy/claude-code-mods/tree/main/plugins/agent-monitor) |
| ai-usage-band | 提示框上方用量带：上下文占用、限额窗口与会话费用（$.session.usage）。 |  | [链接](https://github.com/arvakme/claude-code-butler/tree/main/ai-usage-band) |
| budget-guard | 费用与 5 小时/7 天限额：接近上限警告，超额拒绝工具调用。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/budget-guard) |
| burn-meter | 提示框上方会话花费「火焰」条与限额，/burn 看每回合费用。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/burn-meter) |
| cache-clock | 显示提示缓存还热多久。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/cache-clock) |
| cache-meter | 提示框上方提示缓存剩余 TTL 条。 |  | [链接](https://github.com/DarioFontanel/claude-code-mods/tree/main/cache-meter) |
| cache-refresher | 提示缓存倒计时与 lapse 成本；可选 $.model.fork 保活 ping。备注：使用 $.model.fork。 | MIT | [链接](https://github.com/olddonkey/cache-refresher) |
| cost-meter | 会话费用实时条（同 /cost 口径），可选预算阈值与颜色提示。 | MIT | [链接](https://github.com/zaferayan/claude-cost-meter/tree/main/cost-meter) |
| cost-info | 会话费用与 token 实时显示（同 /cost 口径），可选预算 toast。 | MIT | [链接](https://github.com/falconsw/cost-info/tree/main/cost-info) |
| cache-tax | 提供 /keepwarm 命令，阻止一次冷启动发送。 |  | [链接](https://github.com/karanb192/cache-tax) |
| cache-timer | 倒计时提示缓存何时过期。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/cache-timer) |
| cache-ttl-timer | 提示缓存 TTL 倒计时，并 tail 本地 transcript 文件。 | MIT | [链接](https://github.com/WQGGSEY/cache-ttl-timer) |
| cache-warm | 缓存预热工具。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/cache-warm) |
| cache-watch | 提示缓存重建时 toast 告警并估算回合费用。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cache-watch) |
| ccoverhead | 提示框上方显示上下文窗口、每轮增长、5h/7d 额度与缓存热度（只读会话用量）。 | MIT | [链接](https://github.com/shengyy/ccoverhead/tree/main/plugin) |
| cctop | btop 风格侧栏面板，展示上下文、tokens、成本、工具延迟等。 |  | [链接](https://github.com/tomstagl/cctop/tree/main/plugin) |
| clawd-spinner | Clawd 按 spinner 词表演动画（本地绘制，零 token）。 | MIT | [链接](https://github.com/saiharsha03/clawd-spinner) |
| context-bar | 提示下方（可改上方）显示上下文窗口进度条与 prompt-cache TTL 倒计时。备注：可 tail 本地 transcript；仅本地读。 |  | [链接](https://github.com/k-wolfe99/claude-context-bar/tree/main/mod) |
| context-band | 限额/token/缓存/费用状态带。备注：本机 process（主题检测与本地 python 估价）。 |  | [链接](https://github.com/EricJamie/claude-code-mods/tree/main/plugins/context-band) |
| context-tokens | 桌面端提示脚旁显示上下文 token 用量（绿/黄/红阈值）。纯 UI，只读 $.session.usage。 | MIT | [链接](https://github.com/0xBADC0FFEE/claude-code-mods/tree/main/context-tokens) |
| context-weather | 提示框上方上下文占用条、会话费用与计划限额，接近压缩时 toast。纯 UI。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/context-weather) |
| context-xray | 窗格拆开上下文占用：系统提示、工具、记忆、skills、消息。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/context-xray) |
| cost-pane | 费用窗格：本会话与按日花费汇总。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cost-pane) |
| effort-guard | 上下文/token 条带、升级信号与每回合 effort 日志。 | MIT | [链接](https://github.com/stefanochieli/claude-effort-guard) |
| eta | 在 spinner 行显示本轮剩余时间（按任务节奏或历史回合学习，零 token）。 |  | [链接](https://github.com/hamza-siddiq/claude-eta/tree/main/eta) |
| limit-bars | 提示框下四个动画环，显示上下文、会话和周限额。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/limit-bars) |
| limit-watch | 限额监视器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/limit-watch) |
| netrunner-hud | 会话仪表盘：上下文条、token 示波与状态窗格。 | MIT | [链接](https://github.com/ccdwyer/netrunner-hud) |
| omp-quota | omp 各 provider 剩余配额条（/quota）；备注：通过本机 `omp usage --json` 读取，不改写工具。 | MIT | [链接](https://github.com/musingfox/cc-plugins/tree/main/omp-quota) |
| overalls | 提示框上方状态条：上下文预报、用量限额，以及 Ponytail/Caveman 档位（可配置）。 | MIT | [链接](https://github.com/Troepster/overalls) |
| pets | 像素宠物窗格：闲逛、记笔记、完成回合时跳跃、限额 80% 流泪、闲置两分钟午睡；八种动物（猫、小鸡、狗、史莱姆、兔子、仓鼠、企鹅、青蛙），可命名、喂食、升... | MIT | [链接](https://github.com/uppinote20/claude-pets) |
| pro-hud | Pro 计划用量表盘：5 小时、7 天限额、上下文和回合回执。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/pro-hud) |
| quota-meter | 计划限额条与重置倒计时。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/quota-meter) |
| session-dash | 会话仪表盘窗格：用量与回合概览。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/session-dash) |
| session-receipt | /receipt 窗格列出每回合的 token 花费。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/session-receipt) |
| shunt | 用用户自己的 gateway / token（SHUNT_* 或 ANTHROPIC_*）请求 GET /usage，在本地显示配额窗口；请求体为空。 | MIT | [链接](https://github.com/pleaseai/shunt/tree/main/plugins/shunt) |
| spend-meter | 状态行显示会话费用、上下文与 5 小时限额。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/spend-meter) |
| statuspane | 提示框上方浮动状态卡：模型、effort、上下文、5 小时/周限额、费用与分支，另有可供脚本/其他 mod 写入的进度条 API。 | MIT | [链接](https://github.com/xuanji86/claude-statuspane) |
| statusband | 提示框上方两行状态带：上下文、缓存倒计时、限额与 git。备注：本机 git。 | MIT | [链接](https://github.com/dip497/claude-statusband) |
| status-hud | 提示框上方活动阶段与 5h/周限额/上下文窗口状态条。纯 UI。 | MIT | [链接](https://github.com/hymleong/claude-mods/tree/main/plugins/status-hud) |
| token-ledger | 会话成本与上轮 tokens；面板查看近期回合。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/token-ledger) |
| tokens | 侧栏 token 往来：每次请求送出/等待/收到与合计。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/tokens) |
| trek-band | 提示框上方星际迷航风格用量环与像素动画场景。 | MIT | [链接](https://github.com/rb17080/trek-band/tree/main/plugins/trek-band) |
| turn-footer | 每条回答下方改成回合摘要（工具、请求、tokens、缓存命中）。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/turn-footer) |
| turn-meter | 状态行显示当前回合耗时与 token。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/turn-meter) |
| usage-band | 在提示框上方显示 5 小时/7 天限额、上下文窗口与缓存命中率。 | MIT | [链接](https://github.com/JetsonChan/CC-Usage-Band/tree/main/usage-band) |
| usage-bar | 用量条：可调用 Anthropic 的 OAuth 用量 API（使用当前登录凭证，请求体为空）查看 5 小时与 7 天限额、上下文与缓存命中率。 | MIT | [链接](https://github.com/muratkaragozgil/claude-code-usage-bar) |
| usage-bars | 上下文迷你图：把本会话的上下文占用画成字符级走势条，随回合增长刷新。 | MIT | [链接](https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/usage-bars) |
| usage-deck | 计划限额、上下文占用与缓存温度合成动画甲板（/deck 显隐）。 | MIT | [链接](https://github.com/codeclawd/usage-deck/tree/main/plugins/usage-deck) |
| usage-bell | 接近限额时响铃：上下文占用（70/85/95%）、5 小时/7 天限额（80/95%）、自动记忆索引达 200 行或 25 kB；状态栏显示当前百分比，/... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/usage-bell) |
| usage-meter | 提示框上方常显上下文与 5 小时/周限额。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/usage-meter) |
| usage-mod | 提示框上方显示上下文与 5h/7d 额度及重置时间；按钮可触发本机 /compact。 | MIT | [链接](https://github.com/qingyashizi/claude-usage-mod/tree/main/plugins/usage-mod) |
| usage-log | 每回合写本地 jsonl 用量日志，并显示相对 7 日节奏的差距。备注：本机 process 写本地文件。 | MIT | [链接](https://github.com/tanuu5/usage-log/tree/main/plugins/usage-log) |
| usage-limits | 提示框上方显示 5h/周限额剩余与重置倒计时。纯 UI。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/usage-limits) |
| usage-report | 显示会话用量与费用报告。 | MIT | [链接](https://github.com/Schweem/usage-report) |
| usage-status | 状态行显示 5h/周限额占用。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/usage-status) |
| usage-tracker | 实时 5h/7d 用量、节奏与火花线（含本机读 Codex 日志）。备注：本机 process（tail）。 |  | [链接](https://github.com/tylergraydev/cc-mods/tree/main/usage-tracker) |
| vercel-deploy-status | 提示框上方显示 Vercel 部署队列（零 token）。 |  | [链接](https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/vercel-deploy-status) |
| wavy-usage | 波浪动画风格的用量显示条。 | MIT | [链接](https://github.com/BatuhanCakmakk/wavy-usage) |

### 上下文管理 Context Management

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| compact-keeper | 压缩后把摘要与编辑文件清单存到本地 ~/.claude/handoffs/。备注：只写本地 handoff 文件。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/compact-keeper) |
| compact-tools | 压缩工具输出显示（含 MCP/Bash 错误）。 |  | [链接](https://github.com/AJclemendor/my-mods/tree/main/plugins/compact-tools) |
| context-guard | 上下文占用状态行，越过阈值 toast 提醒 /compact。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/context-guard) |
| context-lens | 固定显示上下文占用、增长与距 compaction 的回合数。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/context-lens) |
| context-restore | 恢复上下文状态。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/context-restore) |
| context-view | 提示框上方一行上下文占用与距 auto-compact 余量。 |  | [链接](https://github.com/kongyo2/context-view) |
| ctx-handoff | 上下文达阈值时自动生成 handoff 并 /clear；空闲时还能续热缓存。 |  | [链接](https://github.com/cablate/ctx-handoff-mod) |
| ctx-panel | 侧栏 context 用量面板（分类、每轮成长、前几名）；/ctx full 会走精确计费 API。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/ctx-panel) |
| fast-jev-compaction | session.compact mod。 |  | [链接](https://github.com/tamaratran/fast-jev-compaction) |
| gemini-compact | Gemini 压缩助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-compact) |
| handoff-compact | 用固定大纲的 handoff 替换默认摘要，少丢决策与否决项。 |  | [链接](https://github.com/trytofly94/handoff-compact) |
| idle-compact | 检测会话闲置时自动调用 $.session.compact 压缩上下文。 | MIT | [链接](https://github.com/davidar/claude-idle-compact) |
| micro-compaction | 提供 /compact micro：精简 Read 结果并去掉 thinking，保留对话结构。 | Unlicense | [链接](https://github.com/ruihe774/cc-micro-compaction) |
| segmem | 长期记忆：区分身份（你是谁）、过程（仓库如何工作）、情节（周二发生了什么）与人物档案；按衰减窗口加载，项目级作用域，压缩历史为摘要，无需服务器或守护进程。 |  | [链接](https://github.com/mahuebel/segmem) |
| sidebar-controls | 把 compact-tools/live-thinking 开关放进右上侧栏。 |  | [链接](https://github.com/AJclemendor/my-mods/tree/main/plugins/sidebar-controls) |
| workface | 长任务工作笔记，compaction 时保住 workface 状态。 |  | [链接](https://github.com/scodge-24/workface) |

### UI 与主题 UI & Themes

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| 12ui-plugin | 提供设计面板。 |  | [链接](https://github.com/just-every/12ui-plugin) |
| aside | /aside 只读侧聊：基于会话 transcript fork 问答，不写回主线程。 | MIT | [链接](https://github.com/JayDoubleu/aside) |
| at-work | 提示框上方像素场景动画，按当前工具活动切换画面；spinner 计算机笑话；节日装饰。纯 UI，不改写工具/提示。 | MIT | [链接](https://github.com/zhuoxingzhang/pixel-at-work) |
| catch-me-up | 侧栏实时 catch-up 摘要：为何开始、做了什么、卡在哪里。 | MIT | [链接](https://github.com/oliverow/catch-me-up) |
| cc-pokedex | 在侧栏查看宝可梦图鉴，按名字或编号搜索。 |  | [链接](https://github.com/deonmenezes/claude-mods-pokedex) |
| chameleon | 在 /rename 与 /branch 时给会话随机上色（/color），便于区分窗口。 | MIT | [链接](https://github.com/aksh1618/claude-mods/tree/main/chameleon) |
| change-journal | 编辑变更的即时说明窗格。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/change-journal) |
| collapse-answers | 折叠过长回复，界面更干净。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/collapse-answers) |
| message-timestamps | 在 transcript 里给每条 Claude 回复加本地到达时间戳；无模型调用、不上网。 |  | [链接](https://github.com/benjaminmodayil/live-recap/tree/main/plugins/message-timestamps) |
| commonplace-pane | 侧边窗格展示芝加哥艺术学院公版画，随仓库状态变「天气」。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/commonplace-pane) |
| drift | 漂移动画效果窗格。 | MIT | [链接](https://github.com/azkhh/drift) |
| file-view | 点击 Read/Edit/Write 行的路径，在侧栏打开文件内容。备注：本机读文件。 |  | [链接](https://github.com/ushironoko/dotfiles/tree/main/claude/.claude/skills/file-view) |
| firstmate-calm | /calm 隐藏工具行并换成帆船 spinner；需开启 function hooks。 |  | [链接](https://github.com/kunchenguid/firstmate/tree/main/.claude/mods/firstmate-calm) |
| flowpane | 实时显示工作流程图。 |  | [链接](https://github.com/mpolatcan/flowpane) |
| inner-monologue | 会话旁白式内心独白窗格。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/inner-monologue) |
| netsignal | 网络探针：向 api.anthropic.com 发延迟探测和带宽采样（不上传会话内容），在状态行显示往返时间。 | MIT | [链接](https://github.com/avazibra/claude-statusbar) |
| on-me | 提示框上条带：Claude 正在做什么，以及轮到你处理的事项。 | MIT | [链接](https://github.com/abhibansal60/claude-mods/tree/main/on-me) |
| orange-prompt | 输入草稿白字橙底高亮（可配合 Orange Dark 主题）。纯 UI。 | MIT | [链接](https://github.com/philsimon/orange-prompt) |
| pixelband | 在提示框上方显示像素艺术。 |  | [链接](https://github.com/furqan-khan07/pixelband) |
| pin-message | /pin 把选中文本或上一条回复钉到侧栏，滚动时仍可见。纯 UI。 | MIT | [链接](https://github.com/GruperTal/claude-pin-message) |
| powerline-bar | Powerline 风格 AbovePrompt 条：目录、git、模型与上下文占用。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/powerline-bar) |
| prompt-highlight | 高亮用户消息气泡背景，便于扫读。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/prompt-highlight) |
| prompt-rail | 提示条/侧栏：悬停读、点击跳回历史 prompt。 |  | [链接](https://github.com/oikon48/prompt-rail/tree/main/plugins/prompt-rail) |
| quick-buttons | 侧栏快捷按钮启动已选 slash 命令。备注：点击会 $.command.run。 |  | [链接](https://github.com/DarioFontanel/claude-code-mods/tree/main/quick-buttons) |
| quiet-bash | 精简 Bash 行展示，可选本地 magick 缩略图。备注：会本地调用 magick/identify 生成缩略图。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/quiet-bash) |
| quiet-spinner | 弱化/安静化等待 spinner。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/quiet-spinner) |
| reply-highlight | 用彩虹边和紫色底突出 Claude 的回复。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/reply-highlight) |
| rtl-text | 用 fribidi 把波斯语/阿拉伯语/希伯来语在 transcript 里按 RTL 整形对齐。 |  | [链接](https://github.com/aliir74/claude-code-rtl) |
| ruview-live | /ruview 打开 CSI/雷达传感只读窗格（瀑布图与雷达视图）。备注：运行插件旁的 @ruvnet/ruview CLI（node）；只读设备数据。 | MIT | [链接](https://github.com/ruvnet/RuView/tree/main/harness/ruview/mod) |
| search-meter | 统计模型搜索（Bash grep/find、WebSearch、ToolSearch）命中着色。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/search-meter) |
| shell-highlight | Bash/PowerShell 工具调用语法高亮展示。纯 UI，不改写命令。 | MIT | [链接](https://github.com/Turbo-Thorschten/shell-highlight) |
| sidebar | 侧栏扩展面板。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sidebar) |
| spell-bar | 按 effort 等级绘制的动画施法条（Clawd / Avada Kedavra 六档）。纯 UI，不改写工具或提示。 | MIT | [链接](https://github.com/powerofjinbo/claude-code-spell-bar/tree/main/plugins/spell-bar) |
| spinner-stats | 在 Claude 自带 spinner 后缀追加耗时、当前工具与调用次数。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/spinner-stats) |
| starfleet-panel | 提示框下方 LCARS 风格状态面板（模型/上下文/限额/分支等）；只读跟随 red-alert。本地 git/hostname。 | MIT | [链接](https://github.com/dukechain2333/starfleet-panel/tree/main/plugin) |
| status-band | 可主题化状态条：模型/effort、目录、git、上下文与配额等；/band 配置。 | MIT | [链接](https://github.com/dukechain2333/cc-status-band) |
| status-bar | 把各 mod 状态行折成一行（或上方 band）。纯 UI。 |  | [链接](https://github.com/tylergraydev/cc-mods/tree/main/status-bar) |
| stepscope | 步骤追踪与可视化窗格。 | MIT | [链接](https://github.com/5d0tal1gat0r/stepscope) |
| think-meter | 桌面端回合计时器：等待/思考/写出/工具分段与 tok/s，附 /think-stats。 | MIT | [链接](https://github.com/Huuuuung/think-meter) |
| timeline | 侧栏时间轴：本回合时间花在等待/思考/写出/工具/等帮手等。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/timeline) |
| tps-report | TPS 风格工作报告窗格。 | MIT | [链接](https://github.com/vgnshiyer/tps-report) |
| transcript-fx | 给 transcript 上色：工具块、提示面板和 spinner。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/transcript-fx) |
| turn-timer | 轻量回合计时状态。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/turn-timer) |
| turn-progress | 状态行显示本回合阶段、经过时间与完成标记；可注册 progress 工具申报进度。 | MIT | [链接](https://github.com/tsumugilabo/turn-progress/tree/main/plugins/turn-progress) |
| whats-agent-doing | 提示框上方显示 Claude 当前在做什么（读提示、思考、写回复、跑工具、等审批），可展开历史。 | MIT | [链接](https://github.com/tzafrir/whats-agent-doing) |

### 游戏与娱乐 Games & Entertainment

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| 2048 | 提示框上方玩 2048；仅 UI/命令，不注入 prompt、不改工具。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/2048) |
| agent-race | 多会话任务赛跑分屏。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/agent-race) |
| boss-fight | 失败测试变 boss，通过测试打血条的像素小游戏。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/boss-fight) |
| cc-arcade | 在提示框上方显示游戏，点击不会调用模型。 |  | [链接](https://github.com/sezaakgun/cc-arcade) |
| cc-dino | Chrome 恐龙跑酷游戏，Claude 忙时可玩。 | MIT | [链接](https://github.com/manfye/cc-dino) |
| cc-idle | 挂在 Claude 旁边的放置游戏，只用本机会话进度。 | MIT | [链接](https://github.com/RichardAtCT/cc-idle/tree/main/plugins/cc-idle) |
| cc-subway | 地铁跑酷小游戏，可在右侧窗格或提示框上方游玩。 | MIT | [链接](https://github.com/lucastononro/cc-subway) |
| claude-dino | 提示框上方的恐龙跑酷小游戏（来源与已上架的 cc-dino 不同）。 |  | [链接](https://github.com/swan4er/claude-dino) |
| claude-games | 提示框上方的街机游戏（/racer、/breakout、/dino、/shooter），在 Claude 工作时玩；游戏对 Claude 的行为作出反应：... | MIT | [链接](https://github.com/mohi-devhub/claude-games) |
| claude-maru-run | Claude 工作时在窗格里看方块跑酷小游戏。 |  | [链接](https://github.com/lemonlatte/claude-maru-run) |
| claude-mine | 提示框上方的体素沙盒小游戏（不是扫雷）。 |  | [链接](https://github.com/swan4er/claude-mine) |
| claude-slots | 老虎机游戏，等待时可玩。 | MIT | [链接](https://github.com/WorldInnovationsDepartment/claude_slots) |
| context-dungeon | 把会话做成肉鸽：上下文是 HP，报错出怪，绿测击杀，只观察 tool.call，不改调用。 | MIT | [链接](https://github.com/ccdwyer/context-dungeon) |
| gamba | 在提示框上方玩老虎机小游戏。 |  | [链接](https://github.com/salatmaster/claude-gamba) |
| hyday-pet | 提示框上方虚拟宠物，随 Claude 工作成长、可小游戏/商店。 | MIT | [链接](https://github.com/mukiwu/muki-ai-plugins/tree/main/plugins/hyday-pet) |
| intermission | Claude 工作时在 Ghostty/kitty 窗格里开 Doom 死斗，回合结束或需要输入时自动切回。 | MIT | [链接](https://github.com/jarrodwatts/intermission) |
| korkmaz-trail | 俄勒冈小径风格像素游戏。 | MIT | [链接](https://github.com/BersanKayraKorkmaz/korkmaz-trail) |
| little-harvest | 随回合生长的自动小花园。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/little-harvest) |
| minefield | Claude 工作时在窗格里玩扫雷。 | MIT | [链接](https://github.com/reporails/arcade/tree/main/minefield) |
| night-feast | Claude 工作时的像素小游戏。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/night-feast) |
| pet | 一只嘴碎的火烈鸟吉祥物 Flingo，在侧栏或状态行陪伴你码字，代 Claude 说话、吐槽代码、喂养玩耍、换装（皇冠、礼帽、蝴蝶结、墨镜），用 /fli... | MIT | [链接](https://github.com/graugart/flingo) |
| pong | 在提示框上方玩 Pong 游戏，Claude 工作时可打发时间。 | MIT | [链接](https://github.com/ambareeshav/claude-pong-mod) |
| severance-mdr | Severance 风格 MDR 小游戏面板；代理工作时可自动打开。纯 UI。 |  | [链接](https://github.com/magnuswiderberg/claude-code-mods/tree/main/plugins/severance-mdr) |
| snake | Claude 工作时可玩的贪吃蛇窗格（/snake）。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/snake) |
| wod-band | 提示框上方像素运动员：工具调用计 rep，会话当 AMRAP。纯 UI。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/wod-band) |
| wod-timer | 提交时 3-2-1-GO，每回合计时与白板 split；可选本机语音读出超过一分钟的回合。纯 UI。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/wod-timer) |
| tetris | 提示框上方俄罗斯方块；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/tetris) |

### 安全防护 Security & Safety

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| bash-guardrails | 用本地规则拒绝危险或畸形的 Bash 与 Monitor 调用（只读命令字符串做判定，不改写命令）。 |  | [链接](https://github.com/ruihe774/cc-bash-guardrails) |
| branch-guard | 在受保护分支上拦截 Write/Edit 与变更型 git，可询问后放行或建议 worktree。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/branch-guard) |
| browser-guard | 把 cswap 账号与 Chrome 配置配对，防止用错浏览器画像。备注：可 deny 不匹配的 Chrome 工具调用；依赖本机 `cswap stat... |  | [链接](https://github.com/abhibansal60/claude-mods/tree/main/browser-guard) |
| collision-guard | 另一会话刚改过同一文件时先询问再编辑。备注：可 deny 编辑并询问用户。 |  | [链接](https://github.com/nateherkai/claude-code-mods/tree/main/collision-guard) |
| env | 在面板里编辑 .env；Claude 管理键名但看不到真实密钥值。 | MIT | [链接](https://github.com/davekiss/env) |
| flash-veille | 提示框上方轮播开发者资讯（Human Coders、Anthropic 博客等）。 | MIT | [链接](https://github.com/camilleroux/flash-veille/tree/main/plugins/flash-veille) |
| guardrails | 本地拒绝 Cloudflare 写命令、带归因行的 commit、claude/ 分支前缀。备注：只读 Bash 命令字符串做 deny，不改写。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/guardrails) |
| launch-codes | 危险 Bash 需解锁码才放行。备注：会 deny 危险命令直至用户解锁。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/launch-codes) |
| merge-gate | 除非最新人工消息含 merge，否则拒绝 Bash 里的 merge / gh pr merge / 推送到主干。备注：只 deny，不改写命令；用本机 git。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/merge-gate) |
| path-guard | 拒绝项目根外或 .git 内的 Write/Edit（可选护 Read）。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/path-guard) |
| pii-guard | 台湾 PII 可逆脱敏（经本地 hookd）；需 Python/uv。 |  | [链接](https://github.com/danyuchn/pii-guard/tree/main/examples/claude-code-mod) |
| redact | Read 结果里把疑似密钥字符串替换成 `[REDACTED:…]` 再给模型。备注：改写的是 Read 结果文本，不改写命令。 | MIT | [链接](https://github.com/thkt/dotclaude/tree/main/mods/redact) |
| seatbelt | 本地规则拦截危险 Bash/写文件（只拒绝不改写命令）。备注：会 deny 匹配的工具调用。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/seatbelt) |
| secret-guard | 拦截即将写入文件或 Bash 的疑似密钥内容。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/secret-guard) |
| secret-mask | 在工具输出写入对话前遮罩疑似密钥。备注：会改写展示给模型的工具结果文本（本地遮罩，不外传）。 |  | [链接](https://github.com/homieyangg/claude-code-mods/tree/main/secret-mask) |
| secret-redactor | 在模型看到前把密钥/邮箱/IP 换成占位符，工具输入时再还原。 |  | [链接](https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/secret-redactor) |
| secret-sentry | 双向密钥清洗：模型看到前脱敏，并拦截把密钥写入受跟踪文件或 shell。备注：可 deny；脱敏 prompt/工具结果文本，不外传；本机 git。 | MIT | [链接](https://github.com/ccdwyer/secret-sentry) |
| secrets-veil | 工具执行后遮盖结果中的疑似密钥字符串，不改写命令本身。 | MIT | [链接](https://github.com/yonatangross/orchestkit/tree/main/mods/secrets-veil) |
| sensitive-file-guard | 拦截触及 .env/密钥/凭证路径的工具调用。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/sensitive-file-guard) |
| storage-guard | 存储保护器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/storage-guard) |
| test-guard | 拦截弱化/删除测试的 Write/Edit/Bash。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/test-guard) |

### 开发工具 Dev Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| auto-checkpoint | 每回合开始在 refs/claude-checkpoints 做工作树快照；/checkpoints 与 /undo-turn。纯本地 git。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/auto-checkpoint) |
| boot-sequence | 会话开始时做一次本机开机检查（git、工具链）。 | MIT | [链接](https://github.com/ccdwyer/boot-sequence) |
| change-ledger | /changes 列出本会话改过的文件和行数。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/change-ledger) |
| claude-mermaid | 把助手回复里的 mermaid 块画成彩色 box art。 |  | [链接](https://github.com/galElmalah/claude-mods/tree/main/claude-mermaid) |
| codebase-galaxy | 用盲文点阵把仓库文件画成星空，跟着 Claude 碰过的文件。 | MIT | [链接](https://github.com/ccdwyer/codebase-galaxy) |
| config-parse | 配置文件解析器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/config-parse) |
| diagram-render | 图表实时渲染。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/diagram-render) |
| diff-review | 每次 Edit/Write 后在侧栏展示未提交 hunk，keep/revert 按钮；revert 用本机 git apply -R（新建文件二次确认后 rm）。模型看不到操作。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/diff-review) |
| disk-janitor | 清理临时文件。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/disk-janitor) |
| editor-context | 在桌面端提示框上方显示 Cursor/VS Code 当前文件与选区，并在每次提交时把你正在看的内容悄悄告诉 Claude。 | MIT | [链接](https://github.com/talbarina/claude-editor-context/tree/main/plugins/editor-context) |
| file-explorer | VS Code 风格文件树/变更/历史/diff 窗格。 |  | [链接](https://github.com/tak-kam/claude-mods/tree/main/file-explorer) |
| files | 侧栏本会话新建/修改/删除的文件清单与行数（只观察工具，不改写）。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/files) |
| filetree | 侧栏文件树，跟住 Claude 正在读/写的文件并可点选带入提示。 |  | [链接](https://github.com/data-goblin/claude-code-filetree) |
| git-commit | Git 提交助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/git-commit) |
| git-gates | Git 工作授权与整洁：追踪用户提示，拦截未授权的 commit/push/merge；检查提交消息（Conventional Commits、issue... |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/git-gates) |
| glass | 给终端 transcript 换桌面级外观：着色命令、工具树、回合页脚等。 | MIT | [链接](https://github.com/rashedInt32/glass) |
| lean-comments | 限制注释膨胀：Edit/Write 时标记多注释编辑，回合结束时检查 diff 的新注释行；Haiku 审查不值得保留的注释（复述代码或叙述改动）。 |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-comments) |
| lean-docs | 文档值得保留：Haiku 审查 git checkout 中增长的文档（runbook、设置页、叙述）、标记代码重复标识符的文档行、回合结束时检查 dif... |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-docs) |
| lean-scripts | 脚本值得保留：Haiku 审查在 git checkout 中写入或增长的脚本，标记那些你需要时直接打出来更快的脚本。 |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-scripts) |
| lockfile-sync | 锁文件同步检查。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/lockfile-sync) |
| md-prompt | 输入时把 prompt 框画成 Markdown（代码块高亮等，不改原文）。 | MIT | [链接](https://github.com/nogu66/md-prompt/tree/main/plugins/md-prompt) |
| mdview | 侧栏渲染对话里的 Markdown，可点选让 Claude 改。 |  | [链接](https://github.com/xuanji86/claude-mdview) |
| proc-registry | /procs 面板登记本会话后台 Bash 与子代理；只观察，不改写工具。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/proc-registry) |
| repo-pulse | 显示仓库活动脉搏，仅本地 git status 查询。 | MIT | [链接](https://github.com/5d0tal1gat0r/repo-pulse) |
| skill-session-mods | 按本地 SKILL.md 元数据给 /skill 会话命名与上色（只读本地技能文件）。 | MIT | [链接](https://github.com/aksh1618/claude-mods/tree/main/skill-session-mods) |
| shell-flow | 状态行与窗格跟踪本会话 Bash/后台任务与 runner；只观察。备注：本机 process（tail）。 | MIT | [链接](https://github.com/apolenkov/claude-mods/tree/main/mods/shell-flow) |
| skins | 给 transcript 换肤：主题化工具行、回复边栏与 spinner 文案；桌面端把表格/代码/diff/shell 画成动画卡片。 | MIT | [链接](https://github.com/hellosverre/claude-skins) |
| spx-chart | 在侧栏查看 PHP SPX 性能火焰图（需 php-spx-mcp）。 |  | [链接](https://github.com/zviryatko/claude-spx) |
| statusbar | 状态栏显示当前 git 分支与仓库状态，仅本地 git rev-parse 查询。 | MIT | [链接](https://github.com/sgmonda/statusbar) |
| touch-map | 文件活动热力图：把 Claude 本会话读过、写过的文件画成文件树热力图，按访问频率着色。 | MIT | [链接](https://github.com/y-hirakaw/claude-code-mods/tree/main/touch-map) |
| transit-map | 把 git 历史画成地铁图，分支是线，提交是站。 | MIT | [链接](https://github.com/ccdwyer/transit-map) |

### 子代理管理 Subagent Management

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| agents-view | 侧栏列出本会话子代理状态，点选查看 prompt/工具结果。纯 UI。 |  | [链接](https://github.com/ushironoko/dotfiles/tree/main/claude/.claude/skills/agents-view) |
| agent-radar | 每个运行中子代理一行实时状态。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/agent-radar) |
| agent-router | 代理路由器，管理子代理调用。 |  | [链接](https://github.com/alexandernicholson/agent-router/tree/main/agent-router) |
| agent-watch | 子代理侧栏：在窗格里列出活跃子代理、状态与简报，点击可查看 transcript。 | MIT | [链接](https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/agent-watch) |
| claude-council | 并行运行多个编码代理，可并排查看。 |  | [链接](https://github.com/hex/claude-council) |
| council | 代理协商决策。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/council) |
| fable-pin | 每个子代理运行你选的模型，不是提示要的那个：在 agent.spawn 时将 model 改写为 fable（除非是 fork 继承父级），/fable-... |  | [链接](https://github.com/karanb192/claude-code-mods/tree/main/plugins/fable-pin) |
| flightdeck | 只读观测面板，集中看权限裁决与子代理进度。 |  | [链接](https://github.com/scasella/claude-flightdeck) |
| multi-core | 把 ChatGPT/Cursor/Zen 等接入 /model（需 claude-multi launcher）。 |  | [链接](https://github.com/greenpolo/cc-multi-cli-plugin/tree/main/plugins/multi-core) |
| plan-progress | 计划进度条 + 子代理条带。 |  | [链接](https://github.com/zycck/claude-mods/tree/main/plugins/plan-progress) |
| subagent-ledger | 子代理账本。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/subagent-ledger) |
| swarm | 子代理/团队任务控制室窗格。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/swarm) |

### 通知提醒 Notifications & Alerts

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| atelier-bell | 告知 atelier 完成时机：flux7-studio 渲染进度显示为 toast 和状态行（studio: rendering、studio: las... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/atelier-bell) |
| avatar7 | 机器脸随工具调用作评论，可选声线（SHODAN、HAL、GLaDOS 风格实验室 AI、Ada、duck7、Pod 042、Kaneda、Commis），... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/avatar7) |
| cc-pr-tracker | 在提示框上方盯着 GitHub PR 的合并状态、评审与必需检查，有变化时 toast。 | MIT | [链接](https://github.com/sezaakgun/cc-pr-tracker) |
| commit-cadence | 提交节奏提醒。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/commit-cadence) |
| commit-drift | 状态行未提交文件数与距上次提交时间，久未提交会提醒。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/commit-drift) |
| desk-notify | 桌面通知提醒。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/desk-notify) |
| ding | 长回合结束 toast+可选音效提醒。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/ding) |
| done-blink | 主回合结束后闪烁 iTerm2 标签页，直到再次输入或超时。仅本机 tty/本地 shell。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/done-blink) |
| error-poke | 错误提醒助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/error-poke) |
| gfm-render | 在 transcript 里渲染 GFM：alerts、任务列表、删除线与 Mermaid。 | MIT | [链接](https://github.com/briangtn/claude-gfm-render) |
| mesh7-pane | 从 localhost:9090 每 1.5 秒轮询 mesh7 决策：每次调用的 ALLOW/DENY/HUMAN 及规则参数、待批准请求、紧急停止横幅... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/mesh7-pane) |
| notice-board | 同仓库各会话共享通知板。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/notice-board) |
| notify | 桌面通知：Claude 回合完成或等待决策时发系统原生通知，后台时召回焦点。 | MIT | [链接](https://github.com/XD3an/cc-notify) |
| notify-on-finish | 长回合结束后桌面通知（macOS osascript / Linux notify-send / 否则 toast）。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/notify-on-finish) |
| nowloading | 显示加载动画与进度提示。 | MIT | [链接](https://github.com/vgnshiyer/nowloading) |
| pomodoro | 番茄钟状态条与配置面板，纯本地计时与提醒。 | MIT | [链接](https://github.com/sneycampos/claude-pomodoro) |
| reminder-log | 本地提醒日志窗格。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/reminder-log) |
| task-poke | 任务提醒助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/task-poke) |

### 吉祥物与宠物 Mascots & Pets

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| clawd | 思考行旁的像素 Clawd 吉祥物，按工具/命令表演动作。 |  | [链接](https://github.com/raresmun/claude-mods/tree/main/plugins/clawd) |
| clawdgotchi | 电子宠物 Clawd，在侧栏养成与互动。 | MIT | [链接](https://github.com/arthurseredaa/clawdgotchi) |
| code-pet | 像素宠物窗格，随 Claude 活动反应。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/code-pet) |
| maomao | 提示框上方 8-bit 毛毛（垂耳兔）随工作状态跑跳；/maomao 收起或叫出。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/maomao) |
| mize-coworker | 像素 Claude 吉祥物，随 spinner 词表演场景，空闲时在状态行呼吸走动。 | MIT | [链接](https://github.com/TheMizeGuy/clawdagotchi/tree/main/plugins/mize-coworker) |
| muse-pet | 提示框上方像素 Muse：等待时招手/叮咚，长回合结束跳跃，显示上下文与费用；/muse 可从 gadget.mububu.app 拉取自定义形象。备注：可选访问外网拉宠物料 JSON，不上传会话；本机 process（claude --version）。 | MIT | [链接](https://github.com/Soyn/mububu-pet) |
| plushie | 提示框上方的毛绒 Clawd，会随工具/上下文做出反应。 | MIT | [链接](https://github.com/xyc/plushie) |
| pocket-familiar | 伴随工作的养成伙伴窗格。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/pocket-familiar) |
| quota-pets | 额度假宠扭蛋：每对话抽猫/狗，限额告急讲鬼故事、用完阵亡；context 当肚子（/petdex 肚子）。备注：本机读 session.messages 估算肚子内容。 |  | [链接](https://github.com/Open01277/claude-mods/tree/main/plugins/quota-pets) |

### 图片与媒体 Images & Media

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| adlib-lyrics | 用 osascript 读取本机 Music/Spotify 当前曲目，并向 lrclib.net 拉取歌词显示在提示框上方（会访问外网歌词 API）。 | MIT | [链接](https://github.com/bixxter/adlib-lyrics) |
| figures | 在 kitty-graphics 终端内联绘制 mermaid/LaTeX/工具结果图片。需本机 mmdc/mmdr/dot/d2 等渲染器在 PATH。 | Apache-2.0 | [链接](https://github.com/natsukium/claude-code-figures-plugin) |
| claude-image-generation | 通过 tool.call 生成图像。 |  | [链接](https://github.com/hex/claude-image-generation) |
| darkroom | 把 Claude 读/写/生成以及你粘贴的图片做成聊天里的胶片条预览。 | MIT | [链接](https://github.com/govlog/claude-darkroom) |
| image-peek | 文本光标移到粘贴的 [Image #1] 标记上时显示图像，移开隐藏；宽窗口用大预览窗格（深色画布居中），窄窗口用提示框上方区域；键盘焦点保持在提示框。 |  | [链接](https://github.com/karanb192/claude-code-mods/tree/main/plugins/image-peek) |
| image-preview | 会话图片窗格预览。备注：本地 sips/magick 转 PNG，不外传。 |  | [链接](https://github.com/scoobynko/claude-code-mods/tree/main/plugins/image-preview) |
| image-view | 粘贴图片后在提示框上方显示像素缩略图。 |  | [链接](https://github.com/jarrodwatts/claude-image-view) |
| jukebox7 | 白话点播音乐（"放点环境音"）：YouTube 音频通过隐藏 VLC 播放，无需浏览器也不抢焦点；窗格带流派按钮（每个是艺人电台）和当值头像的精选。 | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/jukebox7) |
| lightbox | 粘贴图片时在提示框上方大预览，并带说明缩略图。 | MIT | [链接](https://github.com/arihantbansal/claude-lightbox) |
| mathcat | 把公式渲成 PNG 并在窗格展示。备注：依赖本机已安装的 `mathcat` CLI（同仓库 Python 包）。 | Do No Harm | [链接](https://github.com/johndpope/mathcat) |
| md-view | 点击回复里的 Markdown 文件渲染预览。 |  | [链接](https://github.com/scoobynko/claude-code-mods/tree/main/plugins/md-view) |
| music-mod | 通过 osascript 控制 macOS Music.app 播放音乐。 | MIT | [链接](https://github.com/zyx1121/music-mod) |
| paste-peek | 粘贴图片实时像素预览（⌥←/→ 切换，⌥↑ 放大，⌥↓ 侧栏）；需支持图片的终端。 | MIT | [链接](https://github.com/nokiy/claude-code-mods/tree/main/plugins/paste-peek) |
| paste-view | 在提示框上方预览粘贴的图片缩略图与长文本。 | MIT | [链接](https://github.com/Amorfx/claude-paste-view) |
| radio | /radio 在会话里听网络电台，状态行与提示框上方控制。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/radio) |
| shot-view | 收集 Read/工具里的 PNG，/shots 侧栏翻页预览。备注：本机 process（sips/open）。 | MIT | [链接](https://github.com/Bearisbug/cc-mods/tree/main/shot-view) |
| mermaid-inline | 把助手回复里的 mermaid 围栏画进 transcript（图片或盒装 ASCII）；本机 node 跑插件内置 render-svg。fork of claude-mermaid。 | MIT | [链接](https://github.com/Conte777/mermaid-inline/tree/main/mermaid-inline) |
| terminal-browser | 在会话旁嵌入终端浏览器，预览网页/本地 HTML/PR。 | MIT | [链接](https://github.com/zenbu-labs/terminal-browser/tree/main/claude-code-plugin) |
| yt-control | 用本机 cliamp 控制 YouTube 播放。缩略图只按视频 id 从 i.ytimg.com 拉取，不上传会话内容。备注：本机 process（需已装 cliamp/yt-dlp）。 | MIT | [链接](https://github.com/Unayung/cc-mods-youtube/tree/main/plugins/yt-control) |

### 任务与项目 Task & Project

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| backlog-band | 提示框上方显示 BACKLOG.md 的 Now 项。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/backlog-band) |
| backlog-pane | 侧栏看 git 状态和 Backlog.md 任务。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/backlog-pane) |
| bg-tasks | 后台任务管理器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bg-tasks) |
| check-ledger | 记录跑过哪些检查、之后又有哪些编辑（/evidence）。 |  | [链接](https://github.com/LeeHigma0201/claude-code-mods/tree/main/mods/check-ledger) |
| cockpit | 计划/todo 进度条，并按 quick/normal/hard 路由模型与 effort。 |  | [链接](https://github.com/Brxerq/claude-cockpit/tree/main/plugins/cockpit) |
| deadlines | 状态行的截止日期倒计时，/ddl 增删。 |  | [链接](https://github.com/richardcsuwandi/claude-mods/tree/main/plugins/deadlines) |
| departure-board | 翻牌式出发板，把当前任务翻成车站到发显示。 | MIT | [链接](https://github.com/ccdwyer/departure-board) |
| dev-dash | 开发者仪表板窗格，集中显示会话状态与项目信息。 |  | [链接](https://github.com/RanaRauff/claude-dev-dashboard/tree/main/plugins/dev-dash) |
| gsd-status-mod | 面向 GSD 项目：在提示框上方显示阶段/进度与 STATE.md 漂移警告，并把下一步动作放进提示行。 | MIT | [链接](https://github.com/helenkwok/gsd-status-mod) |
| human-in-the-loop | 把只有用户能做的事挂在 My tasks 窗格里，完成后再回给 Claude。 | MIT | [链接](https://github.com/tzafrir/human-in-the-loop) |
| loose-ends | 追踪会话中未完成的待办事项，回合结束用 $.model.complete 总结剩余任务。 | MIT | [链接](https://github.com/fernandomoraes/loose-ends) |
| party | 本机多会话面板；别的会话碰过同一 PR 时 ask，不改写命令。/broadcast 把用户刚输入的文字发给本机另一个会话。备注：本机 git。 | MIT | [链接](https://github.com/pourya7/claude-code-mods/tree/main/party) |
| standup | 跨会话记录你的提问与改动文件，/standup 用模型写成日报摘要。 | MIT | [链接](https://github.com/claudemodz/mods/tree/main/plugins/standup) |
| sticky-todos | 待办侧栏；观察 TodoWrite/Task*，不改写工具。 | MIT | [链接](https://github.com/paweechinagarn/claude-code-mods/tree/main/sticky-todos) |
| sudus | 本地运行 sudus wake（或插件自带 node bin）在提示框上方或窗格显示项目 verdict；不调用模型。 | MIT | [链接](https://github.com/eas4ai/sudus) |
| taskcut | turn.step mod。 | MIT | [链接](https://github.com/wasd96040501/taskcut) |
| task-eta | 长任务步骤与剩余时间。超时用 $.model.fork，提示里带工具轨迹、用户新消息和回复片段。备注：使用 $.model.fork。 | MIT | [链接](https://github.com/Bearisbug/cc-mods/tree/main/task-eta) |
| tasknotes-preview | 侧栏按 Obsidian Bases 视图展示 TaskNotes（看板/列表/日程/依赖图）；本机读 vault，本机 process 打开 Obsidian。 | MIT | [链接](https://github.com/cbruyndoncx/claude-tasknotes-renderer-mod) |

### 外部集成 External Integrations

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| calendar | AbovePrompt 显示即将到来的 Google Calendar 事件（/cal）。备注：通过用户已配置的「claude.ai Google Calendar」MCP 读取。 | MIT | [链接](https://github.com/musingfox/cc-plugins/tree/main/calendar) |
| gh-ci-status | 提示框上方钉住 GitHub Actions 状态。 |  | [链接](https://github.com/diegorv/claude-functions-hook/tree/main/plugins/gh-ci-status) |
| inbox-pane | 侧栏窗格展示 claude-inbox 各分区会话，支持快捷键操作。备注：读写本机 `~/.config/claude-inbox/`；可在无写入时拉起 ... |  | [链接](https://github.com/jordanbyron/claude-inbox/tree/main/mod) |
| linear-claude-mod | Linear 指派工单面板；点击可加载详情、评论或改状态。 | MIT | [链接](https://github.com/rjohnt/linear-claude-mod) |
| oneform-line | 提示框上方显示 OneForm 当日睡眠/蛋白/训练与下周计划；/oneform 查看全日。备注：用用户配置的 OneForm URL + API key... |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/oneform-line) |
| pr-pane | /prs 提示框上方列出你的 GitHub PR 并可打开。 | MIT | [链接](https://github.com/ASRagab/asragab-claude-marketplace/tree/main/plugins/pr-pane) |
| pr-relay | 监视会话 PR，合并或 Codex 评论时唤醒。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/pr-relay) |
| pulse-cc | 提示框上方显示股票报价（Yahoo 或 Pulse Mac 自选）。 | MIT | [链接](https://github.com/fatwang2/Pulse/tree/main/plugins/claude-code) |
| tw-stock-mod | 提示框上方的台股/美股观察清单带状栏，台股交易时段显示台股（红涨绿跌）、美股交易时段显示美股（绿涨红跌）；支持 Yahoo 延迟报价或券商即时行情（永豐 ... |  | [链接](https://github.com/darrell-tw/darrelltw-mods/tree/main/mods/tw-stock-mod) |

### 本地工具 Local Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| adhkar | 在 Claude Code 中显示赞念/记主内容。 |  | [链接](https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/adhkar) |
| copy-band | 上一条回答的代码块/引用草稿一键复制到剪贴板，并本地 stash。依赖本机 pbcopy（macOS）与本地文件。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/copy-band) |
| daily-ayah | 每日经文展示。 |  | [链接](https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/daily-ayah) |
| garde-du-corps | 本地拒绝访问 .env 与危险 Bash（rm -rf、force push、hard reset、DROP TABLE）；只读路径/命令字符串做 den... | MIT | [链接](https://github.com/Para-FR/claude-code-mods-fr/tree/main/garde-du-corps) |
| prayer-times | 提示框下方显示下次礼拜时间。 | MIT | [链接](https://github.com/mkbuilds4/mods/tree/main/plugins/prayer-times) |
| prompt-stash | 本地 /stash 提示词栈：存、列、弹出到输入框，不进模型上下文。 |  | [链接](https://github.com/gonzaloserrano/cc-prompt-stash) |
| push | /push 把当前分支推到上游；本机 git。 |  | [链接](https://github.com/robertgregorywest/claude-mods/tree/main/mods/push) |
| sportscaster | 会话实况解说（本地 $.audio.speak，不上传会话）。备注：使用本机 TTS。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/sportscaster) |
| tmux-status | 把 Claude 状态（working/waiting/done）写到本机 tmux 窗口选项。备注：本机 process（tmux）。 | MIT | [链接](https://github.com/XavierYounan/claude-code-tmux-status) |

### 其他工具 Other Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| action-pin | 把常用动作钉在提示框上方。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/action-pin) |
| ask-autopick | 自动采纳或拒绝提问。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ask-autopick) |
| behavior-map | 改动前后行为流图。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/behavior-map) |
| bughunt | 追踪与报告 bug。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bughunt) |
| cc-side | 提供 /side 命令开启第二个对话。 |  | [链接](https://github.com/Ahmad8864/cc-side) |
| claude-queue | /q 在回合进行中排队提示，回合结束后自动发出。 |  | [链接](https://github.com/galElmalah/claude-mods/tree/main/claude-queue) |
| constellation-claude | 注册导出 mod。 | AGPL-3.0 | [链接](https://github.com/ShiftinBits/constellation-claude) |
| ContextSaver | 标记浪费会话习惯。 | MIT | [链接](https://github.com/AlmogBaku/ContextSaver) |
| contract-watch | 监视合约变更。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/contract-watch) |
| cost-bar | AbovePrompt 费用条：本会话花费、5h/7d 计划限额与可选预算条。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/cost-bar) |
| cueloop | tool.call mod。 | Apache-2.0 | [链接](https://github.com/mmurakaru/cueloop) |
| dep-sentinel | 依赖变更哨兵。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/dep-sentinel) |
| doc-drift-watch | 监视文档漂移。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/doc-drift-watch) |
| edit-loop | 编辑循环检测。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/edit-loop) |
| effort-auto | 自动切换 effort。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/effort-auto) |
| effort-cycle | Alt+E / Alt+Shift+E 切换 effort，页脚显示模型与档位。 | MIT | [链接](https://github.com/Anerco/claude-code-effort-cycle) |
| env-sync | 环境变量同步。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/env-sync) |
| essential-conversation | 精简对话显示，只保留核心内容。 |  | [链接](https://github.com/SuzumiyaAoba/claude-essential-conversation-mod) |
| fault-lacquer | 失败的操作在漆片上裂开，修好后愈合。 | MIT | [链接](https://github.com/ccdwyer/fault-lacquer) |
| flaky-memory | 不稳定记忆诊断。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/flaky-memory) |
| fortune-cookie | 提示框上方随机显示程序员幸运饼干语录。 | Apache-2.0 | [链接](https://github.com/tobinsouth/fortune-cookie-mod) |
| gemini-advisor | Gemini 顾问模式。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-advisor) |
| gemini-core | Gemini 核心集成。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-core) |
| gemini-plan-review | Gemini 计划审查。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-plan-review) |
| gemini-review | Gemini 代码审查。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/gemini-review) |
| holdtime | 显示 Claude 工作耗时，回合结束时用 $.model.complete 生成总结（可能替换默认 turn.complete 文本）。 | MIT | [链接](https://github.com/ItsRohith-A/holdtime) |
| i18n-watch | 国际化监视器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/i18n-watch) |
| idle-art | 空闲时显示艺术。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/idle-art) |
| Katharsis | prompt.submit mod。 | MIT | [链接](https://github.com/OpenScribbler/Katharsis) |
| lcm | tool.call / prompt.submit mod。 | MIT | [链接](https://github.com/lossless-claude/lcm) |
| leftovers | 记下 Claude 留在本机或服务器上的后台进程。 | MIT | [链接](https://github.com/homieyangg/claude-code-mods/tree/main/leftovers) |
| live-thinking | 对话里流式显示 thinking 摘要。 |  | [链接](https://github.com/AJclemendor/my-mods/tree/main/plugins/live-thinking) |
| mcp-doctor | MCP 健康诊断。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/mcp-doctor) |
| memory-save | 记忆保存助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/memory-save) |
| mindful-claude | 显示呼吸带。 |  | [链接](https://github.com/halluton/Mindful-Claude) |
| mod-doctor | Mod 健康检查。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/mod-doctor) |
| mod-hub | /mods 列出同目录的 mod；用户按开关时，在本机改写那个 mod 的 hooks/hooks.json，关掉时再写入 hooks/off.tsx。 |  | [链接](https://github.com/eshin087/claude-code-mods/tree/main/mod-hub) |
| mr-banner | MR/PR 相关横幅提示。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/mr-banner) |
| no-attribution | 去掉或替换 Co-Authored-By 提交尾注与 "Generated with Claude Code" PR 页脚。 | MIT | [链接](https://github.com/claudemodz/mods/tree/main/plugins/no-attribution) |
| orphan-server | 孤儿进程检测。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/orphan-server) |
| output-flood | 输出洪水控制。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/output-flood) |
| pin-note | 固定便签功能。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/pin-note) |
| probe-runner | 探针运行器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/probe-runner) |
| prompt-deck | 提示卡片管理。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-deck) |
| prompt-offload | 提示卸载优化。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-offload) |
| prompt-time | 提示时间标记。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/prompt-time) |
| prompter | 边聊边整理需求：把零散想法变成干净 brief，并填入本仓库上下文。 |  | [链接](https://github.com/niijoey/prompter-mod/tree/main/plugins/prompter) |
| sage-memory | 智慧记忆系统。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sage-memory) |
| self-command | 自定义命令系统。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/self-command) |
| session-brief | 提示框上方保持会话简报；/brief 补充已做决定与下一步。 |  | [链接](https://github.com/skanehira/claude-session-brief) |
| session-watch | 会话监视器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/session-watch) |
| session-wrapped | 会话「年终总结」式统计动画。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/session-wrapped) |
| shot-inline | 内联截图功能。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/shot-inline) |
| slash-chain | 斜杠命令链。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/slash-chain) |
| sql-concat-watch | SQL 拼接监视。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sql-concat-watch) |
| time | 每条用户消息上方显示发送时间。 |  | [链接](https://github.com/diegorv/claude-functions-hook/tree/main/plugins/time) |
| tool-coach | 工具使用教练。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/tool-coach) |
| turn-timeline | /timeline 把当前回合画成时间线。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/turn-timeline) |
| typing-speed | 提示框上方打字速度计，提交后显示 WPM、准确率与个人最佳。 | MIT | [链接](https://github.com/borabiricik/claude-mods/tree/main/plugins/typing-speed) |
| ua-fallback | 用户代理降级。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ua-fallback) |
| where-am-i | 提示上方只读回顾：目标/正在做/等你什么（观察工具调用，不改写）。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/where-am-i) |
| winnow | 精简大型未使用的工具结果。 |  | [链接](https://github.com/GhalebDweikat/winnow) |
| zsh-safe | 把 bash 写法的 Bash 命令改写成 macOS zsh 可跑。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/zsh-safe) |

---

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

# Claude Code Mod Marketplace · Claude Code 插件市场

**cc-mod-hub** is a curated Claude Code mod marketplace. A mod is a TypeScript event hook (such as tool.call, ui.render, etc.) packaged inside a plugin, not a general skill or slash command.

**cc-mod-hub** 是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。这个 plugin marketplace 提供 795 个精选的 Claude Code mods，包括内置核心 mod、官方示例以及社区开发的 TypeScript hooks。

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

**cc-mod-hub** is a curated Claude Code plugin marketplace featuring 795 hand-picked mods. Mods are TypeScript hooks that extend Claude Code's behavior by intercepting events like `tool.call`, `ui.render`, `prompt.submit`, and more.

This marketplace includes:
- **Built-in mods** from the Claude Code core repository
- **Official examples** from Anthropic's playground
- **Community mods** contributed by developers worldwide

### How to Use

1. Add this marketplace: `/plugin marketplace add shuizhengqi1/cc-mod-hub`
2. Browse the [mod list below](#mod-列表--available-mods) (organized by category)
3. Install: `/plugin install <mod-name>@cc-mod-hub`

For detailed descriptions of all 795 mods, see the Chinese section below.

---

## 📦 Mod 列表 | Available Mods

以下是本市场的 795 个精选 Claude Code mods，按类别组织：


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
| barra-usage-model | 提示框上方显示 5 小时、每周与上下文用量条（界面文字为葡萄牙语），提示框下方显示精简百分比、模型与 effort，可点击收起或展开（只读 $.session.usage）。备注：有内容时 AbovePrompt 与 SessionMode 不调 next，会盖掉其他 mod 在这两处的显示。 | MIT | [链接](https://github.com/sidneyfrancois/barra-usage-model) |
| budget-guard | 费用与 5 小时/7 天限额：接近上限警告，超额拒绝工具调用。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/budget-guard) |
| burn | 提示框上方限额/用量积分与花费；/burn 看近 7 天。备注：用本机 Anthropic OAuth 读官方用量 API，不带会话正文。 | MIT | [链接](https://github.com/PickleBoxer/burn) |
| burn-meter | 提示框上方会话花费「火焰」条与限额，/burn 看每回合费用。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/burn-meter) |
| cache-bar | 提示框上方显示 prompt 缓存 TTL 倒计时、命中率和缓存失效原因，带详情窗格；只观察提示段和工具描述，原样返回。备注：AbovePrompt 显示时不调 next，可能盖住同样改这块的 mod；保活用 $.model.fork，只多发一句「Reply with the single word: ok」（默认手动点按钮或 /cache-extend，设为 auto 时在快过期时自动 fork）；每秒刷新倒计时。 | MIT | [链接](https://github.com/TheTsungYing/claude-cache-bar/tree/main/plugins/cache-bar) |
| cache-clock | 显示提示缓存还热多久。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/cache-clock) |
| cache-countdown | 提示框上方缓存导火索与上下文/限额条；可按钮 Keep warm 或 Compact。备注：Keep warm 用 $.model.fork；可读本地 transcript（process/fs）。 | MIT | [链接](https://github.com/iamomiid/cache-countdown) |
| cache-meter | 提示框上方提示缓存剩余 TTL 条。 |  | [链接](https://github.com/DarioFontanel/claude-code-mods/tree/main/cache-meter) |
| cache-refresher | 提示缓存倒计时与 lapse 成本；可选 $.model.fork 保活 ping。备注：使用 $.model.fork。 | MIT | [链接](https://github.com/olddonkey/cache-refresher) |
| cost-meter | 会话费用实时条（同 /cost 口径），可选预算阈值与颜色提示。 | MIT | [链接](https://github.com/zaferayan/claude-cost-meter/tree/main/cost-meter) |
| cost-info | 会话费用与 token 实时显示（同 /cost 口径），可选预算 toast。 | MIT | [链接](https://github.com/falconsw/cost-info/tree/main/cost-info) |
| cache-tax | 提供 /keepwarm 命令，阻止一次冷启动发送。 |  | [链接](https://github.com/karanb192/cache-tax) |
| cache-timer | 倒计时提示缓存何时过期。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/cache-timer) |
| cache-ttl-timer | 提示缓存 TTL 倒计时，并 tail 本地 transcript 文件。 | MIT | [链接](https://github.com/WQGGSEY/cache-ttl-timer) |
| cache-warm | 缓存预热工具。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/cache-warm) |
| cache-warmer | 提示缓存保温：缓存过期前自动用 $.model.fork 复刻主会话最后一次请求，添加提示 "Prompt cache refresh. Reply with the single word ok."，不拒绝工具也不限输出长度，按普通请求计费；空闲时默认最多 5 次，且每次须预计省下至少 $0.05，并显示每次刷新费用与估算节省；可在 5m 与 1h 缓存寿命间切换（本会话设 CLAUDE_CODE_PROMPT_CACHE_TTL 环境变量，1h 写入为 2 倍输入价）。备注：每次刷新用 $.session.append 往会话记录写一条系统通知；提示框上方条显示时 AbovePrompt 不调 next，可能盖住别的条；开调试时本机写 ~/.claude/cache-warmer/debug。 | MIT | [链接](https://github.com/paulbkim-dev/claude-code-cache-warmer) |
| cache-watch | 提示缓存重建时 toast 告警并估算回合费用。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cache-watch) |
| ccoverhead | 提示框上方显示上下文窗口、每轮增长、5h/7d 额度与缓存热度（只读会话用量）。 | MIT | [链接](https://github.com/shengyy/ccoverhead/tree/main/plugin) |
| cctop | btop 风格侧栏面板，展示上下文、tokens、成本、工具延迟等。 |  | [链接](https://github.com/tomstagl/cctop/tree/main/plugin) |
| clawd-dash | 输入框下方的会话仪表盘（用量额度、上下文、费用、模型、effort、改动行数、git 状态），并带 Clawd 动画。备注：本机只跑 `git status --porcelain --branch`；tool.call 原样 next，只统计；显示时替换 PromptHint 并自绘原提示文字（不调 next）。 | Apache-2.0 | [链接](https://github.com/pinkpixel-dev/clawd-dash) |
| clawd-spinner | Clawd 按 spinner 词表演动画（本地绘制，零 token）。 | MIT | [链接](https://github.com/saiharsha03/clawd-spinner) |
| clawd-hud | 提示框上方像素 Clawd 用量带：上下文与限额，回合中显示实时 token 估计。纯 UI。 |  | [链接](https://github.com/segfaultlab/clawd-hud) |
| claude-chef | 提示框上方上下文占用预报与火花图，纯 UI。 | MIT | [链接](https://github.com/schalkneethling/claude-chef) |
| context-bar | 提示下方（可改上方）显示上下文窗口进度条与 prompt-cache TTL 倒计时。备注：可 tail 本地 transcript；仅本地读。 |  | [链接](https://github.com/k-wolfe99/claude-context-bar/tree/main/mod) |
| context-band | 限额/token/缓存/费用状态带。备注：本机 process（主题检测与本地 python 估价）。 |  | [链接](https://github.com/EricJamie/claude-code-mods/tree/main/plugins/context-band) |
| context-tokens | 桌面端提示脚旁显示上下文 token 用量（绿/黄/红阈值）。纯 UI，只读 $.session.usage。 | MIT | [链接](https://github.com/0xBADC0FFEE/claude-code-mods/tree/main/context-tokens) |
| context-weather | 提示框上方上下文占用条、会话费用与计划限额，接近压缩时 toast。纯 UI。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/context-weather) |
| context-xray | 窗格拆开上下文占用：系统提示、工具、记忆、skills、消息。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/context-xray) |
| cost-pane | 费用窗格：本会话与按日花费汇总。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/cost-pane) |
| effort-guard | 上下文/token 条带、升级信号与每回合 effort 日志。 | MIT | [链接](https://github.com/stefanochieli/claude-effort-guard) |
| eta | 在 spinner 行显示本轮剩余时间（按任务节奏或历史回合学习，零 token）。 |  | [链接](https://github.com/hamza-siddiq/claude-eta/tree/main/eta) |
| glance | 提示下方 HUD：模型、本机 git、费用、上下文与 5h/7d 条、工具/技能/MCP/子代理与 todo；只读会话与本机 git status。备注：本机 process（git）；PromptHint 不调 next（可把引擎 hint 画在 HUD 下方）。 | MIT | [链接](https://github.com/VibeMage/claude-mod-glance) |
| limit-bars | 提示框下四个动画环，显示上下文、会话和周限额。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/limit-bars) |
| limit-meter | 提示框上方 5h/周限额条与重置倒计时；/limits；可 toast 告警。纯 UI，只读会话用量。 | MIT | [链接](https://github.com/Alyan-khattak/Claude-Code-Mods/tree/main/limit-meter) |
| limit-watch | 限额监视器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/limit-watch) |
| medidor-de-caixa | 提示框上方一行（葡萄牙语）显示本会话按 API 价格估算的花费、上一次请求的增量、上下文百分比，以及 1 小时提示缓存还剩几分钟，剩 5 分钟时弹提醒。只读 session.usage，AbovePrompt 调 next，不改提示或工具，不联网。 |  | [链接](https://github.com/plasdigital/mods-claude-code-kit-aluno/tree/main/mods/medidor-de-caixa) |
| mod-usage | 桌面/VS Code/移动端提示框上方显示上下文与 5 小时/7 天用量渐变条（只读 $.session.usage / session.measure）；AbovePrompt 会先调 next 再叠在其他 band 下方；可配置语言。备注：本机 process 可能读 macOS defaults 以解析显示语言。 | MIT | [链接](https://github.com/jack21/claude-mod-usage) |
| native-hud | 输入框下方原生 HUD：模型、路径、git/worktree、上下文、5h/7d 用量、输出速度与缓存命中。备注：本机 git。 | MIT | [链接](https://github.com/Luban-Labs/native-hud) |
| netrunner-hud | 会话仪表盘：上下文条、token 示波与状态窗格。 | MIT | [链接](https://github.com/ccdwyer/netrunner-hud) |
| omp-quota | omp 各 provider 剩余配额条（/quota）；备注：通过本机 `omp usage --json` 读取，不改写工具。 | MIT | [链接](https://github.com/musingfox/cc-plugins/tree/main/omp-quota) |
| overalls | 提示框上方状态条：上下文预报、用量限额，以及 Ponytail/Caveman 档位（可配置）。 | MIT | [链接](https://github.com/Troepster/overalls) |
| pets | 像素宠物窗格：闲逛、记笔记、完成回合时跳跃、限额 80% 流泪、闲置两分钟午睡；八种动物（猫、小鸡、狗、史莱姆、兔子、仓鼠、企鹅、青蛙），可命名、喂食、升... | MIT | [链接](https://github.com/uppinote20/claude-pets) |
| pro-hud | Pro 计划用量表盘：5 小时、7 天限额、上下文和回合回执。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/pro-hud) |
| prompt-cache-control | 提示框上方提示缓存命中/写入与过期倒计时；/cache 打开每回合表。纯 UI，只读会话缓存用量。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/observability/prompt-cache-control) |
| quota-meter | 计划限额条与重置倒计时。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/quota-meter) |
| session-dash | 会话仪表盘窗格：用量与回合概览。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/session-dash) |
| session-receipt | /receipt 窗格列出每回合的 token 花费。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/session-receipt) |
| shunt | 用用户自己的 gateway / token（SHUNT_* 或 ANTHROPIC_*）请求 GET /usage，在本地显示配额窗口；请求体为空。 | MIT | [链接](https://github.com/pleaseai/shunt/tree/main/plugins/shunt) |
| slick-bar | 提示脚状态条：模型/目录/分支/上下文/限额与可选 cache-warm。备注：PromptHint 渲染时不调用 next，可能覆盖其他 mod 的提示行；本机 git。 | MIT | [链接](https://github.com/mustafa89/my-claude-code-mods/tree/main/slick-bar) |
| spend-meter | 状态行显示会话费用、上下文与 5 小时限额。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/spend-meter) |
| statuspane | 提示框上方浮动状态卡：模型、effort、上下文、5 小时/周限额、费用与分支，另有可供脚本/其他 mod 写入的进度条 API。 | MIT | [链接](https://github.com/xuanji86/claude-statuspane) |
| statusband | 提示框上方两行状态带：上下文、缓存倒计时、限额与 git。备注：本机 git。 | MIT | [链接](https://github.com/dip497/claude-statusband) |
| statusline | 桌面端提示框上方显示上下文 tokens、会话费用与缓存冷却估计。纯 UI。 | MIT | [链接](https://github.com/david-crespo/dotfiles/tree/main/claude/mods/statusline) |
| status-hud | 提示框上方活动阶段与 5h/周限额/上下文窗口状态条。纯 UI。 | MIT | [链接](https://github.com/hymleong/claude-mods/tree/main/plugins/status-hud) |
| token-ledger | 会话成本与上轮 tokens；面板查看近期回合。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/token-ledger) |
| token-limit | 在提示框底栏用彩色小条显示上下文占用和 5 小时/7 天等限额（含 5 小时重置时间），以及当前模型和推理强度。只读用量，turn.step 原样转发；SessionMode 插槽不调用 next 而自绘（保留模式名）。不联网。 |  | [链接](https://github.com/akagaya/claude-code-mods/tree/main/plugins/token-limit) |
| token-meter | 提示框上方会话 token/工具次数/工作时长与缓存倒计时带。不只是纯 UI：除非调查显示时，AbovePrompt 带不调 next，可覆盖其他 mod 行。 |  | [链接](https://github.com/tunglt1810/claude-gadgets/tree/main/mods/token-meter) |
| token-usage | 窗格与提示上方条显示上下文、限额窗口和费用；只读 $.session.usage；条显示时 AbovePrompt 不调 next；/usage-band 命令可能与已有 usage-band 冲突。 | MIT | [链接](https://github.com/monowu/claude-mod-token-usage) |
| tokens | 侧栏 token 往来：每次请求送出/等待/收到与合计。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/tokens) |
| trek-band | 提示框上方星际迷航风格用量环与像素动画场景。 | MIT | [链接](https://github.com/rb17080/trek-band/tree/main/plugins/trek-band) |
| turn-footer | 每条回答下方改成回合摘要（工具、请求、tokens、缓存命中）。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/turn-footer) |
| turn-meter | 状态行显示当前回合耗时与 token。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/turn-meter) |
| u | 在状态栏显示 5 小时、7 天等限额用量和按 API 价格折算的费用，/meter 打开详情面板；只读会话用量；无显示内容时状态文本为 undefined，$.ui.status(undefined) 会清除其他 mod 的状态；不使用网络。 | MIT | [链接](https://github.com/Humpens/claude-mods/tree/main/u) |
| usage-band | 在提示框上方显示 5 小时/7 天限额、上下文窗口与缓存命中率。 | MIT | [链接](https://github.com/JetsonChan/CC-Usage-Band/tree/main/usage-band) |
| usage-bar | 用量条：可调用 Anthropic 的 OAuth 用量 API（使用当前登录凭证，请求体为空）查看 5 小时与 7 天限额、上下文与缓存命中率。 | MIT | [链接](https://github.com/muratkaragozgil/claude-code-usage-bar) |
| usage-bars | 上下文迷你图：把本会话的上下文占用画成字符级走势条，随回合增长刷新。 | MIT | [链接](https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/usage-bars) |
| usage-deck | 计划限额、上下文占用与缓存温度合成动画甲板（/deck 显隐）。 | MIT | [链接](https://github.com/codeclawd/usage-deck/tree/main/plugins/usage-deck) |
| usage-bell | 接近限额时响铃：上下文占用（70/85/95%）、5 小时/7 天限额（80/95%）、自动记忆索引达 200 行或 25 kB；状态栏显示当前百分比，/... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/usage-bell) |
| usage-meter | 提示框上方常显上下文与 5 小时/周限额。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/usage-meter) |
| usage-mod | 提示框上方显示上下文与 5h/7d 额度及重置时间；按钮可触发本机 /compact。 | MIT | [链接](https://github.com/qingyashizi/claude-usage-mod/tree/main/plugins/usage-mod) |
| usage-log | 每回合写本地 jsonl 用量日志，并显示相对 7 日节奏的差距。备注：本机 process 写本地文件。 | MIT | [链接](https://github.com/tanuu5/usage-log/tree/main/plugins/usage-log) |
| usage-limits | 提示框上方显示 5h/周限额剩余与重置倒计时。纯 UI。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/usage-limits) |
| usage-line | 提示框上方一行显示会话费用、上下文占用、5 小时与每周额度及消耗速度，/usage-style 换条形样式；备注：读本机 ~/.claude.json 只取邮箱 @ 前的用户名显示。 | MIT | [链接](https://github.com/achapla/cc-mods/tree/main/usage-line) |
| usage-pace | 提示框上方一行显示 5 小时窗口已用百分比、距重置时间和节奏红黄绿灯；只读 $.session.usage。备注：AbovePrompt 显示时不调 next，可能盖住同样改这块的 mod；每 60 秒刷新显示。 | MIT | [链接](https://github.com/diazgonza17/usage-pace) |
| usage-pet | 提示框上方 Clawd 宠物信息栏，显示上下文与 5 小时/周限额并随用量养成；/clawd-card 导出战报 PNG（本机 process：macOS 用 qlmanage/sips/osascript，Windows 用 PowerShell 跑自带脚本调 Edge/Chrome 无头截图，旧卡片移进废纸篓）；AbovePrompt 显示时不调 next。 | MIT | [链接](https://github.com/manson341349-beep/claude-desktop-mods/tree/main/plugins/usage-pet) |
| usage-report | 显示会话用量与费用报告。 | MIT | [链接](https://github.com/Schweem/usage-report) |
| usage-status | 状态行显示 5h/周限额占用。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/usage-status) |
| usage-tracker | 实时 5h/7d 用量、节奏与火花线（含本机读 Codex 日志）。备注：本机 process（tail）。 |  | [链接](https://github.com/tylergraydev/cc-mods/tree/main/usage-tracker) |
| usage-forecast | 提示上方用量带：5 小时/周限额、重置时间与是否会用尽；/forecast。可能遮挡其他提示框上方条。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/usage-forecast) |
| usage-widget | 限额用量与费用卡片；只读 $.session.usage，需配合 widgets。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/usage-widget) |
| vercel-deploy-status | 提示框上方显示 Vercel 部署队列（零 token）。 |  | [链接](https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/vercel-deploy-status) |
| wavy-usage | 波浪动画风格的用量显示条。 | MIT | [链接](https://github.com/BatuhanCakmakk/wavy-usage) |
| ration-book | 按历史给每个会话设读取额度（Read/Grep/Glob/WebFetch/WebSearch 结果字节数），用完后拒绝这些调用，/ration grant <KB> 手动加额度。备注：只拒绝不改写；额度历史存本机 $.store。 | MIT | [链接](https://github.com/arazvan-ec/xmarks/tree/main/mods/ration-book) |
| weektoken | 提示框上方 5 小时/周限额配速条与 /weektoken 面板。备注：本机 process（perl/tail/bash 读用量；macOS defaults 读语言）。 | MIT | [链接](https://github.com/3dnow/claude-mods/tree/main/weektoken) |
| gas-gauge | 提示上方油量表风格显示 5h/周限额剩余；纯 UI，只读 session.usage/measure。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/gas-gauge) |
| odometer | 提示上方里程表：本会话时长与花费；纯 UI。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/odometer) |
| tach | 提示上方转速表：近期 token 燃烧速率（可设窗口）；纯 UI。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/tach) |
| speedometer | 提示上方速度表：上下文窗口占用 0→MAX；纯 UI。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/speedometer) |
| oil | 提示上方机油表：本周 Fable 用量计数（本机 store）；纯 UI。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/oil) |
| claude-code-usage-quota | 提示框上方计划限额/上下文与耗尽预报；可一键或自动 compact。备注：本机 process（主题检测）；用用户 OAuth 读官方用量 API，不带会话正文；用量带显示时（默认开启，一旦存在快照），AbovePrompt slot 返回自己的行且不调用 next，因此可覆盖其他 mod 的行。 | MIT | [链接](https://github.com/anantraghunath/claude-code-usage-quota-mod) |
| cache-band | Auto cache 使用 $.model.fork 保持缓存热度且不把会话文本注入对话；通过本地 fs/process 读本地 transcript mtime；AbovePrompt 调用 next；Auto compact 与 Compact 按钮运行 $.command.run({ command: 'compact' })。 | MIT | [链接](https://github.com/MohabYasser2/claude-code-mods/tree/main/cache-band) |
| runway | 提示框上方 Command Code 套餐额度与节奏；读本机凭据调 billing API，不上传会话正文。备注：本机读配置文件/密钥。 | MIT | [链接](https://github.com/Jovan1666/claude-code-runway) |
| otto-hud | 桌面端提示框上方 Otto 章鱼用量预报（上下文/5h/7d）；终端不绘制。纯 UI。 | Apache-2.0 | [链接](https://github.com/manuacl/claude-mods/tree/main/plugins/otto-hud) |
| chai-meter | 会话花费用「几杯 chai」展示；/chai。纯 UI，只读会话用量。 | MIT | [链接](https://github.com/ShriD5/claude-mods/tree/main/chai-meter) |
| pixelbar | 提示框上方像素状态带：模型/上下文/限额/费用/git 与回合摘要；/session-files。备注：本机 git；AbovePrompt 显示时可不调 next。 |  | [链接](https://github.com/elkinaguas/claude-mods/tree/main/pixelbar) |
| cache-buster | 提示框上方条带显示缓存剩余时间与命中率。**调用 next 可堆叠**。仅在用户按钮时压缩。 |  | [链接](https://github.com/dblanken-yale/cache-buster) |
| cc-usage | 状态行显示 5 小时与 7 天用量。**注册 /usage-bar，可能与已列出的 usage-bar mod 冲突，请二选一**。隐藏时 $.ui.status(undefined) 清除状态行。 | MIT | [链接](https://github.com/leonardokidd/cc-usage) |
| status-line | 提示框下方一行显示目录、模型、上下文占比和 5 小时/每周用量及本地重置时间，/quota 展开详情，用量过 90% 弹提示；纯 UI，只读会话用量，不用网络。 | MIT | [链接](https://github.com/mikljohansson/claude-code-status-line) |
| desktop-statusline | 只在 Claude Desktop 的 Code 页提示框上方画状态条：目录、git 分支与改动、会话时长、提问数与费用、上下文条、5 小时/每周用量与重置倒计时、上一轮模型/耗时/缓存命中、空闲对比缓存 TTL、压缩次数和运行中的子代理，用量到 80%/95% 弹提示；本机 git，只改显示，不用网络。 | MIT | [链接](https://github.com/centminmod/claude-plugins/tree/master/plugins/desktop-statusline) |
| usage-dollars | 把订阅 5 小时窗口和一周用量折算成 API 等价美元，估算额度、生成花费报表（/usage-dollars）。备注：本机 process（node 跑仓库自带 scripts/usage-cost.mjs），读本机 ~/.claude/projects 会话记录与 ~/.claude.json 账号信息，不联网。 |  | [链接](https://github.com/hyvanmielenpelit/claudecodemods/tree/main/usage-dollars) |
| barometer | 提示框上方显示上下文与套餐限额仪表，上下文到红线时出现 Compact 按钮（点按才压缩），并显示账号和 effort。备注：本机 process（跑 claude auth status 读账号邮箱与套餐），只读会话用量，不用网络。 | MIT | [链接](https://github.com/Alchez/claude-mods/tree/main/barometer) |
| session-panel | 提示框上方显示模型、上下文、5 小时/7 天限额、会话花费和 Git 分支。备注：本机 git（symbolic-ref、rev-parse 读当前分支），不用网络。 | MIT | [链接](https://github.com/arsenii-cmd/Claude-mod) |
| meter | 提示框上方的会话用量条（上下文、限额、费用），/meter 打开详细指标窗格；只观察事件、工具调用原样放行，提示框条显示时不调 next。 |  | [链接](https://github.com/theishandubey/claude-mods/tree/main/plugins/meter) |
| hud | 提示框下方两行彩色动态状态：模型、推理强度、上下文、限额、回合计时、工具调用数、子代理、git 状态、费用、会话时长和目录。备注：本机 git status；turn.step 原样转发；不改提示或工具，不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/hud) |
| redline | 转速表：统计本机同时在跑的 Claude 会话数，指针进红区提示别再开新会话；可选 5H/7D/上下文油表。备注：用本机 ps、lsof 读进程与工作目录；AbovePrompt 终端自绘不调 next；不联网。 | MIT | [链接](https://github.com/jamubc/toolbox/tree/main/plugins/redline) |
| turn-usage | 每条 Claude 回复下方加一行暗色小字：当前 5 小时会话额度已用多少、这一回合花了多少；按量付费时显示美元花费；language 设为西语时显示西语，否则英语。备注：只读 $.session.usage，不改写回复，只在 AssistantMessage 下方追加一行。 | MIT | [链接](https://github.com/gmorubio/claude-mods/tree/main/turn-usage) |
| llm-speed | 右下用量条上方加一行：平均首 token 时间（TTFT）、输出 tokens/s 和请求次数。备注：turn.step 只计时、原样透传流；纯本机 UI。 |  | [链接](https://github.com/Lunik/gmz-claude-marketplace/tree/master/llm-speed) |
| usage-hint | 输入框下方提示行显示 5h / 7d / Fable 额度与上下文百分比，超过 75% 变黄；/usage-hint 列出原始限额窗口。备注：只读用量；终端里整行重画 PromptHint 不调 next（保留原提示文字），会盖住其他改同位置的 mod；界面文案为日语。 |  | [链接](https://github.com/tett23/dotfiles/tree/master/claude/mods/usage-hint) |
| session-stats | 提示框上方一条：模型、effort、上下文填充和各限额窗口及重置倒计时；/session-stats 或 + 按钮打开面板看 token 拆分、缓存命中、各模型占比和上下文类别。备注：只读用量；/model、/effort 命令原样透传，只记录结果；纯本机 UI。 |  | [链接](https://github.com/cjmellor/mella-marketplace/tree/main/plugins/session-stats) |
| rtk-quota | 右下用量条上方叠一行 rtk 统计：已节省 tokens 和保住的额度百分比；可配置订阅档位（pro/5x/20x，默认 20x）。备注：本机运行 `claude auth status` 取订阅类型、运行 `rtk gain` 取数字，需自行安装 rtk；先调 next 再叠加，纯本机 UI。 |  | [链接](https://github.com/Lunik/gmz-claude-marketplace/tree/master/rtk-quota) |
| usage-ring | 提示框上方一排圆环：5 小时与每周额度、上下文、待办进度、本会话 tokens、费用和提示缓存剩余时间，配像素小 Claude 动画（仅终端）。备注：只读用量；tool.call 只读 TaskCreate/TaskUpdate/TaskList/TodoWrite 结果数待办，原样返回；可选 limitsFile（默认关）把额度快照写到本机 ~/.claude/usage-limits.json。 | MIT | [链接](https://github.com/oualid0/claude-mods/tree/main/plugins/usage-ring) |
| burnrate | 提示框上方一条显示各额度窗口的消耗速度和预计耗尽时间，以及提示缓存未命中次数与估算重写的 tokens；/burnrate 打开面板看最近请求明细。备注：turn.step 只记录 usage、原样透传；纯本机 UI。 | MIT | [链接](https://github.com/nemke82/claude-code-burnrate/tree/main/burnrate) |
| usage-dash | /usage-dash 面板显示额度、本机各 Claude 会话状态和后台任务（子代理、后台 Bash）。备注：需安装 aqua5230/usage 应用（本机运行 usage CLI）；各钩子只记录状态并原样返回，prompt.submit 只记录不改写；状态写到 ~/.usage/claude-pane/live/ 并清理过期文件，读本机 transcript 取会话标题。 | AGPL-3.0 | [链接](https://github.com/aqua5230/usage/tree/main/claude_pane/usage-dash) |
| subagent-meter | 状态行显示本会话子代理调用次数、子代理占输出/全部 token 的比例和用得最多的子代理类型。备注：只读 turn.complete 的用量并原样返回；纯本机 UI。 | MIT | [链接](https://github.com/NarenDawar/narens-claude-toolkit/tree/main/plugins/subagent-meter) |
| turn-telemetry | 提示框上方一行显示每回合耗时、首 token 延迟、tok/s 走势、输入/输出 token、请求数和卡顿次数；/tps 切换或清空。备注：turn.step 只计时并原样转发流式内容；纯本机 UI。 | MIT | [链接](https://github.com/MiguelMachado-dev/miguel-mods/tree/main/turn-telemetry) |
| turn-budget | 单个回合超过 +5 个会话额度点或 50 万未缓存输入 token 时，在两次请求之间弹框问你是否继续，可停止该回合；/turn-budget 调整阈值或关闭。备注：只在请求之间检查，不打断正在运行的命令；你选「Stop here」时会往会话追加一条说明「用户已在此停止」的消息并中止回合（你选才会）。 | MIT | [链接](https://github.com/VedantAndhale/claude-pro-kit/tree/main/plugins/turn-budget) |
| cache-shot-clock | 提示缓存 TTL 倒计时：提示框下方一行小倒计时，快过期的最后几秒在上方显示大号 LED 时钟。备注：本机 tail 读取本会话 transcript 末尾判断 5m/1h TTL；纯本机 UI。 |  | [链接](https://github.com/cjavdev/mods/tree/main/cache-shot-clock) |
| Cache | 状态行显示 1 小时提示缓存窗口倒计时（从上一次回复算起），恢复会话时接着算。备注：本机读本会话 transcript 取上次回复时间；纯本机 UI。 | MIT | [链接](https://github.com/hymleong/claude-mods/tree/main/plugins/Cache) |
| aimux | 只在由 aimux 启动的会话里生效：提示框上方显示所有 aimux 订阅的 5 小时/每周用量，快用完时提醒，用完时可一键 /exit 交给 aimux 切到最空闲的订阅。备注：需安装 aimux（Digital-Threads/aimux）；本机运行 aimux status --json；额度用完且提示框为空时会在提示框预填 /exit（不改写你已输入的内容，需你按回车）。 | MIT | [链接](https://github.com/Digital-Threads/aimux/tree/master/mod) |
| session-models | 显示主模型、每个模型被多少子代理使用（几个正在跑），子代理扎堆或某个子代理上下文过大时弹提醒。备注：只读会话与子代理用量，纯本机 UI。 | MIT | [链接](https://github.com/AbhiramDwivedi/claude-mods/tree/main/plugins/session-models) |
| omp-statusline | Oh My Pi 风格的状态条：模型、当前目录、git 分支、PR 号、订阅标记、上下文占用和窗口大小。备注：本机运行只读 git rev-parse；分支变化时运行 gh pr view 查 PR 号（需本机 gh 登录才显示）。 |  | [链接](https://github.com/yi-john-huang/claude-garage/tree/main/plugins/omp-statusline) |
| linha-do-tempo | 会话时间线面板：逐回合显示模型、推理强度、用过的工具、token 和耗时（/timeline，可导出或清空）。备注：只观察回合事件，纯本机 UI；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/linha-do-tempo) |
| rich-statusline | 提示框下的多行状态面板：模型、目录、git 分支与改动、上下文构成、用量限额与费用，三种布局，提示框上方有设置菜单。备注：本机运行只读 git（rev-parse、diff --shortstat）；运行 gh pr view 查当前分支 PR 号（需本机 gh 登录才显示）；纯本机 UI。 | Apache-2.0 | [链接](https://github.com/blackpaw-studio/claude-plugins/tree/main/plugins/rich-statusline) |
| glyph-hud | 点阵风 HUD 面板（/glyph）：按模型统计聊天 token、5 小时限额估算、缓存计时和代码改动统计。备注：prompt.edit/prompt.submit 只用来估算草稿 token，不改写提示；大 transcript 用插件自带的本机 python 脚本读用量；可选开关 blockAttribution（默认关）开启后只拒绝带 Co-Authored-By 的 git commit；不调用模型。 | MIT | [链接](https://github.com/MridulNegi2005/glyph-hud) |
| session-band | 提示框上方一行状态条：当前模型与推理强度、上下文已用/窗口大小及百分比、距自动压缩还剩多少 token（不足 10 万变黄），5 小时/每周/花费限额用到 50% 以上时显示百分比。备注：只读 $.session.usage，纯本机 UI，不调用模型、不联网。 |  | [链接](https://github.com/howells/howells-plugins/tree/main/mods/session-band) |
| cache-keepalive | 保持 1 小时提示缓存不冷：主线程空闲约 55 分钟后用 $.model.fork 发一句「Reply with exactly: ok」重读缓存前缀，免得下一轮整段重写缓存；默认连续最多 6 次（约 5.5 小时），机器睡眠后过期就跳过，未命中缓存即停到下一轮；/cache-keepalive status/on/off/now 控制，状态栏显示是否已武装。备注：每次 ping 按一次缓存读加短输出计费；fork 只发往会话本身所用的模型，回复丢弃、不写回会话、不联网到第三方；可设 idleMinutes（1–58）与 maxPings（0 为不限）。 | MIT | [链接](https://github.com/krika2810/keep-cache-warm) |
| tablero-consumo | 西班牙语用量面板（面向 Pro/Max 套餐）：/consumo 打开，实时显示上一次请求和本会话 token、各项套餐限额的用量与重置时间、上下文占用、工具调用次数和会话时长。备注：只读 session.usage 和每步返回的 usage，所有钩子原样传递；纯本机，不联网。 | MIT | [链接](https://github.com/kit-para-devs/mods/tree/main/plugins/tablero-consumo) |

### 上下文管理 Context Management

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| compact-keeper | 压缩后把摘要与编辑文件清单存到本地 ~/.claude/handoffs/。备注：只写本地 handoff 文件。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/compact-keeper) |
| compact-tools | 压缩工具输出显示（含 MCP/Bash 错误）。 |  | [链接](https://github.com/AJclemendor/my-mods/tree/main/plugins/compact-tools) |
| context-guard | 上下文占用状态行，越过阈值 toast 提醒 /compact。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/context-guard) |
| context-lens | 固定显示上下文占用、增长与距 compaction 的回合数。 |  | [链接](https://github.com/Arunjay4213/claude-mods/tree/main/plugins/context-lens) |
| context-meter | 在底部模式栏显示上下文用量（已用/窗口与百分比），到 80% 时弹出提示建议 /compact；只读会话用量。 | MIT | [链接](https://github.com/Vibe-Commit/claude-context-mods/tree/main/plugins/context-meter) |
| context-pane | /context-pane 侧边窗格列出本会话读过和改过的文件、用过的 skill、MCP 服务器调用次数，以及已载入的记忆文件（CLAUDE.md 等）和估算 token；会话开始时自动打开。只观察：tool.call、skill.prompt、session.compact 都先 next 再记录，不改写；用量用本机 summary 估算，不发计数请求。不联网。 |  | [链接](https://github.com/akagaya/claude-code-mods/tree/main/plugins/context-pane) |
| context-restore | 恢复上下文状态。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/context-restore) |
| context-view | 提示框上方一行上下文占用与距 auto-compact 余量。 |  | [链接](https://github.com/kongyo2/context-view) |
| context-widget | 上下文窗口按类别分色的堆叠条卡片，六种视图；只读 $.session.usage，需配合 widgets。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/context-widget) |
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
| context-card | 提示框上方上下文占用拆解与周限额；可展开分类条。备注：本机写缓存；用用户 OAuth 读官方用量 API，不带会话正文；卡片显示后，AbovePrompt 返回自己的行且不调用 next（除非正在显示调查），因此可覆盖其他 mod 的行；另 tail 本地会话 transcript 但不上传。 | MIT | [链接](https://github.com/Nongfsq/frank-claude-cockpit/tree/main/context-card) |
| teach-me | 改代码后在提示框上方出一道多选题；/a 作答。备注：使用 $.model.complete（本机 diff，不外传）。 | MIT | [链接](https://github.com/saksham10arora-dotcom/claude-mods/tree/main/plugins/teach-me) |
| bubble-contesto | 面板里一个随会话上下文用量变满的气泡（SVG），/bubble 开关；终端里显示文字进度条，/compact 后清空。只读 $.session.usage，只改显示。 | MIT | [链接](https://github.com/maxturazzini/bubble-contesto) |
| context-cache | 右下加一行：上下文窗口占比、提示缓存命中率和按 API 报告 TTL 的倒计时；上下文到 70/85/95%、缓存即将过期或已过期、大量缓存未命中时弹 toast。备注：只读用量，不自动发送或压缩；纯本机 UI。 |  | [链接](https://github.com/Lunik/gmz-claude-marketplace/tree/master/context-cache) |
| context-watch | 上下文到 80%/90% 时弹 toast 提醒；/context-top 打开面板列出本会话占上下文最多的工具结果（按 4 字符≈1 token 估算）。备注：tool.call 只读结果长度，原样返回，不改写。 |  | [链接](https://github.com/wmayner/dotfiles/tree/main/claude/context-watch) |
| token-face | 提示框上方一张随上下文变满越来越诡异的脸，配百分比、近 12 回合迷你柱状图和上回合增量；桌面版可用插件目录 faces/1-4 的自定义图片。备注：只读用量；提示框上方条不调 next，会盖住其他 mod 的同位置内容。 | MIT | [链接](https://github.com/MohamedEmbarak/token-face/tree/main/plugins/token-face) |
| compact-large-idle-context | 会话空闲 50 分钟且上下文超过 20 万 tokens 时，在 1 小时提示缓存过期前自动压缩一次；你一开新回合或手动/自动压缩就取消。备注：会自动调用 $.session.compact（标准压缩，会消耗一次压缩请求），结果写到日志；不改写消息。 | MIT | [链接](https://github.com/mataku/dotfiles/tree/develop/claude/mods/compact-large-idle-context) |
| context-level | 给 Claude 一个读取剩余上下文百分比的工具，方便它决定何时收尾或压缩。备注：只在 Claude 调用该工具时返回一个百分比，不注入其他上下文。 | MIT | [链接](https://github.com/tobihagemann/turbo/tree/main/claude/skills/context-level) |
| dashboard | 状态行显示上下文已用/总量和百分比，以及主循环输出 tok/s。备注：turn.step 只计时并原样转发；纯本机 UI。 |  | [链接](https://github.com/Cohey0727/CodingAgentTools/tree/main/claude/mods/dashboard) |
| handoff-relay | 提示框上方的 Handoff 按钮：点击运行 /handoff，上下文到 18 万 token 时亮起；可与 cache-meter、next-steps 合成一条。备注：只有你点按钮才运行 /handoff；纯本机；界面英语或乌克兰语。 | MIT | [链接](https://github.com/drdickgraysonjr/chalkery/tree/main/plugins/handoff-relay) |

### UI 与主题 UI & Themes

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| 12ui-plugin | 提供设计面板。 |  | [链接](https://github.com/just-every/12ui-plugin) |
| a2ui-claude-code | 在窗格里原生渲染 A2UI 目录块（/a2ui 读文件或内联 JSON，并自动画 a2uicatalog MCP 载荷），带动画进度和长任务仪表盘（/a2ui-job，回合超过 60 秒后打开）。备注：tool.call 原样放行；只读本机文件，不联网；源仓库约 800 MB，首次安装较慢。 | MIT | [链接](https://github.com/a2uicatalog/a2ui/tree/main/claude-code-surface) |
| agent-diary | 斯多葛工程日记窗格（/diary、/diary-note、/diary-open），改 spinner 与提示框上方文字。备注：tool.call 原样放行；turn.complete 时跑本机 `agent-diary sync`（同仓库 CLI，需 `npm i -g` 或 `npm link`，没有就静默跳过），把本机 ~/.claude/projects 会话记录读进 ~/.agent-diary 并生成本地 HTML 日记；不联网。 | MIT | [链接](https://github.com/hemanth/agent-diary) |
| ambient | 提示框上方动画场景带与本地音效。**显示时 AbovePrompt 不调用 next 并盖住其他带**。/ambient weather 仅发送城市名与坐标到 Open-Meteo，不含会话内容。**在无指针终端上 PromptHint 改写提示尾部但仍调用 next**。 | MIT | [链接](https://github.com/barisdemirhan/claude-ambient) |
| aside | /aside 只读侧聊：基于会话 transcript fork 问答，不写回主线程。 | MIT | [链接](https://github.com/JayDoubleu/aside) |
| at-work | 提示框上方像素场景动画，按当前工具活动切换画面；spinner 计算机笑话；节日装饰。纯 UI，不改写工具/提示。 | MIT | [链接](https://github.com/zhuoxingzhang/pixel-at-work) |
| better-tool-rows | Read/Edit/Write 显示相对路径，Edit/Write 结果显示加减行数，长 Bash 命令截成一行并折叠长输出；只改显示，Bash 工具调用只记命令形状、原样返回。备注：Bash/Edit/Write 的 ToolResult 槽在已显示输出或行数时直接画空、不调 next，可能盖住其他改这个槽的 mod；在本机读会话记录来算行间距。 | MIT | [链接](https://github.com/akilin/claude-plugins/tree/main/plugins/better-tool-rows) |
| btw-fix | 接管内置 /btw（不调 next），把答案作为普通对话行输出而不是阻塞侧栏；用 $.model.fork 带当前会话问模型（与内置 /btw 相同）。 |  | [链接](https://github.com/m-mahiro/claude-code-mods/tree/main/mods/btw-fix) |
| bunny-spinner | 把加载提示行改成小兔子口吻（名字可配置），工具运行时加「nom nom…」；只改 Spinner 显示。 |  | [链接](https://github.com/DenisGuiraudet/claude-mods/tree/main/bunny-spinner) |
| catch-me-up | 侧栏实时 catch-up 摘要：为何开始、做了什么、卡在哪里。 | MIT | [链接](https://github.com/oliverow/catch-me-up) |
| cc-math-renderer | 把回复里的 LaTeX 显示成 Unicode 数学符号（只改绘制，不改存储消息）；钩 classic.MessageDisplay 与 AssistantMessage。 | MIT | [链接](https://github.com/andrewroxby/cc-math-renderer) |
| al-syntax | 把回复里 ```al 代码块（Business Central AL 语言）用 tree-sitter 着色显示，其他回复不动。备注：本机 process 用 node 运行仓库自带的 tree-sitter 高亮脚本和 wasm 语法文件（随插件一起，不另下载）；只改回复显示，不改原文，不联网。 | MIT | [链接](https://github.com/abonckus/claude-code-al-syntax) |
| cc-pokedex | 在侧栏查看宝可梦图鉴，按名字或编号搜索。 |  | [链接](https://github.com/deonmenezes/claude-mods-pokedex) |
| chameleon | 在 /rename 与 /branch 时给会话随机上色（/color），便于区分窗口。 | MIT | [链接](https://github.com/aksh1618/claude-mods/tree/main/chameleon) |
| change-journal | 编辑变更的即时说明窗格。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/change-journal) |
| chat-bubbles | 聊天气泡式界面：你的提示在右、Claude 在左，运行中或失败的工具高亮、已完成的变暗，441 套主题（/bubbles）；只改显示，不改提示或工具，不联网。应用主题后，这些 ui.render 插槽不调用 next 而绘制自己的元素，因此可以覆盖其他 mod 的渲染：完整模式下的 UserMessage 和 AssistantMessage、SessionMode、TurnDuration，以及终端外的 PromptHint 和 Spinner。还会为每个 mod 的 Pane 添加背景色（该插槽调用 next）。默认无主题，因此在执行 /bubbles 前一切都透传。 | MIT | [链接](https://github.com/angeldelbiondo/claude-chat-bubbles/tree/main/chat-bubbles) |
| clawd-tracker | Domino 式订单进度条（主题 pizza/coffee/rocket/construction）：读本机会话与 $.tool.check 只判断是否会询问许可，不改写工具；prompt.submit 只本地取标题后原样 next；送达可 $.audio.play 自建 WAV。备注：进度显示时 AbovePrompt 不调 next（可点隐藏）。 | MIT | [链接](https://github.com/IKnowJot/clawd-plugins/tree/main/plugins/clawd-tracker) |
| clawdify | /clawdify 改 spinner、页脚、提示、横幅、状态行和对话行样式，可用自然语言描述（走 $.model.complete，只发当前设置和你的请求）；可按你设的规则改写回答的显示文本（只改显示）、替换 PromptHint/UserMessage、横幅开启时 AbovePrompt 不调 next、可隐藏提示通知；启动时 $.ui.status(undefined)，并扫描本机 ~/.claude/plugins/store 迁移旧设置；读取本地 .git/HEAD 获得分支名。 | MIT | [链接](https://github.com/viik2k/clawdify) |
| looks | 提示框上方显示配色主题切换菜单，纯 UI。 | MIT | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/looks) |
| collapse-answers | 折叠过长回复，界面更干净。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/collapse-answers) |
| meadow | 把助手回复画成像素草地气泡（首块上方天空山丘、末块下方草地）；只改 AssistantMessage 显示，画图时不调 next，可能盖住其他改回复样式的 mod。 |  | [链接](https://github.com/DenisGuiraudet/claude-mods/tree/main/meadow) |
| message-timestamps | 在 transcript 里给每条 Claude 回复加本地到达时间戳；无模型调用、不上网。 |  | [链接](https://github.com/benjaminmodayil/live-recap/tree/main/plugins/message-timestamps) |
| commonplace-pane | 侧边窗格展示芝加哥艺术学院公版画，随仓库状态变「天气」。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/commonplace-pane) |
| crosstalk | /crosstalk 打开窗格，记录本会话与其他 Claude Code 会话的 peer 收发，并可在窗格内回复；只读观察、不改写工具。备注：hook 本机 find/grep 扫描 session journal；thread 存 local store。 | MIT | [链接](https://github.com/kbrdn1/claude-crosstalk) |
| diff-seismograph | 提示框上方 braille 地震图式编辑幅度、大改 quake 提醒与仓库热力 treemap。备注：使用本机 git。 | MIT | [链接](https://github.com/ccdwyer/diff-seismograph) |
| drift | 漂移动画效果窗格。 | MIT | [链接](https://github.com/azkhh/drift) |
| diff-minimap | Edit/Write 旁细迷你图条，标记改动位置；仅 UI。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/diff-minimap) |
| file-view | 点击 Read/Edit/Write 行的路径，在侧栏打开文件内容。备注：本机读文件。 |  | [链接](https://github.com/ushironoko/dotfiles/tree/main/claude/.claude/skills/file-view) |
| files-seen | 状态行与 /seen 窗格列出本会话读过/改过的文件。纯 UI，只观察 tool.call。 | MIT | [链接](https://github.com/Alyan-khattak/Claude-Code-Mods/tree/main/files-seen) |
| firstmate-calm | /calm 隐藏工具行并换成帆船 spinner；需开启 function hooks。 |  | [链接](https://github.com/kunchenguid/firstmate/tree/main/.claude/mods/firstmate-calm) |
| flashmodel | 提示框上方点选切换模型与 effort（走内置 /model、/effort），纯 UI。 | MIT | [链接](https://github.com/Rafael-CRL/FlashModel) |
| flowpane | 实时显示工作流程图。 |  | [链接](https://github.com/mpolatcan/flowpane) |
| helix-spinner | 把 spinner 行换成旋转的盲文双螺旋、随机动词和本回合用时与 token；/helix-dex 收集动词，/helix-theme 节日主题，/helix-demo 预览。只改显示，不改提示或工具，不联网；在终端和桌面端 Spinner 插槽不调用 next 而自绘（其他界面仍调 next，只换动词）；$.store 存收集和设置。 |  | [链接](https://github.com/dylan-chalkboard/helix-spinner/tree/main/plugins/helix-spinner) |
| hide-diffs | 把 Edit/Write/NotebookEdit/Bash 的完整 diff 收成一行加减摘要，ctrl+q 切换显示。纯 UI，不改写工具。 | MIT | [链接](https://github.com/gixxy22/hide-diffs) |
| hint-mod | 隐藏输入框下方的灰色提示行（如 ? for shortcuts、esc to interrupt），只改 PromptHint 的显示。 | MIT | [链接](https://github.com/zyx1121/hint-mod) |
| hyperspace | Spinner 行换成 X-wing 或 TIE 战机穿越视差星空的动画（激光齐射，每 24 秒跳一次超空间），/ship 切换战机；提示语为俄语。只改显示，不改提示或工具，不联网；终端且宽度足够时 Spinner 插槽不调用 next 而自绘（其他情况调 next，只换文案）；$.store 记住所选战机。 | MIT | [链接](https://github.com/alexregrets/hyperspace) |
| inner-monologue | 会话旁白式内心独白窗格。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/inner-monologue) |
| kit-sink | /kit sink 打开组件厨房水槽窗格，演示候选 UI 组件；只观察 tool.call/turn.complete 且先调 next，不改写工具或提示。 | MIT | [链接](https://github.com/eduardocruz/cc-kit/tree/main/mods/kit-sink) |
| msg-timestamps | 在每段 Claude 回复前加彩色本地时间戳（到达时间）。turn.step 流式内容原样转发不改写；session.start 本机运行 `date +%z` 取时区；**有时间戳时 AssistantMessage 自绘该行、不调用 next**；不上网。 |  | [链接](https://github.com/FukKwang/claude-msg-timestamps) |
| netsignal | 网络探针：向 api.anthropic.com 发延迟探测和带宽采样（不上传会话内容），在状态行显示往返时间。 | MIT | [链接](https://github.com/avazibra/claude-statusbar) |
| on-me | 提示框上条带：Claude 正在做什么，以及轮到你处理的事项。 | MIT | [链接](https://github.com/abhibansal60/claude-mods/tree/main/on-me) |
| orange-prompt | 输入草稿白字橙底高亮（可配合 Orange Dark 主题）。纯 UI。 | MIT | [链接](https://github.com/philsimon/orange-prompt) |
| pixelband | 在提示框上方显示像素艺术。 |  | [链接](https://github.com/furqan-khan07/pixelband) |
| pin-message | /pin 把选中文本或上一条回复钉到侧栏，滚动时仍可见。纯 UI。 | MIT | [链接](https://github.com/GruperTal/claude-pin-message) |
| powerline-bar | Powerline 风格 AbovePrompt 条：目录、git、模型与上下文占用。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/powerline-bar) |
| pr-links | 把回复里的 #123 变成可点 PR 链接；备注：本机 git 读 origin。 |  | [链接](https://github.com/AydinHassan/claude-mods/tree/main/plugins/pr-links) |
| prompt-bubbles | 把自己的提问画成右对齐的圆角气泡；只改显示。备注：终端里自己的消息由 UserMessage 槽直接绘制、不调 next，可能盖住其他改这个槽的 mod。 | MIT | [链接](https://github.com/akilin/claude-plugins/tree/main/plugins/prompt-bubbles) |
| prompt-highlight | 高亮用户消息气泡背景，便于扫读。 |  | [链接](https://github.com/adriancoman/claude-code-mods/tree/main/prompt-highlight) |
| prompt-rail | 提示条/侧栏：悬停读、点击跳回历史 prompt。 |  | [链接](https://github.com/oikon48/prompt-rail/tree/main/plugins/prompt-rail) |
| quick-buttons | 侧栏快捷按钮启动已选 slash 命令。备注：点击会 $.command.run。 |  | [链接](https://github.com/DarioFontanel/claude-code-mods/tree/main/quick-buttons) |
| quiet-bash | 精简 Bash 行展示，可选本地 magick 缩略图。备注：会本地调用 magick/identify 生成缩略图。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/quiet-bash) |
| quiet-spinner | 弱化/安静化等待 spinner。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/quiet-spinner) |
| readout | 只改显示：折叠的工具行里显示 Read 打开了哪些文件和行、搜索查了什么，失败或被拒原因附在后面；可选按主题给工具块加底色。备注：tool.call 原样 next，只记录原因。 | MIT | [链接](https://github.com/lucenity0/claude-readout) |
| reply-frame | 给助手回复套上圆角彩色边框；超过 1 万字符的回复回退到默认渲染。 | MIT | [链接](https://github.com/takosasi-dev/reply-frame) |
| reply-highlight | 用彩虹边和紫色底突出 Claude 的回复。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/reply-highlight) |
| review-pane | 侧边阅读窗格：显示本会话最新回复、计划、提问与任务，可翻看前几轮、冻结、复制；/claude-review 开关，默认会话开始时打开（可在设置关掉）。只读本会话消息，复制键会写入剪贴板，不改写工具或提示。隐藏快捷键获得焦点时，ui.focus 拒绝并不调用 next。 | MIT | [链接](https://github.com/r3al1tym/claude-review) |
| rtl-text | 用 fribidi 把波斯语/阿拉伯语/希伯来语在 transcript 里按 RTL 整形对齐。 |  | [链接](https://github.com/aliir74/claude-code-rtl) |
| ruview-live | /ruview 打开 CSI/雷达传感只读窗格（瀑布图与雷达视图）。备注：运行插件旁的 @ruvnet/ruview CLI（node）；只读设备数据。 | MIT | [链接](https://github.com/ruvnet/RuView/tree/main/harness/ruview/mod) |
| search-meter | 统计模型搜索（Bash grep/find、WebSearch、ToolSearch）命中着色。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/search-meter) |
| sea | 输入栏上方像素浅海动画（昼/夕/夜）与可选波声音效；/sea 开关。备注：本机 process 播放插件内 wav。 | MIT | [链接](https://github.com/himazintom/claude-code-sea) |
| shell-highlight | Bash/PowerShell 工具调用语法高亮展示。纯 UI，不改写命令。 | MIT | [链接](https://github.com/Turbo-Thorschten/shell-highlight) |
| sidebar | 侧栏扩展面板。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sidebar) |
| smooth-stream | 打字机效果：流式回复按约 30 帧/秒逐字显示，只改显示，不改回复内容。 | MIT | [链接](https://github.com/kyongsik-yoon/claude-mods/tree/main/smooth-stream) |
| speaker-colours | 你的消息加浅蓝竖条和底色，Claude 的回复加橙色竖条和底色。只改显示，不联网；输入框里键入的提示由它自绘 UserMessage、不调用 next（其他来源的消息照常交给引擎），AssistantMessage 调 next 后在外面包一层。 |  | [链接](https://github.com/herman925/925-cc-plugins/tree/main/speaker-colours) |
| spell-bar | 按 effort 等级绘制的动画施法条（Clawd / Avada Kedavra 六档）。纯 UI，不改写工具或提示。 | MIT | [链接](https://github.com/powerofjinbo/claude-code-spell-bar/tree/main/plugins/spell-bar) |
| spinner-stats | 在 Claude 自带 spinner 后缀追加耗时、当前工具与调用次数。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/spinner-stats) |
| starfleet-panel | 提示框下方 LCARS 风格状态面板（模型/上下文/限额/分支等）；只读跟随 red-alert。本地 git/hostname。 | MIT | [链接](https://github.com/dukechain2333/starfleet-panel/tree/main/plugin) |
| status-band | 可主题化状态条：模型/effort、目录、git、上下文与配额等；/band 配置。 | MIT | [链接](https://github.com/dukechain2333/cc-status-band) |
| status-bar | 把各 mod 状态行折成一行（或上方 band）。纯 UI。 |  | [链接](https://github.com/tylergraydev/cc-mods/tree/main/status-bar) |
| stepscope | 步骤追踪与可视化窗格。 | MIT | [链接](https://github.com/5d0tal1gat0r/stepscope) |
| themes | 用 Monokai Pro 配色（6 套，/plugin configure 选）重绘 Claude 回复：标题、粗斜体、行内代码、链接、列表和代码块高亮。只改显示，存储的消息和 Claude 下一轮读到的内容不变，不联网。备注：终端里 AssistantMessage 插槽自绘时不调用 next；仓库内置了 marked 与 highlight.js 的压缩版 JS（均 MIT）。 | MIT | [链接](https://github.com/danishmughal/claude-code-themes) |
| think-meter | 桌面端回合计时器：等待/思考/写出/工具分段与 tok/s，附 /think-stats。 | MIT | [链接](https://github.com/Huuuuung/think-meter) |
| thinking-band | 提示框上方显示本回合最新 thinking 文本（只观察 turn.step，不改写工具/提示）。 | MIT | [链接](https://github.com/orfevre-34/thinking-band) |
| timeline | 侧栏时间轴：本回合时间花在等待/思考/写出/工具/等帮手等。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/timeline) |
| title-bar | 在提示下方的 PromptHint 显示会话名、文件夹和 git 分支，并同步成终端窗口标题。本机每 5 秒跑 git branch/rev-parse；读本会话 transcript 只取标题行；设置 CLAUDE_CODE_DISABLE_TERMINAL_TITLE=1 关掉引擎自带标题；macOS/Linux 用 printf 写 /dev/tty，Windows 运行仓库里的 scripts/set-title.ps1（-ExecutionPolicy Bypass，只调 SetConsoleTitleW）。classic.UserPromptSubmit 只记录 transcript 路径和会话标题后原样 next，不改写提示；Bash 工具调用原样 next 后再刷新。显示标题时 PromptHint 不调用 next 而自绘（保留原提示文字）。不联网。 |  | [链接](https://github.com/akagaya/claude-code-mods/tree/main/plugins/title-bar) |
| tool-cards | 终端里把工具调用画成卡片（高亮 Bash、可展开输出）；纯 UI，不改写工具。 | MIT | [链接](https://github.com/mustafa89/my-claude-code-mods/tree/main/tool-cards) |
| tool-timing-badge | 给每次工具调用旁加耗时彩色徽章；只测时+画 UI，不改写工具。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/ui/tool-timing-badge) |
| tps-report | TPS 风格工作报告窗格。 | MIT | [链接](https://github.com/vgnshiyer/tps-report) |
| transcript-fx | 给 transcript 上色：工具块、提示面板和 spinner。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/transcript-fx) |
| turn-timer | 轻量回合计时状态。 |  | [链接](https://github.com/anthonyhungnguyen/claude-code-mods/tree/main/turn-timer) |
| turn-progress | 状态行显示本回合阶段、经过时间与完成标记；可注册 progress 工具申报进度。 | MIT | [链接](https://github.com/tsumugilabo/turn-progress/tree/main/plugins/turn-progress) |
| vurgu | 把连续工具调用折成一行、按发言者给消息上色，并在提示框上方加跳转按钮；本机 process（python3 读本机会话记录），tool.call 只观察，只改显示，显示时 AbovePrompt 不调 next。 | MIT | [链接](https://github.com/yasinozmeen/claude-code-mods/tree/main/vurgu) |
| whats-agent-doing | 提示框上方显示 Claude 当前在做什么（读提示、思考、写回复、跑工具、等审批），可展开历史。 | MIT | [链接](https://github.com/tzafrir/whats-agent-doing) |
| bumper-sticker | 用自定义词替换 Spinner 忙碌文案；纯 UI。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/bumper-sticker) |
| logo | 提示上方显示自设 PNG logo（终端 Raster）；备注：本机 process（powershell 缩图）。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/logo) |
| steering-wheel | /steering-wheel 写入 ~/.claude/keybindings.json 绑定 F5 立即发送，并改写 PromptHint「send now」文案；备注：本机写配置文件。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/steering-wheel) |
| progress-bar | 提示框上方本回合进度条、估时与工具次数；等待审批时暂停计时。纯 UI，只观察 turn/tool，不改写。 |  | [链接](https://github.com/kshitiz-swim/claude-plugins/tree/main/plugins/progress-bar) |
| progress-bar-3000 | 注册自己的 `progress` 工具和 /progress-bar-3000 命令，驱动本机渲染器在 tmux 里画两行进度窗格。备注：Go 程序，同仓库 `make build`，把路径设到 `binary` 选项；只处理自己的工具；只开本机 tmux 进程，不联网。 | MIT | [链接](https://github.com/atomicstack/progress-bar-3000/tree/main/claude-code-mod) |
| qa-guide | prompt.submit 仅记录然后调用 next 且不注入上下文，AskUserQuestion 说明文字使用 $.model.fork / $.model.complete 并默认开启直至手动切换。 | MIT | [链接](https://github.com/aieo-product/claude_qamods/tree/main/plugins/qa-guide) |
| cc-cli-rail | prompt-rail 的竖向分叉：在对话旁列出本会话的历史 prompt，点击或 /cc-cli-rail next/prev/编号/find 跳回。备注：本机 process（用 tail 读本会话记录文件）；隐藏或窄屏时 AbovePrompt 不调 next，会盖住别的提示框上方行；与已有 prompt-rail 同源，二选一。 | MIT | [链接](https://github.com/afu-it/cc-cli-rail) |
| widgets | 小部件卡片布局：/widgets 把卡片放在提示框上方、下方或全屏时的侧边窗格，下面所有 *-widget 都依赖它；只改显示。备注：上次选了侧栏时，会话开始约 0.4 秒后会自动重新打开侧栏。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/widgets) |
| message-banniere | 用黑底黄字的粗体横幅和状态行显示当前会话名，/banniere 打开面板；纯 UI，只观察 prompt.submit、原样放行，不用网络。 |  | [链接](https://github.com/177cubicube-star/claude-code-mods/tree/main/message-banniere) |
| turn-timestamp | 每个回合结束处加上日期时间、用时和工具调用次数（终端替换回合用时行，桌面端加在回复下方）。备注：prompt.submit/tool.call 只计数原样放行；本机 date 取时区；不联网。 |  | [链接](https://github.com/shissncg/claude-mods/tree/main/mods/turn-timestamp) |
| explorai-loading | 提示框上方显示 Explorai 标志，随任务完成逐步填上品牌色，旁边有小人跳舞。备注：prompt.submit 只启动动画不改写；Task/Todo 工具调用原样放行；不联网。 |  | [链接](https://github.com/Tomy-Phillip/claude-mods/tree/main/plugins/explorai-loading) |
| rtl | 让 Claude Code 终端正确显示希伯来语、阿拉伯语、波斯语等从右到左文字（消息、命令输出、提示预览）。备注：只改显示，提交内容不变；可选的 recap 横幅默认关闭，开启后会在空闲时对本会话额外调用一次模型（$.model.fork，计费）；内置 MIT 的 bidi-js 源码；不联网。 | MIT | [链接](https://github.com/ofekbetzalel/claude-code-cli-rtl/tree/main/mod/rtl) |
| md-render | 把助手回复重绘成带颜色的 Markdown（标题、粗斜体、代码、列表、引用）。备注：只在 AssistantMessage 槽位终端自绘，不调 next；表格/代码块交回内置 Markdown；不联网、不跑进程。 | MIT | [链接](https://github.com/deepskyblue86/claude-markdown-mod) |
| model-band | 提示框上方一条显示当前模型与 reasoning effort，可下拉直接切换。备注：只在用户手动选择时执行 /model、/effort 命令；模型列表写死在源码里，不在列表的当前模型仍会显示。 |  | [链接](https://github.com/Lunik/gmz-claude-marketplace/tree/master/model-band) |
| prompt-hint-trim | 从输入框下方提示行去掉「N shells」和「← for agents」两段，其余原样保留。备注：只改提示行显示文字，纯本机 UI。 | MIT | [链接](https://github.com/mataku/dotfiles/tree/develop/claude/mods/prompt-hint-trim) |
| prompt-clock | 在对话里给每条你发出的消息前加发送时间，并在回合耗时行加开始→结束时间；可配置是否显示秒。备注：session.append 只记录时间不改写消息，显示时只改 UI 文本；恢复会话时读本机 transcript 文件取旧时间。 | Apache-2.0 | [链接](https://github.com/vampik33/claude-plugins/tree/main/plugins/prompt-clock) |
| model-search | /ms 或 /model-search 打开搜索面板，按名称、提供商或 ID 筛选模型，回车选第一个直接切换；/model 原样保留。备注：读本机 settings 的 modelPicker 列表和引擎的模型选项；只在你选择时执行 /model 命令；纯本机 UI。 | MIT | [链接](https://github.com/junjiezhou1122/plugins/tree/main/model-search) |
| ailang-brand | AILANG 风格：提示行旁显示 λ AILANG 版本号，加载词换成编译器味的 Unifying…、Inferring effects… 等；/ailang 打开带 logo 的面板。备注：本机运行 `ailang --version`；只改 PromptHint、Spinner、TurnDuration 显示文字并调 next。 | MIT | [链接](https://github.com/sunholo-data/ailang_bootstrap/tree/stable/plugins/ailang-brand) |
| neon-sumi | 霓虹水墨风驾驶舱：/neon-sumi-cockpit 打开面板，显示额度条、你的 PR/通知、worktree、本机在服务的端口和最近用过的 skills。备注：面板定时运行插件自带、源码可读的 Python 脚本（statusline/cockpit.py，需 python3）；用 gh CLI 只读查询（需已登录 gh），只探测 127.0.0.1 端口，读本机 transcript 统计 skills，缓存写 ~/.cache/neon-sumi。 | MIT | [链接](https://github.com/danneftw1/neon-sumi/tree/main/plugins/neon-sumi) |
| statusline-band | 把 statusline 脚本移植成 mod：提示框上方两行彩色信息（目录、git、模型、effort、时长、额度、上下文、费用、内存等），主要给桌面版 Code 标签页用，终端默认关闭（可配置）。备注：本机只读运行 git、ps、pgrep；turn.step 只读取 effort 并原样透传。 |  | [链接](https://github.com/zakattack9/agentic-coding/tree/main/claude-code/plugins/statusline-band) |
| ultimate-hud | 提示框上方 emoji HUD：模型、仓库、分支、上下文、输入/输出 token、缓存命中/写入比例、费用和额度；/hud 显示或隐藏。备注：只读本地 .git/HEAD 取分支；纯本机 UI；与 devhud 都注册 /hud，同时安装时后加载的那个 /hud 会被拒绝。 | Apache-2.0 | [链接](https://github.com/RaDeleon/Claude-Code-Ultimate-Setup/tree/main/mods/ultimate-hud) |
| devhud | 余烬配色的费用、上下文和 git HUD，/hud 打开面板，可显示子代理和 PR 状态。备注：本机只读运行 git status/log 和 gh pr view、gh api graphql（需已登录 gh）；tool.call 原样返回；与 ultimate-hud 都注册 /hud，同时安装时后加载的那个 /hud 会被拒绝。 |  | [链接](https://github.com/codywilliamson/claude-mods/tree/main/devhud) |
| ccbar | 提示框上方一条安静的状态带：模型和 effort、仓库（GitHub owner/name、分支、暂存+未暂存改动）、按 /context 类别着色的上下文条、本会话新增 token、会话和每周额度及重置倒计时。备注：本机只读运行 git，用 tail/head 读本会话 transcript 统计 token；纯本机 UI。 | MIT | [链接](https://github.com/emaballarin/ccplugins/tree/main/plugins/ccbar) |
| quickbar | 提示框上方一行启动栏：实时上下文百分比，加上已安装的 claude-mods 面板一键按钮。备注：只列出你已安装的 mishgoldenberg/claude-mods 面板命令，按按钮才运行对应命令；纯本机 UI。 | MIT | [链接](https://github.com/mishgoldenberg/claude-mods/tree/main/plugins/quickbar) |
| clock | 状态行里一个按定时器跳动的小时钟。备注：本机运行 date +%z 取时区偏移；纯本机 UI。 |  | [链接](https://github.com/ryanthedev/dot-config/tree/main/claude/mods/clock) |
| account-badge | 在提示框页脚显示当前登录组织的缩写（个人账号显示 PERS，用 API key 时显示 API）。备注：只读本机 ~/.claude.json 里的 oauthAccount，每 15 秒刷新；纯本机 UI。 | MIT | [链接](https://github.com/Amnesiac9/claude-mods/tree/main/account-badge) |
| green-lantern | 绿灯侠主题：戒指能量 spinner、电池式用量条、新会话徽章和翡翠配色。备注：prompt.submit 只用来收起欢迎画面和刷新动画，不改写提示；纯本机 UI。 | MIT | [链接](https://github.com/vogiaan1904/green-lantern-claude) |
| dock | 提示框下方一排可点的按钮：开关 deck、files、preview 等 mod，或运行你钉上去的任意斜杠命令。备注：只有你点按钮才运行对应命令；纯本机。 | MIT | [链接](https://github.com/manikosto/dock) |
| switch | /switch 打开模型与推理强度面板，一键切换；/switch opus 或 /switch high 直接切换。备注：点击时运行 Claude Code 自带的 /model 或 /effort；engine.create 只用来拿界面句柄；说明为法语。 | MIT | [链接](https://github.com/devohmycode/claude-mods/tree/main/claude-switch-mod) |
| echo-widget | 提示框上方的方框小部件，用命令开关：番茄钟和日历。备注：纯本机计时与绘制。 |  | [链接](https://github.com/echo724/echo-claude-mod/tree/main/mods/echo-widget) |
| syntax | 输入时给提示框草稿上色：Markdown、代码围栏里的代码，以及 shell 模式下的命令。备注：prompt.edit 只追加颜色装饰，不改动草稿文字；纯本机，不联网、不跑进程；若装了同仓库 statusline 会读取其编辑模式（本市场已有同名 statusline，未收录 thefuga 版）。 | MIT | [链接](https://github.com/thefuga/claude-x/tree/main/mods/syntax) |
| vim | 提示框上方的 vim 命令行：:w / :e 按会话保存和读回草稿，:q 退出（:q! 强制），输入其他名字就执行对应斜杠命令，支持 Tab 补全；用聚焦快捷键打开。备注：prompt.fill 只把你自己 :w 保存的草稿回填到空提示框，不自动提交；classic.UserPromptSubmit 只在发送后删掉已存草稿，不改写 prompt；草稿存于插件本地 store，不联网。 | MIT | [链接](https://github.com/thefuga/claude-x/tree/main/mods/vim) |
| attachments | 把草稿里的附件显示成提示框上方的小卡片：粘贴的图片和文本、@ 提到的文件与文件夹，各带类型图标、路径和简介，点 × 从草稿里移除。备注：prompt.fill 只在你点 × 时删掉对应占位或 @ 引用；会用本机 ffprobe（若已安装）读取媒体尺寸时长，并跑 id -u 定位临时图片目录；不联网、不提交 prompt。 | MIT | [链接](https://github.com/thefuga/claude-x/tree/main/mods/attachments) |
| message-time | 在对话记录里你发的每条消息下面加一行暗色「sent HH:MM」发送时间，跨天的第一条带星期和日期；Remote Control 发来的也会标。备注：只改 UserMessage 行的显示，不碰消息内容；纯本机，不联网；恢复的旧会话里的消息会标成模块加载时间。 |  | [链接](https://github.com/jonathan-fielding/dotclaude/tree/main/plugins/message-time) |
| clean-view | 西班牙语「简洁视图」：隐藏工具调用和结果行，在提示框上方显示步骤清单、进度条和结束时的一句话总结（改了哪些文件、跑了几条命令、几个错误）；/clean-view 或按 0 开关。备注：tool.call 只观察结果、原样传递；turn.complete 只把回合结束提示文字换成本地总结；不改 prompt，纯本机，不联网。 |  | [链接](https://github.com/Dos2Locos/claude-code-mods/tree/main/plugins/clean-view) |
| spinner-packs | 主题化的加载词：工作时显示「Plundering…」、结束时「Plundered for 1m 3s」这类词，内置海盗、莎士比亚、巫师、厨师、太空等 10 套，也可以填自己的词；/spinner 切换。备注：只改 Spinner 和 TurnDuration 的显示文字，压缩/重试等状态文字保持原样；纯本机，不联网。 | MIT | [链接](https://github.com/Singh-AP/awesome-claude-mods/tree/main/mods/fun/spinner-packs) |

### 游戏与娱乐 Games & Entertainment

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| 2048 | 提示框上方玩 2048；仅 UI/命令，不注入 prompt、不改工具。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/2048) |
| agent-race | 多会话任务赛跑分屏。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/agent-race) |
| blackjack | 侧栏二十一点牌桌，Claude 工作时可玩；仅 UI，不改工具、不外传。 | MIT | [链接](https://github.com/michaeldavodovski/claude-code-blackjack) |
| tokencraft | Minecraft 风格 HUD：工具调用变方块与 XP，爱心=限额、饥饿=上下文。备注：本机读 .git/HEAD 与 maios/planning/sprint.local.md；回合结束把战利品行拼进回答文本，不外传。 | MIT | [链接](https://github.com/DanielPodolsky/tokencraft) |
| doom | 提示框上方 Doom 走廊射击；仅 UI/命令，不注入 prompt、不改工具。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/doom) |
| pacman | 提示框上方吃豆人；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/pacman) |
| flappy | 提示框上方 Flappy；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/flappy) |
| flappy-claude | /flappy-claude 在输入框上方玩 Flappy Bird 式小游戏，只存最高分到 $.store，带本地音效。备注：与已有的 flappy（davila7）是不同作者的独立实现，二选一即可；打开时 AbovePrompt 不调 next。 | MIT | [链接](https://github.com/narze/flappy-claude-mod) |
| invaders | 提示框上方太空侵略者；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/invaders) |
| minesweeper | 提示框上方扫雷；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/minesweeper) |
| tool-defense | 塔防：每个敌人对应一次 Claude 工具调用；仅 UI，监听 tool.call 不改写。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/tool-defense) |
| tokenrun | /tokenrun 跑酷小游戏窗格：空提示框时空格跳跃；仅 UI/命令，不注入 prompt、不改工具。 | MIT | [链接](https://github.com/NipunBinjola/tokenrun) |
| diff-invaders | Diff 侵略者：Edit/Write 新增行变成波次；仅 UI，不改工具。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/diff-invaders) |
| boss-fight | 失败测试变 boss，通过测试打血条的像素小游戏。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/boss-fight) |
| cc-arcade | 在提示框上方显示游戏，点击不会调用模型。 |  | [链接](https://github.com/sezaakgun/cc-arcade) |
| samurai-dojo | 每次工具调用变成武士斩击动画，跨会话记斩杀；备注：赛季可写 ~/.claude/mods/active-game。 | MIT | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/samurai-dojo) |
| slayer-corps | 鬼灭队主题战斗动画：工具调用出招、回合收尾；纯 UI。 | MIT | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/slayer-corps) |
| cc-dino | Chrome 恐龙跑酷游戏，Claude 忙时可玩。 | MIT | [链接](https://github.com/manfye/cc-dino) |
| cc-idle | 挂在 Claude 旁边的放置游戏，只用本机会话进度。 | MIT | [链接](https://github.com/RichardAtCT/cc-idle/tree/main/plugins/cc-idle) |
| cc-range | 提示上方像素射击馆小游戏（鼠标瞄准开火，零 token）。 | MIT | [链接](https://github.com/germanfndez/cc-range) |
| cc-subway | 地铁跑酷小游戏，可在右侧窗格或提示框上方游玩。 | MIT | [链接](https://github.com/lucastononro/cc-subway) |
| cielinux-scenes | 随 Claude Code 活动（回合、工具、子代理、权限提示）切换 CieLinux 壁纸场景并发提醒：把场景名和提醒名 POST 到本机 CieLinux HTTP API（默认 http://127.0.0.1:43811，bearer token 读本机 token 文件）。备注：tool.call 原样放行，不发送会话内容；需要 CieLinux（仅 Linux）。 |  | [链接](https://github.com/JamsMendez/CieLinux/tree/main/integrations/claude-code) |
| claude-dino | 提示框上方的恐龙跑酷小游戏（来源与已上架的 cc-dino 不同）。 |  | [链接](https://github.com/swan4er/claude-dino) |
| claude-games | 提示框上方的街机游戏（/racer、/breakout、/dino、/shooter），在 Claude 工作时玩；游戏对 Claude 的行为作出反应：... | MIT | [链接](https://github.com/mohi-devhub/claude-games) |
| claude-maru-run | Claude 工作时在窗格里看方块跑酷小游戏。 |  | [链接](https://github.com/lemonlatte/claude-maru-run) |
| claude-mine | 提示框上方的体素沙盒小游戏（不是扫雷）。 |  | [链接](https://github.com/swan4er/claude-mine) |
| claude-slots | 老虎机游戏，等待时可玩。 | MIT | [链接](https://github.com/WorldInnovationsDepartment/claude_slots) |
| clawd-park | Spinner 下方像素恐龙公园：随工具活动表演，连续失败测试逼近陨石；只观察 tool.call，零模型调用。 | MIT | [链接](https://github.com/falkoro/clawd-park/tree/main/plugins/clawd-park) |
| context-dungeon | 把会话做成肉鸽：上下文是 HP，报错出怪，绿测击杀，只观察 tool.call，不改调用。 | MIT | [链接](https://github.com/ccdwyer/context-dungeon) |
| cs-radio | 会话/长回合/部署时播放 CS 电台音效；/radio 开关；不改写、不外泄。 | MIT | [链接](https://github.com/ben-rogerson/claude-counter-strike) |
| daily-grind | /grind 每日开发者谜题窗格（猜词、分组、逻辑格等），进度存本机。备注：每天首次会话弹一次提示。 | MIT | [链接](https://github.com/sreshtalluri/claude-mods/tree/main/plugins/daily-grind) |
| gamba | 在提示框上方玩老虎机小游戏。 |  | [链接](https://github.com/salatmaster/claude-gamba) |
| hyday-pet | 提示框上方虚拟宠物，随 Claude 工作成长、可小游戏/商店。 | MIT | [链接](https://github.com/mukiwu/muki-ai-plugins/tree/main/plugins/hyday-pet) |
| intermission | Claude 工作时在 Ghostty/kitty 窗格里开 Doom 死斗，回合结束或需要输入时自动切回。 | MIT | [链接](https://github.com/jarrodwatts/intermission) |
| kiko | 提示框上方拳击小游戏：每回合开打，工具调用当出拳；/kiko on|off|stats。正常 K.O. 时默认调用 $.session.append 添加系统消息，包含得分行（对手名取自用户提示）、读写次数与 token 计数；只观察会话事件，不改写工具调用。 | MIT | [链接](https://github.com/kikostefanov-lab/claude-code-mods/tree/main/kiko) |
| korkmaz-trail | 俄勒冈小径风格像素游戏。 | MIT | [链接](https://github.com/BersanKayraKorkmaz/korkmaz-trail) |
| lava-lamp | 提示框旁熔岩灯侧栏动画；仅 UI/命令，不注入 prompt、不改工具。 | MIT | [链接](https://github.com/CtrlAltFocus/claude-mods/tree/main/plugins/lava-lamp) |
| little-harvest | 随回合生长的自动小花园。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/little-harvest) |
| minefield | Claude 工作时在窗格里玩扫雷。 | MIT | [链接](https://github.com/reporails/arcade/tree/main/minefield) |
| night-feast | Claude 工作时的像素小游戏。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/night-feast) |
| pet | 一只嘴碎的火烈鸟吉祥物 Flingo，在侧栏或状态行陪伴你码字，代 Claude 说话、吐槽代码、喂养玩耍、换装（皇冠、礼帽、蝴蝶结、墨镜），用 /fli... | MIT | [链接](https://github.com/graugart/flingo) |
| pong | 在提示框上方玩 Pong 游戏，Claude 工作时可打发时间。 | MIT | [链接](https://github.com/ambareeshav/claude-pong-mod) |
| roll-credits | /credits 电影片尾字幕窗格：本会话编辑文件与工具调用统计（本地、零 token）。 | MIT | [链接](https://github.com/smukh/roll-credits) |
| severance-mdr | Severance 风格 MDR 小游戏面板；代理工作时可自动打开。纯 UI。 |  | [链接](https://github.com/magnuswiderberg/claude-code-mods/tree/main/plugins/severance-mdr) |
| snake | Claude 工作时可玩的贪吃蛇窗格（/snake）。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/snake) |
| snake-widget | 自己会玩、可随时接手的贪吃蛇卡片，只存最高分，需配合 widgets。备注：卡片显示时每 160 毫秒刷新。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/snake-widget) |
| wod-band | 提示框上方像素运动员：工具调用计 rep，会话当 AMRAP。纯 UI。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/wod-band) |
| wod-timer | 提交时 3-2-1-GO，每回合计时与白板 split；可选本机语音读出超过一分钟的回合。纯 UI。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/wod-timer) |
| tetris | 提示框上方俄罗斯方块；仅 UI/命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/tetris) |
| tetris-widget | 自己会玩、可随时接手的俄罗斯方块卡片，只存最高分，需配合 widgets。备注：卡片显示时每 250 毫秒刷新。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/tetris-widget) |
| tiktok-break | /tiktok 在侧边窗格播放 TikTok。备注：需要本机 bun 和 Chromium 系浏览器；用单独的浏览器资料目录（需在里面自己登录 TikTok）；本机 sh、pgrep、pkill 只管这个资料目录；viewer 通过 127.0.0.1 的 DevTools 端口控制无头 Chrome，只访问 tiktok.com，不发送会话内容。 | MIT | [链接](https://github.com/Chinteyley/tiktok-break) |
| typing-test | 提示框上方打字测速；Claude 工作时可玩，回合结束暂停，记录最佳成绩；零 token。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/games/typing-test) |
| tool-snake | Claude 每调用一次工具就往贪吃蛇里掉一颗食物（/snake）；每次提交提示会自动打开窗格，结束时用本机语音朗读成绩；和已有的 snake 都注册 /snake，二选一安装。 | MIT | [链接](https://github.com/Yash1927/claude-code-snake) |
| gamble-with-claude-code | 用今天烧掉的 token 当筹码玩老虎机、轮盘和二十一点（/casino），不涉及真钱；会在本机 process 运行 python3，读取本机 ~/.claude 下的会话记录统计 token，不外传。 | MIT | [链接](https://github.com/szarkans/gamble-with-claude-code) |
| sidequest | Claude 工作时在侧栏窗格玩贪吃蛇（/sidequest [on|off|游戏名]）。默认开启：回合开始约 2 秒后自动开窗，需要你确认权限或回答问题时自动收起；窗格放不下时在提示框上方给"开始玩"按钮（会调 next）。只用 $.store 存进度，纯 UI。 | MIT | [链接](https://github.com/farhad-aman/claude-sidequest) |
| code-quest | 把会话变成小冒险：读文件、改文件、测试通过、git commit 得 XP 升级解锁成就，提示框上方显示等级条，/quest 设任务。只观察首条提示（前 60 字存本机）和工具结果、原样放行。 |  | [链接](https://github.com/vardhankirti/claude-code-mods/tree/main/code-quest) |
| ptt | 在 Claude Code 面板里刷 PTT（中文论坛），可自定义看板，带老板键。备注：会联网读 www.ptt.cc 的公开看板页面，不发送任何会话内容；看板列表存在 $.store。 | MIT | [链接](https://github.com/chenyao0910/claude-ptt-mod/tree/main/plugins/ptt) |
| sushida | /sushida 在面板里打开寿司打风格的日语打字游戏，支持假名输入的多种罗马字写法。备注：纯本机 UI；界面为日文。 |  | [链接](https://github.com/sontixyou/sushi-uchi/tree/main/sushida) |
| combo-meter | 格斗游戏连击计：每次成功的工具调用算一击，出错就断连，D 到 SSS 评级、特殊招式和历史最高分。备注：tool.call 原样返回，只计数；可选音效；纯本机。 | MIT | [链接](https://github.com/SARTHAK2511/claude-combo) |

### 安全防护 Security & Safety

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| admin-capability-lockdown | 组织级管控：剥夺下层插件的 http/process，并可拒绝 Bash 或网络客户端。备注：只 deny/能力剥夺，不改写命令；宜放 managed prepend。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/enterprise/admin-capability-lockdown) |
| anchorwatch-mod | Bash 危险命令本地 deny（rm -rf、force push、DROP、curl\|sh、读 .env 等）；备注：只 deny 不改写；本机 git 查当前分支。 | MIT | [链接](https://github.com/anchorwatch-dev/anchorwatch/tree/main/plugins/anchorwatch-mod) |
| assertion-guardian | 拦截削弱测试的 Edit/Write/Bash（删断言、加 skip 等）；只拒绝不改写。备注：本机 git 读旧版对比。 | MIT | [链接](https://github.com/ccdwyer/assertion-guardian) |
| bash-guardrails | 用本地规则拒绝危险或畸形的 Bash 与 Monitor 调用（只读命令字符串做判定，不改写命令）。 |  | [链接](https://github.com/ruihe774/cc-bash-guardrails) |
| block-destructive-commands | 按模式拒绝危险 Bash（递归删根、force push、硬重置、破坏性 SQL 等）。备注：只 deny，不改写命令。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/security/block-destructive-commands) |
| branch-guard | 在受保护分支上拦截 Write/Edit 与变更型 git，可询问后放行或建议 worktree。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/branch-guard) |
| browser-guard | 把 cswap 账号与 Chrome 配置配对，防止用错浏览器画像。备注：可 deny 不匹配的 Chrome 工具调用；依赖本机 `cswap stat... |  | [链接](https://github.com/abhibansal60/claude-mods/tree/main/browser-guard) |
| collision-guard | 另一会话刚改过同一文件时先询问再编辑。备注：可 deny 编辑并询问用户。 |  | [链接](https://github.com/nateherkai/claude-code-mods/tree/main/collision-guard) |
| council-of-elrond | 按规则给每次工具调用分级：放行、拦下、问你，或交给 $.model.complete 审核（会发送工具调用、最近一次提示和本会话写过的脚本内容，已脱敏）；只拒绝不改写；在本机项目里写审计日志。 | MIT | [链接](https://github.com/Deluha/council-of-elrond/tree/main/mods/council-of-elrond) |
| danger-check | rm -rf、git reset --hard、强推等会毁掉工作的命令先弹窗问你，选阻止就拒绝；备注：只拒绝不改写；本机 git 预览（git status / clean -n / stash list）。 | MIT | [链接](https://github.com/achapla/cc-mods/tree/main/danger-check) |
| delete-guard | 拦截 rm -rf 等危险删除，可拒绝或移入本机回收站；不改写命令。备注：本机 process。 |  | [链接](https://github.com/Tihi321/claude-mods/tree/main/plugins/delete-guard) |
| env | 在面板里编辑 .env；Claude 管理键名但看不到真实密钥值。 | MIT | [链接](https://github.com/davekiss/env) |
| flash-veille | 提示框上方轮播开发者资讯（Human Coders、Anthropic 博客等）。 | MIT | [链接](https://github.com/camilleroux/flash-veille/tree/main/plugins/flash-veille) |
| guard | 拦截危险 Bash 与密钥文件读写，只拒绝不改写。备注：本机 $.fs.stat；无拦截时可用 $.ui.status(undefined) 清状态行。 | MIT | [链接](https://github.com/StanislavKozachenko/claude-mods/tree/main/plugins/guard) |
| guardclaw | 只拒绝、失败即关闭：每条 shell 命令交给本机 `guardclaw-scan` 扫描，并挡住文件工具碰凭据与设置文件。备注：完整模式需要本机 guardclaw-scan 二进制（同仓库 `go install github.com/TakeInterestInc/guardclaw-core/cmd/guardclaw-scan@latest`；没有则退回内置规则）；不联网；会拒绝加载钩住风险事件的其他非信任 mod（包括本市场里的 mod），除非加进它的 `allowMods` 选项。 | Apache-2.0 | [链接](https://github.com/TakeInterestInc/guardclaw-core/tree/main/claude-code-mod) |
| guardrails | 本地拒绝 Cloudflare 写命令、带归因行的 commit、claude/ 分支前缀。备注：只读 Bash 命令字符串做 deny，不改写。 |  | [链接](https://github.com/arasovic/claude-code-mods/tree/main/guardrails) |
| launch-codes | 危险 Bash 需解锁码才放行。备注：会 deny 危险命令直至用户解锁。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/launch-codes) |
| machine-guard | 改机器的 Bash 先征求确认；仅拒绝，不改写命令。 | MIT | [链接](https://github.com/MichaelP17/claude-mods/tree/main/machine-guard) |
| large-edit-confirmation | 编辑或覆盖超大文件前用 AskUserQuestion 确认；无人应答默认拒绝。备注：可 deny，不改写内容。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/security/large-edit-confirmation) |
| merge-gate | 除非最新人工消息含 merge，否则拒绝 Bash 里的 merge / gh pr merge / 推送到主干。备注：只 deny，不改写命令；用本机 git。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/merge-gate) |
| no-new-branch | 要新建 git 分支、worktree 或带 worktree 的子代理时先问你；备注：只拒绝不改写。 | MIT | [链接](https://github.com/achapla/cc-mods/tree/main/no-new-branch) |
| no-process-kill | 要 kill / 停止正在运行的进程或 TaskStop 时先问你；备注：只拒绝不改写。 | MIT | [链接](https://github.com/achapla/cc-mods/tree/main/no-process-kill) |
| path-guard | 拒绝项目根外或 .git 内的 Write/Edit（可选护 Read）。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/path-guard) |
| pii-guard | 台湾 PII 可逆脱敏（经本地 hookd）；需 Python/uv。 |  | [链接](https://github.com/danyuchn/pii-guard/tree/main/examples/claude-code-mod) |
| pnpm-only | 拒绝 npm / npx 命令并告诉 Claude 对应的 pnpm 写法；备注：只拒绝不改写。 | MIT | [链接](https://github.com/achapla/cc-mods/tree/main/pnpm-only) |
| protected-paths-guard | 拒绝 Edit/Write/NotebookEdit 触及 .env、锁文件、CI 工作流、git 内部与私钥等路径（可配置 allow）。备注：只 deny，不改写。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/security/protected-paths-guard) |
| redact | Read 结果里把疑似密钥字符串替换成 `[REDACTED:…]` 再给模型。备注：改写的是 Read 结果文本，不改写命令。 | MIT | [链接](https://github.com/thkt/dotclaude/tree/main/mods/redact) |
| safety-guard | 拦下 curl 管道进 shell、对根目录/家目录的 rm -r、git 强推/reset --hard/clean -f、dd 写设备、mkfs、chmod -R 777，以及读写 .env、私钥、.aws 凭据等密钥文件；只拒绝不改写。 |  | [链接](https://github.com/pradyb/claude-mods/tree/main/safety-guard) |
| script-gate | Bash 拦截「下载即执行」管道、Encoded PowerShell、LOLBin 等；只拒绝不改写命令。备注：只拒绝不改写。 | MIT | [链接](https://github.com/ABDUAZIZX/script-gate) |
| seatbelt | 本地规则拦截危险 Bash/写文件（只拒绝不改写命令）。备注：会 deny 匹配的工具调用。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/seatbelt) |
| secret-guard | 拦截即将写入文件或 Bash 的疑似密钥内容。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/secret-guard) |
| secret-mask | 在工具输出写入对话前遮罩疑似密钥。备注：会改写展示给模型的工具结果文本（本地遮罩，不外传）。 |  | [链接](https://github.com/homieyangg/claude-code-mods/tree/main/secret-mask) |
| secret-redactor | 在模型看到前把密钥/邮箱/IP 换成占位符，工具输入时再还原。 |  | [链接](https://github.com/ray-amjad/awesome-claude-code-function-hooks/tree/main/plugins/secret-redactor) |
| secret-sentry | 双向密钥清洗：模型看到前脱敏，并拦截把密钥写入受跟踪文件或 shell。备注：可 deny；脱敏 prompt/工具结果文本，不外传；本机 git。 | MIT | [链接](https://github.com/ccdwyer/secret-sentry) |
| secrets-guard | 拒绝 Edit/Write/NotebookEdit/Bash 写入密钥文件（.env、密钥、~/.ssh、~/.aws/credentials 等）或内容呈凭据形态的调用，并拒绝 cat/head .env 与 id_rsa。备注：只拒绝不改写，不联网；与已有的 `secret-guard` 是不同项目。 | MIT | [链接](https://github.com/BioInfo/slopless/tree/main/mods/secrets-guard) |
| secrets-veil | 工具执行后遮盖结果中的疑似密钥字符串，不改写命令本身。 | MIT | [链接](https://github.com/yonatangross/orchestkit/tree/main/mods/secrets-veil) |
| sensitive-file-guard | 拦截触及 .env/密钥/凭证路径的工具调用。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/sensitive-file-guard) |
| shared-file-guard | 共享文件本会话未读或已被别会话改过时拒绝 Bash 写入；只拒绝不改写。备注：本机 $.fs.stat。 | MIT | [链接](https://github.com/mutlumehmet/claude-plugins/tree/main/plugins/shared-file-guard) |
| stay-put | 拦截 `cd dir && …` 链式 Bash/PowerShell，只拒绝并提示单命令写法（不改写命令）；teach/watch/off。除非 off，会在 Bash 与 PowerShell 工具描述追加不要链 cd 的指示。弹跳带显示时 AbovePrompt 不调 next，可覆盖其他 mod 行。 | MIT | [链接](https://github.com/ivanvyd/ground-rules/tree/main/plugins/stay-put) |
| storage-guard | 存储保护器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/storage-guard) |
| test-guard | 拦截弱化/删除测试的 Write/Edit/Bash。备注：可 deny，不改写命令。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/test-guard) |
| mogger-status | 配合 claude-mogger 守卫钩子，读本机 .claude/state/mogger-events.log，在状态行、提示框上方显示触发与拦截次数，拦截时弹 toast。只观察。读取日志抛错时会调用 $.ui.status(undefined) 并可能清除其他 mod 的状态行。备注：显示时 AbovePrompt 会盖住别的行（可点 Hide）。 | MIT | [链接](https://github.com/yonitesser/claude-mogger/tree/master/mods/mogger-status) |
| reins-status | 只读显示 reins 审批队列（本机 .reins/pending）：状态行计数、提示框上方一行、/reins 窗格看完整输入，新挂起时 toast。不批准也不拒绝。.reins/pending 队列为空时会调用 $.ui.status(undefined) 并可能清除其他 mod 的状态行。备注：有挂起项时 AbovePrompt 会盖住别的行。 | MIT | [链接](https://github.com/manishkumar/reins/tree/main/mods/reins-status) |
| hands-off | 用户标记路径后拒绝 Edit/Write/NotebookEdit。备注：只 deny，不改写。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/hands-off) |
| query-guard | Bash 中疑似危险/慢 SQL（无 WHERE 的 DELETE/UPDATE、DROP 等）先询问再放行。备注：只 deny，不改写命令。 | MIT | [链接](https://github.com/nu0ma/query-guard/tree/main/plugins/query-guard) |
| valet-mode | 代客模式：除 Read/Grep/Glob/WebSearch/WebFetch 外一律 deny；锁文件跨窗口。备注：只 deny，不改写。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/valet-mode) |
| main-guard | 在受保护分支上拦截危险 git（force-push/hard reset 等）；可询问后放行 push。显示阻断理由时，其 AbovePrompt 返回自己的行且不调 next，可能覆盖其他 mod 的行。备注：只 deny，不改写命令；本机 git。 | MIT | [链接](https://github.com/ShriD5/claude-mods/tree/main/main-guard) |
| whoopgate | 心率超阈值时拒绝危险 Bash（读本机 ~/.whoopgate/hr.json）。备注：只 deny，不改写；本机读文件/git。 | MIT | [链接](https://github.com/ShriD5/claude-mods/tree/main/whoopgate) |
| explain-permission | 收到权限请求时在侧窗格用 $.model.fork 或 $.model.complete（haiku）解释。**仅解释：不拒绝、不改写**。 |  | [链接](https://github.com/petershk/explain-permission) |
| open-file-guard | Claude 要写/改你正打开的 Word、Excel、PowerPoint 文件前，先问你关掉（最多问 3 次），否则拒绝这次调用。备注：tool.call 只放行或 deny，不改参数；只检查本机锁文件，不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/open-file-guard) |
| registro-scritture | 每轮结束在提示框上方列出本轮写到仓库外的操作（MCP 写入、git push、gh 修改、curl POST 等），带结果链接与失败/被拒标记。备注：tool.call 只观察，原样调用 next 并返回结果，不改写；只在本机读工具结果找第一个 https 链接；意大利语界面；不联网。 | MIT | [链接](https://github.com/andreabrugnoli/mods/tree/main/registro-scritture) |
| dot-guard | 拦截对整个 $HOME 工作树的 git add（如 dot add -A / . / *），避免把整个家目录提交进 dotfiles 仓库；可配置包装命令名（默认 dot）。备注：只 deny，不改写命令。 |  | [链接](https://github.com/theagitist/claude-mods/tree/main/dot-guard) |
| package-gate | Claude 要安装软件包（npm/pnpm/yarn/pip/uv/npx/winget/brew 等）或往依赖清单里加包前，弹框列出包名和注册表链接问你是否允许；本会话已批准的不再问。备注：只 deny，不改写命令；`claude -p` 等无人可问时一律拒绝。 |  | [链接](https://github.com/cleverfakealias/agents/tree/main/mods/package-gate) |
| repo-lock | 用错包管理器（按最近的 lockfile 判断）跑依赖命令时拒绝执行，状态行显示 仓库 · 包管理器 · 分支。备注：只 deny，不改写命令；本机只运行 `git rev-parse` 取仓库和分支。 |  | [链接](https://github.com/cleverfakealias/agents/tree/main/mods/repo-lock) |
| guards | 会丢弃本会话没碰过的改动的 git 命令（reset --hard、checkout --force、clean 等）和会开始 vast.ai 计费的命令先暂停等你确认；拒绝在 .py/.ipynb 里写全局随机种子。备注：只 deny/暂停确认，不改写命令；本机运行 git status。 |  | [链接](https://github.com/wmayner/dotfiles/tree/main/claude/guards) |
| prod-guard | Claude 要跑生产部署（kamal deploy/redeploy/rollback）、生产 psql 或 make 删库类命令时先拦住，弹框显示将上线的提交、迁移、未提交改动和 CI 状态，你按 Deploy/Run 才执行，否则 deny。备注：只等待/deny，不改写命令；本机只读运行 git、kamal app version、gh run list；无人值守会话（claude -p）直接 deny。 | MIT | [链接](https://github.com/JeremyDwayne/dotfiles/tree/main/roles/claude/files/mods/prod-guard) |
| pm-guard | Claude 用 npm/npx/yarn 时，若仓库锁文件指定 bun 或 pnpm 就 deny 并提示改用对应包管理器；没有锁文件时默认要求 bun。备注：只 deny，不改写命令；「无锁文件默认 bun」是作者偏好。 |  | [链接](https://github.com/narrowstacks/claude-code-mods/tree/master/pm-guard) |
| vigia-api | 付费 API 看门：调用会花钱或花额度的工具和命令（Magnific、Kling、HeyGen、OpenRouter、Groq 等）前先问你，可授权 1 小时（/vigia）。备注：只拒绝不改写（deny）；没人在屏前时直接拒绝；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/vigia-api) |
| guarda-colisao | 编辑前检查文件是否在本会话之外被改过（其他会话、你的编辑器或别的程序），有就问你怎么办（/colisao）。备注：只拒绝不改写（deny）；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/guarda-colisao) |
| pdpa-blur | 把 transcript 里的个人数据（泰国身份证号、电话、邮箱、银行卡/账号、IP、token/密码等）画成灰块，鼠标悬停才显示；/pdpa-blur 开关。备注：只改本机显示，复制仍得原文；纯本机正则识别，不外发。 | | [链接](https://github.com/Boom-Vitt/claude-mods-boombignose/tree/main/pdpa-blur) |
| bash-guard | 本地解析 Bash 命令（含 sh -c 嵌套、包装命令），拒绝 `&` 后台/disown/setsid/coproc、pkill/killall 按名批量杀进程、`kill %作业号` 和 sleep 等待，并提示改用 run_in_background、TaskStop 等内置方式。备注：只 deny 不改写命令；纯本机，不联网。 |  | [链接](https://github.com/mary-ext/claude-skills/tree/trunk/plugins/bash-guard) |
| cluide | 拒绝 Edit 工具修改 .env 及 .env.* 文件（如 .env.local），并提示该文件受保护。备注：只 deny 不改写；只拦 Edit，不拦 Write/Bash；纯本机。 | AGPL-3.0 | [链接](https://github.com/TWim3/cluide) |
| file-guard | 把 Claude 的文件改动限制在项目内：拒绝写到项目外（解析符号链接）、不许碰 .git 内部；改锁文件、CI workflow、迁移文件、.env 和密钥前弹窗询问（允许一次/本会话/拒绝）；/file-guard check <路径> 预检。备注：只对 Read/Edit/Write 等文件工具做 deny 或询问，不改写工具参数；保护列表、额外目录、是否限制读取可在插件配置里改；无人可问（-p 模式）时默认拒绝；纯本机，不联网。 | MIT | [链接](https://github.com/Singh-AP/awesome-claude-mods/tree/main/mods/safety/file-guard) |

### 开发工具 Dev Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| auto-checkpoint | 每回合开始在 refs/claude-checkpoints 做工作树快照；/checkpoints 与 /undo-turn。纯本地 git。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/auto-checkpoint) |
| boot-sequence | 会话开始时做一次本机开机检查（git、工具链）。 | MIT | [链接](https://github.com/ccdwyer/boot-sequence) |
| branch-status | Git 面板画 main/develop/当前分支相对位置。备注：本机 git / 本机 process。 | MIT | [链接](https://github.com/Spardutti/claude-mods/tree/main/plugins/branch-status) |
| change-ledger | /changes 列出本会话改过的文件和行数。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/change-ledger) |
| changed-files | 侧栏列出本会话 Claude 改过的文件与 +/- 行数；仅 UI 侧栏，只观察。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/changed-files) |
| classifier-telemetry | 把每次工具调用的权限判定与耗时写到本机 ~/.claude/classifier-telemetry/。备注：本机写本地文件。 | MIT | [链接](https://github.com/bendrucker/claude/tree/main/plugins/classifier-telemetry) |
| claude-mermaid | 把助手回复里的 mermaid 块画成彩色 box art。 |  | [链接](https://github.com/galElmalah/claude-mods/tree/main/claude-mermaid) |
| codebase-galaxy | 用盲文点阵把仓库文件画成星空，跟着 Claude 碰过的文件。 | MIT | [链接](https://github.com/ccdwyer/codebase-galaxy) |
| codebase-atlas | 代码库架构图随读写点亮；可选用本机 $.model.complete 与 $.model.fork 提取决策，向用户模型发函数源码与 git diff HEAD，不外传。备注：本机 git。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/codebase-atlas) |
| command-buttons | 在助手 shell 代码块下画 Run/Copy 按钮与热键带；备注：本机 process（剪贴板），用户按按钮才经 tool.call 跑 Bash。 | MIT | [链接](https://github.com/faridmurzone/command-buttons-claude-code) |
| config-parse | 配置文件解析器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/config-parse) |
| dash-guard | 拒绝在 md/txt 写入 em dash、en dash 或双连字符；只拒绝不改写。备注：本机 $.fs.read。 | MIT | [链接](https://github.com/mutlumehmet/claude-plugins/tree/main/plugins/dash-guard) |
| diagram-render | 图表实时渲染。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/diagram-render) |
| diff-review | 每次 Edit/Write 后在侧栏展示未提交 hunk，keep/revert 按钮；revert 用本机 git apply -R（新建文件二次确认后 rm）。模型看不到操作。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/diff-review) |
| disk-janitor | 清理临时文件。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/disk-janitor) |
| editor-context | 在桌面端提示框上方显示 Cursor/VS Code 当前文件与选区，并在每次提交时把你正在看的内容悄悄告诉 Claude。 | MIT | [链接](https://github.com/talbarina/claude-editor-context/tree/main/plugins/editor-context) |
| file-explorer | VS Code 风格文件树/变更/历史/diff 窗格。 |  | [链接](https://github.com/tak-kam/claude-mods/tree/main/file-explorer) |
| files | 侧栏本会话新建/修改/删除的文件清单与行数（只观察工具，不改写）。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/files) |
| filetree | 侧栏文件树，跟住 Claude 正在读/写的文件并可点选带入提示。 |  | [链接](https://github.com/data-goblin/claude-code-filetree) |
| git-commit | Git 提交助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/git-commit) |
| git-sidebar | lazygit 风格侧栏：worktree/分支列表；本机 git（可 git switch，脏树拒绝）与 /cd。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/ui/git-sidebar) |
| git-gates | Git 工作授权与整洁：追踪用户提示，拦截未授权的 commit/push/merge；检查提交消息（Conventional Commits、issue... |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/git-gates) |
| git-widget | 分支、改动数、领先落后与最近提交标题卡片；本机 process 只读跑 git status 和 git log，工具调用原样返回，需配合 widgets。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/git-widget) |
| gitgraph | /branches 打开本机 git 分支提交线图画板，可勾选多条分支对比。备注：本机只读 git status、for-each-ref、log；面板打开时每 15 秒刷新，Claude 跑含 git 的 Bash 后也会刷新；Bash 工具调用只观察原样返回。 |  | [链接](https://github.com/TCcodemaster/claude-mods/tree/main/gitgraph) |
| glass | 给终端 transcript 换桌面级外观：着色命令、工具树、回合页脚等。 | MIT | [链接](https://github.com/rashedInt32/glass) |
| i18n-pixel | /i18n-pixel 像素风 i18n 检查窗格：本机只读扫描语系 key 是否齐全、占位参数、未知或动态 key、写死的中日韩文字，并注册只读 i18n_report 工具；Edit/Write 只观察原样返回后重扫。 | MIT | [链接](https://github.com/Ponpon55837/i18n-check-mods/tree/main/plugins/i18n-pixel) |
| lean-comments | 限制注释膨胀：Edit/Write 时标记多注释编辑，回合结束时检查 diff 的新注释行；Haiku 审查不值得保留的注释（复述代码或叙述改动）。 |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-comments) |
| lean-docs | 文档值得保留：Haiku 审查 git checkout 中增长的文档（runbook、设置页、叙述）、标记代码重复标识符的文档行、回合结束时检查 dif... |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-docs) |
| lean-scripts | 脚本值得保留：Haiku 审查在 git checkout 中写入或增长的脚本，标记那些你需要时直接打出来更快的脚本。 |  | [链接](https://github.com/bahaospanov/claude-mods/tree/main/lean-scripts) |
| loc-split | 相对 main 的改动行数按代码/注释/测试/文档/生成文件拆分，可展开逐提交表；本机只读 git；条显示时 AbovePrompt 不调 next。 | MIT | [链接](https://github.com/RomanHotsiy/claude-mods/tree/main/loc-split) |
| lockfile-sync | 锁文件同步检查。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/lockfile-sync) |
| md-prompt | 输入时把 prompt 框画成 Markdown（代码块高亮等，不改原文）。 | MIT | [链接](https://github.com/nogu66/md-prompt/tree/main/plugins/md-prompt) |
| mdview | 侧栏渲染对话里的 Markdown，可点选让 Claude 改。 |  | [链接](https://github.com/xuanji86/claude-mdview) |
| mission-control | 工具调用时间线：输入/输出/状态与子代理泳道；只观察。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/mission-control) |
| multirepo-diff-mod | /multi-diff 面板：浏览当前文件夹下每个 git 仓库（含 worktree）的未提交改动，可切换对比 HEAD、暂存区、分支相对基线或本会话改动。备注：本机 git，只读（status、diff、rev-parse、worktree list 等）；Edit/Write 类工具运行前把原文件复制到本机 /tmp/multirepo-diff-mod 供本会话对比，不改工具参数。 | MIT | [链接](https://github.com/nvsravank/multirepo-diff-mod) |
| open-in-vscode | 仅桌面版：把回复里指向本地文件的链接改成可点链接，点击后用 VS Code 打开到对应行。有可点的文件链接时 AssistantMessage 不调用 next 而用 Markdown 自绘（只改显示，不改会话内容），否则原样 next；点击时本机运行仓库里的 scripts/open-in-vscode.sh（调 code CLI，Remote-SSH 下走 VS Code 的 IPC socket）。可选：手动运行 scripts/install-vscode-extension.sh 从仓库源码打包安装 Claude Open Bridge 扩展，它只在本机 unix socket 上监听，用于 Markdown 预览定位。不联网。 | MIT | [链接](https://github.com/gggg5151/claude-desktop-links-to-vscode-mod) |
| proc-registry | /procs 面板登记本会话后台 Bash 与子代理；只观察，不改写工具。 | MIT | [链接](https://github.com/Chronosauros/claude-mods/tree/main/plugins/proc-registry) |
| query-table | 把 BigQuery MCP 和 bq query / dbt show 的结果画成对齐、上色的表格；只改显示，tool.call 只记录 SQL 后原样 next，不改命令。 |  | [链接](https://github.com/michelr/query-table) |
| repo-pulse | 显示仓库活动脉搏，仅本地 git status 查询。 | MIT | [链接](https://github.com/5d0tal1gat0r/repo-pulse) |
| session-activity | 侧栏 ledger 记录本会话外泄动作，等待中工作显示在 spinner；execute_sql 写操作可询问后 deny。备注：只 deny，不改写。 | MIT | [链接](https://github.com/bennewton999/claude-code-mods/tree/main/session-activity) |
| skill-audit | 记录技能调用与文件改动的审计时间线窗格，/skill-audit-pane 开关。本机 process：自带 shell 钩子记录技能名称、调用参数与变更文件路径，不写入 stdout，追加到本机 ~/.claude/skill-audit/<会话>.ndjson，窗格读取同一本机日志。不改写工具或提示，不外发。 | MIT | [链接](https://github.com/DepickereSven/skill-audit) |
| skill-session-mods | 按本地 SKILL.md 元数据给 /skill 会话命名与上色（只读本地技能文件）。 | MIT | [链接](https://github.com/aksh1618/claude-mods/tree/main/skill-session-mods) |
| shiplog | 跨会话记录成功的 gh pr create/merge、gh release create 和部署命令；/shipped [天数] 汇总并起草 X 帖子。备注：只观察 Claude 跑的 Bash 命令，不自己运行 gh，工具结果原样返回；每记一条弹提示；记录存在插件本地存储（最多 1000 条，含命令前 200 字和输出前 3 行）；只有运行 /shipped 时才用 $.model.complete（sonnet），发送这段时间每条记录的日期、文件夹名、类型和输出（或命令），草稿只显示不发布。 |  | [链接](https://github.com/codywilliamson/claude-mods/tree/main/shiplog) |
| skins | 给 transcript 换肤：主题化工具行、回复边栏与 spinner 文案；桌面端把表格/代码/diff/shell 画成动画卡片。 | MIT | [链接](https://github.com/hellosverre/claude-skins) |
| spx-chart | 在侧栏查看 PHP SPX 性能火焰图（需 php-spx-mcp）。 |  | [链接](https://github.com/zviryatko/claude-spx) |
| statusbar | 状态栏显示当前 git 分支与仓库状态，仅本地 git rev-parse 查询。 | MIT | [链接](https://github.com/sgmonda/statusbar) |
| test-progress | 后台测试进度窗格（backend/frontend）；/test-progress 查询或启动已配置的本机测试命令；AbovePrompt 先调 next 再叠加一行摘要。备注：本机 process（bash/PowerShell 收集器可跑本机测试）。 | MIT | [链接](https://github.com/fabiopbarbieri/claude-test-progress) |
| tool-heatmap | 窗格统计每个工具的调用与失败次数；工具调用只观察原样返回。备注：会话开始自动打开窗格。 |  | [链接](https://github.com/vincentlauriat/ModsTools/tree/main/mods/tool-heatmap) |
| tool-meter | 提示框上方显示本会话各工具调用次数的条形图，并在状态栏显示最近工具与总次数；只计数、不改写工具调用，显示时不调 next。 |  | [链接](https://github.com/VerbodhDev/tool-meter) |
| tools-usage | 侧边窗格统计本会话各工具（内置、MCP、技能、子代理、插件、hook）的调用次数与 token 估算；只观察原样返回。备注：会话开始自动打开窗格。 |  | [链接](https://github.com/Fazzani/claude-mods/tree/main/plugins/tools-usage) |
| touch-map | 文件活动热力图：把 Claude 本会话读过、写过的文件画成文件树热力图，按访问频率着色。 | MIT | [链接](https://github.com/y-hirakaw/claude-code-mods/tree/main/touch-map) |
| transit-map | 把 git 历史画成地铁图，分支是线，提交是站。 | MIT | [链接](https://github.com/ccdwyer/transit-map) |
| telescreen | 读本机 .claude/flywheel/LEARNINGS.md，读写到被引用的文件时在提示框上方显示对应经验条目，/telescreen 看统计。只观察。备注：显示时 AbovePrompt 会盖住别的行（可点 Hide）。 | MIT | [链接](https://github.com/arazvan-ec/xmarks/tree/main/mods/telescreen) |
| workbench | 工作台：状态带 + Now/Changes/Preview/Artifacts/Code Map/Usage；只观察。备注：本机 git 与启动已安装的 Chrome/Chromium headless 截本地屏，不下载浏览器。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/workbench) |
| universal-audit-log | 把 tool/prompt/turn 等事件记成本地 JSONL 审计日志（含拒绝）。备注：只写本地文件，不外传。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/observability/universal-audit-log) |
| git-graph | 可折叠 Git 提交图面板（/git-graph）。备注：本机 git。 |  | [链接](https://github.com/nemokoala/claude-mods/tree/main/plugins/git-graph) |
| vhs | /vhs 回放本会话每次 Edit/Write 的本地录像；可 rewind 写回文件。备注：本机读/写文件。 | MIT | [链接](https://github.com/saksham10arora-dotcom/claude-mods/tree/main/plugins/vhs) |
| bg-task-band | 提示框上方后台 Bash/Monitor/Agent 任务条。备注：本机 process（find/tail）；AbovePrompt 显示时可不调 next。 | MIT | [链接](https://github.com/ipartington/claude-mods/tree/main/bg-task-band) |
| git-diff-timeline | 提示框上方的 git 提交时间线：点提交看 diff、点两个比较，分支标签页比较两个分支（/gitdiff）；只在本机运行 git log、git diff 等只读 git 命令。当默认带状显示时（git 就绪或错误），AbovePrompt 返回自己的条带不调用 next，会覆盖其他 mod 的行。 |  | [链接](https://github.com/liawzishen/git-diff-timeline) |
| git-ops | /git 在提示框上方显示可点的 git 面板：分支按钮带筛选、切换前确认，pull、push、fetch、全部暂存和提交，也可用文本子命令。备注：本机 git（$.process.run 参数数组），只在你点按钮或输入子命令时运行，不提供强推、reset、rebase；面板显示时 AbovePrompt 仍调 next。 |  | [链接](https://github.com/nogu66/claude-code/tree/main/git-ops) |
| wxmp-preview | 在侧边面板预览微信小程序 / uni-app 页面，Edit/Write 原样 next 后自动刷新；本机 process：node 桥接脚本、可自动 npm run 启动项目 dev server、无头 Chrome 截图、微信开发者工具 CLI，只连 localhost；桥接依赖需自行 npm 安装。 | Apache-2.0 | [链接](https://github.com/GrubbyLee/claude_wechat_view_mod) |
| sources | 侧栏列出本会话 Claude 读过的文件并按来源分组，可开“只读项目文件夹”锁（/sources allow 放行目录）。备注：Read/Grep/Glob 的 tool.call 只放行或 deny，不改参数；不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/sources) |
| outputs | 侧栏列出本会话新建或改过的文件（新的在前），点一下用系统程序打开或复制路径。备注：只扫描项目目录，打开时本机调用 open/xdg-open/start；tool.call 原样放行；不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/outputs) |
| bdt-status | 提示框上方显示当前分支的 PR、构建状态和它关闭的 issue（可点链接）。备注：需本机 PATH 上有 bmsuisse/devtools 的 bdt CLI，每 30 秒及每轮结束调用 bdt pr info --json；AbovePrompt 先调 next 再追加一行；仓库无许可证文件。 |  | [链接](https://github.com/bmsuisse/skills/tree/main/mods/bdt-status) |
| aichemist-pr-review-pane | 只读面板显示当前 PR 的 Copilot 审查状态、CI 与未解决评论线程。备注：用本机已登录的 gh 读 GitHub PR 数据（不发送会话内容）；「Run review loop」按钮只在你点时以你的身份发一句固定提示，需配合 AIchemist 的 pr-review-loop skill。 | MIT | [链接](https://github.com/Anras573/AIchemist/tree/main/mods/pr-review-pane) |
| git-diff | 提示框上方显示未提交改动：文件数、增删行数和 GitHub 式色块条，右侧显示分支；/git-diff 或 + 按钮打开面板按列表/树看每个文件。备注：本机只读调用 git diff/ls-files/branch；tool.call 只在 Edit/Write 后刷新统计，原样返回。 |  | [链接](https://github.com/cjmellor/mella-marketplace/tree/main/plugins/git-diff) |
| ailang-lens | 编辑 .ail 文件后自动打开面板，显示该 AILANG 模块的函数、类型、副作用和类型错误；/ail-lens 可手动分析某个文件。备注：本机运行 `ailang iface` / `ailang check`；tool.call 只在 Edit/Write/Bash 后刷新，原样返回，不把结果加进模型上下文。 | MIT | [链接](https://github.com/sunholo-data/ailang_bootstrap/tree/stable/plugins/ailang-lens) |
| prepush-gate | Claude 执行 git push 或 gh pr create/merge 前，先在本机跑 gofmt、make lint、make check-file-sizes（仓库有对应目标才跑），失败就拒绝这次推送并给出输出；启动环境设 AILANG_SKIP_PREPUSH=1 可跳过。备注：只 deny，不改写命令；会执行当前仓库自己的 Makefile 目标。 | MIT | [链接](https://github.com/sunholo-data/ailang_bootstrap/tree/stable/plugins/prepush-gate) |
| inline-review | /inline-review <文件> 或 /inline-diff 在面板里显示文件或 diff，可逐行写评论；注册 show_file、list_comments 两个工具让 Claude 打开文件、读取你的评论。备注：本机只读运行 git diff/status；你的评论只在 Claude 调用 list_comments 时作为该工具结果返回，不另外注入上下文。 | MIT | [链接](https://github.com/elayeek/elayeek-ai/tree/main/inline-review) |
| worktrees | 面板列出本会话涉及的 git worktree（仓库、分支、未提交文件数），会话开始时自动打开并定时刷新；/worktrees 重新打开。备注：从工具调用参数识别路径后本机只读运行 git；tool.call 原样返回。 |  | [链接](https://github.com/mirakui/dotfiles/tree/main/claude/mods/worktrees) |
| review-watch | 提示框上方为每个进行中的代码审查（Codex `codex review` 或审查类子代理）显示一行：模型、审查对象、用时、最新输出，结束时弹 toast。备注：只观察，tool.call 原样执行；本机读取 Codex 输出和 ~/.codex 配置里的模型名；纯本机 UI。 | MIT | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/review-watch) |
| ci-watch | Claude 推送、开 PR 或推 tag 后，在提示框上方显示对应 GitHub Actions 运行的进度和通过/失败。备注：本机运行 gh/git 只读查询，需已登录 gh；prompt.submit 只清除已结束的条目，不改写提示；tool.call 原样返回。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/ci-watch) |
| promote-lights | 有打开中的 promote PR（base 为 main、head 为 dev 或 PROMOTE_HEAD，或带 promote 标签）时在提示框上方显示 CI 状态灯，/lights 查看详情。备注：本机运行 gh 只读查询，需已登录 gh；纯本机 UI。 | MIT | [链接](https://github.com/yonatangross/orchestkit/tree/main/mods/promote-lights) |
| cc-daniel | 状态行显示 git 分支和改动数，提示框上方一排额度/上下文进度条，/graph 打开 git 提交图面板（会话开始时自动打开）。备注：本机只读运行 git；纯本机 UI。 |  | [链接](https://github.com/dsanchezp18/ai-configs-daniel/tree/main/mods/cc-daniel) |
| ci-pipeline | 面板显示当前分支在 CI/CD 流水线中的位置：本地开发、PR、检查、合并、预发/生产部署和冒烟测试；/pipeline 可钉住某个 PR。备注：本机只读运行 git 和 gh pr view/gh run（需已登录 gh）；可在插件配置里改部署/冒烟 job 的匹配规则。 | MIT | [链接](https://github.com/alamine42/claude-mods/tree/main/plugins/ci-pipeline) |
| xcode-mods | Xcode 集成：构建/运行/测试面板、scheme 和目标设备条、通知，以及通过无头 Xcode MCP 渲染 SwiftUI 预览。备注：仅 macOS，需 Xcode MCP；tool.call 原样返回；面板里「Fix with Claude / Ask Claude」按钮会以你的身份提交一条包含构建错误、失败测试或控制台日志的提示（你按才会）。 | MIT | [链接](https://github.com/artemnovichkov/xcode-mods/tree/main/mods/xcode-mods) |
| xcode-status | 仅在 Xcode 项目里：一行显示最近一次构建/测试结果和已启动的模拟器，标出 0 个测试的运行；已有 xcodebuild 在跑时 deny 第二个。备注：只 deny，不改写命令；本机运行 pgrep、xcrun simctl 只读查询；prompt.submit 只检测项目，不改写提示。 |  | [链接](https://github.com/narrowstacks/claude-code-mods/tree/master/xcode-status) |
| pr-view | 面板列出项目根仓库打开中的 PR 标题，点一个在浏览器中打开。备注：本机运行 gh pr list（需已登录 gh），用 open 打开链接（macOS）。 |  | [链接](https://github.com/ushironoko/dotfiles/tree/main/claude/.claude/skills/pr-view) |
| followthrough-band | 提示框上方显示本仓库到期的 followthrough 跟进检查（Run / Snooze / Close）；会话里部署/发布后若没登记检查会提醒。备注：需安装 followthrough CLI；本机运行 followthrough 固定子命令；tool.call 原样返回；按「Run」或「Register checks」会以你的身份提交一条提示（你按才会）。 | MIT | [链接](https://github.com/BayramAnnakov/followthrough/tree/main/mod) |
| mapa-calor | 项目文件夹热力图：每个文件夹有多少文件、占多少空间，带彩色条（/mapa、/mapa bytes）。备注：只用 fs.list 列文件，不读内容；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/mapa-calor) |
| replay-edicoes | 回放本会话的编辑：逐步查看每次 Edit/Write 的 diff，前后翻页并可复制（/replay）。备注：只读会话消息，纯本机 UI；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/replay-edicoes) |
| where-were-we | 给 transcript 里每条你的提示打上时间戳，页脚加上/下跳转；/where-were-we 列最近提示、last 回顾本项目上一个会话；新会话开头弹一条回顾提示（可关）。备注：session.append 只读不改；本机 grep 读当前 transcript 和 Claude Code 的提示历史；纯本机。 | MIT | [链接](https://github.com/scarrillo/agent-plugins/tree/main/where-were-we) |
| session-tracker | 侧栏列出本机所有打开的 Claude Code 会话，需要你处理的排最前，带提示音。备注：本机 ps/grep/tail 读会话文件；可在面板里给其它会话发消息（$.session.send），并在二次确认后 kill -TERM 其它会话进程（只在你点击时）。 | MIT | [链接](https://github.com/fixter-dev/claude-code-session-tracker) |
| watch-loop | 防止空转轮询：同一代理连续第三次执行轮询/等待类 Bash（gh run watch、gh pr checks、vercel logs、until/while 循环、sleep ≥10 秒）且中间没有任何 Edit/Write 时拒绝，并弹提示。备注：只 deny 不改写命令；prompt.submit 只用来清零计数，不改写提示；纯本机。 |  | [链接](https://github.com/howells/howells-plugins/tree/main/mods/watch-loop) |
| tool-radar | 工具调用实时面板：每次调用的状态、参数预览、耗时和失败/被拒原因，/radar 打开，/radar summary 看汇总和最慢的调用。备注：tool.call 只计时观察、原样传递；数据只在内存，不落盘；纯本机，不联网。 | MIT | [链接](https://github.com/Singh-AP/awesome-claude-mods/tree/main/mods/awareness/tool-radar) |
| git-pulse | 状态栏显示当前分支、和上游的领先/落后、改动数；切分支和本回合新提交时弹提示；/git-pulse 看分支、最近提交和 stash 一览。备注：只在本机跑只读 git 命令（status --porcelain、rev-list、log、stash list），不 fetch、不改仓库；tool.call 原样传递；不联网。 | MIT | [链接](https://github.com/Singh-AP/awesome-claude-mods/tree/main/mods/awareness/git-pulse) |

### 子代理管理 Subagent Management

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| agents-view | 侧栏列出本会话子代理状态，点选查看 prompt/工具结果。纯 UI。 |  | [链接](https://github.com/ushironoko/dotfiles/tree/main/claude/.claude/skills/agents-view) |
| agent-radar | 每个运行中子代理一行实时状态。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/agent-radar) |
| agent-narrator | 窗格白话叙述每步工具与节省时间；可选 haiku 润色（$.model.complete）。 | MIT | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/agent-narrator) |
| agent-router | 代理路由器，管理子代理调用。 |  | [链接](https://github.com/alexandernicholson/agent-router/tree/main/agent-router) |
| agent-tracker | /agent-tracker 窗格列出本会话启动的子代理及运行状态；只观察。 |  | [链接](https://github.com/vincentlauriat/ModsTools/tree/main/mods/agent-tracker) |
| agent-watch | 子代理侧栏：在窗格里列出活跃子代理、状态与简报，点击可查看 transcript。 | MIT | [链接](https://github.com/AndreasOA/claude-code-mods/tree/main/plugins/agent-watch) |
| agentpane | 侧栏列出本会话子代理、各自在做什么和 token 花费，点开看对话；只观察 tool.call/agent.spawn/turn.step 且都先调 next 不改写；Stop 按钮需确认后调用 TaskStop 停掉该子代理；面板不在屏幕上时用状态行显示；$.ui.status(undefined) 在首次同步、面板打开或状态行关闭时都会运行，而非仅无批次时，会清除其他 mod 的状态。 | MIT | [链接](https://github.com/xuanji86/claude-agentpane) |
| claude-council | 并行运行多个编码代理，可并排查看。 |  | [链接](https://github.com/hex/claude-council) |
| council | 代理协商决策。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/council) |
| crew | 子代理像素小队侧栏：模型/effort/上下文/费用与任务依赖；/crew。 |  | [链接](https://github.com/harshitmywork17/claude-mods/tree/main/plugins/crew) |
| fable-pin | 每个子代理运行你选的模型，不是提示要的那个：在 agent.spawn 时将 model 改写为 fable（除非是 fork 继承父级），/fable-... |  | [链接](https://github.com/karanb192/claude-code-mods/tree/main/plugins/fable-pin) |
| flightdeck | 只读观测面板，集中看权限裁决与子代理进度。 |  | [链接](https://github.com/scasella/claude-flightdeck) |
| multi-core | 把 ChatGPT/Cursor/Zen 等接入 /model（需 claude-multi launcher）。 |  | [链接](https://github.com/greenpolo/cc-multi-cli-plugin/tree/main/plugins/multi-core) |
| plan-progress | 计划进度条 + 子代理条带。 |  | [链接](https://github.com/zycck/claude-mods/tree/main/plugins/plan-progress) |
| prompt-posse | 主代理和每个子代理化身像素小人在提示框上方来回走动，速度随输出量变化，可显示子代理任务描述图例；只改显示，/posse 开关，显示时不调 next。 | MIT | [链接](https://github.com/RyanEmslie/prompt-posse) |
| subagent-ledger | 子代理账本。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/subagent-ledger) |
| subagents-monitor | 侧边窗格列出本会话子代理的状态、耗时、模型、effort 和估算费用；工具调用只观察原样返回。备注：会话开始自动打开窗格，每秒刷新；无 subagent 时 $.ui.status(undefined) 会清掉其他 mod 的状态行。 |  | [链接](https://github.com/Fazzani/claude-mods/tree/main/plugins/subagents-monitor) |
| swarm | 子代理/团队任务控制室窗格。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/swarm) |
| maestro-lanes | 配合 Maestro，每 2 秒读本机 /tmp/maestro-lanes 下的 lane 输出文件，在提示框上方显示各外部 lane 的状态与耗时。只观察。备注：有运行项时 AbovePrompt 会盖住别的行。 | MIT | [链接](https://github.com/ricardosuman/maestro/tree/main/mods/lanes) |
| agent-party | 把运行中的子代理画成 16×16 像素英雄放在提示框上方，显示任务、当前动作、耗时和上下文，可选语音播报。备注：本机 process（Linux 下用 spd-say 播报）；只观察 agent.spawn 与工具调用、原样放行。 | MIT | [链接](https://github.com/ytruong11201/claude-code-mods/tree/main/plugins/agent-party) |
| agent-aquarium | /aquarium 在窗格里把会话画成鱼缸（kitty 图形，不支持时用半块字符）：主循环是大鱼，子代理是出生又游走的小鱼，工具调用是鱼的动作，水位跟随上下文占用。备注：只观察 tool.call、agent.spawn，先调 next 原样放行；只读插件自带图片素材，不跑进程、不联网。 |  | [链接](https://github.com/nogu66/claude-code/tree/main/agent-aquarium) |
| agent-graph | 桌面端窗格，把正在运行的子代理画成从左到右的关系图（模型、步数、费用估计）；/agent-graph 打开，只观察、工具调用原样放行。 |  | [链接](https://github.com/theishandubey/claude-mods/tree/main/plugins/agent-graph) |
| workflow-watch | 实时显示正在运行的 Workflow 各阶段（模型、effort、token、当前工具），带面板、提示框上方横条与状态行，/workflow-watch 输出文本报告。备注：只读本机 ~/.claude/projects 下本会话的 workflow journal 与子代理 transcript；不联网。 | MIT | [链接](https://github.com/alonbaron/claude-skills/tree/main/mods/workflow-watch) |
| session-board | 提示框上方一个小卡片，列出本机其他正在运行的 Claude 会话及其状态（运行中/完成/空闲），每 5 秒刷新（仅终端，且有其他会话时才出现）。备注：每 5 秒在本机调用 ListAgents 工具读会话列表；先画自己再调 next 把其他 mod 放下方；纯本机 UI。 | MIT | [链接](https://github.com/oualid0/claude-mods/tree/main/plugins/session-board) |
| fleet | 面板按 GitHub 看板的 epic/工单分组显示本会话的子代理：工单状态、epic 完成度、各工单下的代理。备注：通过本机 gh api 只读 GET（需已登录 gh，需配置看板）；只在本机从子代理描述/提示开头匹配工单号；tool.call 原样返回。 | MIT | [链接](https://github.com/neonelemental/claude-code-board-mods/tree/main/fleet) |
| browser-lanes | 显示本会话的 Playwright 浏览器及当前占用者；子代理要用浏览器时排队等前一个用完（等超过 5 分钟则拒绝）；/browser clean 关掉残留浏览器。备注：只等待/deny，不改写工具调用；/browser clean 会结束本会话残留的浏览器进程（你执行才会）。 | MIT | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/browser-lanes) |
| agent-jobs | /jobs 面板列出运行中的子代理和后台 shell（用时、Stop 按钮），后台任务结束时弹 toast。备注：tool.call 原样返回；prompt.submit/session.receive 只读取任务通知，不改写。 |  | [链接](https://github.com/narrowstacks/claude-code-mods/tree/master/agent-jobs) |
| activity | 实时面板显示 Claude 正在做什么：运行中的工具（真实命令和计时）、等你批准的调用、子代理和当前待办计划；/activity 打开。备注：tool.call 原样返回，只用 $.tool.check 读取是否需要批准；纯本机 UI。 | MIT | [链接](https://github.com/mishgoldenberg/claude-mods/tree/main/plugins/activity) |
| agents-panel | /agents-panel 打开侧栏，列出本项目、用户和插件定义的子代理（描述、模型、token），每个带 ▶ run 按钮。备注：读本机 .claude/agents/*.md；只有你点 ▶ run 才会用 $.agent.spawn 启动该子代理。 | | [链接](https://github.com/Boom-Vitt/claude-mods-boombignose/tree/main/agents-panel) |
| vnext-session-record | 记录本会话启动的子代理（类型、模型、状态、简短描述）、每次请求的模型和 token 用量，并在 /vnext 面板里显示。备注：所有钩子只观察、原样传递；不保存提示词正文，只存子代理描述前 120 字；写到项目 .vnext/host/<会话id>.jsonl（项目没有 .vnext 时写 ~/.vnext/host/），单文件上限 3 MB；纯本机，不联网；为 vNext workforce 设计，单独用也能看子代理面板。 | MIT | [链接](https://github.com/RazAndAlex/vnext-workforce/tree/main/plugins/vnext-session-record) |

### 通知提醒 Notifications & Alerts

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| atelier-bell | 告知 atelier 完成时机：flux7-studio 渲染进度显示为 toast 和状态行（studio: rendering、studio: las... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/atelier-bell) |
| avatar7 | 机器脸随工具调用作评论，可选声线（SHODAN、HAL、GLaDOS 风格实验室 AI、Ada、duck7、Pod 042、Kaneda、Commis），... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/avatar7) |
| baton-notify | 回合结束、提问、等待计划或权限确认时发 macOS 通知（可选提示音和语音），标出文件夹名和最近一次提问的前 40 字。备注：本机 process（osascript、afplay）。 | MIT | [链接](https://github.com/Humpens/claude-mods/tree/main/baton-notify) |
| cc-notify-mod | 任务完成、Bash 连续失败、AskUserQuestion 时发 macOS 通知；本机 process（osascript），通知内容含回复摘要、报错或提问文字，只在本机显示；仅 macOS。许可证 Apache-2.0。 | Apache-2.0 | [链接](https://github.com/kukaka/cc-mods/tree/main/cc-notify-mod) |
| cc-pr-tracker | 在提示框上方盯着 GitHub PR 的合并状态、评审与必需检查，有变化时 toast。 | MIT | [链接](https://github.com/sezaakgun/cc-pr-tracker) |
| commit-cadence | 提交节奏提醒。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/commit-cadence) |
| commit-drift | 状态行未提交文件数与距上次提交时间，久未提交会提醒。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/commit-drift) |
| desk-notify | 桌面通知提醒。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/desk-notify) |
| ding | 长回合结束 toast+可选音效提醒。 |  | [链接](https://github.com/lucenity0/claude-code-mods/tree/main/ding) |
| done-blink | 主回合结束后闪烁 iTerm2 标签页，直到再次输入或超时。仅本机 tty/本地 shell。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/done-blink) |
| error-poke | 错误提醒助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/error-poke) |
| gfm-render | 在 transcript 里渲染 GFM：alerts、任务列表、删除线与 Mermaid。 | MIT | [链接](https://github.com/briangtn/claude-gfm-render) |
| goodfriend | 生日提醒（仅 macOS）：本机 process 用 osascript 读通讯录生日和「信息」App 的聊天成员与群名（不读消息正文；电话号码和邮箱留在本机，不发给模型）；/seed 会把最多 80 个联系人姓名和群名通过 $.model.complete 发给模型挑出 10 个重要的人；改写 Spinner 文案时仍调 next，生日卡片显示时 AbovePrompt 不调 next；点「Text」用 open sms: 打开信息并预填祝福，由你自己按发送；注册 set_birthday/list_birthdays 两个工具。 | MIT | [链接](https://github.com/nicodunks/goodfriend) |
| mesh7-pane | 从 localhost:9090 每 1.5 秒轮询 mesh7 决策：每次调用的 ALLOW/DENY/HUMAN 及规则参数、待批准请求、紧急停止横幅... | MIT | [链接](https://github.com/KTCrisis/flux7-mods/tree/main/mesh7-pane) |
| notice-board | 同仓库各会话共享通知板。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/notice-board) |
| notify | 桌面通知：Claude 回合完成或等待决策时发系统原生通知，后台时召回焦点。 | MIT | [链接](https://github.com/XD3an/cc-notify) |
| notify-on-finish | 长回合结束后桌面通知（macOS osascript / Linux notify-send / 否则 toast）。 | MIT | [链接](https://github.com/Justmalhar/awesome-claude-mods/tree/main/mods/notify-on-finish) |
| notify-router | 按规则决定何时提醒（完成、等待你、出错）和发到哪里：macOS 通知（本机 osascript）、提示音、可选 ntfy。备注：**ntfy 默认关闭**，只有填写 ntfy topic 后才 $.http POST 到 ntfy 服务器，内容仅为状态文字（耗时、结束原因、Claude Code 通知文案，最多 200 字）和可关闭的文件夹名，不含对话内容；prompt.submit/tool.call 只用于取消待发提醒，原样 next 不改写；仅 macOS 有桌面通知与提示音。 |  | [链接](https://github.com/pradyb/claude-mods/tree/main/notify-router) |
| nowloading | 显示加载动画与进度提示。 | MIT | [链接](https://github.com/vgnshiyer/nowloading) |
| pomodoro | 番茄钟状态条与配置面板，纯本地计时与提醒。 | MIT | [链接](https://github.com/sneycampos/claude-pomodoro) |
| pomodoro-widget | 番茄钟卡片，本地计时，到点 toast 提醒，需配合 widgets。备注：计时期间每秒刷新，卡片被隐藏也照跑。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/pomodoro-widget) |
| reminder-log | 本地提醒日志窗格。 |  | [链接](https://github.com/schreibse/claude-code-mods/tree/main/reminder-log) |
| streak | 状态行显示连续活跃天数，到 7/30/100/365 天弹提示；记录存本机。备注：连续天数为 0 时 $.ui.status(undefined) 会清掉其他 mod 的状态行。 |  | [链接](https://github.com/vincentlauriat/ModsTools/tree/main/mods/streak) |
| task-poke | 任务提醒助手。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/task-poke) |
| bus-band | 读本机 ~/.agent-team-os（或 AB_HOME）收件箱，在提示框上方列出本会话待处理的 Agent Team OS 消息，紧急消息弹 toast，/bus-band 显隐。只观察。备注：有消息时 AbovePrompt 会盖住别的行。 | MIT | [链接](https://github.com/mariomosca/agent-team-os/tree/main/mods/bus-band) |
| done-sound | 主会话回合结束时播放 macOS 系统提示音（出错用另一种），/sound on/off/test 开关。备注：本机 process（afplay）；仅 macOS。 |  | [链接](https://github.com/myudav4iik/claude-mods/tree/main/done-sound) |
| turn-chime | 长回合结束或 Claude 停下来问你时播放提示音并弹 toast，阈值分钟数可配（默认 3）。备注：prompt.submit 只记时间不改写；Windows 上用本机 PowerShell 播放 mod 自带的 wav；不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/turn-chime) |
| ailang-inbox-band | 提示框上方显示 AILANG 未读消息数和最新标题，新消息到达时弹 toast；/ail-inbox 打开面板可展开阅读和 Ack；可配置监听的收件箱和轮询间隔。备注：本机运行 `ailang messages list/ack`，需装 ailang；消息内容只给人看，不进模型上下文。 | MIT | [链接](https://github.com/sunholo-data/ailang_bootstrap/tree/stable/plugins/ailang-inbox-band) |
| cuelume | 两种提示音：长回合结束时播放「就绪」，有权限请求等你处理时播放「注意」；/cuelume 切换音色或关闭。备注：只播放插件自带的 wav 音频，不改权限决定；纯本机。 | MIT | [链接](https://github.com/danielwh2/cuelume/tree/main/claude-code) |
| inbox-band | 提示框上方显示共享收件箱文件里有几条新报告、几条可能需要你处理。备注：需配合 herdr（只读 ~/.config/herdr/inbox.md 与 inbox.read）；纯本机。 | MIT | [链接](https://github.com/soyakaai-studio/claude-herdr-mods/tree/master/mods/inbox-band) |

### 吉祥物与宠物 Mascots & Pets

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| cc-mod-ferro | 回合超过 20 秒时，提示框上方一只像素诺维奇梗犬 Ferro 在草地上奔跑（偶尔追橙色小球或停下便便），3 分钟后趴下睡觉；仅桌面版显示，纯本地 clock/ui，不改工具、不外传。 |  | [链接](https://github.com/Vatroslav/cc-mod-ferro/tree/main/plugin) |
| clawd | 思考行旁的像素 Clawd 吉祥物，按工具/命令表演动作。 |  | [链接](https://github.com/raresmun/claude-mods/tree/main/plugins/clawd) |
| clawd-actor | 回合进行中在提示框上方让 Clawd 按 spinner 的 -ing 词或正在运行的工具表演场景（26 个场景），只改显示。 | MIT | [链接](https://github.com/BrianHuang813/clawd-actor) |
| clawd-band | 提示框上方像素猫，随思考/编辑/搜索等状态动画；仅 UI。 | MIT | [链接](https://github.com/tomada1114/clawd-band/tree/main/plugins/clawd-band) |
| clawd-factory | /clawd-factory 打开窗格（每次会话开始也会自动打开并弹出"已加载"提示），每次工具调用多一只 Clawd 在对应工位（查阅、编辑、命令、子代理、其他）干活，显示当前工具、回合计时与失败次数。备注：使用 $.model.complete（Haiku，最多每 6 秒一次，只针对主代理 10 秒内的工具调用），把作业类别、工具名和目标（文件路径末两段，或命令、任务描述、搜索模式、URL、查询的首行）发去生成 12 字以内的日文台词。 | MIT | [链接](https://github.com/HayatoKonya/clawd-factory/tree/main/plugins/clawd-factory) |
| clawdgotchi | 电子宠物 Clawd，在侧栏养成与互动。 | MIT | [链接](https://github.com/arthurseredaa/clawdgotchi) |
| code-pet | 像素宠物窗格，随 Claude 活动反应。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/code-pet) |
| coding-pet | 从蛋里孵出的宠物（/pet 打开窗格），随回合、提交、测试、成就成长，可喂养照顾，有日记和成就页；界面为日语。备注：prompt.submit 原样放行，只检测是否说了「谢谢」，不保存提示文字；tool.call 原样放行，只计数（日记只写固定句子，不记命令或文件）；开启聊天能力后经 $.model.complete（Haiku）只发宠物种类、名字、心情和计数，不发代码、路径、命令或提示；$.store 存档，$.audio 播放自带的 wav 音效；不联网。 | MIT | [链接](https://github.com/ytskmt14/coding-pet/tree/main/plugins/coding-pet) |
| desk-pet | 提示框上方/侧栏小宠物，随工具与回合反应；仅 UI，不改工具、不外传。 | MIT | [链接](https://github.com/isr431/desk-pet) |
| dotpet | 输入框上方的像素宠物（待机、工作、完成、睡觉换图）；/dotpet 开关和改大小。备注：AbovePrompt 会先调 next；只用 $.store；附带浏览器里的画图编辑器；画作另见 LICENSE-ART.md。 | MIT | [链接](https://github.com/i-noma-ru/claude-dotpet) |
| familiar | 提示框上方像素伙伴，随会话反应并可手绘；可选 Haiku 吐槽。备注：可选 $.model.complete 与 $.model.fork。 | MIT | [链接](https://github.com/lucenity0/claude-familiar) |
| maomao | 提示框上方 8-bit 毛毛（垂耳兔）随工作状态跑跳；/maomao 收起或叫出。 |  | [链接](https://github.com/jessetsai1024/claude-mods/tree/main/maomao) |
| mize-coworker | 像素 Claude 吉祥物，随 spinner 词表演场景，空闲时在状态行呼吸走动。 | MIT | [链接](https://github.com/TheMizeGuy/clawdagotchi/tree/main/plugins/mize-coworker) |
| mod-ferro | 长回合时提示框上方像素诺福克梗 Ferro 跑过草地，过久会睡着。纯 UI（桌面 Svg）。 |  | [链接](https://github.com/Vatroslav/mod-ferro/tree/main/plugin) |
| muse-pet | 提示框上方像素 Muse：等待时招手/叮咚，长回合结束跳跃，显示上下文与费用；/muse 可从 gadget.mububu.app 拉取自定义形象。备注：可选访问外网拉宠物料 JSON，不上传会话；本机 process（claude --version）。 | MIT | [链接](https://github.com/Soyn/mububu-pet) |
| oyen | 输入框上方的橘猫，对 commit、测试和构建结果做反应；/oyen feed、pet、play。备注：prompt.submit 只记录活跃时间、原样 next；Edit/Write 编辑 todo.md 时前后各读一次本机文件、数勾选；显示时 AbovePrompt 不调 next；$.store 存等级。 | MIT | [链接](https://github.com/zulfikar-ditya/claude-mods-oyen) |
| pet-widget | 像素 Clawd 宠物卡片，随工具成败和上下文占用变换心情并升级；工具调用只观察原样返回，需配合 widgets。备注：开启时每 600 毫秒重绘一次，卡片被隐藏也照跑；升级时弹提示；经验值存在本机，多个会话共享宠物所在会话。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/pet-widget) |
| pixel-buddy | /buddy 打开侧边像素陪伴娃娃窗格（小橘、史莱姆、机器人、幽灵四种形象），用来问和主会话无关的小问题，可复制回答。备注：在窗格按 Enter 时用 $.model.complete（Haiku）发送你的问题和这个侧聊最近 10 条对话，不带主会话内容；每次开会话都会弹一条载入提示；会话全程每 400ms 触发一次界面重绘（窗格关着也一样）；形象选择存本机 $.store；不联网。 | MIT | [链接](https://github.com/monowu/claude-mod-pixel-buddy) |
| pixipet | 像素宠物，观察 Claude 的工作成长；/pet 窗格；tool.call 与 prompt.submit 原样 next；$.store 存状态。 | MIT | [链接](https://github.com/VibeMage/claude-mod-pet) |
| plushie | 提示框上方的毛绒 Clawd，会随工具/上下文做出反应。 | MIT | [链接](https://github.com/xyc/plushie) |
| pocket-familiar | 伴随工作的养成伙伴窗格。 |  | [链接](https://github.com/theonly1me/claude-code-mods/tree/main/plugins/pocket-familiar) |
| quota-pets | 额度假宠扭蛋：每对话抽猫/狗，限额告急讲鬼故事、用完阵亡；context 当肚子（/petdex 肚子）。备注：本机读 session.messages 估算肚子内容。 |  | [链接](https://github.com/Open01277/claude-mods/tree/main/plugins/quota-pets) |
| gopher-spinner | 回合进行时在终端 spinner 旁显示像素地鼠动画；/gopher 打开预览窗格。纯 UI，窄于阈值或非终端时交还默认 spinner，终端够宽时 Spinner render 替换引擎 spinner 且不调用 next。 | MIT | [链接](https://github.com/ripta/coding_agent_standards/tree/main/mods/gopher-spinner) |
| pokemon | 提示框上方像素宝可梦：随回合战斗、升级与组队动画，纯 UI。 |  | [链接](https://github.com/dgokcin/claude-pokemon-mod) |
| ricky-pixel-mod | 像素猫 Ricky：夜空窗格看板 + 提示框上方猫带；只观察会话事件做动画，不改写工具/提示。 | MIT | [链接](https://github.com/muxia23/ricky-pixel-mod) |
| ember | 一团小火苗跟着会话：在转圈行写当前步骤，提示框上方显示轮到谁，轮到你时本机播放提示音（/ember mute 静音，/ember pane 打开窗格）。默认 AbovePrompt 行除非 hasSurvey 不调用 next，会覆盖其他 mod 的行；带状还会显示上一条用户提示。 | MIT | [链接](https://github.com/nickdemari/ember) |
| sidebot | 侧边像素机器人小窗旁路问答（/buddy）。备注：会话开始自动打开小窗；提问时用 $.model.fork 带上主会话全文，prompt 另含侧窗最近约 20 条对话；主会话尚无内容时改用 Haiku $.model.complete，只发人设与侧窗对话；每 400 毫秒重绘（关窗也跑）；/buddy 命令与 pixel-buddy 的 /buddy 冲突。 | MIT | [链接](https://github.com/monowu/claude-mod-sidebot) |
| pixel-pet | 提示框上方的像素宠物随每次工具调用做动作，下方 HP/MP/ST 用量 HUD，子代理显示小跟班；注册 preview_theme/set_theme/get_theme 三个换主题工具，preview_theme 会把 HTML 预览写到本机指定路径；工具调用只观察原样返回，不用网络。 | MIT | [链接](https://github.com/Namenomeaning/pixel-pet/tree/main/plugins/pixel-pet) |
| clawd-dance | 提示框上方的帯里 Clawd 随工作状态跳舞并显示用量，回合结束和提问时可播合成提示音或语音。备注：本机 process（/bin/date 取时区），读本机 ~/.claude/usage-log/pace.json；只观察 prompt.submit 与工具调用、原样放行。 | MIT | [链接](https://github.com/tanuu5/clawd-dance/tree/main/plugins/clawd-dance) |
| goblin-chrome | 提示框上方的哥布林随会话状态换表情、说怪话，按模型档位换边框，带昼夜循环，提问框上方加哥布林脸，可选播放自带音效。备注：PromptHint 改写提示尾巴但仍调 next；读本机 ~/.claude/skills 下的 SKILL.md 判断指定模型、读本机主题配色；工具调用只观察、原样返回，不用网络。 |  | [链接](https://github.com/JasonWarrenUK/goblin-mode/tree/main/marketplace/goblin-chrome) |
| pikachu | 在面板里养一只宝可梦（五条进化线可选），随上下文占用进化，带进度条和曲线。备注：只读上下文用量；不改提示或工具，不联网。 | MIT | [链接](https://github.com/ottho-nocode/claude-mod-pokemon) |
| token-printer | Clawd 在提示框上方开「token 印钞机」，随 Claude 工作强度加速，回复下附 token/费用小票，/brrr 生成梗图，/token-reserve 打开统计面板。备注：Spinner 只改文案后调 next；prompt.edit 只读草稿让 Clawd 眼睛跟光标，原样返回；turn.complete 只在回答下加一行小票；不联网。 | MIT | [链接](https://github.com/BorjaGM1/token-printer) |
| clawd-gotchi | 左下复古 RPG 小宠物：缓存命中和 git commit 喂养它，跑测试失败的套件变成 Boss，测试全过击败得 XP；可配置名字。备注：tool.call 只读 Bash 输出数失败数，原样返回；状态存本机 $.store；界面文案为法语。 |  | [链接](https://github.com/Lunik/gmz-claude-marketplace/tree/master/clawd-gotchi) |
| clawd-buddy | 提示框上方一个 Claude 小吉祥物，旁边显示用量、上下文、缓存、目录和 git 状态；Claude 用 SendUserFile 发图片时在面板显示或用系统查看器打开。备注：本机只读运行 git status；图片转换/打开用 macOS 的 sips/open，临时文件在 /tmp/clawd-buddy；tool.call 原样返回。 | MIT | [链接](https://github.com/prabowosd/clawd-buddy/tree/main/plugins/clawd-buddy) |
| claude-buddy-bridge | 把 Claude Code 的额度、上下文、花费和任务起止写成小文件，给桌宠「Claude娘」读取。备注：需配合 Ancean/claude-musume 桌宠；只写 ~/.claude/buddy-pet/live/<会话id>.json（不含提示词、回答或项目路径）；说明为中文。 | MIT | [链接](https://github.com/Ancean/claude-musume/tree/main/buddy-pet/claude-plugin) |
| nukey | 微波炉 Nukey 站在提示框上方，按 Claude 在读、写代码、思考、搜索等表演动作，回合结束「叮」一声；旁边的控制面板显示上下文和额度用量。备注：只观察事件并原样返回，纯本机 UI。 | MIT | [链接](https://github.com/arifamir/nukey-kit/tree/main/plugins/nukey) |
| martian-base | Martian Base 的火星人站在提示框上方，随 Claude 的动作变换动画，并显示 5 小时和每周用量条。备注：tool.check/tool.call 只观察并原样返回；说明为法语。 |  | [链接](https://github.com/Chaveex/martians-mods-4-claude/tree/main/martian-base) |
| bichinho | 提示框上方的 ASCII 小宠物，会「吃掉」Claude 读、改、新建的文件（/bichinho on 或 off）。备注：只观察 Read/Edit/Write 结果；说明为葡萄牙语。 |  | [链接](https://github.com/inematds/inema-mods/tree/main/mods/bichinho) |
| tamaclaude | 提示框上方的像素宠物：会随会话长大，写文件时蹦跳、测试通过时跳舞、被拒绝或测试失败时生闷气、久不操作就睡觉，上下文快满或额度快用完时会提醒；/tamaclaude 查看、喂食、改名或重置。备注：prompt.submit 只读取提示里有没有夸奖来触发跳舞，原样传递不改写；tool.call 只观察结果；宠物状态存在插件本地 store；可在插件配置里调大小、安静模式和入睡时间。 | MIT | [链接](https://github.com/settivishal/tamaclaude/tree/main/tamaclaude) |
| buddy | 住在提示框上方的 ASCII 小宠物，会对 Claude 的每个动作做反应（工具被拦时紧张、失败时吓一跳、提交和测试通过时开心），随你的工作升级；/buddy 改名、换物种、隐藏。备注：tool.call 只观察结果、原样传递；经验和统计存在插件本地 store；纯本机，不联网。 | MIT | [链接](https://github.com/Singh-AP/awesome-claude-mods/tree/main/mods/fun/buddy) |

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
| md-preview | `/md-preview` 也会打开同一侧栏预览（斜杠或点击 .md 链接）。点击回复里的 .md 文件链接，在侧栏按文档页样式预览（表格、提示块、代码高亮、mermaid 图），文件改动自动重载。备注：本机 process 调已装的 nvim（tree-sitter 高亮）和 mermaid-ascii；回复显示会改写成可点链接（只改显示，不改原文）；只读本机文件，不外传。 | MIT | [链接](https://github.com/abonckus/claude-code-md-preview) |
| file-preview | `/preview <路径>` 或点击回复里的 .md/.json/.yaml 文件链接，在侧栏按文档页样式预览（可搜索，文件改动自动重载）。备注：回复显示会把存在的本机文件改写成可点链接（只改显示，不改原文）；本机 process 调 mermaid-ascii 和你在设置里自配的外部高亮命令；只读本机文件，不外传；与 md-preview 都会改写回复里的文件链接，同时装可能互相覆盖。 | MIT | [链接](https://github.com/abonckus/claude-code-file-preview) |
| md-view | 点击回复里的 Markdown 文件渲染预览。 |  | [链接](https://github.com/scoobynko/claude-code-mods/tree/main/plugins/md-view) |
| music-mod | 通过 osascript 控制 macOS Music.app 播放音乐。 | MIT | [链接](https://github.com/zyx1121/music-mod) |
| paste-peek | 粘贴图片实时像素预览（⌥←/→ 切换，⌥↑ 放大，⌥↓ 侧栏）；需支持图片的终端。 | MIT | [链接](https://github.com/nokiy/claude-code-mods/tree/main/plugins/paste-peek) |
| paste-view | 在提示框上方预览粘贴的图片缩略图与长文本。 | MIT | [链接](https://github.com/Amorfx/claude-paste-view) |
| radio | /radio 在会话里听网络电台，状态行与提示框上方控制。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/radio) |
| shot-view | 收集 Read/工具里的 PNG，/shots 侧栏翻页预览。备注：本机 process（sips/open）。 | MIT | [链接](https://github.com/Bearisbug/cc-mods/tree/main/shot-view) |
| mermaid-inline | 把助手回复里的 mermaid 围栏画进 transcript（图片或盒装 ASCII）；本机 node 跑插件内置 render-svg。fork of claude-mermaid。 | MIT | [链接](https://github.com/Conte777/mermaid-inline/tree/main/mermaid-inline) |
| terminal-browser | 在会话旁嵌入终端浏览器，预览网页/本地 HTML/PR。 | MIT | [链接](https://github.com/zenbu-labs/terminal-browser/tree/main/claude-code-plugin) |
| vitrin | 媒体侧栏：把回复和工具生成的图片、视频、PDF、音频、Markdown 收进窗格预览与对比；仅 macOS，本机 process（node 起本机无头 Chrome，sips、qlmanage、ffmpeg、open），只开本机 127.0.0.1 服务，tool.call 原样 next，只改回复显示。 | MIT | [链接](https://github.com/yasinozmeen/claude-code-mods/tree/main/vitrin) |
| yt-control | 用本机 cliamp 控制 YouTube 播放。缩略图只按视频 id 从 i.ytimg.com 拉取，不上传会话内容。备注：本机 process（需已装 cliamp/yt-dlp）。 | MIT | [链接](https://github.com/Unayung/cc-mods-youtube/tree/main/plugins/yt-control) |
| image-thumbs | 在终端显示缩略图，使用本地 process（macOS sips、mktemp、base64 与临时文件清理）。不改写消息。 |  | [链接](https://github.com/ohade/claude-mods/tree/main/image-thumbs) |
| lofi | 会话配乐：idle/focus/flow 与测试通过/失败提示音；/lofi on。备注：本机音频（插件内 mp3）。 | MIT | [链接](https://github.com/saksham10arora-dotcom/claude-mods/tree/main/plugins/lofi) |
| show-me | /show-me <问题> 让 Claude 用 mermaid 图回答，并在面板里把回答中的 mermaid 图渲染成图片；不带参数则打开面板。备注：带问题时会以你的身份提交该问题并附加「用 mermaid 图回答」说明（你执行命令才会）；需本机 mmdc 和支持 kitty 图形协议的终端；临时文件在 $TMPDIR/show-me，旧目录会被清理。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/show-me) |
| now-playing | 提示框上方一行显示 Spotify 正在播放的歌曲、进度和当前歌词，带上一首/暂停/下一首按钮，/music 也能控制（仅 macOS）。备注：本机 osascript 控制 Spotify；经 $.http 向 lrclib.net 查歌词，只发送歌名、歌手等曲目信息，不发送会话内容。 | MIT | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/now-playing) |
| clauisc | 提示框上方的 Apple Music 正在播放条：像素封面、歌名、歌手和跟着节拍晃动的 Claude 玩偶。备注：仅 macOS；每 2 秒用本机 osascript 只读查询正在播放信息（首次会弹 macOS 授权）；其它系统只显示无法读取。 | MIT | [链接](https://github.com/mireabot/Clauisc/tree/main/plugins/clauisc) |

### 任务与项目 Task & Project

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| backlog-band | 提示框上方显示 BACKLOG.md 的 Now 项。 |  | [链接](https://github.com/sivori/claude-mods/tree/main/plugins/backlog-band) |
| backlog-pane | 侧栏看 git 状态和 Backlog.md 任务。 | MIT | [链接](https://github.com/LegendSilvia/claude-code-mods/tree/main/plugins/backlog-pane) |
| bg-tasks | 后台任务管理器。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bg-tasks) |
| bw-peek | Beadwork 工单侧栏：/bw 与回复下 id 按钮；备注：本机 process 跑 bw，不上网。 | MIT | [链接](https://github.com/iautom8things/bw-peek) |
| cc-mod-park | /park 记下当前会话（本机 ~/.local/state/cc-mod-park/parked.json）并退出；同目录新会话在提示框上方给出按钮一键接回（本机 /resume、/model、/effort），接回后若默认 model/effort 被改动会写回本机 settings.json；读本机 transcript 取首条提示作标题，本机 git 读分支，不联网。 | MIT | [链接](https://github.com/GGGODLIN/cc-mod-park) |
| check-ledger | 记录跑过哪些检查、之后又有哪些编辑（/evidence）。 |  | [链接](https://github.com/LeeHigma0201/claude-code-mods/tree/main/mods/check-ledger) |
| cockpit | 计划/todo 进度条，并按 quick/normal/hard 路由模型与 effort。 |  | [链接](https://github.com/Brxerq/claude-cockpit/tree/main/plugins/cockpit) |
| deadlines | 状态行的截止日期倒计时，/ddl 增删。 |  | [链接](https://github.com/richardcsuwandi/claude-mods/tree/main/plugins/deadlines) |
| departure-board | 翻牌式出发板，把当前任务翻成车站到发显示。 | MIT | [链接](https://github.com/ccdwyer/departure-board) |
| dev-dash | 开发者仪表板窗格，集中显示会话状态与项目信息。 |  | [链接](https://github.com/RanaRauff/claude-dev-dashboard/tree/main/plugins/dev-dash) |
| gsd-status-mod | 面向 GSD 项目：在提示框上方显示阶段/进度与 STATE.md 漂移警告，并把下一步动作放进提示行。 | MIT | [链接](https://github.com/helenkwok/gsd-status-mod) |
| human-in-the-loop | 把只有用户能做的事挂在 My tasks 窗格里，完成后再回给 Claude。 | MIT | [链接](https://github.com/tzafrir/human-in-the-loop) |
| ix-flow | 在提示框上方显示 ix-flow 工作流的阶段进度条（`/flow-status RUN_ID [绝对状态目录]\|demo\|off`）。备注：需自行 `npm i -g @agent-ix/ix-flow`，插件不下载 CLI；选中运行后每 2 秒，以及每轮结束和 Claude 每次用 Bash 调用 ix-flow 后，在本机执行 `ix-flow progress <运行ID> --json [--state-dir 目录]`（超时 3 秒，可用环境变量 `IX_FLOW_MOD_CLI` 换成别的可执行文件路径），只传运行 ID 和状态目录，不传会话内容；会读取 Claude 运行 ix-flow 的 Bash 输出来自动选中运行，工具结果原样返回，但会先等一次查询（最多约 3 秒）；AbovePrompt 调用 next，不遮挡其他 mod；附带 `/ix-flow`、`/ix-flow-create` 命令和两个技能，会让 Claude 用 Bash 运行 ix-flow 创建和推进工作流，并在 `~/.ix/flows` 写状态文件，人工审批关卡需用户确认；mod 本身不联网。 | MIT | [链接](https://github.com/agent-ix/ix-flow) |
| loose-ends | 追踪会话中未完成的待办事项，回合结束用 $.model.complete 总结剩余任务。 | MIT | [链接](https://github.com/fernandomoraes/loose-ends) |
| party | 本机多会话面板；别的会话碰过同一 PR 时 ask，不改写命令。/broadcast 把用户刚输入的文字发给本机另一个会话。备注：本机 git。 | MIT | [链接](https://github.com/pourya7/claude-code-mods/tree/main/party) |
| recap-plus | 在提示框上方显示本会话的目的与现状，/recap-plus 打开窗格查看已完成、决定、待你确认和下一步。备注：会读本地会话记录；每轮主回答结束后（以及打开已有会话时）调用 $.model.complete（Haiku），发送上一版摘要、本轮请求（≤800 字）与回答（≤3000 字）、本轮问答、工具活动（Bash 命令或描述首行、编辑的文件路径、URL、搜索词、子代理描述、MCP 工具名），首次还会带上压缩摘要（≤2000 字）和前 20 条请求首行；AbovePrompt 条有内容时不调用 next，可能盖住其他 mod 的内容；不联网。 | MIT | [链接](https://github.com/skanehira/claude-recap-plus) |
| standup | 跨会话记录你的提问与改动文件，/standup 用模型写成日报摘要。 | MIT | [链接](https://github.com/claudemodz/mods/tree/main/plugins/standup) |
| sticky-todos | 待办侧栏；观察 TodoWrite/Task*，不改写工具。 | MIT | [链接](https://github.com/paweechinagarn/claude-code-mods/tree/main/sticky-todos) |
| sudus | 本地运行 sudus wake（或插件自带 node bin）在提示框上方或窗格显示项目 verdict；不调用模型。 | MIT | [链接](https://github.com/eas4ai/sudus) |
| taskcut | turn.step mod。 | MIT | [链接](https://github.com/wasd96040501/taskcut) |
| task-eta | 长任务步骤与剩余时间。超时用 $.model.fork，提示里带工具轨迹、用户新消息和回复片段。备注：使用 $.model.fork。 | MIT | [链接](https://github.com/Bearisbug/cc-mods/tree/main/task-eta) |
| task-list | 把项目 TASKS.md 显示成侧边任务面板，/task 添加任务，注册 tasks 工具让 Claude 读改清单；其他工具调用原样 next；粘贴按钮在本机跑 pbpaste（本机 process）。 |  | [链接](https://github.com/amaezey/task-list) |
| task-progress-mod | 提示框上方 TodoWrite 进度条；tool.call 只观察 TodoWrite 原样放行；进度条显示时 AbovePrompt 不调 next。 | MIT | [链接](https://github.com/hahahahahahahahah6/task-progress-mod) |
| tasknotes-preview | 侧栏按 Obsidian Bases 视图展示 TaskNotes（看板/列表/日程/依赖图）；本机读 vault，本机 process 打开 Obsidian。 | MIT | [链接](https://github.com/cbruyndoncx/claude-tasknotes-renderer-mod) |
| taskrail | 在输入框上方显示本会话计划的波次任务看板，Claude 通过它注册的 plan/set/show 三个工具更新；/taskrail 切换 off/bar/full/both；看板显示时 AbovePrompt 不调 next；计划按会话存在本机 $.store。 | MIT | [链接](https://github.com/drolosoft/taskrail) |
| ssi-cockpit | 配合 ssi 流程，读本机 .ssi/state.json，在提示框上方显示 8 阶段进度条，阶段变化时 toast，/ssi-map 打开阶段图。只观察。没有 .ssi/state.json 快照时会调用 $.ui.status(undefined) 并可能清除其他 mod 的状态行。备注：有状态时 AbovePrompt 会盖住别的行。 | MIT | [链接](https://github.com/ssime-git/ssi-ai-skill/tree/main/mods/ssi-cockpit) |
| tasks-widget | 把 TodoWrite、TaskCreate、TaskUpdate 的任务列成卡片；工具调用只观察原样返回，需配合 widgets。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/tasks-widget) |
| today | 按 Today/◎/○/△ 分级管理本机 todo.md（默认 ~/todo.md），状态栏显示今日件数，/todo 打开面板，并注册 add_task、move_task 工具供 Claude 改清单；AbovePrompt 带默认关闭，仅在 /todo band 后显示且不调用 next；/todo off 设置 $.ui.status(undefined)，会清除其他 mod 的状态。 | MIT | [链接](https://github.com/Humpens/claude-mods/tree/main/today) |
| workflow-band | 在提示框上方显示 Document Workflow 关卡（workflow-cli status）的检查结果与下一步。只观察。备注：本机 process（workflow-cli）；AbovePrompt 会盖住别的行。 |  | [链接](https://github.com/berlysia/dotfiles/tree/master/mods/workflow-band) |
| todos | 会话开始在提示上方列出仓库 TODO/FIXME/HACK（git blame 排序）；备注：本机 git。 | MIT | [链接](https://github.com/bengous/claude-code-plugins/tree/main/todos) |
| task-line | 提示框上方任务列表进度行（TodoWrite/TaskCreate 等填充）；测试失败时标红。纯 UI，只观察，不改写。 | MIT | [链接](https://github.com/muellerei/task-line) |
| handover-report | /handover-report 打开窗格，汇总仓库里 .handovers/handover_log.md 的未完成交接、相关分支、未决问题和过期 worktree；只在本机跑只读 git（log/show/rev-parse/worktree list），不 fetch、不写入。 |  | [链接](https://github.com/bzatrok/claudemods/tree/main/handover-report) |
| blaze | 面板浏览 jj 工作副本及祖先提交的 .blaze/<change_id>/ 计划与工单，/blaze 打开。备注：本机 process（只读 jj workspace root / jj log），读本机 .blaze 文件。 |  | [链接](https://github.com/mashiro-no-rabo/blaze-mod) |
| aichemist-beads-band | 提示框上方显示 beads（bd）中进行中与就绪的任务，/beads-band 显示/隐藏。备注：需本机装 bd（steveyegge/beads）；通过随附的透明脚本 tools/beads-db.sh（不带 --init，不写入）找库，bd 调用均带 --readonly；不联网。 | MIT | [链接](https://github.com/Anras573/AIchemist/tree/main/mods/beads-band) |
| keel-progress | 提示框上方每个 keel 运行一行进度，/keel-progress 打开面板看各步骤与下一个 issue；可选完成提示音。备注：需本机装 keel CLI；只读调用 keel status/activity --json、git worktree list、gh pr list；tool.call 只观察 Bash 里的 keel 命令，原样返回；不驱动运行。 | Apache-2.0 | [链接](https://github.com/berkayturanci/keel/tree/main/mods/keel-progress) |
| sprint-status | 状态行显示当前项目 .ailang/state/sprints 下最近更新的进行中 sprint：已通过几个里程碑、下一个是什么。备注：只读本机文件；纯本机 UI。 | MIT | [链接](https://github.com/sunholo-data/ailang_bootstrap/tree/stable/plugins/sprint-status) |
| task-progress-hud | 提示框上方显示当前 OpenSpec change 的 tasks.md 完成数、百分比和剩余任务，/task-progress 打开面板。备注：只读本机 openspec 文件；tool.call 只在工具执行后刷新，结果原样返回。 | MIT | [链接](https://github.com/liamkarlmitchell/liams-claude-plugins/tree/main/plugins/openspec/task-progress-hud) |
| board | GitHub Projects v2 看板面板，/board 按 Status 列显示一个或多个看板的卡片。备注：通过本机 gh api 只读 GET（需已登录 gh）；需在插件配置里填 owner 和看板编号。 | MIT | [链接](https://github.com/neonelemental/claude-code-board-mods/tree/main/board) |
| orch-session | 显示本会话持有的 orch 工单：状态行、提示框上方「轮到谁」一行、/orch 面板和交接 toast。备注：本机只读运行 `orch list --mine` / `orch show`（需安装 orch-core CLI）；tool.call 只在 orch 命令后刷新，原样返回。 | Apache-2.0 | [链接](https://github.com/severinlindenmann/orch-core/tree/main/plugins/orch-session) |
| moai-board | 只读侧边面板 /moai-board 显示 MoAI 看板队列、工厂 lanes 和 SPEC 文档，可刷新、打开、pick。备注：本机运行 moai CLI 的固定命令（需安装 moai-adk）；pick 前弹框确认。 | Apache-2.0 | [链接](https://github.com/modu-ai/moai-adk/tree/main/mods/moai-board) |
| moai-status | MoAI 只读状态：提示框上方显示用量/上下文警告条和健康状态行，lane 通知弹 toast。备注：只观察；本机运行 moai 固定只读命令；session.receive 只弹 toast 并原样传递；只改 Spinner 后缀文字。 | Apache-2.0 | [链接](https://github.com/modu-ai/moai-adk/tree/main/mods/moai-status) |
| workflow-pane | /workflow-pane 打开面板，按任务列出 workflow-graph 日志（.workflow/log.jsonl）里的节点、状态、退回次数和周期，提示框下方一行显示计数，任务等你处理时弹 toast。备注：只读日志、只显示，不写日志也不发起回合；需配合同仓库 workflow-graph skill 生成的日志；界面文字为中文。 |  | [链接](https://github.com/RoacherM/Wayne-Skills/tree/main/skills/workflow-graph/pane) |
| todo-pane | 停靠的待办面板：在输入框里加条目、点一下划掉；/todo <文字> 直接添加；注册 todo 工具让 Claude 把计划步骤写进列表并实时勾选。备注：todo 工具只读写本插件自己的待办列表（存在插件本地 store），不碰别的工具调用；纯本机，不联网。 | MIT | [链接](https://github.com/NewSoulOnTheBlock/personal-agentic-core/tree/main/plugins/todo-pane) |

### 外部集成 External Integrations

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| calendar | AbovePrompt 显示即将到来的 Google Calendar 事件（/cal）。备注：通过用户已配置的「claude.ai Google Calendar」MCP 读取。 | MIT | [链接](https://github.com/musingfox/cc-plugins/tree/main/calendar) |
| ci-status | /ci 打开面板显示当前仓库最近的 GitHub Actions 运行，打开时每 30 秒刷新，跑完弹提示。备注：需要本机 gh，只调用 gh run list；不改提示或工具。 |  | [链接](https://github.com/shissncg/claude-mods/tree/main/mods/ci-status) |
| crypto-band | 提示框上方横幅显示 RLC、ETH、BTC 价格和 24 小时涨跌（/crypto on、off、status，可隐藏）。备注：每 2 分钟向 CoinGecko 公共 API 发 GET 拉固定币种行情，不发送会话、提示或文件内容；横幅显示时 AbovePrompt 不调 next。 |  | [链接](https://github.com/thewhitewizard/crypto-band) |
| gh-ci-status | 提示框上方钉住 GitHub Actions 状态。 |  | [链接](https://github.com/diegorv/claude-functions-hook/tree/main/plugins/gh-ci-status) |
| github-panel | 侧栏 GitHub 面板列出当前仓库的开放 PR 和 issue，点一下在浏览器打开。备注：需要本机已登录的 gh，只调用 gh 读列表和 --web 打开；不改提示或工具。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/github-panel) |
| inbox-pane | 侧栏窗格展示 claude-inbox 各分区会话，支持快捷键操作。备注：读写本机 `~/.config/claude-inbox/`；可在无写入时拉起 ... |  | [链接](https://github.com/jordanbyron/claude-inbox/tree/main/mod) |
| lavish-pages | 在提示框上方列出本会话打开的 Lavish 页面和状态，可 open、end、reopen；本机 process（find、grep 读本机会话记录，open，lavish-axi），http 只 GET 页面服务的 /health（默认 127.0.0.1:4387），$.model.complete 把页面可见文字（最多 4000 字）交给 Haiku 生成一行描述，tool.call 原样 next，显示时 AbovePrompt 不调 next。 | MIT | [链接](https://github.com/FoCDoT/lavish-pages/tree/main/lavish-pages) |
| linear-claude-mod | Linear 指派工单面板；点击可加载详情、评论或改状态。 | MIT | [链接](https://github.com/rjohnt/linear-claude-mod) |
| linear-tickets | /linear 只读侧栏，使用用户的 API key 调用 api.linear.app，不发送会话内容。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/integrations/linear-tickets) |
| pr-pane | /prs 提示框上方列出你的 GitHub PR 并可打开。 | MIT | [链接](https://github.com/ASRagab/asragab-claude-marketplace/tree/main/plugins/pr-pane) |
| pr-relay | 监视会话 PR，合并或 Codex 评论时唤醒。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/pr-relay) |
| pulse-cc | 提示框上方显示股票报价（Yahoo 或 Pulse Mac 自选）。 | MIT | [链接](https://github.com/fatwang2/Pulse/tree/main/plugins/claude-code) |
| tw-stock-mod | 提示框上方的台股/美股观察清单带状栏，台股交易时段显示台股（红涨绿跌）、美股交易时段显示美股（绿涨红跌）；支持 Yahoo 延迟报价或券商即时行情（永豐 ... |  | [链接](https://github.com/darrell-tw/darrelltw-mods/tree/main/mods/tw-stock-mod) |
| vercel-deploys | /vercel 只读侧栏，使用用户的 token 调用 api.vercel.com，不发送会话内容；健康检查 GET 部署域名时不携带会话主体。 | MIT | [链接](https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/integrations/vercel-deploys) |
| vn-stockmarket-heatmap | 越南股市热力图与报价窗格；联网拉取 SSI iBoard 公开行情（只发送股票代码）；自选列表存本机。 | MIT | [链接](https://github.com/NgoTuong12345/claude-mod-vn-stock-watch) |
| xmuse | Cross-Muse（xmuse）房间看板配套：状态行、toast、窗格和状态工具，以及需人批准的分屏决定（短时授权）。备注：只连本机 xmuse API（默认 http://127.0.0.1:8201，网页界面 127.0.0.1:3000），不发送会话内容；需要 Cross-Muse 在运行。 | MIT | [链接](https://github.com/iiyazu/Cross-Muse/tree/main/integrations/claude-code) |
| autodream-focus | 在每条用户消息/回复右上角加「+ autodream focus」按钮，标记该轮给 autodream 夜间复盘重点看。备注：只在你点按钮时把该条文本（截断 2000 字）写入本机 ~/.claude/autodream/tags.jsonl；渲染先调 next 再叠加按钮；autodream 本体需另装，本条只装 mod；不联网。 | MIT | [链接](https://github.com/STRML/autodream/tree/main/mods/autodream-focus) |
| devbrain-live | 状态行显示 DevBrain 本会话保存/已知/召回了多少条记忆，/devbrain-session 列出明细。备注：tool.call 只观察 save_entry / devbrain note 调用，原样返回；只读本机 ~/.devbrain/sessions/<会话>.json；DevBrain 本体需另装；不联网。 | MIT | [链接](https://github.com/pushthev1be/devbrain/tree/main/mods/devbrain-live) |
| agent-state-observer | 只观察：把代理状态（working/idle/awaiting_approval/ended）、状态切换历史和限额读数写进一个 JSON 文件，供 Marveen 启动器读取。备注：只有设置了 MARVEEN_AGENT_ID 与 MARVEEN_STATE_OBSERVER_DIR 环境变量才写文件，否则什么都不做；所有钩子原样 next，不拒绝不改写；无界面；不联网。 | MIT | [链接](https://github.com/Szotasz/marveen/tree/develop/plugins/agent-state-observer) |
| cortex-bar | 提示框上方用分色堆叠条显示 Cortex Hub 工具调用、/cs 会话进度、token 节省与代码检索 hit@k；/cortex-bar 开关，/cortex-calls 看明细。备注：tool.call 只观察 cortex MCP 及 Read/Bash/Edit/Write 调用，原样返回结果；读项目内 cortex 状态标记文件；需配合 Cortex Hub MCP；不联网。 | MIT | [链接](https://github.com/lktiep/cortex-hub/tree/master/mods/cortex-bar) |
| vast-cost | 输入框下方状态行显示 vast.ai 上正在运行的实例数和每小时费用，还有几台停止中（仍按磁盘计费），每 5 分钟刷新。备注：本机运行 `vastai show instances`，需自行安装并登录 vastai；tool.call 只在 Bash 里出现 vastai 后刷新，原样返回。 |  | [链接](https://github.com/wmayner/dotfiles/tree/main/claude/vast-cost) |
| ado-link-bar | 提示框上方一行列出对话里最近提到的 Azure DevOps PR 和工作项链接（带标题和状态）。备注：session.append 只读取链接并原样传递；本机运行 `az boards work-item show` 取标题（需安装并登录 az）；恢复会话时读本机 transcript 末尾。 |  | [链接](https://github.com/ntaksh42/dotfiles/tree/main/claude/mods/ado-link-bar) |
| ado-pr-status | 后台获取当前分支对应的 Azure DevOps PR（审批、草稿等）写到 ~/.claude/ado-pr-status/，配合附带的 statusline/pr-line.mjs 在 ccstatusline 里显示。备注：本机运行 git 和 `az repos pr list` 只读查询（需安装并登录 az）；需自行配置 ccstatusline；说明为日文。 |  | [链接](https://github.com/ntaksh42/dotfiles/tree/main/claude/mods/ado-pr-status) |
| vome-automation | 侧边面板显示 Claude 正在处理的 Home Assistant 自动化：触发器/条件/动作按 HA 编辑器方式嵌套，保存时高亮改动。备注：需先接入 Vome 的 Home Assistant MCP；只通过你已配置的 MCP 只读调用（$.mcp.call），无 $.http；tool.call 原样返回。 | MIT | [链接](https://github.com/vortitron/home-assistant-mcp/tree/main/claude-plugin/vome-automation) |
| vome-dash | 侧边面板里的可操作 Home Assistant 仪表盘：实时状态、开关/调节控件、摄像头画面。备注：需 Vome Home Assistant MCP；按面板控件会经 $.mcp.call 调用 ha_call_service 直接控制设备（你按才会）；tool.call 原样返回。 | MIT | [链接](https://github.com/vortitron/home-assistant-mcp/tree/main/claude-plugin/vome-dash) |
| vome-esphome | ESPHome 侧边面板：从设备 YAML 画出板子、总线、实体、引脚等结构，保存时标出改动、构建时显示进度。备注：需 Vome MCP；只读调用 MCP 工具，密码/key 等字段显示时隐藏；tool.call 原样返回。 | MIT | [链接](https://github.com/vortitron/home-assistant-mcp/tree/main/claude-plugin/vome-esphome) |
| vome-health | 侧边面板显示 Home Assistant 健康评分和检查发现（按严重度并附建议），标出 Claude 正在处理的项。备注：需 Vome MCP；按面板「修复」会以你的身份提交一条修复提示（你按才会）；tool.call 原样返回。 | MIT | [链接](https://github.com/vortitron/home-assistant-mcp/tree/main/claude-plugin/vome-health) |
| remctl | Apple 提醒事项：RemCTL 的 MCP 工具，加上提示框上方今日任务一行，/reminders 面板可勾选完成。备注：需自行安装 RemCTL 到 ~/bin/remctl（仅 macOS）；面板勾选经 $.mcp.call 完成提醒（你按才会）；tool.call 原样返回。 | MIT | [链接](https://github.com/viticci/remctl/tree/main/plugins/claude-code) |
| board-pane | /board 打开面板显示 dwarves-kit 看板输出，带刷新按钮，可一键把选中工单写进提示框。备注：需安装 dwarves-kit（DWARVES_KIT 环境变量或默认路径）；本机运行 kit 的 board 命令和只读 git/gh；按钮只预填提示框，不自动提交。 | MIT | [链接](https://github.com/dwarvesf/dwarves-kit/tree/master/integrations/claude-code/board-pane) |
| vox | vox 说话或聆听时在提示框上方显示动态波形和字幕；/vox-wave 预览或改颜色。备注：需安装 vox（rtk-ai/vox）；tool.call 只观察 vox 工具和 vox 命令并原样返回；纯本机 UI。 | Apache-2.0 | [链接](https://github.com/rtk-ai/vox/tree/main/plugins/vox) |

### 本地工具 Local Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| adhkar | 在 Claude Code 中显示赞念/记主内容。 |  | [链接](https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/adhkar) |
| copy-band | 上一条回答的代码块/引用草稿一键复制到剪贴板，并本地 stash。依赖本机 pbcopy（macOS）与本地文件。 | MIT | [链接](https://github.com/yash-gadodia/claude-mods/tree/main/copy-band) |
| daily-ayah | 每日经文展示。 |  | [链接](https://github.com/ashafizullah/claude-code-muslim-mods/tree/main/daily-ayah) |
| garde-du-corps | 本地拒绝访问 .env 与危险 Bash（rm -rf、force push、hard reset、DROP TABLE）；只读路径/命令字符串做 den... | MIT | [链接](https://github.com/Para-FR/claude-code-mods-fr/tree/main/garde-du-corps) |
| herdr | 向本地 herdr 窗格报告会话生命周期。本机 process（herdr）。 | MIT | [链接](https://github.com/bendrucker/claude/tree/main/plugins/herdr) |
| lights-out | 显示本会话留下的后台任务与可用内存，可停本会话启动的任务。备注：本机 process（读内存）。 | MIT | [链接](https://github.com/ivanvyd/ground-rules/tree/main/plugins/lights-out) |
| prayer-times | 提示框下方显示下次礼拜时间。 | MIT | [链接](https://github.com/mkbuilds4/mods/tree/main/plugins/prayer-times) |
| prompt-stash | 本地 /stash 提示词栈：存、列、弹出到输入框，不进模型上下文。 |  | [链接](https://github.com/gonzaloserrano/cc-prompt-stash) |
| push | /push 把当前分支推到上游；本机 git。 |  | [链接](https://github.com/robertgregorywest/claude-mods/tree/main/mods/push) |
| config-snapshots | 快照/回滚 Claude Code 配置；备注：本机 process 跑插件内 claude-config。 | MIT | [链接](https://github.com/MichaelP17/claude-mods/tree/main/config-snapshots) |
| service-radar | 跟踪 Claude 拉起的后台服务并可关掉；只观察 Bash，不改写。备注：本机 process（docker、colima、brew、launchctl）。 | MIT | [链接](https://github.com/MichaelP17/claude-mods/tree/main/service-radar) |
| session-journal | 每回合把提问/改文件/命令追加到本机 .claude/journal/日期.md；/standup。备注：本机写本地文件。 | MIT | [链接](https://github.com/Alyan-khattak/Claude-Code-Mods/tree/main/session-journal) |
| sportscaster | 会话实况解说（本地 $.audio.speak，不上传会话）。备注：使用本机 TTS。 |  | [链接](https://github.com/OneWave-AI/claude-code-mods/tree/main/sportscaster) |
| tmux-status | 把 Claude 状态（working/waiting/done）写到本机 tmux 窗口选项。备注：本机 process（tmux）。 | MIT | [链接](https://github.com/XavierYounan/claude-code-tmux-status) |
| clip | /clip 清洗终端装饰后写入本机剪贴板。备注：本机 process（pbcopy/wl-copy/xclip/powershell）。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/clip) |
| pop | /pop 用本机打开器打开 URL/文件。备注：本机 process（open/xdg-open/powershell）。 |  | [链接](https://github.com/DJPalefaceSD/rostech-mods/tree/main/plugins/pop) |
| usage-reporter | 把计划限额与 credits 写到本机 ~/.claude/usage-reporter/usage.json 供其他工具读取。备注：本机写本地文件；用用户 OAuth 读官方用量 API，不带会话正文。 | MIT | [链接](https://github.com/tksunw/usage-reporter) |
| agent-shell-watch | 状态行与窗格跟踪本会话 Bash/后台任务与 runner（Codex/Pi 等）；只观察，不改写。备注：本机 process（tail）。 | MIT | [链接](https://github.com/apolenkov/agent-shell-watch) |
| tts-lite | 回合结束后本机 TTS 朗读短回复；长回复用 $.model.complete 摘要。空闲且旧 status hook 移除时调用 $.ui.status(undefined)，会清除其他 mod 使用的状态行。备注：本机 process（piper/espeak/paplay）；使用 $.model.complete。 | MIT | [链接](https://github.com/ipartington/claude-mods/tree/main/tts-lite) |
| quickswitch | 提示框下方点击切换 Claude 账号。本地进程运行用户自己的 ccswitch，仅在点击时切换。**账号列表显示时 PromptHint 不调用 next，可能覆盖其他提示行**。 | MIT | [链接](https://github.com/Rocha101/claude-code-quickswitch) |
| shelf | 在提示框上方放命名的文件夹/文件捷径，点一下把路径插到正在输入的位置（不发送）；/shelf add、/shelf remove 管理。备注：路径存在 $.store；不改提示，不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/shelf) |
| pulse | /pulse 打开面板显示 CPU 曲线、内存条和当前仓库的 git 状态与最近提交。备注：会用本机 node 启动仓库里自带的小 sidecar（只读 git、只监听 127.0.0.1），mod 通过 localhost 拉 JSON；不联网，需装 Node。 |  | [链接](https://github.com/gfsaaser24/claude-code-mod-examples/tree/main/pulse) |
| hal-grammar-check | 你输入提示时在提示框上方实时做语法检查并给出修改建议。备注：草稿（前 500 字）只发给本机 Ollama（localhost:11434），需自行安装 Ollama 和模型；prompt.edit/prompt.submit 只读、原样返回，不改写提示。 | MIT | [链接](https://github.com/vinta/hal-9000/tree/main/plugins/hal-grammar-check) |

### 其他工具 Other Tools

| 名称 Name | 功能 Description | 许可证 License | 来源 Source |
|-----------|------------------|----------------|-------------|
| action-pin | 把常用动作钉在提示框上方。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/action-pin) |
| ask-autopick | 自动采纳或拒绝提问。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ask-autopick) |
| bughunt | 追踪与报告 bug。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/bughunt) |
| capi | 提示框上方的水豚语言学习卡片，一张卡同时教一个真实知识点和一个外语词句。说明：用 $.model.complete 生成卡片，请求里带最近用过的工具名和 Bash 程序名；横幅显示时 AbovePrompt 不调 next；本机 process（hostname/scutil、brctl、mkdir、mv）；学习记录写到 ~/Library/Mobile Documents/com~apple~CloudDocs/capi（会随 iCloud 同步）；可用 $.audio.speak 本机朗读。 | MIT | [链接](https://github.com/danieldeusing/capi-cc-mod) |
| cc-side | 提供 /side 命令开启第二个对话。 |  | [链接](https://github.com/Ahmad8864/cc-side) |
| claude-queue | /q 在回合进行中排队提示，回合结束后自动发出。 |  | [链接](https://github.com/galElmalah/claude-mods/tree/main/claude-queue) |
| clocks-widget | 多时区时钟卡片，可增删时区，需配合 widgets。备注：开启时每 15 秒刷新，卡片被隐藏也照跑。 | MIT | [链接](https://github.com/oMaN-Rod/claude-code-widgets/tree/main/plugins/clocks-widget) |
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
| side-chat | /side 或 /btw 打开侧边问答窗格，主对话看不到。备注：会接管内置 /btw；问题经 $.model.fork 带主会话上下文发给同一个 Claude 模型（不经第三方）；`@名字 问题` 用 $.agent.spawn 起一个子代理回答。 | MIT | [链接](https://github.com/varunmoka7/side-chat) |
| slash-chain | 斜杠命令链。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/slash-chain) |
| sql-concat-watch | SQL 拼接监视。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/sql-concat-watch) |
| time | 每条用户消息上方显示发送时间。 |  | [链接](https://github.com/diegorv/claude-functions-hook/tree/main/plugins/time) |
| tool-coach | 工具使用教练。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/tool-coach) |
| turn-timeline | /timeline 把当前回合画成时间线。 | MIT | [链接](https://github.com/arasovic/claude-code-mods/tree/main/turn-timeline) |
| typing-speed | 提示框上方打字速度计，提交后显示 WPM、准确率与个人最佳。 | MIT | [链接](https://github.com/borabiricik/claude-mods/tree/main/plugins/typing-speed) |
| ua-fallback | 用户代理降级。 |  | [链接](https://github.com/KilimcininKorOglu/claude-code-mods/tree/main/plugins/ua-fallback) |
| where-am-i | 提示上方只读回顾：目标/正在做/等你什么（观察工具调用，不改写）。 |  | [链接](https://github.com/hamzafer/claude-code-mods/tree/main/mods/where-am-i) |
| winnow | 精简大型未使用的工具结果。 |  | [链接](https://github.com/GhalebDweikat/winnow) |
| xhs-count | 小红书字数哨兵：选中文字后在提示框上方实时显示够不够标题（≤20 字）、正文超没超（≤1000 字）。备注：纯本机 UI；提示框上方条显示时不调 next，会盖住其他 mod 的同位置内容。 | MIT | [链接](https://github.com/eddiezhan/xhs-count-mod) |
| zen-breath | /meditate 侧边冥想呼吸面板（方箱、4-7-8、平静三种节奏），ASCII 佛祖敲木鱼，状态栏显示剩余时间；次数和连续天数存本机 $.store；开会话起每秒 tick（未在冥想时几乎无操作）；结束时会清掉其他 mod 的状态行。 | MIT | [链接](https://github.com/mindthink/zen-breath) |
| zsh-safe | 把 bash 写法的 Bash 命令改写成 macOS zsh 可跑。 |  | [链接](https://github.com/HolyGrail/claude-mods/tree/main/plugins/zsh-safe) |
| notes-panel | 每个会话一份 markdown 便签窗格（/note），可追加、勾选、清空和清理旧笔记，只存在本机。 |  | [链接](https://github.com/Sickin/claude-code-notes-panel) |
| tldr | /tldr 把 Claude 最后一条回复用 $.model.complete（haiku）总结成几行，只以通知行显示、不进对话；会把最后一条回复文本交给 $.model.complete。 |  | [链接](https://github.com/bzatrok/claudemods/tree/main/tldr) |
| quick-reply | 在提示框上方给出一键回复按钮：Claude 刚列出的选项、Yes、按你的推荐、Continue。备注：只有你点按钮时才以你的身份发出那句回复；prompt.submit 只清状态不改写；不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/quick-reply) |
| auto-resume | 回合因限流或 API 过载中断时倒计时到重置，然后自动替你发一句 continue（文字可配）；你自己发消息就取消。备注：会以你的身份自动发出这句配置好的提示；prompt.submit 只检测接管不改写；不联网。 |  | [链接](https://github.com/seanrobertwright/claude-mods/tree/main/mods/auto-resume) |
| freeze | /freeze 在下一个安全点冻结会话，之后恢复如初；冻结期间暂缓工具调用和模型请求。备注：Linux 上默认会 SIGSTOP 本会话的后台任务（pauseBackground 可关）；/freeze shortcut on 时才写 ~/.claude/keybindings.json；冻结中重复的自动提示会被丢弃；用透明的 sh 脚本，不联网。 | MIT | [链接](https://github.com/francktrouillez/claude-freeze) |
| prompts | 侧栏“我问过的”：列出本次对话你打过的每句话，可看全文、复制或放回输入框；/prompts 开关。备注：prompt.submit 只记录不改写；放回输入框只在你按键时发生；不联网、不写文件。 | MIT | [链接](https://github.com/jessetsai1024/claude-prompts) |
| conferma | Claude 以提议/确认问题收尾时，在提示框上方显示该段与「Sì, procedi / No, fermati」两个按钮。备注：只有你点按钮时才以你的身份发出固定回复；prompt.submit 只清状态不改写；不用模型、不联网；意大利语界面。 | MIT | [链接](https://github.com/andreabrugnoli/mods/tree/main/conferma) |
| lezioni | 记录本会话的「绊脚石」（工具失败、被拒的操作、你的纠正语），满 2 条后显示按钮让 Claude 分析原因并提出 skill/CLAUDE.md 修改建议（不自动应用）；/lezioni 列出记录。备注：tool.call 只观察原样返回；prompt.submit 只记录不改写；只有你点按钮时才发出分析请求；意大利语界面；不联网。 | MIT | [链接](https://github.com/andreabrugnoli/mods/tree/main/lezioni) |
| needs-you | 高亮回复中的「Needs you」段落，旁边加跳动的 Claude 小人，并把其中的选项变成按钮。备注：只在回复含 **Needs you:** 段落时生效（需你的提示词/CLAUDE.md 约定这种写法）；只有你点按钮时才以你的身份发出所选答复；prompt.submit 只清状态不改写；不联网。 | MIT | [链接](https://github.com/robfresh2o/fresh2o-plugins/tree/main/plugins/needs-you) |
| buffer-pane | 转录旁的面板，Claude 干活时先写好下一步要说的话（多块文本），按 [+] 把一块放进提示框，按 [>] 直接提交。备注：只提交你自己写的文本（你按才会）；纯本机。 | MIT | [链接](https://github.com/meganemura/buffer-pane/tree/main/plugin) |
| output-ladder | 把上一条回答换种方式重讲：ASD-STE100 简明英语、图示、HTML 页面或讲解视频，并给回答的 STE 风格打分。备注：对应命令或按钮会以你的身份提交一条改写请求（你执行才会）；prompt.submit/session.append 只记录回答文本，不改写。 | MIT | [链接](https://github.com/0xGondarxyz/claude-code-mods/tree/main/output-ladder) |
| enable-todo-tools | 给默认不带待办工具的新模型重新打开 Claude Code 的待办（todo）工具。备注：会话开始时，若你没设 CLAUDE_CODE_ENABLE_TODO_TOOLS 就设为 1；你已设的值（包括 0）不动。 | MIT | [链接](https://github.com/muellerei/enable-todo-tools) |

---

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

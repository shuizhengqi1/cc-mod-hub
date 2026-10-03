# cc-mod-hub

这是一个精选的 Claude Code mod 市场。Mod 是一种打包在插件内的 TypeScript 事件钩子（如 tool.call、ui.render 等），而不是通用技能或斜杠命令。需要 Claude Code 2.1.287 或更高版本。

## 安装指南

### 添加此市场

在 Claude Code 中运行以下命令添加此市场：

```
/plugin marketplace add shuizhengqi1/cc-mod-hub
```

### 安装 mod

从此市场安装 mod：

```
/plugin install <mod名称>@cc-mod-hub
```

**重要提示**：Mod 以与 Claude Code 相同的访问权限运行，请仅从您信任的来源安装 mod。

## Mod 列表

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

## 许可证

此市场仓库本身不包含代码，仅作为插件目录。各个 mod 的许可证请参阅其源仓库。

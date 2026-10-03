# Claude Code Mod Hub

这是一个精选的 Claude Code mods 市场，收录了经过验证的真实 Claude Code mods。

## 安装方法

在 Claude Code 中运行以下命令添加此市场：

```
/plugin marketplace add shuizhengqi1/cc-mod-hub
```

## 收录的 Mods

以下所有 mods 均已于 2026-10-03 从链接页面审核验证：

1. **diff** - https://github.com/anthropics/claude-code/tree/main/mods/diff  
   显示未提交更改的 /diff 面板

2. **agents-md** - https://github.com/anthropics/claude-code/tree/main/mods/agents-md  
   加载 AGENTS.md 文件

3. **sec-default** - https://github.com/anthropics/claude-code/tree/main/mods/sec-default  
   防护机制，防止用户 mods 覆盖托管钩子

4. **telemetry** - https://github.com/anthropics/claude-code/tree/main/mods/telemetry  
   内置 mods 的遥测支持（分析关闭时不发送任何数据）

5. **token-weather** - https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/token-weather  
   在提示框上方显示上下文预测（Apache-2.0 许可证）

6. **blast-radius** - https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/blast-radius  
   拦截危险的 Bash 命令并显示继续/取消选项（Apache-2.0 许可证）

7. **replay-theater** - https://github.com/anthropics/claude-code-playground/tree/main/claude-code/mods/replay-theater  
   逐步回放上一轮的文件编辑（Apache-2.0 许可证）

8. **cache-tax** - https://github.com/karanb192/cache-tax  
   /keepwarm 命令

9. **claude-council** - https://github.com/hex/claude-council  
   并行代理，并排面板显示

10. **winnow** - https://github.com/GhalebDweikat/winnow  
    缩减大型工具结果

11. **flowpane** - https://github.com/mpolatcan/flowpane  
    实时工作流程图

12. **pixelband** - https://github.com/furqan-khan07/pixelband  
    在提示框上方显示像素艺术

13. **cc-side** - https://github.com/Ahmad8864/cc-side  
    /side 第二对话

14. **ContextSaver** - https://github.com/AlmogBaku/ContextSaver  
    标记浪费会话习惯（MIT 许可证）

15. **cc-arcade** - https://github.com/sezaakgun/cc-arcade  
    在提示框上方显示游戏，点击不调用模型

16. **mindful-claude** - https://github.com/halluton/Mindful-Claude  
    呼吸带显示

17. **12ui-plugin** - https://github.com/just-every/12ui-plugin  
    设计面板

18. **cueloop** - https://github.com/mmurakaru/cueloop  
    工具调用监控（Apache-2.0 许可证）

19. **lcm** - https://github.com/lossless-claude/lcm  
    无损上下文管理（MIT 许可证）

20. **taskcut** - https://github.com/wasd96040501/taskcut  
    任务步骤管理（MIT 许可证）

21. **Katharsis** - https://github.com/OpenScribbler/Katharsis  
    提示提交增强（MIT 许可证）

22. **fast-jev-compaction** - https://github.com/tamaratran/fast-jev-compaction  
    快速会话压缩

23. **claude-image-generation** - https://github.com/hex/claude-image-generation  
    图像生成工具

24. **constellation-claude** - https://github.com/ShiftinBits/constellation-claude  
    项目管理工具（AGPL-3.0 许可证）

## 关于 Claude Code Mods

Mod 是一个 TypeScript/JS 模块，它可以钩取 Claude Code 事件（tool.call、ui.render、prompt.submit 等）并作为插件的一部分发布。

更多信息请参考：
- https://code.claude.com/docs/en/plugins/mods
- https://claude.com/blog/claude-code-mods

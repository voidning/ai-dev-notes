# ai-dev-notes

我的 AI 开发学习笔记仓库：日常学习中沉淀的最佳实践、提示词模板和读书摘录。

文件变更通过 [gitwatch](https://github.com/gitwatch/gitwatch) 实时自动同步到本仓库。

## 目录结构

```
├── best-practices/    # AI 编程工具的最佳实践笔记
└── quality-prompts/   # 保障 AI 交付质量的提示词模板
```

### best-practices/

AI 编程工具（Claude Code 等）的使用心得与最佳实践摘录。

- [Best practices for Claude Code](best-practices/best-practices-for-%20claude-code.md)

### quality-prompts/

约束 AI 协作流程的提示词模板，覆盖任务全生命周期：

- **执行前**：先调研最佳实践，给出方案和验收清单，确认后再动手
- **完成后**：多 Subagent 交叉验证，多数通过才交付

详见 [quality-prompts/README.md](quality-prompts/README.md)。

## 自动同步

本仓库由 gitwatch 监听，文件保存后约 10 秒内自动 commit + push：

```bash
nohup gitwatch -r https://github.com/voidning/ai-dev-notes.git -b main \
  -m "auto-sync: %d" -s 10 ~/Desktop/ai-dev-notes &
```

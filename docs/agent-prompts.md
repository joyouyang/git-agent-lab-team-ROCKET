# Git Agent 协作提示词指南

## 1. 通用安全提示词 (开始工作前)
请帮我：
1. 检查当前 `git status`；
2. 确认当前分支；
3. 拉取远程最新版本；
4. 如果有未提交修改，请先提醒我，不要覆盖。

## 2. 通用安全提示词 (提交前)
请帮我查看当前 `diff`，用中文总结：
1. 修改了哪些文件；
2. 每个文件主要改了什么；
3. 有没有看起来不该提交的文件；
4. 建议的 commit message。
*注意：先不要提交。*

## 3. Worktree 专用提示词 (示例)
### 为 Worktree A 设置：
- 确认当前分支是 `feature/worktree-a`。
- 不要切换分支，不要使用 `reset`，不要 `force push`，不要修改 `main`。
- 只修改 `docs/worktree-notes.md`。

### 给 worktree B 的 agent 提示词
你现在只能在当前目录工作。先运行 pwd、git branch --show-current、git status。
确认当前分支是 feature/worktree-b。
不要切换分支，不要使用 reset，不要 force push，不要修改 main。
只修改 docs/agent-prompts.md。
完成后总结 diff，先不要 commit，等我确认。
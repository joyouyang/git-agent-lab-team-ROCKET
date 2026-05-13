# 多 Agent 并行工作安全提示词 (Worktree 专项)

## 1. 环境识别指令
在开始任何操作前，Agent 必须执行以下检查：
* **当前路径**：运行 `pwd` 确认处于指定的 worktree 目录。
* **分支确认**：运行 `git branch --show-current` 确认分支为 `feature/worktree-prompts-haonan`。
* **状态检查**：运行 `git status` 确保工作区干净。

## 2. 行为边界约束
* **禁止切换**：严禁执行 `git checkout` 或 `git switch`。你只能在当前分配的 worktree 目录中工作。
* **禁止越权**：严禁修改当前目录以外的任何文件。
* **提交规范**：每次 commit 前必须展示 `git diff` 结果，并由人工确认修改范围是否符合预期。
* **禁用危险命令**：严禁使用 `git reset --hard`、`git push -f` 或任何可能破坏主仓库历史的操作。

## 3. 并行协作逻辑
当多个 Agent 同时工作时，每个 Agent 应被视为独立的实体，仅对自己的 worktree 路径负责。通过物理目录的隔离，确保代码修改不会产生冲突。
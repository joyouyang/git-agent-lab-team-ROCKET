# Worktree 使用说明

## worktree 是什么

worktree 是同一个 Git repo 的多个本地工作目录。每个 worktree 通常对应一个不同的 branch。

branch 是修改路线，worktree 是本地文件夹。只用 branch 时，一个目录一次只能切到一个分支；使用 worktree 时，可以同时打开多个目录，每个目录对应不同分支。

## 什么时候需要 worktree

当一个人需要同时处理多个任务，或者同一台电脑上要让多个 coding agent 并行工作时，worktree 很有用。

例如：

- Worktree A 负责修改 `docs/worktree-notes.md`
- Worktree B 负责修改 `docs/agent-prompts.md`

两个 agent 分别在不同目录工作，就不容易互相改错文件或切错分支。

如果只用 branch、不用 worktree，虽然也能切换任务，但同一时间通常只能在一个目录里工作。比如两个 agent 都在同一个项目目录里并行操作，一个 agent 正在改 feature-a，另一个 agent 又切到 feature-b，就可能出现这些问题：

两边修改的文件互相覆盖；
git status 里混在一起，不清楚哪些改动属于哪个任务；
一个任务还没提交，另一个任务就切分支，容易把未完成的改动带到错误的分支；
冲突更难排查，因为你不知道是谁、在哪个任务里改乱了。

## 安全规则

一个 agent 一个 worktree，一个 worktree 一个任务分支。不要让两个 agent 在同一个目录里并行操作，也不要让两个 worktree 使用同一个任务分支。

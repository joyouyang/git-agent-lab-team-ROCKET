核对日期：2026-05-18  
Repo URL：https://github.com/joyouyang/git-agent-lab-team-ROCKET

## PR 清单

负责人按 GitHub assignee 优先；无 assignee 时按 PR author 记录。

| PR | 状态 | 用途 | 负责人 |
|---|---|---|---|
| [#1 补充PPT版本管理案例](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/1) | merged | 新增 PPT 版本管理案例 | joyouyang |
| [#2 Feature/conflict-a](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/2) | merged | 冲突练习 A：修改 shared-summary.md | joyouyang |
| [#3 补充 worktree 使用场景](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/3) | merged | worktree 使用说明 | joyouyang |
| [#4 补充多 agent 并行工作的安全提示词](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/4) | merged | 多 agent 并行安全提示词 | joyouyang |
| [#5 补充 worktree 审计证据](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/5) | merged | 记录 worktree 审计证据 | joyouyang |
| [#6 补充毕业论文版本管理案例](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/6) | merged | 毕业论文版本管理案例 | jsun07363-lang |
| [#7 Contributor C: 提交 Agent 提示词文档](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/7) | merged | Contributor C 提交 Agent 提示词文档 | zhanghaonanmaxx-del |
| [#8 Revert "补充PPT版本管理案例"](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/8) | merged | 回滚初版 PPT 案例 | joyouyang |
| [#9 Contributor C: 补充 Agent 提示词实验日志](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/9) | open | Agent 提示词实验日志 | zhanghaonanmaxx-del |
| [#10 Worktree Operator: 补充 worktree 使用场景说明](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/10) | open | Worktree Operator 使用场景说明 | zhanghaonanmaxx-del |
| [#11 Worktree Operator: 补充并行 Agent 安全提示词](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/11) | open | Worktree Operator 并行安全提示词 | zhanghaonanmaxx-del |
| [#12 docs: B 认为 Git 的核心价值是多人协作](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/12) | merged | 冲突练习 B：修改 shared-summary.md | zhanghaonanmaxx-del |
| [#13 Update shared-summary.md](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/13) | merged | shared-summary.md 冲突后更新 | joyouyang |
| [#14 补充手动作答题](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/14) | merged | Stella 手动作答题 | jsun07363-lang |
| [#15 重新补充PPT管理案例](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/15) | merged | 重新补充 PPT 管理案例 | joyouyang |
| [#16 Feature/ppt case joy](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/16) | merged | PPT case 分支合并 | joyouyang |
| [#17 整理关键词表](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/17) | merged | 整理关键词表 | joyouyang |
| [#18 新增乐泉的手动回答](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/18) | merged | 乐泉手动回答 | joyouyang |

## 有 review comment 的 PR

以下 PR 均有 GitHub review comment，可满足“至少 3 个”的要求：

- [#3 补充 worktree 使用场景](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/3)
- [#4 补充多 agent 并行工作的安全提示词](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/4)
- [#7 Contributor C: 提交 Agent 提示词文档](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/7)
- [#14 补充手动作答题](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/14)
- [#15 重新补充PPT管理案例](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/15)
- [#16 Feature/ppt case joy](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/16)
- [#17 整理关键词表](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/17)
- [#18 新增乐泉的手动回答](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/18)

## 冲突 PR 与解决说明

冲突相关 PR：

- [#2 Feature/conflict-a](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/2)
- [#12 docs: B 认为 Git 的核心价值是多人协作](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/12)
- [#13 Update shared-summary.md](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/13)

冲突说明：#2 和 #12 都修改了 `docs/shared-summary.md` 的同一行。解决时没有直接丢弃任何一方，而是合并两边语义，保留“记录修改历史”和“多人协作”两个重点。当前主分支内容为：

```text
本项目展示了 Git 如何记录修改历史并帮助多人协作，减少最终版地狱和文件来回传。
```

## git worktree list 输出

以下为已提交证据中记录的 `git worktree list --porcelain` 输出：

```text
worktree /Users/ouyanglequan/工作/实习/做实习/极群科技2603-/GitLab-ROCKET
HEAD a19f6f9336822f51bfb68af71288324e63f3db60
branch refs/heads/main

worktree /Users/ouyanglequan/工作/实习/做实习/极群科技2603-/GitLab-ROCKET-wt-a
HEAD a5e8c1f2753492a4c2593b92e71d02b3959b291d
branch refs/heads/feature/worktree-notes-joy

worktree /Users/ouyanglequan/工作/实习/做实习/极群科技2603-/GitLab-ROCKET-wt-b
HEAD 0643a6bb26313ccbae97f64d8491343da935159f
branch refs/heads/feature/worktree-prompts-joy
```

## Worktree 两个 PR 链接

与上方两个 worktree 分支对应的 PR：

- [#3 补充 worktree 使用场景](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/3)，对应 `feature/worktree-notes-joy`
- [#4 补充多 agent 并行工作的安全提示词](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/4)，对应 `feature/worktree-prompts-joy`

## 偏离说明

- 当前有 3 个 PR 仍为 open：[#9](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/9)、[#10](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/10)、[#11](https://github.com/joyouyang/git-agent-lab-team-ROCKET/pull/11)。它们已纳入“所有 PR”清单并标注状态。
- worktree 输出采用 `git worktree list --porcelain` 形式，包含 worktree 路径、HEAD 和 branch，比普通 `git worktree list` 输出更完整。

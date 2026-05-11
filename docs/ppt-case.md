# 用小组 PPT 理解 Git

## 传统协作的问题

以前做小组 PPT 时，常见问题是每个人都在传不同版本的文件，例如：

- 汇报PPT_A改.pptx
- 汇报PPT_B改.pptx
- 汇报PPT_最终版.pptx
- 汇报PPT_最终版真的最终版.pptx

这样很容易不知道哪个才是最新版，也很难看出每个人具体改了什么。

## Git 怎么解决

Git 可以把每个人的修改记录下来。每位成员可以从 main 新建自己的 branch，在自己的分支上修改内容，再通过 Pull Request 请求别人检查。

例如：

- A 负责背景介绍
- B 负责案例分析
- C 负责总结页

每个人都在自己的 branch 上提交 commit，最后通过 PR review 后合并到 main。

## 一个具体场景

假设小组要做一次项目汇报 PPT。Owner 先创建 repo 和基础目录，其他成员分别负责不同部分。

成员 A 修改大纲，成员 B 补充案例，成员 C 整理演讲提示词。每个人完成后都发 PR，请其他成员 review。确认没有问题后，再 merge 到 main。

这样 main 就始终代表小组认可的正式版本。

## Summary
- 新增小组 PPT 协作案例初稿，用传统文件传递协作类比解释 Git 工作流
- 补充 branch、commit、PR review、merge 到 main 的协作过程说明
- 新增 .gitignore，忽略 macOS 临时文件 .DS_Store

## Test
- 未运行测试，文档内容修改

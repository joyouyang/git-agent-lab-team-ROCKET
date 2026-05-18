# Manual Answers

> 声明：以下回答由本人独立完成，未使用 AI 生成或润色。

## <欧阳乐泉Joy>

### Q1. Git 和 GitHub 分别是什么？repo 和 remote 又是什么？
Git是一个项目版本管理器。相比于我熟悉的共享文档版本追溯功能来说，留痕更自动化且对于文件类型兼容度更高。

GitHub直译就很形象——很多Git聚集的地方，是团队协作平台，也是信息和资源共享平台。区别于以往我熟悉平台的地方是，GitHub多了一层以团队作为单位的社交功能，不仅为团队内成员沟通提供平台，而且也为团队间交流提供了默认的窗口。如果说飞书是有严格门禁的大厦，GitHub更像是玻璃透明的讨论间，路过的人可以张望看看，甚至可以直接推门加入讨论，这还挺有趣的。

repo是Git管理的对象。Repository的缩写，直译过来是代码库/知识库，指的是被管理的整个项目文件夹，类比“毕业论文”或者“课程汇报PPT”这个大文件夹。

remote是repo存储的一个位置，相对应的是本地。就像手机资料要时不时同步备份云盘一样，在使用GitHub工作的时候也要确认remote和本地的版本是否同步。

### Q2. commit 是什么？为什么 commit message 不能只写“update”或“final”？
commit是一次更新的版本，类似于游戏的一个存档点，或者lark的“另存为版本”。

commitmessage是为了提示合作者或reviewer这一版commit到底改变了什么的，如果只写update不清楚究竟update了什么；只写final因为在merge之前并不是真的final，而merge需要reviewer同意。

### Q3. branch 是什么？main 分支代表什么？为什么不建议直接在 main 上改？
branch是一条本地的存档线路，或者用大白话说就是把主线路复制了一套单独修改，不同的人可以同时在不同的branch上修改，修改之后可以通过commit合并回主线路，如果同时有多个branch被修改了就判断冲突然后处理冲突。

main分支代表这个项目最权威的正式版本。如果直接在main上修改会使协作更混乱，降低效率。因为缺少审核过程，没有确认的内容变成正式版本，所以将给其他协作者造成误解，使其未审核的内容上工作。

### Q4. Pull Request 做了什么？reviewer 应该看什么，而不是只点 approve？
pullrequest意味着把用户新更改的内容上传到了GitHub，在合并到main之前召唤reviewer审核。我认为一次PR意味着一次项目的更新。reviewer应该首先看pullrequest需要审核员确认的部分，其次关注和base的差异，在比较权衡之后再点approve。

### Q5. 你们组哪一个 PR 是你负责的？你做了哪些 commit？每个 commit 大概改了什么？
1.补充PPT版本管理案例：
commit1:补充小组PPT协作案例初稿；
commit2:补充PPT协作注意事项；
commit3:小组PPT协作案例初稿结尾修订；

2.Feature/conflict-a：
commit1:Update project description to emphasize history tracking
commit2:Update shared-summary.md

3.Revert "补充PPT版本管理案例"：
commit1:撤销了

4.补充 worktree 审计证据
commit1:把worktree的证据添加进evidence.md了

5.补充多 agent 并行工作的安全提示词
commit1:补充多agent并行工作的安全提示词语
commit2:与浩楠版本的冲突，保留了浩楠版本

6.补充 worktree 使用场景
commit1:补充worktree使用场景
commit2:根据嘉敏的评论更新内容

7.重新补充小组 PPT 协作案例
commit1:把之前撤回的PPT协作案例首先补充进ppt-case-joy branch

8.update shared-summary.md
commit1:更新了shared-summary.md
commit2:解决冲突

9.Feature/ppt case joy
commit1:把最新的main merge进feature/ppt-case-joy
commit2:修改了PPT协作案例内容
commit3:把ppt-case-joy branch中更新的PPT协作案例merge入main

10.整理关键词表
commit1:整理了关键词表格
commit2:补充了关键词的类比理解

### Q6. 你们组如何制造冲突？冲突发生在哪个文件？最终怎样合并两边意思？
我们组的冲突在shared-summary.md。我和浩楠都PR了一个版本的shared-summary，在浩楠首先merge进main之后，我的PR中检测到conflict。对冲突内容首先借助copilot进行判断，然后人工决定兼采众长，把两个版本的summary合并概括之后merge进了main。

### Q7. worktree 是什么？它和 branch 的关系是什么？
branch指一条独立的开发路线，worktree指的是本地存储结构。正常情况下1个worktree对应1个branch，可以给已经存在的branch开1条worktree，可以新建branch的同时建立worktree。

### Q8. 什么时候“多个 branch”已经够了？什么时候需要“一台设备”？
这里的“一台设备”我理解为一个worktree。如果需要同时处理多个问题，尤其是如果需要2个agent同时开跑，那么用worktree增加“一台设备”更适合。

### 09. 如果你是老师，你如何审计一个 repo 是否真的通过 PR 合并，而不是直接改 main？
查看main的分支提交记录，以及merge commit、PR记录。

### 10. 使用 coding agent 做 Git 操作时，你最担心的一个危险动作是什么？你会怎样写提示词避免它？
我最担心的操作是force push，因为可能会把远程 GitHub 上的历史覆盖掉，导致Git中的历史变得十分混乱。

在工作开始前，拉取最新版本时我会写：如果有未提交修改，请先提醒我，不要覆盖。

在工作提交时，我会写：注意：先不要提交。若发现意外文件，请告知 agent 排除；待确认无误之后再提交。


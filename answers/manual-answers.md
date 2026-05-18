# Manual Answers
 
> 声明：以下回答由本人独立完成，未使用 AI 工具生成或润色。
 
## 孙嘉敏 Stella
### Q1. Git 和 GitHub 分别是什么？repo 和 remote 又是什么？
答：Git是一套工具软件，是在我电脑上运行命令行程序，做的事情主要是记录文件变更历史。而GitHub是一个网站，用来存储Git记录的代码，而且可以在这个网站上和别人协作，它是一个可以聚集大家一起参与的网站。repo是一个项目的整体，所有文件和历史都装在一个repo里，比如我今天 clone 的那个 git-agent-lab-team-ROCKET 就是一个 repo。而remote是一个repo在远端的副本的指代称呼，指的是GitHub上的云端repo。我今天用过 git push -u origin feature/thesis-case-stella 这条命令，里面的 origin 就是默认的 remote 名字，它指向我们组在 GitHub 上的那个云端 repo。
 
###  Q2.commit 是什么？为什么 commit message 不能只写“update”或“final”？
答：commit类似于游戏里的存档点，每一次想回看当时的项目长什么样都可以点击commit进行传送，commit方便我的协作者以及检查的人查看我的更改，不会造成理解的混淆，如果说一堆 commit 都叫 "update" 时，根本看不出每次到底改了什么。写 'final' 也是同样的问题，最后会出现 'final2'、'真的 final' 这种情况，跟我在 thesis-case 里写的 '最终版地狱' 是一回事。但比如我写thesis- case用的两个commit message，每一个明确了做了什么，能让阅读者更好看懂。
 
### Q3.branch 是什么？main 分支代表什么？为什么不建议直接在 main 上改？
答：branch是同一个repo里的独立修改路线，而main代表的是repo的默认分支，现在大家打开来看repo默认看到的都是main上的内容，不在main上直接修改是因为这样会导致没人review就直接过了，如果直接在main上修改还会出现改错就让正式版本变坏的结果。我们在做PR#7的时候，就是浩楠现在分支上改动，然后我review，接着她根据我的建议继续修改我再接着approve，这些痕迹都是在分支上留下的。
 
### Q4.Pull Request 做了什么？reviewer 应该看什么，而不是只点 approve？
答：Pull Request主要指的是拉取请求，首先一般我们的修改是发生在分支上，那么PR是提供讨论和审查的入口，其次它还提供了协作记录，merged后整个对话也不会消失，未来我们都能查找到为什么这次进行了修改。reviewer应该看的是改动的内容是否合理，例如逻辑是否正确有没有引入新的问题等等。我在这次作业中review过同伴的案例，比如在#3中我提出来需要在案例中提到“只用branch不用worktree会怎样的反例。
 
### Q5你们组哪一个 PR 是你负责的？你做了哪些 commit？每个 commit 大概改了什么？
答：我负责的是PR#6【补充毕业论文版本管理案例】，第一个commit我写了"最终版_真的最终版.docx"那个例子；用表格把传统做法对应到 Git 概念（commit/branch/PR/merge/conflict）；写了一个具体场景"导师让改研究背景"，从分支到 merge 全流程。第二个commit我在文件末尾追加了"导师意见如何追踪"那一节，对比了 Word 批注 vs PR inline comment 的差别。最后是浩楠merge进了main。
 
### Q6你们组如何制造冲突？冲突发生在哪个文件？最终怎样合并两边意思？
答：我们组一开始尝试了好几次如何制造冲突都失败了，我们的练习文件是docs/shared-summary.md，后来我们发现冲突产生的关键条件是两个PR都要还open着，不能等其中一方merge完再让另一方动，应该让两个人各自在conflict-a和conflict-b分支上改同一句话，然后紧接着一方先merge进main，另一方merge时产生碰撞。由后merge的那个人来resolve，不是二选一，而是把两边意思融合成新的句子。我们组的conflict发生在docs/shared-summary.md 这个文件。
 
### Q7.worktree 是什么？它和 branch 的关系是什么？
答：worktree是同一个repo的多个本地文件夹和工作目录，而branch是修改路线，worktree 是这条路线对应的实际文件夹，一个worktree同一时刻可以打开一条branch。
 
### Q8.什么时候“多个 branch”已经够了？什么时候需要“一台设备多个 worktree”？请各举一个例子。
答：只用“多个branch”就已经够了的情况的核心特征应该是一次只需要做一件事，做完一件事再切下一件事，不需要同时打开两个branch的内容。比如这次训练中我写thesis- case的全过程，我只在feature/thesis-case-stella这一个分支上工作，做完之后再切换别的，从头到尾只有一个worktree。而需要多个worktree的情况下的核心特征是两件事需要同时进行，或者我需要同时打开两条branch的内容。比如说我的组员joy同时做PR#3和#4的时候，他需要让agent同时修改worktree-notes.md和agent-prompts.md，对应两个worktreeA和B。
 
### Q9.如果你是老师，你如何审计一个 repo 是否真的通过 PR 合并，而不是直接改 main？
答：可以在main里直接查看commit历史里有没有Merge pull request #X这种message，或者看Pull request列表里，有没有真实的PR，或者看PR里有没有review评论和approve事件，判断是真协作还是走过场。
 
### Q10.使用 coding agent 做 Git 操作时，你最担心的一个危险动作是什么？你会怎样写提示词避免它？
答：我最担心的coding agent危险动作是git reset --hard,因为这个会覆盖本地修改,没保存过的东西全会消失。我写提示词的时候会显示列出“不允许做什么”的黑名单,让agent先报告状态再行动,且危险操作必须等人确认不能自己率先执行。我昨天在PR#7里留下过review comment,建议补充“暂停后判断逻辑”,这呼应了危险操作需要等人确认的思想。
 
 
 
 
 
 






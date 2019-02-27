Git教程: https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

常用命令：
初始化仓库: git init
仓库中添加文件: git add xxx
                git commit -m "提交说明
                修改后提交也是同样的步骤
                commit是一个快照，之后可恢复到这个commit
                add是把要提交的所有修改放到暂存区stage，commit一次性把暂存区的所有修改提交到分支
常看仓库当前状态: git status
查看不同: git diff xxx
查看提交日志: git log [--pretty=oneline]
更改版本: git reset --hard HEAD^   (从当前版本向之前回退^ ^^ ~20)
          git reset --hard xxxx    (指定版本号)
查看命令历史，也方便了解HEAD指针的变化: git reflog
撤销工作区的全部修改: git checkout -- xxx   (回到最近一次commit或add时的状态，如果add又撤销了，就当没add过)
撤销暂存区的修改: git reset HEAD xxx
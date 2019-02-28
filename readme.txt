Git教程: https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

一般是先创建远程仓库，然后从远程仓库克隆
要推送到远程仓库，远程仓库得public

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
删除文件,在工作区删除文件后，还要从仓库中删除: git rm xxx
                                               git commit -m "删除了某文件
如果误删了工作区的文件，就从仓库恢复: git checkout -- xxx

生成密钥: ssh-keygen -t rsa -C "youremail@example.com"
关联远程仓库: git remote add origin git@server-name:path/repo-name.git
第一次推送master分支所有内容: git push -u origin master
之后本地提交: git push origin master
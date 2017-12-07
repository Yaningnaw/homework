# homework
MyFirstHomework

git config配置本地仓库

常用git config --global user.name、git config --global user.email

git config --list查看配置详情

git init 初始一个仓库，添加--bare可以初始化一个共享（裸）仓库

git status 可以查看当前仓库的状态

git add“文件” 将工作区中的文件添加到暂存区中，其中file可是一个单独的文件，也可以是一个目录、“*”、-A

git commit -m '备注信息' 将暂存区的文件，提交到本地仓库

git log 可以查看本地仓库的提交历史

git branch查看分支

git branch“分支名称” 创建一个新的分支

git checkout“分支名称” 切换分支

git checkout -b deeveloper 他健并切到developer分支

git merge“分支名称” 合并分支

git branch -d “分支名称” 删除分支

git clone “仓库地址”获取已有仓库的副本

git push origin “本地分支名称:远程分支名称”将本地分支推送至远程仓库，

git push origin hotfix（通常的写法）相当于

git push origin hotfix:hotfix

git push origin hotfix:newfeature

本地仓库分支名称和远程仓库分支名称一样的情况下可以简写成一个，即git push “仓库地址” “分支名称”，如果远程仓库没有对应分支，将会自动创建



git remote add “主机名称” “远程仓库地址”添加远程主机，即给远程主机起个别名，方便使用

git remote 可以查看已添加的远程主机

git remote show “主机名称”可以查看远程主机的信息

 

在项目开发过程中，经常性的会遇到远程（共享）仓库和本地仓库不一致，我们可以通过git fetch 命令来更新本地仓库，使本地仓库和远程（共享）仓库保持一致。

 

git fetch  “远程主机”

 

或者

 

git fetch “远程主机” “分支名称”

 

我们要注意的是，利用git fetch 获取的更新会保存在本地仓库中，但是并没有体现到我们的工作目录中，需要我们再次利用git merge来将对应的分支合并（融合）到特定分支。如下

 

git pull origin 某个分支， 上操作相当于下面两步

 

git fetch

 

git merge origin/某个分支

 

问题：如何查看远程主机上总共有多少个分支？

 

git branch -a 便可以查看所有(本地+远程仓库)分支了

 

删除远程分支git push origin --delete 分支名称
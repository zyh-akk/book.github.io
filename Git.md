<h1>Git Start</h1>
git 本地仓库由三棵树组成，一个是工作目录，一个是暂存区（保存改动），一个是HEAD保存最后一次提交的结果。

git基础命令：

1、git init 初始化仓库，git config --global user.name “[name]” 设置用户名，git config --global user.email “[email]” 设置邮箱（必备）

2、git clone path 创建本地仓库或拉取远程仓库

3、git add <fileName>添加修改文件到本地

  git add .添加本分支所有修改文件
4、git commit -m '自定义代码修改注释'

  git commit -a -m '自定义所有提交的文件的代码修改注释'
    commit是把文件提交到本地的HEAD
5、git push origin master // master可以是远程连接的任意分支

6、git checkout -b newBranch // 创建新分支并切换到新分支

7、git branch -d <branch> // 快捷删除另一个分支

  git branch -D &lt;branch&gt;    //  强制删除分支！

  git branch -r    //  列出所有远端分支
8、git push origin <branch> // 将本地分支(包括本地的修改，一次性直接推送，会隐藏注释细节)推送到远端仓库

9、git fetch拉取远端代码，git merge 将拉取的代码与本地代码合并，git pull是集合了前两个的功能，拉取即合并（所有操作都是本地进行，下次提交会包含合并的信息）

10、git log // 查看从最新提交开始的所有提交记录

11、git checkout -- <fileName> // 此命令会使用 HEAD 中的最新内容替换掉你的工作目录中的文件。已添加到暂存区的改动以及新文件都不会受到影响！

12、git grep ‘words’ // 从当前目录查找文本内容

13、git push origin --delete <branch> // 删除远程分支

14、git reset --hard HEAD // 放弃工作目录下所有修改

    git reset HEAD    //  移除缓存区文件，相当于撤销上次的git add

15、git gc       //  项目比较大时，靠压缩历史信息来减小体积

16、 git fsck       //  运行仓库的一致性检查

17、 git submodule
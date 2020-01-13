# 伪元素
# 练习
#  git 使用

使用终端命令行将本地项目上传到Github并提交代码
第一步： 在Github上创建自己的repository

第二步：建立本地仓库cd到你的本地项目根目录下，执行git命令

1：$ cd 到你的项目目录下

2：$ git init

第三步：将本地项目工作区的所有文件添加到暂存区

3：$ git add . 

第三步：将暂存区的文件提交到本地仓库

4：$ git commit -m "注释"

第五步：将本地仓库关联到Github上

5：$ git remote add origin https://github.com/zhibinhsu/ShowAllLabel.git  用自己的url（创建的仓库的地址，赋值地址栏里面的地址即可）

这步骤如果提示错误：fatal: remote origin already exists. 解决办法如下：

　　1、先删除远程 Git 仓库 $ git remote rm origin 

　　2、再重新添加远程 Git 仓库 $ git remote add origin https://github.com/zhibinhsu/ShowAllLabel.git  用自己的url（创建的仓库的地址，赋值地址栏里面的地址即可）

 

同步到服务器

6：$ git push -f origin master


克隆项目在本地
1、进入要存放的目录
2、终端执行 git clone + github 地址




git 提交开发的文件

进入目录
git pull
git add .
git commit -m "描述文件"
git push 



git 删除本地分支命令：
git branch -d + 分支名称
git 删除远程分支命令：
git push  origin -d +分支名称


git 版本回退：
git reset --hard HEAD^    回退到上一个版本


小结
Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>或者git switch <name>

创建+切换分支：git checkout -b <name>或者git switch -c <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>




Git还提供了一个stash功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作：
首先确定要修改的分支，切换到当前分支：
 如：1、git checkout master
     2、git checkout -b issue-101
     在当前分支下开发结束后提交commit 
     在切换到master分支下, 
     执行 合并分支
     3、git merge --on--ff -m "合并临时版本" issue-101

     太棒了，原计划两个小时的bug修复只花了5分钟！现在，是时候接着回到dev分支干活了！

     git switch dev  //切换到dev 

     工作区是干净的，刚才的工作现场存到哪去了？用git stash list命令看看：
     git stash list
     $ git stash list
stash@{0}: WIP on dev: f52c633 add merge
工作现场还在，Git把stash内容存在某个地方了，但是需要恢复一下，有两个办法：

一是用git stash apply恢复，但是恢复后，stash内容并不删除，你需要用git stash drop来删除；

另一种方式是用git stash pop，恢复的同时把stash内容也删了：


思考一个问题 刚才master分支上有bug 但是我们当前dev也是从master上分支出来的，所以dev也是有这个bug的

为了方便操作，Git专门提供了一个cherry-pick命令，让我们能复制一个特定的提交到当前分支：







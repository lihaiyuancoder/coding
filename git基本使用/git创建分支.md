创建一个dev分支
1、创建切换一次完成：
git checkout -b dev 
不好理解，还有一种分开写法
git branch dev
git checkout dev
2、然后在执行：
git branch 
会列出所有分支，如果有* 说明就在当前 分支下。
3、然后在用
git add .
git commit -m "提交说明"
4、切换到master分支
git checkout master 
5、然后把git dev分支上的代码合并到master上,合并指定分支到当前分支
git merge dev
6、然后删除dev
git branch  -d dev
7、查看还有那个分支
git branch 


小结
Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>或者git switch <name>

创建+切换分支：git checkout -b <name>或者git switch -c <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>







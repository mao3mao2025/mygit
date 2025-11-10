# README.md

* 1.first line
* 2.second line
* 3.third line
* 4.hello Java
* 5.hello world

## 1.在任何分支执行：git pull的作用？
		** 拉取当前所在分支上新的commit
		** 追踪其他分支是否有新的commit

## 2.如果我想从远程仓库拉取一个本地版本库没有的分支如何实现？
	** 在本地仓库创建一个同名仓库：`git branch test`
	** 绑定本地仓库与远程仓库的关系:`git branch --set-upstream-to=origin/test test`(可在任意分支执行)
	上面两部也可以合并成一步：
		`git checkout -b test origin/test`:在本地创建一个test分支，并与远程仓库中的分支关联
	** 在test分支中拉取远程仓库：`git pull`
	
## 3.删除远程分支test1：`git push origin -d test1`
## 4.在远程仓库创建一个分支：`git push origin test:test1`(NOTE：同时还会将本地分支test推送到远程仓库,远程本地分支还会建立追踪关系)

## 5.为本地分支设置上游分支：`git branch --set-upstream-to=origin/test1 test`
		NOTE:为本地分支设置上游分支之后，只能本地追踪上游的变化，不能直接推送，即执行git pull,不能直接git push,要想执行：`git push origin test:test1`.
## 6.清楚本地分支的上游分支：`git branch --unset-upstream`(需在对应的分支上执行)
	
## 7.保存当前分支工作去的修改，但是还没有提交记录： `git stash`
## 8.执行git stash保存的记录：`git stash pop`(会删除相应的记录，且执行的是第一条)
## 9.执行git stash保存的记录：`git stash apply`(不会删除记录，且执行的是第一条)




	


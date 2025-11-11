# README.md

* 1.first line
* 2.second line
* 3.third line
* 4.hello Java
* 5.hello world

## 1.在任何分支执行：git pull的作用？
	**拉取当前所在分支上新的commit**
	**追踪其他分支是否有新的commit**

## 2.如果我想从远程仓库拉取一个本地版本库没有的分支如何实现？
	在本地仓库创建一个同名仓库：`git branch test`
	绑定本地仓库与远程仓库的关系:`git branch --set-upstream-to=origin/test test`(可在任意分支执行)
	上面两部也可以合并成一步：
		`git checkout -b test origin/test`:在本地创建一个test分支，并与远程仓库中的分支关联
	在test分支中拉取远程仓库：`git pull`
	
## 3.删除远程分支test1：`git push origin -d test1`
## 4.在远程仓库创建一个分支：`git push origin test:test1`(NOTE：同时还会将本地分支test推送到远程仓库,远程本地分支还会建立追踪关系)

## 5.为本地分支设置上游分支：`git branch --set-upstream-to=origin/test1 test`
		NOTE:为本地分支设置上游分支之后，只能本地追踪上游的变化，不能直接推送，即执行git pull,不能直接git push,要想执行：`git push origin test:test1`.
## 6.清楚本地分支的上游分支：`git branch --unset-upstream`(需在对应的分支上执行)
	
## 7.保存当前分支工作去的修改，但是还没有提交记录： `git stash`
## 8.执行git stash保存的记录：`git stash pop`(会删除相应的记录，且执行的是第一条)
## 9.执行git stash保存的记录：`git stash apply`(不会删除记录，且执行的是第一条)

## 10.`git tag V1.1.0`	创建一个轻量级标签 指向当前最新的一个commit
## 11.`git tag -a V1.1.0 -m "message" `"创建一个带注释的标签,会创建一个tag对象，该标签指向该tag对象，该tag对象指向最新的commit对象" 

## 12.上传标签到远程
1.`git push origin v1.0.0`上传一个本地标签v1.0.0到远程仓库
2.`git push origin v1.0.0 v1.1.0`上传v1.0.0 & v1.1.0到远程仓库
3.`git push origin --tags`上传本地所有标签到远程仓库

## 13.删除标签
1.删除本地标签：`git tag -d v1.0.0`
2.删除远程标签：`git push origin refs/tags/v1.0.0` ** 最好指定标签前缀：refs/tags/ **

## 14.查看标签详细信息
1.`git show v1.0.0`



	


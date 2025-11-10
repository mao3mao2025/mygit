# README.md

* 1.first line
* 2.second line
* 3.third line
* 4.hello Java
* 5.hello world

## 1.在任何分支执行：git pull的作用？
		* 拉取当前所在分支上新的commit
		* 追踪其他分支是否有新的commit

## 2.如果我想从远程仓库拉取一个本地版本库没有的分支如何实现？
	* 在本地仓库创建一个同名仓库：git branch test
	* 绑定本地仓库与远程仓库的关系:git branch --set-upstream-to=origin/test test(可在任意分支执行)
	上面两部也可以合并成一步：
		git checkout -b test origin/test:在本地创建一个test分支，并与远程仓库中的分支关联
	* 在test分支中拉取远程仓库：git pull
	

	


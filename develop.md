# Develop branch

## 分支相关命令

###
	$git branch -a    查看远程分支
	$git branch       查看本地分支
	
	$git branch develop        创建develop分支
	$git push origin develop   将develop分支推送到远程
	$git checkout develop      切换到develop分支
	$git branch -d develop     删除develop分支
	$git push origin :develop  删除远程develop分支
	
	分支合并
	$git checkout -b myfeature develop   从develop分支创建一个myfeature分支
	
	$ do somework on myfeature and push to origin
	
	$git checkout develop        切换到develop分支
	$git merge --no-ff myfeature 合并myfeature分支, --no-ff标志导致合并操作创建一个新commit对象
	$git branch -d myfeature     删除myfeature分支
	$git push origin develop    
	
	
![参见图](http://static.oschina.net/uploads/img/201302/25142847_b6mx.png)

## 特步备注 Git rebase
当你提交的代码后，管理员发现，您的代码不能提交到服务器上，主要原因在于，你的commit 中和服务器中的有些commit不再同一时间轴上，即：你的有些commit要插入到服务器中的某些commit之间，这样就会造成代码的冲突。所以这个时候就要使用git rebase。

具体可以参考： <http://blog.csdn.net/wh_19910525/article/details/7554489>
	
	
	
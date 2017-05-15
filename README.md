# git_study

## 1. Create a new repository on the command line


###
    $echo "# git_study" >> README.md
    $git init
    $git config user.email "dwh0403@163.com"
    $git config user.name "DavadDi"
    $git add README.md
    $git commit -m "first commit"
    $git remote add origin https://github.com/DavadDi/git_study.git
    $git push -u origin master

## 2. Push an existing repository from the command line


###
    $set user.name and email
    $git remote add origin https://github.com/DavadDi/git_study.git
    $git push -u origin master




## 3. Markdown Sytax Resource


[Markdown Resource] (https://github.com/DavadDi/git_study/blob/master/MarkdownSyntax.md)

## 4. 使用原则

### 中心库一直保留两个分支：
* master 用于存档主要稳定的版本
* develop 分支

### 其他辅助开发分支
* feature branchs
* hot fixs branchs
* release branchs

![参见图](http://static.oschina.net/uploads/img/201302/25142840_pKcL.png)

参见：[介绍一个成功的 Git 分支模型](http://www.oschina.net/translate/a-successful-git-branching-model)

## 5. Git常用命令参考

[Git Community Book中文版](http://gitbook.liuhui998.com/index.html)

![git图](http://www.do1618.com/wp-content/uploads/2016/04/git_big_jb51.jpg)
![git命令图](http://wlog.cn/files/img/git.png)

代码审核提交的命令：

将这个commit推送到git 服务器上面一个临时branch：

git push origin HEAD:cr-style-improvement

## 6. 精品教材

* [连猴子都能懂的Git教程](https://backlogtool.com/git-guide/tw/intro/intro1_1.html)
* [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html) [中文](https://marklodato.github.io/visual-git-guide/index-zh-cn.html)
* [Visualizing Git Concepts with D3](http://onlywei.github.io/explain-git-with-d3)
* [Git 取消修改，恢复版本 命令大全](http://blog.csdn.net/cankingapp/article/details/18312117)


## 7. MyBlog


[www.do1618.com](http://www.do1618.com)<br />

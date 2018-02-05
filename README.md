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

###参见
1. [介绍一个成功的 Git 分支模型](http://www.oschina.net/translate/a-successful-git-branching-model)
2. [Git Tutorials](https://www.atlassian.com/git/tutorials)  见过的最简单易懂的介绍 <br \> 中文 [Git工作流指南：Gitflow工作流](http://blog.jobbole.com/76867/) 
3. [Git 版本管理：Git Flow 模型](http://blog.jobbole.com/100264/)  一款方便使用git flow的工具，通过流程简化了git-flow模型的操作，方便同事合作与约定， [GitHub地址](https://github.com/nvie/gitflow)


## 5. Git常用命令参考

1. [Git Community Book中文版](http://gitbook.liuhui998.com/index.html)
2. [分支和Tag相关操作](https://github.com/DavadDi/git_study/blob/develop/develop.md)
3. 命令速查 ![git图](http://www.do1618.com/wp-content/uploads/2016/04/git_big_jb51.jpg)



## 6. 如何保持Fork后的项目同步

From: https://help.github.com/articles/syncing-a-fork/

### Configuring a remote for a fork

```bash
$ git remote -v
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)

$ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git

$ git remote -v
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```



### Syncing a fork

```bash
# Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.
$ git fetch upstream
remote: Counting objects: 75, done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 62 (delta 27), reused 44 (delta 9)
Unpacking objects: 100% (62/62), done.
From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
 * [new branch]      master     -> upstream/master

# Check out your fork's local master branch.
$ git checkout master
Switched to branch 'master'

# Merge the changes from upstream/master into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes.
$ git merge upstream/master
Updating a422352..5fdff0f
Fast-forward
 README                    |    9 -------
 README.md                 |    7 ++++++
 2 files changed, 7 insertions(+), 9 deletions(-)
 delete mode 100644 README
 create mode 100644 README.md
 
# If your local branch didn't have any unique commits, Git will instead perform a "fast-forward":
$ git merge upstream/master
Updating 34e91da..16c56ad
Fast-forward
 README.md                 |    5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)
```





## 7. MyBlog


[www.do1618.com](http://www.do1618.com)<br />

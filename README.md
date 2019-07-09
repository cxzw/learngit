git的使用
===============

# 一.git简介
Git是目前世界上最先进的分布式版本控制系统,由Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件
##git的优点
1.分布式
2.开源免费
3.对非线性开发模式的强力支持(允许成千上万个并行开发的分支)
4.有能力高效管理类似 Linux 内核一样的超大规模项目(速度和数据量)

# 二.git的安装
去官网下载安装并一路下一步,安装完成后，在开始菜单里找到“Git”->“Git Bash”，弹出一个类似命令行窗口的东西，就说明Git安装成功
安装完成后在命令行输入
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
# 三.创建git版本库
使用linux语句创建一个空目录
```
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit
```
通过git init命令把这个目录变成Git可以管理的仓库
```
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
```

# 四,连接并推送至远程仓库
在命令行中输入:
```
$ ssh-keygen -t rsa -C "youremail@example.com"
```
登陆github,在账号设置中找到SSH and GPG keys,点击new sshkeys,填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容,然后确认即可.
在github中新建一个仓库,在命令行中输入:
```
$ git remote add origin git@github.com:cxzw/learngit.git
```
即连接到了远程仓库
然后在命令行中输入:
`$ git push -u origin master`
就可以把本地库中的所有内容推送到远程库中

# 五.git常用命令
## git config命令  
用于获取并设置存储库或全局选项。这些变量可以控制Git的外观和操作的各个方面  
## git help命令  
显示有关Git的帮助信息  
## git init命令  
创建一个空的Git仓库或重新初始化一个现有仓库  
## git add命令  
将文件内容添加到索引(将修改添加到暂存区)。也就是将要提交的文件的信息添加到索引库中  
## git clone命令  
将存储库克隆到新目录中  
## git status命令  
用于显示工作目录和暂存区的状态。使用此命令能看到那些修改被暂存到了, 哪些没有, 哪些文件没有被Git tracked到  
## git diff命令  
用于显示提交和工作树等之间的更改。此命令比较的是工作目录中当前文件和暂存区域快照之间的差异,也就是修改之后还没有暂存起来的变化内容  
## git commit命令  
用于将更改记录(提交)到存储库。将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中  
## git reset命令  
用于将当前HEAD复位到指定状态。一般用于撤消之前的一些操作(如：git add,git commit等)  
## git rm命令  
用于从工作区和索引中删除文件  
## git mv命令  
用于移动或重命名文件，目录或符号链接  
## git branch命令  
用于列出，创建或删除分支  
## git checkout命令  
用于切换分支或恢复工作树文件。git checkout是git最常用的命令之一，同时也是一个很危险的命令，因为这条命令会重写工作区  
## git merge命令  
用于将两个或两个以上的开发历史加入(合并)一起  
## git mergetool命令  
用于运行合并冲突解决工具来解决合并冲突  
## git log命令  
用于显示提交日志信息  
## git stash命令  
用于将更改储藏在脏工作目录中  
## git tag命令  
用于创建，列出，删除或验证使用GPG签名的标签对象。同大多数 VCS 一样，Git 也可以对某一时间点上的版本打上标签  
## git fetch命令  
用于从另一个存储库下载对象和引用  
## git pull命令  
用于从另一个存储库或本地分支获取并集成(整合)。git pull命令的作用是：取回远程主机某个分支的更新，再与本地的指定分支合并，它的完整格式稍稍有点复杂  
## git push命令  
用于将本地分支的更新，推送到远程主机。它的格式与git pull命令相似  
## git remote命令  
管理一组跟踪的存储库  
## git submodule命令  
用于初始化，更新或检查子模块  
## git show命令  
用于显示各种类型的对象  
## git shortlog命令用  
于汇总git日志输出  
## git describe命令  
显示离当前提交最近的标签  
## git rebase命令  
在另一个分支基础之上重新应用，用于把一个分支的修改合并到当前分支  

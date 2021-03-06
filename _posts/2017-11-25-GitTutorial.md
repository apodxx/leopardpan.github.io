---
layout: post
title: "Git及GitHub教程"
date: 2017-11-25   
tag: 工具 
---

### 介绍       

　　Git是做项目的版本管理，你也可以称它们为版本管理工具。假如现在你有一个文件夹，里面可以是项目，也可以是你的个人笔记(如我这个博客)，或者是你的简历、毕业设计等等，都可以使用git来管理。
　　gitHub是一个面向开源及私有软件项目的托管平台，因为只支持git 作为唯一的版本库格式进行托管，故名gitHub。

　　目前常用的版本控制器有Git和SVN，即使这两个你没有全用过，至少也会听过，我这里以Git为例，个人比较喜欢Git，你也可以看看这篇文章：[为什么Git比SVN好](http://www.worldhello.net/2012/04/12/why-git-is-better-than-svn.html)。          

### 安装Git

**在Mac OS X上安装Git**      

提供两种方法参考：      

> 1、通过homebrew安装Git，具体方法请参考[homebrew的文档](http://brew.sh/)      
> 2、直接从AppStore安装Xcode，Xcode集成了Git，不过默认没有安装，你需要运行Xcode。     

**在Windows上安装Git**      

> 从[https://git-for-windows.github.io](https://git-for-windows.github.io) 下载，然后按默认选项安装即可，安装完成后，在开始菜单里找到“Git”->“Git Bash”，蹦出一个类似命令行窗口的东西，就说明Git安装成功！


### 配置Git      

安装完成后，还需要最后一步设置，在命令行输入：

>* $ git config --global user.name "Your Name"
>* $ git config --global user.email "email@example.com"

"Your Name"： 是每次提交时所显示的用户名，因为Git是分布式版本控制系统，当我们push到远端时，就需要区分每个提交记录具体是谁提交的，这个"Your Name"就是最好的区分。          

"email@example.com"： 是你远端仓库的email       

--global：用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然我们也可以对某个仓库指定不同的用户名和Email地址。         



### 开始使用-建立仓库：

你在目标文件夹下使命令：    

>* git init  （创建.git文件）      

就会创建一个 `.git` 隐藏文件，相当于已经建立了一个本地仓库。

**添加到暂存区：**      

>* git add .   （全部添加到暂存区）    
>* git commit -m ' first commit'  （提交暂存区的记录到本地仓库）

**将本地仓库上传到远程仓库中**

>* git push  


**新创建代码后，提交到github的流程**
>* echo "# thinkphp" >> README.md
>* git init
>* git add README.md
>* git commit -m "first commit"
>* git remote add origin git@github.com:apodxx/thinkphp.git
>* git push -u origin master





### 将github的项目clone到本地修改,提交
(以后记得补充)
### GitHub的基本操作:

**仓库(repository)**

	仓库用来存放项目代码每一个仓库对应一个项目
	
**收藏(star)**

	收藏项目,方便下次查看

**复制克隆(fork)**

	该fork项目是独立存在的

**发起请求(pull request)**

	别人将fork项目修改后发送请求给原作者,原作者如果感觉不错 则会合并

**关注(watch)**

	关注项目,当项目更新可以收到通知

**事务卡片(issue)**

	举例:张三有一个仓库 李四在使用的时候 发现了一个bug  于是发起一个issue 然后张三在主页的左侧发现issue动态,查看到李四关于bug的内容 于是修改掉 并且回复给李四 说改好了  然后关闭issue

**搜索文件**

	快捷键:按"t"

### 其它   

git branc 查看时如出现

>*  (HEAD detached at analytics_v2)   
>*  dev
>*  master

代表现在已经进入一个临时的HEAD，可以使用 `git checkout -b temp` 创建一个 temp branch，这样临时HEAD上修改的东西就不会被丢掉了。
然后切换到 dev 分支上，在使用 git branch merge temp，就可以把 temp 分支上的代码合并到 dev 上了。

<br>
   


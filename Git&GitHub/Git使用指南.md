# Git简介与安装

Git是是什么？

Git是目前世界上最先进的分布式版本控制系统。

所有的版本控制系统，其实只能跟踪文本文件的改动，比如TXT文件，网页，所有的程序代码等等，Git也不例外。版本控制系统可以告诉你每次的改动，比如在第5行加了一个单词“Linux”，在第8行删了一个单词“Windows”。而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来，也就是只知道图片从100KB改成了120KB，但到底改了啥，版本控制系统不知道，也没法知道。

不幸的是，Microsoft的Word格式是二进制格式，因此，版本控制系统是没法跟踪Word文件的改动的，如果要真正使用版本控制系统，就要以纯文本方式编写文件，并推荐使用utf-8编码。



[github简明指南（漫画形式）](http://rogerdudler.github.io/git-guide/index.zh.html)

[学习git分支及一些常用命令](https://github.com/pcottle/learnGitBranching)



1. HEAD指向你最后一次提交的结果,`git checkout`改变的是HEAD指向的版本号，默认HEAD与master指向一致（？）。改变HEAD指向的版本，可以先通过`git log`查看的各个版本号（哈希值），直接用`git checkout 版本号`即可，由于哈希值太长，git支持通过输入哈希值的前几个有标志性的字符（很随意，还有至于输入几个字符就很随缘了）。有时候输入版本号太麻烦（比如我就想切换到上个版本或者上上个版本），也可以通过使用`^`操作符来切换，如`git checkout HEAD^`，一个`^`表示一级。但是如果我想切换到前100个版本呢？git又提供了一个很好用的操作符`~`，后面带数字，比如`git checkout HEAD~100`，不加参数时和`^`效果一样

2. master是主分支，可以通过

```
git branch branchName
git checkout branchName
```

或`git checkout -b branchName`创建一个分支，并指向这个分支

3. Git里撤销变更的方法很多，这里主要介绍两种方法来撤销变更。一是`git reset`，还有就是`gitrevert`


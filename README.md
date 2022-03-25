通过 

```
git config --global user.name 

git config --global user.email 
```

配置的用户名和邮箱地址，会被写

入到 C:/Users/用户名文件夹/.gitconfig 文件中。这个文件是 Git 的**全局配置文件**，**配置一次即可永久生效**。



如果自己有一个尚未进行版本控制的项目目录，想要用 Git 来控制它，需要执行如下两个步骤：

① 在项目目录中，通过鼠标右键打开“Git Bash” 

② 执行 

```
git init
```

 命令将当前的目录转化为 Git 仓库

**查看状态**

使用 

```
git status
```

 输出的状态报告很详细，但有些繁琐。如果希望以精简的方式显示文件的状态，可以使用如下

两条完全等价的命令，其中 **-s** 是 **--short** 的简写形式

**暂存区**

使用命令 添加进暂存区

```
git add .
```

 开始跟踪。

取消暂存文件

```
git reset HEAD .
```



**将暂存区文件提交仓库**

现在暂存区中有等待被提交到 Git 仓库中进行保存。可以执行 

```
git commit  -m  ""
```

命令进行提交,

其中 -m 选项后面是本次的提交消息，用来对提交的内容做进一步的描述



**从本地仓库移除文件**

从 Git 仓库中移除文件的方式有两种：

① 从 Git 仓库和工作区中同时移除对应的文件

② 只从 Git 仓库中移除指定的文件，但保留工作区中对应的文件

```
git rm -f xxxx

git rm --cached xxxx
```



**SSH key**

① 打开 Git Bash

② 粘贴如下的命令，并将 your_email@example.com 替换为注册 Github 账号时填写的邮箱：

```
sh-keygen -t rsa -b 4096 -C "your_email@example.com" 
```

③ 连续敲击 3 次回车，即可在 C:\Users\用户名文件夹\.ssh 目录中生成 id_rsa 和 id_rsa.pub 两个文件



**查看分支**

使用如下的命令，可以查看当前 Git 仓库中所有的分支列表

```
git branch
```

**创建分支**

```
git branch newbranch
```

**切换分支**

```
git checkout newbranch
git checkout -b newbranch //创建并快速切换
```

**合并分支**

```
git checkout master

git merge newbranch
```

**删除分支**

```
git branch -d newbranch
```

**查看远程仓库所有分支**

```
git remote show origin
```

**跟踪远程分支**

跟踪分支指的是：从远程仓库中，把远程分支下载到本地仓库中。

```
git checkout 远程分支
//下载到本地仓库并改名
git checkout -b 本地分支名称 origin/远程仓库名称
```

**拉取远程分支最新代码**

```
git pull
```

**删除远程分支**

```
git push origin --delete 远程分支名称
```


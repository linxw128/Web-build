# Git
______
### init
```shell
git init
```


### config origin

```shell
git remote add origin https://github.com/linxw128/Web-build.git
```


### branch

```shell
#show branch
git branch
```

```shell
# rename old branch to new branch name "main"
git branch -M main
# equal to:
git branch -M OLDBRANCH NEWBRANCH
```


```shell
git checkout -b NEWBRANCH
```

```shell
# drop modify and retrieve commit of BRANCH
git checkout BRANCH
```

### push
```shell
git push REMOTE-NAME BRANCH-NAME
```

```shell
git push REMOTE-NAME LOCAL-BRANCH-NAME:REMOTE-BRANCH-NAME
```

```shell
git push -u origin main
# equal to:
# set local branch link to the remote branch of origin/main
git branch --set-upstream-to origin/main
git push origin main

```

### pull
```text
git pull看起来像git fetch+get merge。

不要用git pull，用git fetch和git merge代替它。
git pull的问题是它把过程的细节都隐藏了起来，以至于你不用去了解git中各种类型分支的区别和使用方法。
当然，多数时候这是没问题的，但一旦代码有问题，你很难找到出错的地方。看起来git pull的用法会使你
吃惊，简单看一下git的使用文档应该就能说服你。

将下载（fetch）和合并（merge）放到一个命令里的另外一个弊端是，你的本地工作目录在未经确认的情况下
就会被远程分支更新。当然，除非你关闭所有的安全选项，否则git pull在你本地工作目录还不至于造成
不可挽回的损失，但很多时候我们宁愿做的慢一些，也不愿意返工重来。
```

### add
```shell
# add all file in current directory to stage
git add .
```


```shell
# stages all changes
git add -A
```


### status
```
git status
```





相关链接：
[推送提交到远程仓库](https://docs.github.com/zh/get-started/using-git/pushing-commits-to-a-remote-repository)
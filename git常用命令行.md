# git常用命令行

## 1.提交上传

```
git add
git commit -m "..."
```

## 2.查看当前状态及不同

```
git status(当前状态)
git diff FILENAME(不同)
```

## 3.查看提交日志

```
git log（提交日志，从近到远）
git log --pretty=oneline（简化）
```

## 4.回退

```git
git reset --hard HEAD (回退上一版本)
git reset --hard commitID (回退某个版本，id号前几位即可)
```

## 5.查看之前的命令

```
git reflog
```

## 6.查看工作区和版本库里最新版本的区别

```
git diff HEAD -- FILENAME
```

## 7.撤销工作区的修改

```
git checkout -- FILENAME
(自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态）
(已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态）

git reset HEAD FILENAME
(把暂存区的修改撤销掉（unstage），重新放回工作区)
```

## 8.删除文件

```
git rm FILENAME
git commit -m "..."
```

## 9.添加远程库

```
git remote add origin git@github.com USERNAME/REPOSITORYNAME.git
git remote  列出远程主机（-v 可以查看远程主机网址）
```

## 10.推送至远程库

```
git push -u origin master (-u只需要在第一次)
```

## 11.分支操作

```
git checkout -b dev  创建并切换分支为dev
git branch  查看当前分支（带*）
git branch -a(-va 详细) 查看远程及本地分支
git checkout branchName 切换分支
git merge branchNae 合并分支
git branch -d dev 删除dev分支
git checkout -t origin/branchName 切换远程分支
```

## 12.更新

```
git fetch <远程主机名> <分支名>
git pull (会合并)
```



# 参考：

<http://www.ruanyifeng.com/blog/2014/06/git_remote.html>

<https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001374831943254ee90db11b13d4ba9a73b9047f4fb968d000>
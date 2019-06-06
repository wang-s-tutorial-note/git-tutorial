# Git

git is a source code management，(Abbreviation:SCM）,它对当前文件提供版本管理功能，核心思想是对当前文件建立一个对象数据库（object database），将历史版本信息存放在这个数据库中。

![git](https://i.loli.net/2019/06/01/5cf279425807d52945.png)

`A Working Directory`: where you’ll be doing all the work: creating, editing, deleting and organizing files

`A Staging Area`: where you’ll list changes you make to the working directory

`A Repository`: where Git permanently stores those changes as different versions of the project



## git workflow

- install git
- submit usrname and email

```bash
$ git config --global user.name "Some One"
$ git config --global user.email "someone@gmail.com"
```

1. `git init`：creates a new Git repository
2. `git status`：inspects the contents of the working directory and staging area
3. `git add <文件名>`：adds files from the working directory to the staging area
4. `git commit -m "message"`：permanently stores file changes from the staging area in the repository
5. `git log `shows a list of all previous commits
6.` git remote add origin https://github.com/try-git/try_git.git `: 添加远程指针
7. `git push -u origin master`：将本地的master分支推送到远程origin主机，-u参数表示记住对应关系，下次可以直接git push推送。
8. `git pull origin master`：将远程主机origin的代码取回本地，与本地的master分支合并
9. `git diff (HEAD)`： shows the difference between the working directory and the staging area


# 版本回退

## work area

![](https://i.loli.net/2019/06/01/5cf27ad70563b38850.png)



`git checkout HEAD filename`: Discards changes in the working directory.


## on stage

`git reset HEAD filename`: Unstages file changes in the staging area.


## on repository

`git reset commit_SHA`: Resets to a previous commit in your commit history.

![](https://i.loli.net/2019/06/01/5cf27ba3a75f037273.png)


`git branch`: Lists all a Git project’s branches.

`git branch branch_name`: Creates a new branch.

`git checkout branch_name`: Used to switch from one branch to another.

`git merge branch_name`: Used to join file changes from one branch to another.

`git branch -d branch_name`: Deletes the branch specified.



`git clone`: Creates a local copy of a remote.


`git remote` -v: Lists a Git project’s remotes.

### keep -> up-to-date

`git fetch`: Fetches work from the remote into the local copy.

`git merge origin/master`: Merges origin/master(commits) into your local branch.

`git push origin <branch_name>`: Pushes a local branch to the origin remote.


 > push your branch up to the remote, origin. From there, 管理者 can review your branch and merge your work into the master branch, making it part of the definitive project version.
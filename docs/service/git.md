# git命令

## 拉取Git项目到本地

**1. 打开终端，cd到自己想要存放项目的文件夹**
```bash
cd /Users/ioskaifa/Desktop
```
**2. 输入git clone url,url为你要拉取的项目地址**

```bash
git clone https://github.com/popdo/uewiki.git
```
**3.项目拉取成功。**

## 项目改动后上传到GitHub

**1. git add 你改动后的文件,如果想要全部上传 git add .**
```bash
git add .
```
**2. 执行git commit -m “添加注释”**
```bash
git commit -m "注释"
```
**3. git push 上传，可能会让你输入github账号和密码按提示输入即可**
```bash
git push
# git push是git push origin master的简写，如果要使用git push 你就要保证你的绑定的远程仓库只有一个，并且只有一个分支
```

## 本地新库同步到github新仓库

```bash
git init
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/popdo/wiki.github.io.git
git push -u origin master
```
## 本地现有库同步到github新仓库
```bash
git remote add origin https://github.com/popdo/wiki.github.io.git
git branch -M master
git push -u origin master
```

## git命令
查询当前远程的版本
```bash
git remote -v
```
将新建的文件或修改过的文件添加到索引库
```bash
git add .
```
本地分支代码保存到本地仓库
```bash
git commit -m " 注释"
```

直接拉取并合并最新代码
```bash
git pull origin master // 拉取远端origin/master分支并合并到当前分支

git pull origin dev // 拉取远端origin/dev分支并合并到当前分支
```

从本地提交代码到服务器
```bash
git push origin master // 将当前分支提交到远端origin/master分支
# push到GitHub的文件要求小于100M
```
本地与服务器端同步
```bash
git pull
```

查看所有用户
```bash
git config --list 
```

查看状态
```bash
git status
```

查看变更内容
```bash
git diff
```
查看所有本地分支
```bash
git branch
```

```bash

```

```bash

```

```bash

```

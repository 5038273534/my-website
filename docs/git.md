---
sidebar_position: 2
---

### 相关官网
git:<https://git-scm.com>   
git for windows:<https://gitforwindows.org>  
GitHub:<https://github.com>  
GitLab:<https://about.gitlab.com>  
Gitee:<https://gitee.com>

Git学习网址:<https://www.w3cschool.cn/git>

### 客户端下载
TortoiseGit:<https://tortoisegit.org/download/>


```bash
touch a.txt //创建文件
mkdir dos// 创建目录
cd dos //进入目录
ll
ls //查看文件列表不包含隐藏文件
ls -a //查看文件包含隐藏文件
pwd //查看当前路径
cat //查看文件内容
code . //vscode 打开当前目录
```

### 查询版本
```bash
git -v
git --version
```

### 基本配置与查询
```bash
# 配置提交标识，有空格用双引号，无空格可不加双引号
git config --global user.name <"用户名"> 
git config --global user.email <"用户邮箱">
git config --global credential.helper store # 长期储存密码
git config --global --list # 查询配置

git ls-files # 查看暂存区的文件
```

### 创建化仓库
```bash
git init
git init <项目名>  # 在本地创建个仓库
git clone <远程仓库地址> # 从远程下载个仓库 （克隆项目）
```

### 分支
```bash
# 查询
git branch # 本地所有分支
git branch -r # 远程所有分支
git branch -a #（本地+远程）所有分支

# 创建
git branch <分支名> # 本地分支

# 修改
git branch -M <分支名> 

# 删除
git branch -d <分支名>  # 本地分支
git branch -D  <分支名> # 本地分支（有修改未提交）强制删除
git push <远程分支名|origin> -d <分支名> # 远程分支

# 切换
git checkout -b <分支名> # 创建并且切换分支
git checkout <commitID>  # 切换到指定版本

# 不常用
git branch -v 
git branch -f < 分支名> # 覆盖同名分支
git branch -D/-d <分支名|master> <分支名|develop> # 删除本地库master develop
git branch --merged # 已经合并的分支列表

```

### 查询修改的文件
```bash
git status
git status -s
```

### 添加到暂存区
```bash
git add <文件名>
git add . # 添加所有文件
git add *.txt # 添加所有.txt 后缀的文件
```

### 取消暂存区文件
```bash
git rm <文件名>  # 工作区暂存区文件都删除，要记得commit
git rm <文件名> -f # 强制删除
git rm --cached <文件/目录> # 删除暂存区文件，工作区文件保留
git rm -r --cached <文件/目录>
```


### 提交到本地仓库
```bash
git commit -m "提交备注"
git commit -a -m "提交备注"  # 添加到暂存区并且提交到本地库 只能是所有的修改的文件，新文件不能
```
### 查看提交记录
```bash
git log # 详细
git log --online # 简洁
```

### reset命令 回退版本
```bash
git reset HEAD^ # 工作区保留、暂存区不保留
git reset --soft <commitID> # 回退到指定版本， 工作区和暂存区文件都保留
git reset --hard HEAD^ # 回退到上一个版本， 工作区和暂存区文件都不保留
git reset --mixed # 工作区保留、暂存区不保留
```

### diff命令 文件比对
```bash
git diff # 工作区 vs 暂存区
git diff HEAD # 工作区+ 暂存区 vs 本地仓库
git diff --cached # 暂存区 vs 本地仓库
git diff --staged  # 暂存区 vs 本地仓库
git diff fee9f9cf4b cdd577e352  # 两个版本差异
git diff HEAD~ HEAD # 当前版本与上个版本差异 
git diff HEAD^ HEAD # 当前版本与上个版本差异
git diff HEAD~2 HEAD # 当前版本与上2个版本差异
git diff develop master # 两个分支的差异

```



### 取消修改内容（没有add的状态）
```bash
git restore <文件名> # 取消指定文件
git restore .  # 取消所有文件
```



### 标签
```bash
# 查看所有标签
git tag

git show <标签名>

# 打标签
git tag <标签名>
git tag -a <标签名> -m "标签注释"
git tag <标签名> <提交的commit版本id>

# 删除
git tag -d <标签名>
git push <origin> --delete <标签名>
#删除远程标签

# 提交所有tag到远程
git push origin --tags
```


### 合并分支
```bash
git merge <分支名>

```

### 关联远程地址
```bash
git remote add <远程库名|origin> <远程仓库地址>  # 关联
git remote rm <远程库名|origin> // 解除关联
git remote -v # 查询关联列表
```

### 推送到远程仓库
```bash
git push -u origin <远程分支名:本地分支名>  # 推送到远程，名称相同可以如下简写
git push -u origin <分支名>  #推送到远程
git push origin <分支名> -f // 强制推送到远程仓库 （慎重）
```



### 拉取远程代码到本地仓库
```bash
git pull origin <分支名>  //拉取代码
git pull --rebase origin master
```


### 生成密钥
```bash
# 在命令行 根目录执行
ssh-keygen -t ed25519 -C "xxxxx@xxxxx.com"  #回车三次

ssh-keygen -t rsa -C "your_email@youremail.com"

ssh-keygen -t rsa -b 4096
# 当前电脑用户文件夹下找到：.ssh/id_rsa.pub，里面有密钥

公密钥
~/.ssh/id_ed25519.pub

```



```
遇到的问题：

产生：
在master 本地分支时 切换到 master 指定的commit id 的版本 
提交失败

git push master HEAD:<name-of-remote-branch>

```
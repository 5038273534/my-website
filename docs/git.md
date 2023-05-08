---
sidebar_position: 2
---

git:<https://git-scm.com>   
git for windows:<https://gitforwindows.org>  
GitHub:<https://github.com>  
GitLab:<https://about.gitlab.com>  
Gitee:<https://gitee.com>

### 客户端
TortoiseGit:<https://tortoisegit.org/download/>

### 查询版本
```bash
git -v
git --version
```

### 配置提交标识
```bash
git config --global user.name <"用户名"> 
git config --global user.email <"用户邮箱">
```

### 初始化仓库
```bash
git init <项目名>
```

### 克隆项目
```bash
git clone <远程仓库地址>
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
git push <远程分支名|origin> -d <本地分支名> # 远程分支

# 切换
git checkout -b <分支名> # 创建并且切换分支
git checkout <commitID>  # 切换到指定版本

# 不常用
git branch -v 
git branch -f < 分支名> # 覆盖同名分支
git branch -D/-d <分支名|master> <分支名|develop> # 删除本地库master develop
git branch --merged # 已经合并的分支列表

```

### 取消修改内容（没有add的状态）
```bash
git restore <文件名> # 取消指定文件
git restore .  # 取消所有文件
```

### 查询修改的文件
```bash
git status
```

### 添加到暂存区
```bash
git add . # 添加所有文件
```

### 标签
```bash
# 查看所有标签
git tag

# 打标签
git tag <标签名>
git tag -a <标签名> -m "标签注释"

# 删除
git tag -d <标签名>

# 提交所有tag到远程
git push origin --tags
```
###
```bash
git rm -r --cached <文件|目录>
git rm --cached <文件|目录> //删除暂存区中文件
```



### 提交本地仓库
```bash
git commit -m "提交备注"
git commit -a -m "提交备注"  // 添加到暂存区并且提交到本地库 只能是所有的修改的文件，新文件不能
```


### 合并分支
```bash
git merge <分支名>

```


### 查询版本记录
```bash
git log
```

### 关联远程地址
```bash
git remote add <远程库名|origin> <远程仓库地址> // 关联
git remote rm <远程库名|origin> // 解除关联
git remote -v //查询关联列表
```

### 推送到远程仓库
```bash
git push -u origin <分支名>  //推送到远程
git push origin <分支名> -f // 强制推送到远程仓库 （慎重）
```



### 拉取远程代码到本地仓库
```bash
git pull origin <分支名>  //拉取代码
git pull --rebase origin master
```


### 生成密钥
```bash
gitee
ssh-keygen -t ed25519 -C "xxxxx@xxxxx.com"  #回车三次

公密钥
~/.ssh/id_ed25519.pub

```
### 删除缓存文件
```bash
git rm -r --cached unpackage

```

```
遇到的问题：

产生：
在master 本地分支时 切换到 master 指定的commit id 的版本 
提交失败

git push master HEAD:<name-of-remote-branch>

```
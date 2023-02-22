---
sidebar_position: 2
---

git:<https://git-scm.com>   
git for windows:<https://gitforwindows.org>  
GitHub:<https://github.com>  
GitLab:<https://about.gitlab.com>  
Gitee:<https://gitee.com>

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
git branch -a //查询本地+远程分支列表
git branch <分支名>  //创建分支
git branch -M <分支名> // 修改当前分支名
git branch -d <分支名> //删除分支
```

### 暂存区
```bash
git add . //添加所有文件到暂存区
```

### 标签
```bash
git tag <标签名>
```

### 查询状态
```bash
git status
```

### 提交本地仓库
```bash
git commit -m "提交备注"
git commit -a -m "提交备注"  // 添加到暂存区并且提交到本地库 只能是所有的修改的文件，新文件不能
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
遇到的问题：

hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.


### 拉取远程代码到本地仓库
```bash
git pull origin <分支名>  //拉取代码
```
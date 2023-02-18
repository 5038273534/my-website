---
sidebar_position: 1
---

###### 配置提交时的标识


```
git config --global user.name <"用户名"> //配置用户名 
git config --global user.email <"用户邮箱"> //配置用户邮箱 
```

###### 初始化仓库

```
git init <项目名>
```

###### 克隆项目

```
git clone <远程仓库地址>
```

###### 分支
```
git branch <分支名>  //创建分支
git branch -M <分支名> // 修改当前分支名
```


###### 暂存区
```
git add . //添加所有文件到暂存区
```

###### 关联远程地址

```
git remote add <远程库名|origin> <远程仓库地址> // 关联
git remote rm <远程库名|origin> // 解除关联
git remote -v //查询关联列表
```

###### 推送到远程仓库

```
git push -u origin <分支名>  //推送到远程
```
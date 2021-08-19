# Start

## 方法1：克隆现有的仓库
直接`git clone xx` 克隆，vscode开箱即用

## 方法2：关联远程仓库
1. `git init` 初始化项目（此时在文件夹操作文件，有效提交时会创建默认master分支！）
2. `git remote add xyz abc` 添加远程仓库abc，取名xyz
3. `git pull origin main` 拉取远程origin/main分支，或
4. `git pull xyz abc --allow-unrelated-histories` 拉取远程xyz/abc分支,允许没有关系的分支合并
  - 报 “fatal: couldn't find remote ref master”，远程分支master不存在
3. `git branch`，`git remote show origin` 查看当前分支、远程仓库origin的详细信息
3. `git branch -m xxx yyy` 将本地分支名xxx改为远程分支名yyy
5. `git push -u xyz abc` 推送给远程仓库，并指定xyz为默认主机

# 常用命令

## 基础命令

#### 配置本地账户
1. `git config --global user.name 'xx'`
2. `git config --global user.email 'xx'`
#### 初始化项目
1. `git init`
2. `git clone xxxxx`
3. `git remote add xxx  yyyy` 添加远程仓库yyy，名字为xxx
#### 更改保存
1. `git add .`
2. `git commit -m "xxxx"`
3. `git pull` 相当于拉取和合并！！（出错概率大）
4. `git push` 推送
#### 分支管理
1. `git branch xxx` 创建分支
2. `git checkout xxx` 切换分支
3. `git merge xxx` 合并xxx到当前分支
4. `git branch -d xxx` 删除分支

## 远程仓库
- `git remote -v` 查看远程仓库
- `git remote add pb https://github.com/engureguo/webserver.git` 添加远程仓库起名为pb
- `git fetch pb` 拉取远程仓库
- `git remote remove pb` 移除远程仓库pb
- `git push pb main` 推送到远程仓库origin的main分支
- `git push -u origin main` 推送，同时指定origin为默认主机
- `get remote show origin` 查看origin仓库的更多信息
```
* remote origin
  Fetch URL: git@github.com:engureguo/simple-site.git
  Push  URL: git@github.com:engureguo/simple-site.git
  HEAD branch: main
  Remote branch:
    main tracked
  Local branch configured for 'git pull':
    main merges with remote main
  Local ref configured for 'git push':
    main pushes to main (up to date)
```

## 分支操作

1. `git branch -m oldName  newName` 分支改名
2. `git branch --list` 查看所有分支
3. `git checkout xx` 切换分支
4. `git branch -b 创建并切换分支`
5. `git merge xxxx` 将xxxx分支合并到当前分支

# 参考

- git中文参考：https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%85%B3%E4%BA%8E%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6
- https://blog.csdn.net/weixin_39565021/article/details/111216277
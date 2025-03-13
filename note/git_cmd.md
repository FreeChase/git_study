# 
# git命令记录


## 比较工具

//配置 bc3 为比较工具
git config --global diff.tool bc3
 
git config --global difftool.bc3.cmd '"E:\Program Files\Beyond Compare\BComp.exe" "\$LOCAL" "\$REMOTE"'
 
 
git config --global merge.tool bc3
 
git config --global mergetool.bc3.cmd '"D:\1.software\BeyondCompare3\BComp.exe" "$LOCAL" "$REMOTE"'


## 远端管理

- git remote -v：查看远端仓库地址
- git fetch：更新远端追踪分支
- git status / git branch -vv：查看当前分支与远端的同步情况
- git remote show origin：显示远端详细信息

## 本地管理

- git log //显示操作记录
- git pull //拉去remote仓库
- git push -u origin main   //推送main分支到remote仓库
- git branch    //查看分支信息

## 查看Git 配置信息

### 查看完整的 Git 配置信息

```lua
git config --list --global  # 显示全局 Git 配置
git config --list --local   # 显示当前仓库的 Git 配置
git config --list           # 显示所有（包括系统级、全局和本地）Git 配置

```

###  查看当前用户的 Git 配置信息
```lua
git config --global user.name  # 查看全局用户名
git config --global user.email # 查看全局用户邮箱

git config --local user.name   # 查看当前仓库的用户名
git config --local user.email  # 查看当前仓库的用户邮箱

```

## 其他记录

```lua
commit b0c5ffeb8554cf69d9997a3c3763122c9dfc0cc1 (HEAD -> main, origin/main, origin/HEAD)

```
- commit b0c5ffeb8554cf69d9997a3c3763122c9dfc0cc1
    这是一串40位的十六进制哈希值，用于唯一标识这一提交。
- `(HEAD -> main, origin/main, origin/HEAD)`
    1. `HEAD -> main`：当前本地仓库的 HEAD 指针指向分支 main，表示你当前所在的分支是 main。
    2. `origin/main`：表示远程仓库（名字通常为 origin）上的 main 分支正好指向这个提交。
    3. `origin/HEAD`：远程仓库默认分支的引用（通常指向 main），也指向这个提交。
    这说明本地和远程仓库在 main 分支上都处于同一个提交状态。




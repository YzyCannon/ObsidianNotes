### 1. 确保上游远程仓库已添加： 如果你还没有将上游远程仓库添加为远程仓库，可以使用以下命令添加：
```
git remote add upstream <上游仓库的远程URL>
```
### 2. 获取上游分支的最新代码： 使用以下命令从上游仓库获取最新的代码：
```
git fetch upstream
```
这将从上游仓库获取最新的代码，但不会自动合并到你的本地分支。
### 3. 合并上游分支的最新代码： 如果你想要将上游分支的最新代码合并到你的本地分支（如master 分支），可以使用以下命令：
```
git checkout master # 确保在本地的 master 分支上 
git merge upstream/master
```
这将会将上游仓库的 master 分支的最新代码合并到你的本地 master 分支中。

# 变更远程仓库
要改变远程仓库的设置，您可以使用Git命令来添加、删除或修改远程仓库。下面是一些常用的Git命令示例：

1. 添加远程仓库：
    
    - 使用HTTPS方式：`git remote add origin https://git.nexhome.cn/1552457022/test.git
    - 使用SSH方式：`git remote add origin ggit@git.nexhome.cn:1552457022/test.git
2. 查看远程仓库列表：`git remote -v`
    
3. 修改远程仓库地址：
    
    - 先移除原有的远程仓库：`git remote remove origin`
    - 再添加新的远程仓库地址：`git remote add origin <new_remote_url>`
4. 删除远程仓库：
    
    - `git remote remove origin`
5. 修改远程仓库名称：
    
    - `git remote rename origin new_origin`
6. 更新远程仓库URL：
    
    - `git remote set-url origin <new_remote_url>`
7. 强制推送到远程仓库：
    
    - `git push -f origin <branch_name>`

请注意，执行这些操作会涉及到对远程仓库的修改，因此请确保您有足够的权限以及正确的操作目标。在进行任何修改之前，请确保备份重要的代码。
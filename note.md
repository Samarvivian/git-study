# 常用命令

- **查看用户姓名与邮箱**  
  1. `git config --global user.name`  
  2. `git config --global user.email`

- **创建本地仓库**  
  1. 创建一个文件夹  
  2. 打开 `git bash`  
  3. 执行命令：`git init`  
  4. 若出现 `.git` 文件夹，说明创建成功

- **暂存文件/提交文件**  
  1. 将文件从工作区递交到暂存区：  
     `git add 文件名`  
     若提交所有文件，则使用：`git add .`  
  2. 将文件从缓存区递交进入仓库：  
     `git commit -m "提交信息"`  
  3. 查看文件状态：  
     `git status`  
  4. 查看提交日志：  
     `git log`  
     查看信息优化：  
     `git log --pretty=online --abbrev-commit --all --graph`  
  5. 撤回到原来状态：  
     `git reset --hard commitID`  
     （可以回到任何状态）  
     若不慎 `clear` 之后丢失了 `commitID`，可以利用 `git reflog` 还原以往的提交记录  
  6. 忽略某些文件：  
     创建 `.gitignore` 文件，添加需要忽略的文件后缀名（例如 `*后缀名`）


# 分支

## 命令

1. **查看分支**  
   `git branch`

2. **创建分支**  
   `git branch 分支名`

3. **切换分支**  
   `git checkout 目标分支名`

4. **创建并切换分支**  
   `git checkout -b 分支名`

5. **将新文件合并到 master 上**  
   先切换到 master 上，再执行：  
   `git merge 分支名`

6. **删除分支**  
   `git branch -d 分支名`




# 远程仓库
## 将本地仓库推送到远程仓库
git push 远程仓库的https 分支名(如果失败,关闭加速器)
如果远程仓库与本地仓库有冲突,想要强行推送的话,先键入 
git pull 远程仓库的http 分支名 --allow-unrelated-histories
## 为远程仓库起别名
git remote add 别名 远程仓库的http
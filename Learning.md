# This is the learning notes of how to git.</h1>

## First chapter--How to make a local repository.</h2>

### Basic operate
#### 1. 初始化仓库  (在你想创建仓库的文件夹下运行git bash) 
    mkdir (仓库名)
    cd (仓库名)
    git init

#### 2. 查看仓库状态
    git status

#### 3. 创建一个md文件，用于说明仓库用途。
    touch README.md
   
#### 4. 向暂存区中添加文件
    git add (文件名)
    git add . (将所有文件添加到暂存区)
    
#### 5. 提交保存信息
    git commit -m "描述信息"
    git commit  //打开编辑器详细编辑信息

#### 6. 查看提交日志
    git log
    git log --pretty=short  //只显示第一行的简述信息
    git log -p [文件名]     //显示所有文件[该文件]的改动（能够显示文件前后差别）
    git diff                //查看当前工作树与暂存区的差别
    git diff HEAD           //查看与最新提交的差别  （***养成提交前查看的好习惯***）

### Branch operate

#### 1. 显示分支
    git branch    //显示分支一览表
    git checkout -b   //创建、切换分支
    git log --graph   //图表形式查看分支

#### 2. 切换分支
    git checkout -b (需要切换到的分支名)  //切换到对应的分支
    //同样效果的命令
    git branch (需要切换的分支名)
    git checkout (需要切换的分支名)

    git checkout -    //切换回上一个分支

#### 3. 合并分支
    git checkout (需要合并到的分支名)  //先切换到目标分支，将其他分支合并到该分支
    git merge --no-ff (被合并的分支)  //该被合并的分支被合并到上行分支

### Change operate
#### 1. 回溯历史版本
    git reset --hard (回溯时间点的哈希值)   //所有内容回溯到之前的状态
#### 2. 推进历史
    git reflog      //查看当前仓库执行过的操作日志
    git reset --hard (需要推进到的时间点的哈希值) //推进到该哈希值时间点
### 3. 消除回溯导致的冲突
    //进入文件中修改，提交即可
### 4. 修改提交信息 
    git commit --amend   //启动编辑器
    //修改提交信息，保存按 在末行模式下，输入命令:wq关闭即可
### 5. 压缩历史（更改历史）
    git rebase -i HEAD~2  //编辑器打开2条最新的历史记录
    //使用编辑器修改

### Push to internal storage
#### 1.添加远程仓库
    git remote add origin (仓库的SSH)
#### 2. 推送
    git push -u origin （分支名）  //推送该分支
    git push -b (分支名)   //创建并推送分支

### Pull storage
#### 1. 获取远程仓库
    //在另一个目录下运行git bash
    git clone (SSH)  //将网络仓库克隆到本地
    git checkout -b (本地新建分支名) origin/(远程分支名)  //将远程仓库的分支克隆
    git push  //直接推送处于该情况下的分支
    
#### 2. 获取最新的远程仓库分支
    git pull origin (分支名)
    
    

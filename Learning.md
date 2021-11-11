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

### 1.显示分支
    git branch    //显示分支一览表
    
    git checkout -b
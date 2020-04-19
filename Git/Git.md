# 											**Git**

### 1.初始化

- [ ] ```
  配置信息(只需一次)
  git config --global [该用户] [system :所有用户 ,没有 :该项目] user.name "learnliu"
  git config --global user.email "228625653@qq.com"
  git config --list		查看配置
  ```


- [ ] ```
  git init		初始化仓库
  ```

### 2.Git常用命令

- [ ] ```
  git status														查看当前状态
  git add 文件名		[git add 文件名1 文件名2 ···]		[git add .]   添加到缓存区
  git commit -m "注释内容"	 									 提交到版本库
  ```

### 3.版本回退

- [ ] ```
  git log --pretty=oneline		[git log]				查看版本
  git reset --hard 版本号								  回退操作
  git reflog												查看历史操作，可回到最新版本
  ```

### 4.Github两种使用方式

1. #### 基于http协议

- 克隆仓库

  - [ ] ```
    创建目录，进入
    git clone 线上仓库地址(http地址)				克隆线上仓库到本地
    ```

- 在仓库上做操作

  - [ ] ```
    git add 文件名									 提交暂存区
    git commit -m "注释内容"					     提交本地仓库
    git push									    提交到线上仓库
    git pull										拉取线上仓库
    ```

- 注意：初次提交之前要配置用户名与密码

  - [ ] ```
    vim .git/config
    将
    [remote"origin"]
    	url=https://github.com/用户名/仓库名.git
    改为  
    [remote"origin"]
    	url=https://用户名:密码@github.com/用户名/仓库名.git
    ```

2. #### 基于ssh协议

- 生成客户端公私钥文件

  - [ ] ```
    安装OpenSSH
    ssh-keygen -t rsa -C "注册邮箱"
    ```

- 将公钥上传到Github

  - [ ] ```
    上传  id_rsa.pub
    ```
  

### 5.master分支

- 分支相关命令

  - [ ] ```
    git branch										  查看分支
    git branch 分支名						  			创建分支
    git checkout [-b]    分支名					    [创建并]切换分支
    git branch -d 分支名					 		    删除分支
    git merge 被合并的分支名				  			  合并分支
    ```


### 6.忽略文件

​		有一些不需要改变的目录，或者即使改变了也不想提交至远程仓库，可以使用该机制。
​		忽略文件需要新建一个名为.gitignore 的文件，该文件用于声明忽略文件或不忽略文件的规则，规则对当前目录及其子目录生效。

- [ ] ```
  touch .gitignore					生成.gitignore文件
  添加规则：
  eg:		/js/
  ```

- [ ] ```
  规则：
  /文件夹/							过滤整个文件夹
  *.zip							  过滤所有.zip文件
  /文件/do.c						 过滤某个具体文件
  index.html						  不过滤具体某个文件
  ```

  
### 查看配置:

 	git config -l

### 查看系统配置:

```
git config --system --list
```



### 系统配置文件:

```
Git/etc/gitconfig
```



### 查看当前用户的配置: 	

```
git config --global --list
```



### 用户系统配置文件位置: 

```
C:/用户/当前登录用户/.gitconfig
```



### 配置用户文件: 

```
		git config --global user.name '用户名'

​		git config --global user.email '邮箱'
```





### Git基本理论

```
		本地 -- gti add files --> 暂存区 -- git commit --> 本地仓库 -- git push --> 远程仓库

​		远程仓库 -- git pull --> 本地仓库 -- Git reset --> 暂存区 -- Git checkout --> 本地 
```



### 初始化文件

```
Git init
```



### 克隆远程仓库到本地

```
Git clone [url]
```



## 文件的状态

### 	查看文件状态

```
		Git status 

​		Git status [文件] 查看指定文件的状态
```



```
	Untracked files 未跟踪

​	Git add . 添加当前文件所有内容到暂存区

​	Changes to be committed 暂存区内的文件 , 待提交

​	Git commit -m '提交的信息'  提交到本地仓库, -m 表示提交信息

​	Git push url 提交到远程仓库 
```



## vscode中修改/重置gitlab远程仓库地址

### 方法1：更换git远程仓库地址

```
1.查看当前remotes
     git remote -v
2.修改remotes   
     git remote set-url origin url
```



### 方法2：重置git远程仓库地址

```
 1.删除当前地址
     git remote rm origin
2.新增地址
    git remote add origin url
```





## git上传项目文件

```
ctrl + ~ 打开vscode的控制台(默认在当前打开项目目录)

进入想要上传的目录。以当前目录为例
git init 初始化创建本地仓库
git add 本地文件的名字 把本地想要上传的文件添加到缓存
git commit -m ‘注释’ 提交更新以及提交注释
git remote add origin url 与git远程仓库建立连接
git push -u origin master 将文件传输到仓库中的Master分支中
可以登录github查看提交的项目信息
```

## git的克隆与更新

```
git clone url 命令即可完成项目拉取
注：命令默认拉取Master分支下的文件。若有一定dev（分支）要求可使用：git clone -d Dev名字 url
git push origin master 实现仓库项目的更新(master分支可以替换)
git pull origin master 将clone的项目更新为远程仓库最新内容
```

## 分支

```
创建分支 git branch 分支名称
切换分支 git checkout 分支名称
创建并切换分支 git checkout -b 分支名称
```

## 事例流程

```
git remote add origin http://192.168.55.42/fe/test.git 与远程仓库建立连接
git remote -v 列出详细信息，在每一个名字后面列出其远程url
git checkout -b feature_v1.0 创建并切换分支
git status 查看在你上次提交之后是否有修改
git add . 命令来添加当前项目的所有文件
git commit -m "add: 第一版本所有内容" 提交更新以及提交注释
git push origin feature_v1.0 提交到对应分支
```



## 撤回提交

```
1、查看提交日志git log找到对应commitId
2、回退到之前的版本: git reset --hard commitId
3、git push -f 远程回退
```


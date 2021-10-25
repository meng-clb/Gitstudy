### 查看配置:

 	git config -l

### 查看系统配置:

 	git config --system --list

### 系统配置文件:

​	 Git/etc/gitconfig

### 查看当前用户的配置: 	

​	git config --global --list

### 用户系统配置文件位置: 

​	C:/用户/当前登录用户/.gitconfig

### 配置用户文件: 

​	git config --global user.name '用户名'

​	git config --global user.email '邮箱'



### Git基本理论

本地 -- gti add files --> 暂存区 -- git commit --> 本地仓库 -- git push --> 远程仓库

远程仓库 -- git pull --> 本地仓库 -- Git reset --> 暂存区 -- Git checkout --> 本地 

### 初始化文件

​	Git init

### 克隆远程仓库到本地

​	Git clone [url]

## 文件的状态

### 	查看文件状态

​		Git status 

​		Git status [文件] 查看指定文件的状态

​	Untracked files 未跟踪

​	Git add . 添加当前文件所有内容到暂存区

​	Changes to be committed 暂存区内的文件 , 待提交

​	Git commit -m '提交的信息'  提交到本地仓库, -m 表示提交信息

​	Git push url 提交到远程仓库


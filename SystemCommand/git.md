# git
## 下载与安装
前往[git官网](https://git-scm.com/)下载系统对应版本，无脑安装即可。
          
## 配置用户名和邮箱
```
git config --global user.name "your username"
git config --global user.email "your email"
//针对git config这条命令来说，它有三个参数可供使用，分别是global、local、system
//这三个参数分别是对应全局配置，本地配置以及系统配置
```
配置成功后可以使用以下代码来查看配置信息
```
git config --list
```
## 创建仓库 
一般来说，创建仓库有两种方式，一种是创建本地仓库，另一种则是从远程服务器上克隆一个仓库
```
//这条命令用于初始化当前目录为一个仓库
git init
//如果在这条命令后加上参数，即在后面加上要创建的仓库的名字的话，就会先创建这个目录
//然后再初始化这个目录为一个仓库
git init my_repo
//这条命令则是从远程服务器上克隆一个仓库到本地,url表示的是你需要复制的仓库的地址
git clone url
```
## 
## 添加和提交文件
```
//查看仓库当前状态
git status
//添加文件到暂存区
git add
//提交暂存区的文件到仓库,-m参数用于为这次提交添加提交信息，如果不使用-m参数
//git会默认使用vim编辑器来编写提交信息
git commit -m "message-for-commit"
```
## 版本回退
```
git reset --[soft|hard|mixed]
//soft模式会保留工作区和暂存区的修改
//hard模式不会保留任何修改
//mixed模式只保留工作区的修改
```
## 
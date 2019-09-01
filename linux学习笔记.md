# linux
视频链接https://www.bilibili.com/video/av31976945/?p=8
别人做的笔记：https://blog.csdn.net/weixin_41710054/article/details/89081599#11_6

### 1.linux目录结构
linux系统中，一切皆文件，目录结构为树状
#### 目录用途 (https://www.runoob.com/linux/linux-system-contents.html )
/bin 经常使用的命令  
/boot 启动文件  
/lib 动态链接库  
/etc 系统管理配置  
/boot 启动核心文件  
/dev 外部设备
/media U盘光驱会挂载在该目录下
/opt 安装的软件
/var 日志文件
/selinux 安全子系统，类似于360

### 2.远程登录
远程登录软件：Xshell5 (用SSH中文会乱码)  
远程上传下载软件：Xftp5    

远程登录的条件是远程的linux系统启动了SSHD服务，该服务会监听22号端口  

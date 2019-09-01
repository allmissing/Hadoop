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

### 2.远程登录、上传下载（不需要记，视频P13、P14）
远程登录软件：Xshell5 (用SSH中文会乱码)  
远程上传下载软件：Xftp5    

远程登录的条件是远程的linux系统启动了SSHD服务，该服务会监听22号端口  
linux查看本机ip的方法：ifconfig，在inet address中  

### 3.vi和vim编辑器
正常模式：可以使用快捷键  
插入模式/编辑模式：可以输入内容  
命令行模式：  

### 实用指令
#### 运行级别（配置文件：/etc/inittab）
0： 关机  
1： 单用户（找回丢失密码），进入单用户不需要密码  
2： 多用户无网络
3： 多用户有网络
4： 保留
5： 图形界面
6： 重启

为什么要设置多个级别？->类似于windows有正常模式和安全模式

#### 切换运行级别
命令： init 3

#### 面试题
如何找回root密码，如果不小心忘记root密码，怎么找回？  
答：进入单用户模式，然后修改root密码，因为进入单用户模式，root不需要密码就可以登录。

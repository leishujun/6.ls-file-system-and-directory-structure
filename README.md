# File-system-and-directory-structure
# __文件系统与目录结构__  
  /boot：引导文件存放目录，内核文件(vmlinuz)、引导加载器(bootloader,
grub)都存放于此目录  

/bin：供所有用户使用的基本命令；不能关联至独立分区，OS启动即会用到的
程序  

/sbin：管理类的基本命令；不能关联至独立分区，OS启动即会用到的程序

/lib：启动时程序依赖的基本共享库文件以及内核模块文件(/lib/modules)   

/lib64：专用于x86_64系统上的辅助共享库文件存放位置  

/etc：配置文件目录    

/home/USERNAME：普通用户家目录 

/root：管理员的家目录  

/media：便携式移动设备挂载点  

/mnt：临时文件系统挂载点  

/dev：设备文件及特殊文件存储位置  
b: block device，随机访问    
c: character device，线性访问  

/opt：第三方应用程序的安装位置  

/srv：系统上运行的服务用到的数据  

/tmp：临时文件存储位置

/usr: universal shared, read-only data
bin: 保证系统拥有完整功能而提供的应用程序
sbin:
lib：32位使用
lib64：只存在64位系统
include: C程序的头文件(header files)
share：结构化独立的数据，例如doc, man等
local：第三方应用程序的安装位置
bin, sbin, lib, lib64, etc, share

/var: variable data files
cache: 应用程序缓存数据目录
lib: 应用程序状态信息数据
local：专用于为/usr/local下的应用程序存储可变数据；
lock: 锁文件
log: 日志目录及文件
opt: 专用于为/opt下的应用程序存储可变数据；
run: 运行中的进程相关数据,通常用于存储进程pid文件
spool: 应用程序数据池
tmp: 保存系统两次重启之间产生的临时数据

/proc: 用于输出内核与进程信息相关的虚拟文件系统  

/sys：用于输出当前系统上硬件设备相关信息虚拟文件系统  

/selinux: security enhanced Linux，selinux相关的安全策略等信息的存储位置



# __ls__  

ls -a 包含隐藏文件  

ls -l 显示额外的信息  

ls -R 目录递归通过  

ls -ld 目录和符号链接信息  

ls -1 文件分行显示  

ls –S 按从大到小排序  

ls –t 按mtime排序  

ls –u 配合-t选项，显示并按atime从新到旧排序  

ls –U 按目录存放顺序显示  

ls –X 按文件后缀排序  

stat    
文件：metadata, data  
三个时间戳： 
access time：访问时间，atime，读取文件内容    
modify time: 修改时间, mtime，改变文件内容（数据）   
change time: 改变时间, ctime，元数据发生改变 

*匹配零个或多个字符  
? 匹配任何单个字符  
~ 当前用户家目录  
~lei 用户lei家目录  
~+ 当前工作目录  
~- 前一个工作目录  
[0-9] 匹配数字范围  
[a-z]：字母  
[A-Z]：字母 
[lei]] 匹配列表中的任何的一个字符 
[^lei] 匹配列表中的所有字符以外的字符  

[:digit:]：任意数字，相当于0-9  
[:lower:]：任意小写字母  
[:upper:]: 任意大写字母  
[:alpha:]: 任意大小写字母  
[:alnum:]：任意数字或字母  
[:blank:]：水平空白字符  
[:space:]：水平或垂直空白字符  
[:punct:]：标点符号  
[:print:]：可打印字符  
[:cntrl:]：控制（非打印）字符  
[:graph:]：图形字符  
[:xdigit:]：十六进制字符  


设置语言  
/etc/sysconfig/i18n  

touch -- -a=touch./-a=touch 绝对路径/-a    
删除也是这三种方式  

6版本中有个神奇的目录叫misc，我们只要输入cd /misc/cd 就会进入到挂载好的目录中


看得开心吗？写的这些东西就是想让喜欢Linux以及爱好游戏的童鞋们在这一起扯淡一起装逼!

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [前面的话](#%E5%89%8D%E9%9D%A2%E7%9A%84%E8%AF%9D)
- [A-Z:linux学习路径](#a-zlinux%E5%AD%A6%E4%B9%A0%E8%B7%AF%E5%BE%84)
  - [安装linux和使用ssh工具（一天）](#%E5%AE%89%E8%A3%85linux%E5%92%8C%E4%BD%BF%E7%94%A8ssh%E5%B7%A5%E5%85%B7%E4%B8%80%E5%A4%A9)
  - [用户和群组管理（一天）](#%E7%94%A8%E6%88%B7%E5%92%8C%E7%BE%A4%E7%BB%84%E7%AE%A1%E7%90%86%E4%B8%80%E5%A4%A9)
  - [文件基本属性（一天）](#%E6%96%87%E4%BB%B6%E5%9F%BA%E6%9C%AC%E5%B1%9E%E6%80%A7%E4%B8%80%E5%A4%A9)
  - [文件和目录操作（五天）](#%E6%96%87%E4%BB%B6%E5%92%8C%E7%9B%AE%E5%BD%95%E6%93%8D%E4%BD%9C%E4%BA%94%E5%A4%A9)
  - [linux 目录结构（一天）](#linux-%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84%E4%B8%80%E5%A4%A9)
  - [监控和管理 Linux 进程（一天）](#%E7%9B%91%E6%8E%A7%E5%92%8C%E7%AE%A1%E7%90%86-linux-%E8%BF%9B%E7%A8%8B%E4%B8%80%E5%A4%A9)
  - [文件系统和磁盘管理（两天）](#%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F%E5%92%8C%E7%A3%81%E7%9B%98%E7%AE%A1%E7%90%86%E4%B8%A4%E5%A4%A9)
  - [系统管理（三天）](#%E7%B3%BB%E7%BB%9F%E7%AE%A1%E7%90%86%E4%B8%89%E5%A4%A9)
  - [网络设置与传输访问（两天）](#%E7%BD%91%E7%BB%9C%E8%AE%BE%E7%BD%AE%E4%B8%8E%E4%BC%A0%E8%BE%93%E8%AE%BF%E9%97%AE%E4%B8%A4%E5%A4%A9)
- [shell:第一门编程语言（七天）](#shell%E7%AC%AC%E4%B8%80%E9%97%A8%E7%BC%96%E7%A8%8B%E8%AF%AD%E8%A8%80%E4%B8%83%E5%A4%A9)
  - [解释型语言](#%E8%A7%A3%E9%87%8A%E5%9E%8B%E8%AF%AD%E8%A8%80)
  - [shell 种类](#shell-%E7%A7%8D%E7%B1%BB)
  - [shell 注释](#shell-%E6%B3%A8%E9%87%8A)
  - [shell 换行](#shell-%E6%8D%A2%E8%A1%8C)
  - [shell 变量](#shell-%E5%8F%98%E9%87%8F)
    - [字符串操作](#%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%93%8D%E4%BD%9C)
    - [数组](#%E6%95%B0%E7%BB%84)
    - [定义map](#%E5%AE%9A%E4%B9%89map)
  - [shell 参数传递](#shell-%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92)
  - [shell 流程控制](#shell-%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6)
    - [if - 控制分支](#if---%E6%8E%A7%E5%88%B6%E5%88%86%E6%94%AF)
    - [for - 循环](#for---%E5%BE%AA%E7%8E%AF)
    - [while - 循环](#while---%E5%BE%AA%E7%8E%AF)
    - [until - 循环](#until---%E5%BE%AA%E7%8E%AF)
    - [case ... esac](#case--esac)
    - [break - 跳出当前循环](#break---%E8%B7%B3%E5%87%BA%E5%BD%93%E5%89%8D%E5%BE%AA%E7%8E%AF)
    - [continue - 执行下一次循环（跳出当次循环）](#continue---%E6%89%A7%E8%A1%8C%E4%B8%8B%E4%B8%80%E6%AC%A1%E5%BE%AA%E7%8E%AF%E8%B7%B3%E5%87%BA%E5%BD%93%E6%AC%A1%E5%BE%AA%E7%8E%AF)
  - [shell 运算符](#shell-%E8%BF%90%E7%AE%97%E7%AC%A6)
  - [shell 函数](#shell-%E5%87%BD%E6%95%B0)
  - [shell 输入/输出重定向](#shell-%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E9%87%8D%E5%AE%9A%E5%90%91)
  - [shell 导入](#shell-%E5%AF%BC%E5%85%A5)
  - [shell中的进制问题](#shell%E4%B8%AD%E7%9A%84%E8%BF%9B%E5%88%B6%E9%97%AE%E9%A2%98)
  - [shell中常用命令](#shell%E4%B8%AD%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4)
- [后面的话](#%E5%90%8E%E9%9D%A2%E7%9A%84%E8%AF%9D)
- [参考资料](#%E5%8F%82%E8%80%83%E8%B5%84%E6%96%99)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 前面的话

:point_right:忘记桌面（desktop），回归命令行本质。

:point_right:linux一切皆文件。

:point_right:不要记参数，做help玩家，多查看命令帮助文件减少百度次数。

:point_right:重要的话说三遍，别忘了做笔记，别忘了做笔记，别忘了自己笔记。

# A-Z:linux学习路径

## 安装linux和使用ssh工具（一天）

有了环境才能学习。没有环境的同学要学会安装linux环境。网上安装教程很多。tips:破解版软件请勿用户商业环境。

> 也推荐自己安装环境。为后面的分布式系统，集群、容器编排做打算，可以拷贝副本的方式复制虚拟机

ssh工具：windows系统:推荐使用MobaXterm，Xshell等工具。其他系统用自带的终端ssh连接就好。

:point_right:目标：linux跑起来，ssh能正常连接即可

作为初学者你**只需要知道cpu、显卡、网卡、内存、磁盘有这些东西和对应的功能即可**，不需要过得的关注其深层原理。

## 用户和群组管理（一天）

linux是一个多用户的系统，管理用户和用户组是最重要的工作之一，这是超级管理员root的职责，**用户和用户组首要的学习目标**。

ssh连上的那一刻，你就会进入到登录用户的工作目录下。

> 超级用户在系统中的用户ID和组ID都是0。普通用户的用户ID（UID）从500开始编号，并且默认属于与用户名同名的组。组ID（GID）也从500开始编号。

用户组相关命令

```bash
groupadd #添加用户组
groupmod #修改用户组
groupdel #删除用户组
```

用户相关命令

```bash
useradd #添加用户
usermod #修改用户
userdel #删除用户
```

更改用户密码

```bash
passwd ${user_name}
```

切换用户

```bash
su
```

相关系统文件

```bash
/etc/passwd # 用户文件
/etc/shadow # 主件
/etc/group # 用户组文件
```

:point_right:目标：能对用户、用户口令（密码）、用户组管理自如，知道相关的系统文件

## 文件基本属性（一天）

Linux 中第一个字符代表这个文件是目录、文件或链接文件等等

```bash
# ls -l 
drwxr-xr-x    4 root root  4096 Jun 21 22:18 stonebird
# 首字母含义
d 则是目录
- 则是文件
l 则表示为链接文档(link file)
b 则表示为装置文件里面的可供储存的接口设备(可随机存取装置)
c 则表示为装置文件里面的串行端口设备，例如键盘、鼠标(一次性读取装置)
```

权限含义三个为一组，且均为 rwx 的三个参数的组合。**第一组当前用户、第二组是当前组的其他用户、第三组是其他用户**
```
r 代表可读(read) 对应4
w 代表可写(write) 对应2
x 代表可执行(execute)。对应1
- 说明没有对应权限
```

相关命令

```bash
chown # 改变文件所属用户和组
chmod # 改变文件权限
```

:point_right:目标：能看懂文件类型、所属用户、组、当前用户权限，知道777,755,600,644,augo+x,-x,-w,+w等含义

## 文件和目录操作（五天）

到此，你已经知道了用户和组，以及权限管理。现在学习对文件和目录进行操作。

不要求快，慢慢把命令敲敲一遍。tab键自动补齐命令。

相关命令

```bash
touch # 创建空文件
vi/vim # 编辑文件内容
tree 	# 树状图列出目录的内容
ls	# 文件和目录
cd	# 切换目录
pwd/dirs	# 显示当前工作目录
cp	# 复制文件或目录
scp/rcp # 加密的方式在本地主机和远程主机之间复制文件
mkdir	# 创建一个新目录
rmdir	# 删除一个空目录
rm		# 删除文件或者目录
mv 		# 重命名或者移动文件
cat		# 查看文件全部内容
more 	# 分页显示文本文件内容
less 	# 与more功能类似，比more更适用
head	# 查看文件的后几行
tail	# 查看文件的后几行
grep/egrep    # 过滤文本内容
awk		# 强大的文本工具一般用于分割数据
sed 	# 强大的文本工具一般用于对数据的增删改查
ln 		# 用来为文件创建连接
diff 	# 比较给定的两个文件的不同
which/whereis 	# 查找命令的路径
find/locate/slocate 	# 在指定目录下查找文件
sort 	# 将文件进行排序并输出
uniq    # 去除文件中的重复内容行
split	# 文件分割
shuf    # 打乱顺序产生随机的排列
tar 	# Linux 下的归档使用工具，用于打包和备份
zip/unzip # 加压缩/解压缩由 zip 命令压缩的压缩包
dd 	   # 转换和复制文件
chattr # 更改文件隐藏属性
lsattr # 显示文件隐藏属性
cksum # 检查文件完整性
md5sum # 检查文件md5值
cmp		# 比较文件差异
file	# 命令用于辨识文件类型
cut		# 按列提取文件内容
od		# 八进制输出文件内容
strings # 打印文件可打印的字符串
paste 	# 按对应行合并两个文件
tmpwatch # 删除暂存文件
comm 	# 命令用于比较两个已排过序的文件
tr		# 字符转换
expr/let	# 算术表达式
wc      # 统计文件的字节数、单词数、行数
dos2unix # 将文本转成unix格式
```

:point_right:管道(|)：可以把一系列命令连接起来，这意味着第一个命令的输出会作为第二个命令的输入通过管道传给第二个命令，第二个命令的输出又会作为第三个命令的输入，以此类推

```bash
# 管道例子
cat test.txt |grep -i "stonebird" | awk -F ',' '{print $2}'
```

:point_right:目标：能对文件（文件夹）创建、查看，更新、重命名、移动、删除等操作，配合着管道使用,可以过滤自己想过滤的人任何信息。

## linux 目录结构（一天）

```bash
/bin/	# 存放系统命令，普通用户和 root 都可以执行。放在 /bin 下的命令在单用户模式下也可以执行
/boot/	# 系统启动目录，保存与系统启动相关的文件，如内核文件和启动引导程序（grub）文件等
/dev/	# 设备文件保存位置
/etc/	# 配置文件保存位置。系统内所有采用默认安装方式（rpm 安装）的服务配置文件全部保存在此目录中，如用户信息、服务的启动脚本、常用服务的配置文件等
/home/	# 普通用户的主目录（也称为家目录）。在创建用户时，每个用户要有一个默认登录和保存自己数据的位置，就是用户的主目录，所有普通用户的主目录是在 /home/ 下建立一个和用户名相同的目录。如用户 liming 的主目录就是 /home/liming
/lib/	# 系统调用的函数库保存位置
/media/	# 挂载目录。系统建议用来挂载媒体设备，如软盘和光盘
/mnt/	# 挂载目录。早期 Linux 中只有这一个挂载目录，并没有细分。系统建议这个目录用来挂载额外的设备，如 U 盘、移动硬盘和其他操作系统的分区
/misc/	# 挂载目录。系统建议用来挂载 NFS 服务的共享目录。虽然系统准备了三个默认挂载目录 /media/、/mnt/、/misc/，但是到底在哪个目录中挂载什么设备可以由管理员自己决定。例如，笔者在接触 Linux 的时候，默认挂载目录只有 /mnt/，所以养成了在 /mnt/ 下建立不同目录挂载不同设备的习惯，如 /mnt/cdrom/ 挂载光盘、/mnt/usb/ 挂载 U 盘，都是可以的
/opt/	# 第三方安装的软件保存位置。这个目录是放置和安装其他软件的位置，手工安装的源码包软件都可以安装到这个目录中。不过笔者还是习惯把软件放到 /usr/local/ 目录中，也就是说，/usr/local/ 目录也可以用来安装软件
/root/	# root 的主目录。普通用户主目录在 /home/ 下，root 主目录直接在“/”下
/sbin/	# 保存与系统环境设置相关的命令，只有 root 可以使用这些命令进行系统环境设置，但也有些命令可以允许普通用户查看
/srv/	# 服务数据目录。一些系统服务启动之后，可以在这个目录中保存所需要的数据
/tmp/	# 临时目录。系统存放临时文件的目录，在该目录下，所有用户都可以访问和写入。建议此目录中不能保存重要数据，最好每次开机都把该目录清空
/lost+found/	#当系统意外崩溃或意外关机时，产生的一些文件碎片会存放在这里。在系统启动的过程中，fsck 工具会检查这里，并修复已经损坏的文件系统。这个目录只在每个分区中出现，例如，/lost+found 就是根分区的备份恢复目录，/boot/lost+found 就是 /boot 分区的备份恢复目录
/proc/	#虚拟文件系统。该目录中的数据并不保存在硬盘上，而是保存到内存中。主要保存系统的内核、进程、外部设备状态和网络状态等
	/proc/cpuinfo # 是保存 CPU 信息的
	/proc/devices # 是保存设备驱动的列表
	/proc/filesystems # 是保存文件系统列表的
	/proc/net 是保存网络协议信息的......
/sys/	# 虚拟文件系统。和 /proc/ 目录相似，该目录中的数据都保存在内存中，主要保存与内核相关的信息
# Linux 系统中，所有系统默认的软件都存储在 /usr 目录下
/usr		# 此目录用于存储系统软件资源
/usr/bin/	# 存放系统命令，普通用户和超级用户都可以执行。这些命令和系统启动无关，在单用户模式下不能执行
/usr/sbin/ 	# 存放根文件系统不必要的系统管理命令，如多数服务程序，只有 root 可以使用。
/usr/lib/	# 应用程序调用的函数库保存位置
/usr/XllR6/	# 图形界面系统保存位置
/usr/local/	# 手工安装的软件保存位置。我们一般建议源码包软件安装在这个位置
/usr/share/	# 应用程序的资源文件保存位置，如帮助文档、说明文档和字体目录
/usr/src/	# 源码包保存位置。我们手工下载的源码包和内核源码包都可以保存到这里。
/usr/include # C/C++ 等编程语言头文件的放置目录
/var 		# 目录用于存储动态数据
/var/lib/	# 程序运行中需要调用或改变的数据保存位置。如 MySQL 的数据库保存在 /var/lib/mysql/ 目录中
/var/log/	# 登陆文件放置的目录，其中所包含比较重要的文件如 /var/log/messages, /var/log/wtmp 等。
/var/run/	# 一些服务和程序运行后，它们的 PID（进程 ID）保存位置
/var/spool/	# 里面主要都是一些临时存放，随时会被用户所调用的数据，例如 /var/spool/mail/ 存放新收到的邮件，/var/spool/cron/ 存放系统定时任务。
/var/www/	# RPM 包安装的 Apache 的网页主目录
/var/nis和/var/yp	# NIS 服务机制所使用的目录，nis 主要记录所有网络中每一个 client 的连接信息；yp 是 linux 的 nis 服务的日志文件存放的目录
/var/tmp	# 一些应用程序在安装或执行时，需要在重启后使用的某些文件，此目录能将该类文件暂时存放起来，完成后再行删除
```

:point_right:大致了解即可

## 监控和管理 Linux 进程（一天）

对文件/目录的基本操作已经了解。

对进程监控需要有一定了解（有印象状态即可）

相关命令

```bash
ps 		# 查看进程
top 	# 实时显示系统运行状态
iotop 	# 监视磁盘I/O状态
iftop 	# 套接字及进程的网络利用率
iostat  # 监视系统输入输出设备和CPU的使用情况
kill  	# 杀死进程
pkill 	# 按照进程名杀死进程
killall # 使用进程名称来杀死一组进程
vmstat	# 显示虚拟内存状态
dstat   # 全能系统信息统计工具
netstat # 显示网络状态
ss      # 显示活动套接字信息
free	# 显示系统内存使用量情况
lsof	# 查看文件的进程信息
nohup   # 程序放后台运行
```

:point_right:目标：能查看对应进程、对应进程消耗、磁盘io、网络端口、内存、cpu使用率。

## 文件系统和磁盘管理（两天）

此时已经能基本熟练使用linux，能完成60%的运维工作，存储也是很重要的组成部分，需要对磁盘和文件系统有一定了解。

常用文件系统

```bash
1、XFS是一个具有非常高性能且可扩展的文件系统，同时在大多数要求的应用程序中都会进行常规部署。XFS提供了一种健壮的、优秀的以及功能丰富的文件系统，它具有的可伸缩性能够满足最苛刻的存储需求。
2、ext4：ext3的升级版本，ext4对ext3做了很多深层次的改进，设计更合理、性能更好、更可靠，同时还引入了一些新功能。
3、ext3：ext2的升级版本，其主要优点是在ext2的基础上加入了记录数据的日志功能。
4、ext2：支持标准Unix文件类型，可用于多种存储介质，向上兼容性好

## 网络文件系统-了解即可
nfs
glusterfs
cephfs
```

raid(了解即可)，一般使用raid5

lvm逻辑卷（了解即可）

相关命令

```bash
fsck/fsck.ext2/fsck.ext3/fsck.ext4/fsck.xfs # 检查与修复文件系统
mount 	# 把文件系统挂载到目录
umount # 卸载文件系统
du		# 查看文件或目录的大小
df		# 显示磁盘空间使用情况
parted  # 磁盘分区工具
fdisk	# 管理磁盘分区
lsblk	# 查看块设备
```

:point_right:目标：能正常查看文件系统类型、统计大小、挂载卸载磁盘，知道配置/etc/fstab即可, 

> 可以适当了解分区、逻辑卷

## 系统管理（三天）

对于系统管理掌握必不可少，是排查问题的开始

重要日志说明

```bash
/var/log/messages：日志是核心系统日志文件。它包含了系统启动时的引导消息，以及系统运行时的其他状态消息。IO错误、网络错误和其他系统错误都会记录到这个文件中。其他信息，比如某个人的身份切换为root，也在这里列出。如果服务正在运行，比如DHCP服务器，可以在messages文件中观察它的活动。通常/var/log/messages是在做故障诊断时首先要查看的文件。
/var/log/secure：志是用户登录信息日志文件。它包含用户登录登出信息。
/var/log/maillog：志是系统的邮件日志。它包含邮件服务器的发送和接收邮件信息。
/var/log/dmesg：志是系统硬件的日志。
/var/log/mcelog：志是记录系统运行过程中发现的硬件错误信息，包含内存错误，io错误等日志。
```

SELinux（了解即可）：SELinux是在linux内核的一种强制访问控制机制的实现。SELinux构架提供了多种增强的访问控制策略，包含基于类型加强，基于角色的访问控制，和多级别/多安全。

相关命令

```bash
date 	# 显示或设置系统日期与时间
finger  # 查询其他使用者的资料
who/whoam/w		# 查看当前登录用户信息
su  			# 切换用户 
sleep/usleep 	# 延迟当前命令的执行
crontab 		#  管理定时计划任务 
alias			# 设置命令别名
time			# 指令执行时所消耗的时间
declare			# 声明shell变量
export			# 查看或设置环境变量
systemctl		# 管理系统服务
service			# 管理系统服务
clear			# 清除屏幕（向后翻页）
dmesg			# 显示开机信息
halt			# 关闭服务器
shutdown		# 关闭服务器
reboot			# 重启系统
sysctl			# 配置内核参数
kdump			# 系统崩溃时记录日志
## 内核模块-了解即可
lsmod			# 加载kernel模块管理
modprobe		# kernel模块智能加载工具
insmod			# 用于载入kernel模块
rmmod			# 用于删除kernel模块
modinfo			# 显示kernel模块的信息
```

:point_right:目标：能判断角色，查看系统日志，知道定时任务、环境变量，内核模块管理，关机等操作即可。

## 网络设置与传输访问（两天）

程序的交互离不开网络，加油，快翻越第一座山了。

相关命令

```bash
ping/ping6  # 测试主机间网络连通性
ip			# 显示与配置网卡参数
route		# 显示与设置路由信息
ifup		# 激活网络接口
ifdown		# 关闭网络接口
ifconfig	# 显示或设置网络设备参数信息
ftp			# 与ftp服务器交互
telnet		# 控制远程设备
curl		# 文件传输工具
wget		# 下载网络文件
host		# 域名查询
dig			# 域名查询
nslookup	# 域名查询
tcpdump		# 抓包，监听网络流量
firewalld	# 防火墙查看与配置
iptables	# 防火墙查看与配置
sz			# 从Linux下载文件到本地
rz			# 本地文件上传至linux
```

:point_right:目标：能正常配置ip，路由。防火墙基本配置，了解抓包。了解常见的常见的应用层协议ftp、http等，配合着更进一步学习监控知识

# shell:第一门编程语言（七天）

虽然至此我们能完全熟练运用linux，能完成100%的运维工作。很多时候我们需要让机器去自动完成我们的动作，比起程序启停、定时任务、日志轮转，备份、上传等等操作，这时shell无疑是最方便、简洁的一门语言。

> 强烈建议学习shell作为第一门编程语言，不仅可以轻松完成运维工作，而且对后面的学习高级语言（golang，python或其他语言）会很有帮助

## 解释型语言

shell 脚本的后缀名是.sh

> **#!** 是一个约定的标记，它告诉系统这个脚本需要什么解释器来执行

```bash
#!/bin/bash  # 对于使用bash解释器
#!/bin/sh	#  对应使用sh解释器 ，同理python,perl等解释型语言改成对应的解释器即可。

# 有解释器路径赋予执行权限后系统会自动执行
chmod +x test.sh
./test.sh

# 没有解释器，可以手动带解释器执行，否则系统会当做默认的shell作为解释器（尽管你文本文件可能不是shell脚本）
bash test.sh
```

## shell 种类

 `cat /etc/shells`查看当前环境可以使用的shell

```bash
echo "$SHELL" # 查看当前登录系统shell

# 使用chsh 更改shell
chsh -s /bin/bash # 更改当初shell为bash
```

> 默认shell建议使用bash。

## shell 注释

单行注释：**#** 后面的内容，会被解释器忽略。

```bash
# tips 单行注释
```

多行注释 

```bash
# EOF 可以换成其他符合
:<<EOF
注释内容...
注释内容...
注释内容...
EOF
```

## shell 换行

代码太长 可以使用 \ 进行跨行编写

在 `''`, `""` , `()` , `{}` ,`` 里面的内容可以直接跨行输入  

> 多行命令写成一行，用 `;` 隔开

## shell 变量

定义变量 `=` 两边不能有空格，注意命令规范使用单词数字下划线（lower_with_under）的形式

```bash
file_name="stdout.log"

# 取值
$file_name # 不建议使用
${file_name} # 建议使用
```

> shell变量类型都是字符串
>
> shell只有全局变量，注意值的可靠性，不要取到被更改的值
>
> 为了防止边界问题，建议统一使用${var}的格式

:point_right:使用语句赋值 `$()` 或者 ``

```bash
file_name=`cat config|grep file_name|awk -F = '{print $2}'`
#
file_name=$(cat config|grep file_name|awk -F = '{print $2})
```

:point_right:对变量的操作

```bash
# 只读变量 readonly 
name="stonebird"
readonly name

# 删除变量 unset
unset name
```

:point_right:`''` 和 `""` 的区别

```bash
# '' 原样输出
suff='bird'
name='stone${suff}' # stone${suff}

# "" 支持转义 ${} \n \t \r
name="stone${suff}" # stonebird
```

### 字符串操作

:point_right:拼接

```bash
# shell 拼接直接使用'' 或者 "" 拼接标准输出即可
suff="bird"
name="stone'${suff}'ya'
name="stone${suff}ya"
```

:point_right:字符串长度

```bash
# 使用#获取长度
name="stonebird"
echo "${#name}"   # 9
```

:point_right:提取字符串

```bash
# 使用string:start:end获取子字符串，索引从0开始
name="stonebird"
echo "${name:1:3}" # ton
```

:point_right:`expr` 对字符串的其他操作

```bash
match	中匹配 REGEXP 字符串并返回匹配字符串的长度
substr	从 POS 位置获取长度为 LENGTH 的字符串
index	杳找子字符串的起始位置
length	计算字符串的长度

expr match "123 456 789" ".*5"  # 6 匹配字符串的长度，若找不到则返回 0
expr substr " this is a test" 3 5 # his i 
expr index "test for the game" "e" # 2 
expr length "this is a test" # 14
```

### 数组

数组使用()定义

```bash
array=(ele0 ele1 ele2 ele3)
# 或者 
array=(
ele0 
ele1 
ele2 
ele3
)
```

:point_right:读取数组

```bash
# 读取下标
echo ${array_name[0]}

# 使用 @ 或 * 可以获取数组中的所有元素
echo ${array_name[@]}
echo ${array_name[*]}

# 取得数组元素的个数
length=${#array_name[@]}
# 或者
length=${#array_name[*]}
# 取得数组单个元素的长度
length_ele=${#array_name[n]}
```

### 定义map

:point_right:使用 `declare -A array` 或者 直接使用内嵌“索引-值”列表法定义map

```bash
info=(["name"]="hjx", ["nick_name"]="stonebird", ["age"]="18f")

declare -A info=(["name"]="hjx", ["nick_name"]="stonebird", ["age"]="18f")
# 或者
declare -A info
info["name"]="hjx"
info["nick_name"]="stonebird"
info["nick_name"]="18f"

echo ${info["nick_name"]}
```

```bash

echo ${!array[*]}   #取关联数组所有键
echo ${!array[@]}  #取关联数组所有键
echo ${array[*]}       #取关联数组所有值
echo ${array[@]}      #取关联数组所有值
echo ${#array[*]}  #取关联数组长度
echo ${#array[@]} #取关联数组长度
```

## shell 参数传递

> 参数传递可以在脚本或者函数中传递

```bash
$0  #当前脚本的文件名
$n(n>=1) #传递给脚本或函数的参数
$# #传递给脚本或函数的参数个数
$* #传递给脚本或函数所有参数 不可迭代
$@ #传递给脚本或函数所有参数 ，当参数有""时 $@和$*有所不同 “$*”会把所以参数当成一个 “$@”会迭代
$? #上一条命令的执行结果，如果是执行的命令是0正常 1异常 ,return 0代表函数正常终止,其他异常终止
$$ #显示当前shell的进程ID
$- #显示Shell使用的当前选项，与set命令功能相同，不常用。
$? #上一条命令的运行状态
```

## shell 流程控制

### if - 控制分支

```bash
if condition
then
    something
  	...
fi

## else
if condition
then
    something
    ...
else
    something
    ...
fi

## elif
if condition1
then
    something
elif condition2 
then 
    something
else
    something
fi
```

### for - 循环

for 会遍历带空格的元素

```bash
for var in ele1 ele2 ...
do
    echo "${var}"
done
```

for((;;)) 格式也是支持的

```bash
for (( i = 0; i < 10; i++ )); do
	#statements
done

## 无限循环
for (( ; ; )); do
	#statements
done
```

### while - 循环

```bash
while condition
do
    something
done

## 无限循环
while true    ## while ((1)) 也行
do
    something
done
```

### until - 循环

```bash
until condition
do
    something
done
```

### case ... esac

```bash
case var in
模式1)
    ...
    ;;
模式2)
    ...
    ;;
esac

## 例子
case $aNum in
    1)  echo '你选择了 1'
    ;;
    2)  echo '你选择了 2'
    ;;
    3)  echo '你选择了 3'
    ;;
    4)  echo '你选择了 4'
    ;;
    *)  echo '你没有输入 1 到 4 之间的数字'
    ;;
esac
```

### break - 跳出当前循环

使用for、until、while 所有循环

```bash
a=0
while; do
	if [[ $a -eq 4 ]]; then
		break
	fi
	let a++
done
```

 ### continue - 执行下一次循环（跳出当次循环）

```bash
a=0
for (( i = 0; i < 10; i++ )); do
	if [[ $i -eq 8 ]]; then
		continue
	fi
	a=`expr ${a} + ${i}`
done
```

## shell 运算符

:point_right:算术运算符

```shell
#整数使用expr 、let ，小数使用bc
+、-、*、/、%、
=（#赋值，=左右两边不能有空格）
==	#相等。用于比较两个数字，相同则返回 true。	[ $a == $b ] 返回 false。
!=	#不相等。用于比较两个数字，不相同则返回 true。	[ $a != $b ] 返回 true。

expr `1 + 1`
let a++
echo "2.2+2.5"|bc
```

:point_right:关系运算符

~~~shell
-eq 相等
-ne 不相等
-gt 大于（左大于右）
-ge 大于等于
-lt 小于
-le 小于等于
~~~

:point_right:布尔运算符

~~~shell
！非运算
-a 与运算
-o 或运算
~~~

:point_right:逻辑运算符

~~~shell
&& 逻辑与
|| 逻辑或
~~~

:point_right:字符串运算符

~~~shell
=  相等[$a = $b]  #shell 是一个 =
!=  不等[$a != $b]
-z  检测字符串长度是否为0 ?为0true
-n  检测字符串长度是否为0 ?不为0 ture
$str 检测字符串是否为空?不为空true
~~~

:point_right:文件测试常用运算符

~~~shell
-d file 检测是否是目录
-s file 检测文件是否为空（文件大小是否大于0），不为空返回 true。
-e file 检测目录或文件是否存在
-r -w -x file 检测文件是否可读写执行
-f file 检测文件是否是普通文件
~~~

## shell 函数

函数是多条指令的集合，是单独运行的代码块

```bash
[ function ] func_name [()]
{
    action;
    [return int] 
}

# 调用 
func_name
```

> 推荐使用 function func_name(){} 的格式
>
> 推荐返回状态码；0正常退出，其他异常退出

## shell 输入/输出重定向

```bash
command > file	将输出重定向到 file。
command < file	将输入重定向到 file。
command >> file	将输出以追加的方式重定向到 file。
n > file	将文件描述符为 n 的文件重定向到 file。
n >> file	将文件描述符为 n 的文件以追加的方式重定向到 file。
n >& m	将输出文件 m 和 n 合并。
n <& m	将输入文件 m 和 n 合并。
# command1 < infile > outfile

<< tag	将开始标记 tag 和结束标记 tag 之间的内容作为输入。
# 例子
wc -l << EOF
    test
EOF
```

:point_right:/dev/null

```bash
command > /dev/null 2>&1
```

> 0 是标准输入（STDIN），1 是标准输出（STDOUT），2 是标准错误输出（STDERR）。
> 这里的 2 和 > 之间不可以有空格，2> 是一体的时候才表示错误输出.

## shell 导入

使用 `source`  或者 `.` 导入其他shell

```bash
. filename   # 注意点号(.)和文件名中间有一空格
source filename
```

> 导入shell会导入全部的变量或者函数，注意名称不要重复 

## shell中的进制问题

```bash
#!/bin/bash
vara=08;
varb=10;

## single bracket in if statment is working.
if [ $vara -lt $varb ]; then
echo "yes";
else
echo "no";
fi


## double brackets in if statment is not working; throwing an error like below.
## [[: 08: value too great for base (error token is "08")
if [[ $vara -lt $varb ]]; then
echo "yes";
else
echo "no";
fi
```

> Shell脚本中0开头的数字表示8进制，因此08则超出了8进制的范围
>
> Here my problem is to find the difference of using single bracket [ ] and double brackets [[ ]] in if statement.
>
> 条件最好使用[[ ]]

## shell中常用命令

```bash
chsh   # 改变系统shell
echo   # 打印到终端
readonly # 指定变量
expr	# 算术表达式
let		# 算术表达式
read	# 读取用户或文件输入
test	# 检查条件是否成立
set		# 设置shell
unset	# 删除指定的shell变量或函数
printf	# 格式化打印
xargs	# 参数传递过滤器
bc		# 浮点数计算
```

:point_right:目标：理解shell，有正常的思想，能编写脚本实现自动化运维

# 后面的话

如果你学得不错，至此你已经是中等偏上的linux玩家了。能满足运维工程师条件。学无止境

接下来

:point_right:学习git来控制版本

:point_right:学习使用containerd 或者docker来管理容器

> 优先学习docker，理解掌握基本使用即可
>
> k8s最新的容器运行时是containerd，推荐深度学习

:point_right:除了本地开发环境，其他的都应该使用容器（数据库、消息队列，服务部署）

# 参考资料

[cgsl-用户手册](https://www.gd-linux.com/html/xiazai/system/)

[菜鸟教程]()


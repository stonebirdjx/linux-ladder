<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [系统管理](#%E7%B3%BB%E7%BB%9F%E7%AE%A1%E7%90%86)
  - [groupadd - 添加用户组](#groupadd---%E6%B7%BB%E5%8A%A0%E7%94%A8%E6%88%B7%E7%BB%84)
  - [groupmod - 修改用户组](#groupmod---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7%E7%BB%84)
  - [groupdel - 删除用户组](#groupdel---%E5%88%A0%E9%99%A4%E7%94%A8%E6%88%B7%E7%BB%84)
  - [useradd - 添加用户](#useradd---%E6%B7%BB%E5%8A%A0%E7%94%A8%E6%88%B7)
  - [usermod - 修改用户](#usermod---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7)
  - [userdel - 删除用户](#userdel---%E5%88%A0%E9%99%A4%E7%94%A8%E6%88%B7)
  - [passwd - 修改用户密码](#passwd---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7%E5%AF%86%E7%A0%81)
  - [chpasswd - 修改当前用户](#chpasswd---%E4%BF%AE%E6%94%B9%E5%BD%93%E5%89%8D%E7%94%A8%E6%88%B7)
- [文件管理/目录管理](#%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E7%9B%AE%E5%BD%95%E7%AE%A1%E7%90%86)
  - [chown - 更改文件用户、属组](#chown---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E7%94%A8%E6%88%B7%E5%B1%9E%E7%BB%84)
  - [chmod - 更改文件权限](#chmod---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E6%9D%83%E9%99%90)
  - [touch - 创建文件或修改文件访问时间](#touch---%E5%88%9B%E5%BB%BA%E6%96%87%E4%BB%B6%E6%88%96%E4%BF%AE%E6%94%B9%E6%96%87%E4%BB%B6%E8%AE%BF%E9%97%AE%E6%97%B6%E9%97%B4)
  - [tree - 树状图列出目录的内容](#tree---%E6%A0%91%E7%8A%B6%E5%9B%BE%E5%88%97%E5%87%BA%E7%9B%AE%E5%BD%95%E7%9A%84%E5%86%85%E5%AE%B9)
  - [vi/vim - 编辑文件内容](#vivim---%E7%BC%96%E8%BE%91%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [ls - 列出文件目录](#ls---%E5%88%97%E5%87%BA%E6%96%87%E4%BB%B6%E7%9B%AE%E5%BD%95)
  - [dir - 列出文件](#dir---%E5%88%97%E5%87%BA%E6%96%87%E4%BB%B6)
  - [cd - 切换工作目录](#cd---%E5%88%87%E6%8D%A2%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [pwd - 显示当前工作目录](#pwd---%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [dirs - 显示当前工作目录](#dirs---%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [cp - 文件文件或者目录](#cp---%E6%96%87%E4%BB%B6%E6%96%87%E4%BB%B6%E6%88%96%E8%80%85%E7%9B%AE%E5%BD%95)
  - [scp - 基于SSH协议远程复制文件或目录](#scp---%E5%9F%BA%E4%BA%8Essh%E5%8D%8F%E8%AE%AE%E8%BF%9C%E7%A8%8B%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [rcp - 远程复制文件或目录](#rcp---%E8%BF%9C%E7%A8%8B%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [mkdir - 创建文件或者目录](#mkdir---%E5%88%9B%E5%BB%BA%E6%96%87%E4%BB%B6%E6%88%96%E8%80%85%E7%9B%AE%E5%BD%95)
  - [rmdir - 删除一个空文件夹](#rmdir---%E5%88%A0%E9%99%A4%E4%B8%80%E4%B8%AA%E7%A9%BA%E6%96%87%E4%BB%B6%E5%A4%B9)
  - [rm - 删除文件或目录](#rm---%E5%88%A0%E9%99%A4%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [mv - 移动或改名文件](#mv---%E7%A7%BB%E5%8A%A8%E6%88%96%E6%94%B9%E5%90%8D%E6%96%87%E4%BB%B6)
  - [cat - 查看文件内容](#cat---%E6%9F%A5%E7%9C%8B%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [more - 分页显示文件内容](#more---%E5%88%86%E9%A1%B5%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [less - 分页显示文件内容](#less---%E5%88%86%E9%A1%B5%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [head -  显示文件开头的内容](#head----%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%BC%80%E5%A4%B4%E7%9A%84%E5%86%85%E5%AE%B9)
  - [tail - 显示文件结尾的内容](#tail---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E7%BB%93%E5%B0%BE%E7%9A%84%E5%86%85%E5%AE%B9)
  - [grep/egrep - 文本过滤](#grepegrep---%E6%96%87%E6%9C%AC%E8%BF%87%E6%BB%A4)
  - [awk - 文本和数据进行处理的编程语言](#awk---%E6%96%87%E6%9C%AC%E5%92%8C%E6%95%B0%E6%8D%AE%E8%BF%9B%E8%A1%8C%E5%A4%84%E7%90%86%E7%9A%84%E7%BC%96%E7%A8%8B%E8%AF%AD%E8%A8%80)
  - [sed -  批量编辑文本文件](#sed----%E6%89%B9%E9%87%8F%E7%BC%96%E8%BE%91%E6%96%87%E6%9C%AC%E6%96%87%E4%BB%B6)
  - [ln - 创建链接](#ln---%E5%88%9B%E5%BB%BA%E9%93%BE%E6%8E%A5)
  - [diff - 比较文件内容差异](#diff---%E6%AF%94%E8%BE%83%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9%E5%B7%AE%E5%BC%82)
  - [which - 找查命令文件路径](#which---%E6%89%BE%E6%9F%A5%E5%91%BD%E4%BB%A4%E6%96%87%E4%BB%B6%E8%B7%AF%E5%BE%84)
  - [whereis - 找查命令文件路径](#whereis---%E6%89%BE%E6%9F%A5%E5%91%BD%E4%BB%A4%E6%96%87%E4%BB%B6%E8%B7%AF%E5%BE%84)
  - [find - 查找文件位置](#find---%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
  - [locate/slocate - 查找文件位置](#locateslocate---%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
  - [sort - 将文件进行排序并输出](#sort---%E5%B0%86%E6%96%87%E4%BB%B6%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%E5%B9%B6%E8%BE%93%E5%87%BA)
  - [uniq - 去除文件中的重复内容行](#uniq---%E5%8E%BB%E9%99%A4%E6%96%87%E4%BB%B6%E4%B8%AD%E7%9A%84%E9%87%8D%E5%A4%8D%E5%86%85%E5%AE%B9%E8%A1%8C)
  - [split - 文件分割](#split---%E6%96%87%E4%BB%B6%E5%88%86%E5%89%B2)
  - [shuf - 打乱顺序产生随机的排列](#shuf---%E6%89%93%E4%B9%B1%E9%A1%BA%E5%BA%8F%E4%BA%A7%E7%94%9F%E9%9A%8F%E6%9C%BA%E7%9A%84%E6%8E%92%E5%88%97)
  - [tar - 归档使用工具](#tar---%E5%BD%92%E6%A1%A3%E4%BD%BF%E7%94%A8%E5%B7%A5%E5%85%B7)
  - [zip - zip格式压缩文件](#zip---zip%E6%A0%BC%E5%BC%8F%E5%8E%8B%E7%BC%A9%E6%96%87%E4%BB%B6)
  - [unzip - 解压zip包](#unzip---%E8%A7%A3%E5%8E%8Bzip%E5%8C%85)
  - [dd - 转换和复制文件](#dd---%E8%BD%AC%E6%8D%A2%E5%92%8C%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6)
  - [chattr - 更改文件隐藏属性](#chattr---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E9%9A%90%E8%97%8F%E5%B1%9E%E6%80%A7)
  - [lsattr - 显示文件隐藏属性](#lsattr---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E9%9A%90%E8%97%8F%E5%B1%9E%E6%80%A7)
  - [cksum - 检查文件](#cksum---%E6%A3%80%E6%9F%A5%E6%96%87%E4%BB%B6)
  - [md5sum - 检查文件md5值](#md5sum---%E6%A3%80%E6%9F%A5%E6%96%87%E4%BB%B6md5%E5%80%BC)
  - [cmp - 比较文件差异](#cmp---%E6%AF%94%E8%BE%83%E6%96%87%E4%BB%B6%E5%B7%AE%E5%BC%82)
  - [file - 命令用于辨识文件类型](#file---%E5%91%BD%E4%BB%A4%E7%94%A8%E4%BA%8E%E8%BE%A8%E8%AF%86%E6%96%87%E4%BB%B6%E7%B1%BB%E5%9E%8B)
  - [cut - 按列提取文件内容](#cut---%E6%8C%89%E5%88%97%E6%8F%90%E5%8F%96%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [od - 八进制输出文件内容](#od---%E5%85%AB%E8%BF%9B%E5%88%B6%E8%BE%93%E5%87%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [paste - 按对应行合并两个文件](#paste---%E6%8C%89%E5%AF%B9%E5%BA%94%E8%A1%8C%E5%90%88%E5%B9%B6%E4%B8%A4%E4%B8%AA%E6%96%87%E4%BB%B6)
  - [tmpwatch - 删除暂存文件](#tmpwatch---%E5%88%A0%E9%99%A4%E6%9A%82%E5%AD%98%E6%96%87%E4%BB%B6)
  - [comm - 命令用于比较两个已排过序的文件](#comm---%E5%91%BD%E4%BB%A4%E7%94%A8%E4%BA%8E%E6%AF%94%E8%BE%83%E4%B8%A4%E4%B8%AA%E5%B7%B2%E6%8E%92%E8%BF%87%E5%BA%8F%E7%9A%84%E6%96%87%E4%BB%B6)
  - [tr - 字符转换](#tr---%E5%AD%97%E7%AC%A6%E8%BD%AC%E6%8D%A2)
  - [expr - 算术表达式](#expr---%E7%AE%97%E6%9C%AF%E8%A1%A8%E8%BE%BE%E5%BC%8F)
  - [let - 算术表达式](#let---%E7%AE%97%E6%9C%AF%E8%A1%A8%E8%BE%BE%E5%BC%8F)
  - [wc-  统计文件的字节数、单词数、行数](#wc---%E7%BB%9F%E8%AE%A1%E6%96%87%E4%BB%B6%E7%9A%84%E5%AD%97%E8%8A%82%E6%95%B0%E5%8D%95%E8%AF%8D%E6%95%B0%E8%A1%8C%E6%95%B0)
  - [zcat/zgrep - 过滤压缩包里面的内容](#zcatzgrep---%E8%BF%87%E6%BB%A4%E5%8E%8B%E7%BC%A9%E5%8C%85%E9%87%8C%E9%9D%A2%E7%9A%84%E5%86%85%E5%AE%B9)
  - [tac - 反向打印文本](#tac---%E5%8F%8D%E5%90%91%E6%89%93%E5%8D%B0%E6%96%87%E6%9C%AC)
- [文件传输](#%E6%96%87%E4%BB%B6%E4%BC%A0%E8%BE%93)
  - [ftp - ftp协议文件传送](#ftp---ftp%E5%8D%8F%E8%AE%AE%E6%96%87%E4%BB%B6%E4%BC%A0%E9%80%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 系统管理

## groupadd - 添加用户组

:point_right:用户文件/etc/group。

```bash
groupadd [options] ${group_name}

#	常用options
-g, --gid GID # 用户组 组id
```

## groupmod - 修改用户组

## groupdel - 删除用户组

 ## useradd - 添加用户

:point_right:用户文件/etc/passwd。

```bash
 useradd [options] ${user_name}
 
 #	常用options
 -d, --home-dir HOME_DIR  #	用户工作目录
 -g, --gid GROUP   # 用户组id
 -p, --password PASSWORD #	用户密码
 -u, --uid UID # 用户id
 
 #	例子 
 useradd stonebird
```

## usermod - 修改用户

```bash
usermod [options] ${user_name}
# 和useradd一致
# 例子
usermod -g 1002 stonebird
```

## userdel - 删除用户

```bash
userdel [options] ${user_name}
# options
-r, --remove 删除用户目录

# 例子
userdel stonebird
userdel -r stonebird
```

## passwd - 修改用户密码

:point_right:用户文件/etc/shadow。

```bash
passwd ${user_name}

# 非交互模式 root 
--stdin             read new tokens from stdin (root only)
echo "123456"|passwd --stdin stonebird
```

## chpasswd - 修改当前用户

# 文件管理/目录管理

## chown - 更改文件用户、属组

```bash
 chown [OPTION]... [OWNER][:[GROUP]] FILE
 
 # 常用options
 -R	递归目录
 
 # 例子
 chown root test.txt
 chown -R stonebird:stonebird test.txt
```

## chmod - 更改文件权限

```bash
chmod [OPTION]... MODE[,MODE]... FILE...

u 表示该文件的拥有者，g 表示与该文件的拥有者属于同一个群体(group)者，o 表示其他以外的人，a 表示这三者皆是。
+ 表示增加权限、- 表示取消权限、= 表示唯一设定权限。
r 表示可读取，w 表示可写入，x 表示可执行，X 表示只有当该文件是个子目录或者该文件已经被设定过为可执行。

# 例子
chmod +x test.sh
chmod 644 test.sh
chmod a=rwx file
chmod ug=rwx,o=x file
```

## touch - 创建文件或修改文件访问时间

```bash
touch ${file_name}
```

## tree - 树状图列出目录的内容

```bash
tree path
```

## vi/vim - 编辑文件内容

```bash
# 常用快捷键
:set nu=每行显示行号  
:set nonu=取消显示行号
:${line}   ## 0，$
## 编辑模式
0=单行首  
$=单行末
gg=文件首行  
G=文件末行  
u 撤销
:m,ns/old/new/g=第m行到n行，所有“old“串替为“new“  
```

## ls - 列出文件目录

```bash
ls [OPTION]... [FILE]...

# 常用options
-a	# 显示所有文件 含.开头
-l  # 详细信息
-d  # 只列出文件夹
-f  # 只列出文件
-r  # 对列出的排序
-t  # 通过时间排序access time (-u): atime, access, use;
	# change time (-c): ctime, status;
```

## dir - 列出文件

```bash
dir [OPTION]... [FILE]...

# 常用和 ls 一样 
```

## cd - 切换工作目录

```bash
cd dir

# 常用例子
cd # 切换工作目录
cd dir # 切断到dir
cd - # 切换到之前的目录
cd . # 当前
cd .. # 切换到上层
```

## pwd - 显示当前工作目录

## dirs - 显示当前工作目录

## cp - 文件文件或者目录

```bash
cp [OPTION]... [-T] SOURCE DEST

## 常用options 
-f	若目标文件已存在，则会直接覆盖原文件
-i	若目标文件已存在，则会询问是否覆盖
-p	保留源文件或目录的所有属性
-r	递归复制文件和目录
```

## scp - 基于SSH协议远程复制文件或目录

```bash
scp [OPTION]... SOURCE DEST

## 常用options 
-4	使用ipv4
-6	使用ipv6
-P	指定远程主机的端口号
-q	不显示复制进度
-r	以递归方式复制

# 例子
scp -r 192.168.10.10:/root/stonebird /root
scp -r /root 192.168.10.10:/root/stonebird
```

## rcp - 远程复制文件或目录

```bash
rcp [OPTION]... SOURCE DEST

## 常用options 
-r	递归处理，将指定目录下的文件与子目录一并处理
-D	指定远程服务器的端口号
```

## mkdir - 创建文件或者目录

```bash
mkdir [OPTION]... DIRECTORY...

## 常用options
-m, --mode=MODE   设置文件或者目录权限, not a=rwx - umask
-p, --parents     递归创建多级目录

## 例子
mkdir -p /home/stonebird/data/run.sh
mkdir -m 755 -p /home/stonebird/data/run.sh
```

## rmdir - 删除一个空文件夹

```bash
rmdir [OPTION]... DIRECTORY...

## 常用options
-p	用递归的方式删除指定的目录路径中的所有父级目录，非空则报错
-v	显示命令的详细执行过程
```

## rm - 删除文件或目录

```bash
rm [OPTION]... [FILE]...

## 常用options
-f	强制删除（不二次询问）
-i	删除前会询问用户是否操作
-r/R	递归删除
-v	显示指令的详细执行过程

## 例子
rm -rf /home/stonebird
```

## mv - 移动或改名文件

```bash
mv [OPTION]... SOURCE... DIRECTORY

## 常用options
-i	若存在同名文件，则向用户询问是否覆盖
-f	覆盖已有文件时，不进行任何提示
-b	当文件存在时，覆盖前为其创建一个备份

## 例子
mv data /home/stonebird/
mv run.sh run_test.sh
```

## cat - 查看文件内容

```bash
cat [OPTION]... [FILE]...

## 常用options
-n	显示行数（空行也编号）
-s	显示行数（多个空行算一个编号）
-b	显示行数（空行不编号）
-E	每行结束处显示$符号
-T	将TAB字符显示为 ^I符号
-v	使用 ^ 和 M- 引用，除了 LFD 和 TAB 之外
-e	等价于”-vE”组合
-t	等价于”-vT”组合
-A	等价于 -vET组合

## 例子
cat -A run.txt
cat -n run.txt
```

## more - 分页显示文件内容

```bash
more [options] <file>...

## 常用options
-num	指定每屏显示的行数
-l	more在通常情况下把 ^L 当作特殊字符, 遇到这个字符就会暂停,-l选项可以阻止这种特性
+/pattern	在每个文档显示前搜寻该字(pattern)，然后从该字串之后开始显示
+num 	从第 num 行开始显示

## 常用键
Enter 向下n行，需要定义。默认为1行
Ctrl+F 向下滚动一屏
空格键 向下滚动一屏
Ctrl+B 返回上一屏
```

## less - 分页显示文件内容

```bash
less  [options] <file>...

## 常用键
空格键 滚动一页
回车键 滚动一行
[pagedown]： 向下翻动一页
[pageup]： 向上翻动一页
```

## head -  显示文件开头的内容

```bash
head [OPTION]... [FILE]...
 
## 常用options
-n <数字>	定义显示行数
 
## 例子
head -n 50 run.txt
```

## tail - 显示文件结尾的内容

```bash
tail [OPTION]... [FILE]...
 
## 常用options
-f	持续显示文件最新追加的内容
-n <N>	输出文件的尾部N（N位数字）行内容

## 例子
tail -n 50 run.txt
tail -f run.log
```

## grep/egrep - 文本过滤

```BASH
grep [OPTION]... PATTERNS [FILE]...

## 常用options
-i	忽略大小写
-n	列出所有的匹配行，显示行号
-v	显示不包含匹配文本的所有行
-o	仅显示匹配的行的非空部分
-E	支持扩展的正则表达式
```

## awk - 文本和数据进行处理的编程语言

```bash
awk [POSIX or GNU style options] -f progfile [--] file ...

## 常用options
-F	指定输入时用到的字段分隔符

## 内置变量
ARGC	命令行参数个数
ARGV	命令行参数排列
ENVIRON	支持队列中系统环境变量的使用
FILENAME	awk浏览的文件名
FNR	浏览文件的记录数
FS	设置输入域分隔符，等价于命令行 -F选项
NF	浏览记录的域的个数
NR	已读的记录数
OFS	输出域分隔符
ORS	输出记录分隔符
RS	控制记录分隔符
```

## sed -  批量编辑文本文件

```bash
sed [OPTION]... {script-only-if-no-other-script} [input-file]...
 
## 常用options
-i 在原文件编辑
-n或--quiet或--silent 仅显示script处理后的结果。

## 动作说明
a ：新增， a 的后面可以接字串，而这些字串会在新的一行出现(目前的下一行)～
c ：取代， c 的后面可以接字串，这些字串可以取代 n1,n2 之间的行！
d ：删除，因为是删除啊，所以 d 后面通常不接任何东东；
i ：插入， i 的后面可以接字串，而这些字串会在新的一行出现(目前的上一行)；
p ：打印，亦即将某个选择的数据印出。通常 p 会与参数 sed -n 一起运行～
s ：取代，可以直接进行取代的工作哩！通常这个 s 的动作可以搭配正则表达式！例如 1,20s/old/new/g 就是啦！
```

## ln - 创建链接

软连接：L开始，删除源文件，会影响链接文件
硬链接：和源文件一样的基本信息，删除原文件对链接文件没影响

```bash
ln [OPTION]... [-T] TARGET LINK_NAME

## 常用options
-s  创建软连接
```

## diff - 比较文件内容差异

```bash
diff [OPTION]... FILES

## 常用options
-a	逐行比较文本文件
-y	以并列的方式显示文件的异同之处
```

## which - 找查命令文件路径

## whereis - 找查命令文件路径

```bash
## 常用options
-b	查找二进制程序或命令
-B	从指定目录下 查找二进制程序或命令
-m	查找man手册文件
```

## find - 查找文件位置

```bash
find [path...] [expression]

## 常用options
-name	按名称查找
-size	按大小查找
-user	按属性查找
-type	按类型查找
-iname	忽略大小写
-mount, -xdev : 只检查和指定目录在同一个文件系统下的文件，避免列出其它文件系统中的文件
-amin n : 在过去 n 分钟内被读取过
-anewer file : 比文件 file 更晚被读取过的文件
-atime n : 在过去n天内被读取过的文件
-cmin n : 在过去 n 分钟内被修改过
-cnewer file :比文件 file 更新的文件
-ctime n : 在过去n天内被修改过的文件
-empty : 空的文件-gid n or -group name : gid 是 n 或是 group 名称是 name
-ipath p, -path p : 路径名称符合 p 的文件，ipath 会忽略大小写
-name name, -iname name : 文件名称符合 name 的文件。iname 会忽略大小写
-size n : 文件大小 是 n 单位，b 代表 512 位元组的区块，c 表示字元数，k 表示 kilo bytes，w 是二个位元组。
-type c : 文件类型是 c 的文件。
d: 目录
c: 字型装置文件
b: 区块装置文件
p: 具名贮列
f: 一般文件
l: 符号连结

## 例子
find / -type d -perm 1777
```

## locate/slocate - 查找文件位置

```bash
locate ${file_name}

## 常用options
-d 指定目录
```

## sort - 将文件进行排序并输出

```bash
sort [OPTION]... [FILE]...

## 常用options
-n	依照数值的大小排序
-r	以相反的顺序来排序
-t <分隔字符>	指定排序时所用的栏位分隔字符
-k	指定需要排序的栏位

## 例子
sort -t : -k 3 -n user.txt
```

## uniq - 去除文件中的重复内容行

```bash
uniq [OPTION]... [INPUT [OUTPUT]]

## 常用options
-c	打印每行在文本中重复出现的次数
-d	每个重复纪录只出现一次
-u	只显示没有重复的纪录
-i, --ignore-case   忽略大小写差异
```

## split - 文件分割

```bash
split [OPTION]... [FILE [PREFIX]]

##  常用options
-b	指定每多少字节切成一个小文件
-l  指定多少行
```

## shuf - 打乱顺序产生随机的排列

```bash
-e	将每个ARG视为输入行
```

## tar - 归档使用工具

```bash
tar [OPTION...] [FILE]...

## 常用options
-c	建立新的备份文件
-C <目录>	仅压缩指定目录里的内容或解压缩到指定目录
-x	从归档文件中提取文件
-z	通过gzip指令压缩/解压缩文件，文件名最好为*.tar.gz
-f  <备份文件>	指定备份文件
-v	显示指令执行过程
-r	添加文件到已经压缩的文件
-v	显示操作过程
-j	通过bzip2指令压缩/解压缩文件，文件名最好为*.tar.bz2

# 例子
tar czvf backup1.tar.gz /etc
tar cjvf backup2.tar.bz2 /etc
tar xvf backup4.tar -C /etc
```

## zip - zip格式压缩文件

```bash
## 常用options
-d	更新压缩包内文件

# 例子
zip -r backup1.zip /etc
```

## unzip - 解压zip包

```bash
unzip backup1.zip
```

## dd - 转换和复制文件

```bash
dd OPTION

## 例子
dd if=anaconda-ks.cfg of=ana.cfg count=1 bs=50
```

## chattr - 更改文件隐藏属性

```bash
chattr [-pRVf] [-+=aAcCdDeijPsStTuFx] [-v version] files...

## 常用options
-R	递归处理目录下的所有文件
-v	设置文件或目录版本
-V	显示指令执行过程
+	开启文件或目录的该项属性
--	关闭文件或目录的该项属性
=	指定文件或目录的该项属性

# 常用权限
i	无法对文件进行修改；若对目录设置了该参数，则仅能修改其中的子文件内容而不能新建或删除文件
a	仅允许补充（追加）内容，无法覆盖/删除内容（Append Only）

## 例子
chattr +i run.sh
```

## lsattr - 显示文件隐藏属性

```bash
## 常用options
-a 	列出目录中的所有文件，包括隐藏文件
-d 	只显示目录名称
-R	递归地处理指定目录下的所有文件及子目录

## 例子
lsattr run.sh
```

## cksum - 检查文件

```bash
cksum ${file_name}
```

## md5sum - 检查文件md5值

```bash
md5sum ${file_name}
```

## cmp - 比较文件差异

```bash
cmp file...
```

## file - 命令用于辨识文件类型

```bash
file ${file_name}
```

## cut - 按列提取文件内容

```bash
cut [OPTIONS] FILE...

## 常用options
-c	以字符为单位进行分割
-b	以字节为单位进行分割
-d	自定义分隔符，默认为制表符”TAB”
-f	显示指定字段的内容
-n	取消分割多字节字符

## 例子
cut -d : -f 1 /etc/passwd
```

## od - 八进制输出文件内容

## paste - 按对应行合并两个文件

```bash
## 例子
paste  f1 f2
```

## tmpwatch - 删除暂存文件

```bash
## 常用options

-a	删除任何类型的文件
-f	强制删除文件或目录，其效果类似rm指令的”-f”参数

## 例子
tmpwatch 24 /tmp/  #删除tmp目录24小时未使用的文件
```

## comm - 命令用于比较两个已排过序的文件

```bash
## 常用options
-1 	不显示只在第1个文件里出现过的列
-2	不显示只在第2个文件里出现过的列
-3	不显示只在第1和第2个文件里出现过的列
```

## tr - 字符转换

```bash
## 常用options
-c ——complerment：取代所有不属于第一字符集的字符；
-d ——delete：删除所有属于第一字符集的字符；
-s --squeeze-repeats：把连续重复的字符以单独一个字符表示；
-t --truncate-set1：先删除第一字符集较第二字符集多出的字符。

## 例子
echo "HELLO WORLD" | tr 'A-Z' 'a-z'
```

## expr - 算术表达式

```bash
## 例子
match	中匹配 REGEXP 字符串并返回匹配字符串的长度
substr	从 POS 位置获取长度为 LENGTH 的字符串
index	杳找子字符串的起始位置
length	计算字符串的长度

expr match "123 456 789" ".*5"  # 6 匹配字符串的长度，若找不到则返回 0
expr substr " this is a test" 3 5 # his i 
expr index "test for the game" "e" # 2 
expr length "this is a test" # 14
expr 10 + 10
expr 10 - 10
expr 20 / 10
expr 10 \* 10 # * 需要转义
expr \( 10 + 10 \) \* 2 + 100
```

## let - 算术表达式

```bash
## 例子
a=1
let a++ # a=`expr $a + 1`
```

## wc-  统计文件的字节数、单词数、行数

```bash
## 常用options
-w	统计字数，或--words：只显示字数。一个字被定义为由空白、跳格或换行字符分隔的字符串
-c	统计字节数，或--bytes或--chars：只显示Bytes数
-l	统计行数，或--lines：只显示列数
-m	统计字符数
-L	打印最长行的长度

## 例子
wc -l stonebird.txt
```

## zcat/zgrep - 过滤压缩包里面的内容

## tac - 反向打印文本

 

# 文件传输

## ftp - ftp协议文件传送

```bash
FTP>ascii: 设定以ASCII方式传送文件(缺省值)
FTP>bell: 每完成一次文件传送,报警提示.
FTP>binary: 设定以二进制方式传送文件.
FTP>bye: 终止主机FTP进程,并退出FTP管理方式.
FTP>case: 当为ON时,用MGET命令拷贝的文件名到本地机器中,全部转换为小写字母.
FTP>cd: 同UNIX的CD命令.
FTP>cdup: 返回上一级目录.
FTP>chmod: 改变远端主机的文件权限.
FTP>close: 终止远端的FTP进程,返回到FTP命令状态, 所有的宏定义都被删除.
FTP>delete: 删除远端主机中的文件.
FTP>dir [remote-directory] [local-file] 列出当前远端主机目录中的文件.如果有本地文件,就将结果写至本地文件.
FTP>get [remote-file] [local-file] 从远端主机中传送至本地主机中.
FTP>help [command] 输出命令的解释.
FTP>lcd: 改变当前本地主机的工作目录,如果缺省,就转到当前用户的HOME目录.
FTP>ls [remote-directory] [local-file] 同DIR.
FTP>macdef: 定义宏命令.
FTP>mdelete [remote-files] 删除一批文件.
FTP>mget [remote-files] 从远端主机接收一批文件至本地主机.
FTP>mkdir directory-name 在远端主机中建立目录.
FTP>mput local-files 将本地主机中一批文件传送至远端主机.
FTP>open host [port] 重新建立一个新的连接.
FTP>prompt: 交互提示模式.
FTP>put local-file [remote-file] 将本地一个文件传送至远端主机中.
FTP>pwd: 列出当前远端主机目录.
FTP>quit: 同BYE.
FTP>recv remote-file [local-file] 同GET.
FTP>rename [from] [to] 改变远端主机中的文件名.
FTP>rmdir directory-name 删除远端主机中的目录.
FTP>send local-file [remote-file] 同PUT.
FTP>status: 显示当前FTP的状态.
FTP>system: 显示远端主机系统类型.
FTP>user user-name [password] [account] 重新以别的用户名登录远端主机.
FTP>? [command]: 同HELP. [command]指定需要帮助的命令名称。如果没有指定 command，ftp 将显示全部命令的列表。
FTP>! 从 ftp 子系统退出到外壳。
```




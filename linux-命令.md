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


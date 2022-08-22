<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [系统管理](#%E7%B3%BB%E7%BB%9F%E7%AE%A1%E7%90%86)
  - [:point_right:groupadd - 添加用户组](#point_rightgroupadd---%E6%B7%BB%E5%8A%A0%E7%94%A8%E6%88%B7%E7%BB%84)
  - [:point_right:groupmod - 修改用户组](#point_rightgroupmod---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7%E7%BB%84)
  - [:point_right:groupdel - 删除用户组](#point_rightgroupdel---%E5%88%A0%E9%99%A4%E7%94%A8%E6%88%B7%E7%BB%84)
  - [:point_right:useradd - 添加用户](#point_rightuseradd---%E6%B7%BB%E5%8A%A0%E7%94%A8%E6%88%B7)
  - [:point_right:usermod - 修改用户](#point_rightusermod---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7)
  - [:point_right:userdel - 删除用户](#point_rightuserdel---%E5%88%A0%E9%99%A4%E7%94%A8%E6%88%B7)
  - [:point_right:passwd - 修改用户密码](#point_rightpasswd---%E4%BF%AE%E6%94%B9%E7%94%A8%E6%88%B7%E5%AF%86%E7%A0%81)
  - [:point_right:su - 切换用户](#point_rightsu---%E5%88%87%E6%8D%A2%E7%94%A8%E6%88%B7)
  - [chpasswd - 修改当前用户](#chpasswd---%E4%BF%AE%E6%94%B9%E5%BD%93%E5%89%8D%E7%94%A8%E6%88%B7)
  - [:point_right:date - 显示或设置系统日期与时间](#point_rightdate---%E6%98%BE%E7%A4%BA%E6%88%96%E8%AE%BE%E7%BD%AE%E7%B3%BB%E7%BB%9F%E6%97%A5%E6%9C%9F%E4%B8%8E%E6%97%B6%E9%97%B4)
  - [finger - 查询其他使用者的资料](#finger---%E6%9F%A5%E8%AF%A2%E5%85%B6%E4%BB%96%E4%BD%BF%E7%94%A8%E8%80%85%E7%9A%84%E8%B5%84%E6%96%99)
  - [:point_right:who/whoami/w - 查看当前登录用户信息](#point_rightwhowhoamiw---%E6%9F%A5%E7%9C%8B%E5%BD%93%E5%89%8D%E7%99%BB%E5%BD%95%E7%94%A8%E6%88%B7%E4%BF%A1%E6%81%AF)
  - [:point_right:sleep - 延迟当前命令的执行(s)](#point_rightsleep---%E5%BB%B6%E8%BF%9F%E5%BD%93%E5%89%8D%E5%91%BD%E4%BB%A4%E7%9A%84%E6%89%A7%E8%A1%8Cs)
  - [usleep - 延迟当前命令的执行(us)](#usleep---%E5%BB%B6%E8%BF%9F%E5%BD%93%E5%89%8D%E5%91%BD%E4%BB%A4%E7%9A%84%E6%89%A7%E8%A1%8Cus)
  - [:point_right:crontab - 管理定时计划任务](#point_rightcrontab---%E7%AE%A1%E7%90%86%E5%AE%9A%E6%97%B6%E8%AE%A1%E5%88%92%E4%BB%BB%E5%8A%A1)
  - [at - 一次性定时计划任务](#at---%E4%B8%80%E6%AC%A1%E6%80%A7%E5%AE%9A%E6%97%B6%E8%AE%A1%E5%88%92%E4%BB%BB%E5%8A%A1)
  - [batch - 指定时间执行任务](#batch---%E6%8C%87%E5%AE%9A%E6%97%B6%E9%97%B4%E6%89%A7%E8%A1%8C%E4%BB%BB%E5%8A%A1)
  - [:point_right:alias - 设置命令别名](#point_rightalias---%E8%AE%BE%E7%BD%AE%E5%91%BD%E4%BB%A4%E5%88%AB%E5%90%8D)
  - [:point_right:time - 指令执行时所消耗的时间](#point_righttime---%E6%8C%87%E4%BB%A4%E6%89%A7%E8%A1%8C%E6%97%B6%E6%89%80%E6%B6%88%E8%80%97%E7%9A%84%E6%97%B6%E9%97%B4)
  - [declare - 声明shell变量](#declare---%E5%A3%B0%E6%98%8Eshell%E5%8F%98%E9%87%8F)
  - [:point_right:export - 查看或设置环境变量](#point_rightexport---%E6%9F%A5%E7%9C%8B%E6%88%96%E8%AE%BE%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F)
  - [:point_right:systemctl - 管理系统服务](#point_rightsystemctl---%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F%E6%9C%8D%E5%8A%A1)
  - [:point_right:service - 管理系统服务](#point_rightservice---%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F%E6%9C%8D%E5%8A%A1)
  - [:point_right:clear - 清除屏幕](#point_rightclear---%E6%B8%85%E9%99%A4%E5%B1%8F%E5%B9%95)
  - [:point_right:dmesg - 显示开机信息](#point_rightdmesg---%E6%98%BE%E7%A4%BA%E5%BC%80%E6%9C%BA%E4%BF%A1%E6%81%AF)
  - [:point_right:halt - 关闭当前服务器系统](#point_righthalt---%E5%85%B3%E9%97%AD%E5%BD%93%E5%89%8D%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%B3%BB%E7%BB%9F)
  - [shutdown - 关闭服务器的系统](#shutdown---%E5%85%B3%E9%97%AD%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%9A%84%E7%B3%BB%E7%BB%9F)
  - [:point_right:reboot - 重启系统](#point_rightreboot---%E9%87%8D%E5%90%AF%E7%B3%BB%E7%BB%9F)
  - [lsmod - 加载kernel模块管理](#lsmod---%E5%8A%A0%E8%BD%BDkernel%E6%A8%A1%E5%9D%97%E7%AE%A1%E7%90%86)
  - [:point_right:modprobe - kernel模块智能加载工具](#point_rightmodprobe---kernel%E6%A8%A1%E5%9D%97%E6%99%BA%E8%83%BD%E5%8A%A0%E8%BD%BD%E5%B7%A5%E5%85%B7)
  - [insmod - 用于载入kernel模块](#insmod---%E7%94%A8%E4%BA%8E%E8%BD%BD%E5%85%A5kernel%E6%A8%A1%E5%9D%97)
  - [rmmod - 用于删除kernel模块](#rmmod---%E7%94%A8%E4%BA%8E%E5%88%A0%E9%99%A4kernel%E6%A8%A1%E5%9D%97)
  - [modinfo - 显示kernel模块的信息](#modinfo---%E6%98%BE%E7%A4%BAkernel%E6%A8%A1%E5%9D%97%E7%9A%84%E4%BF%A1%E6%81%AF)
  - [:point_right:sysctl - 配置内核参数](#point_rightsysctl---%E9%85%8D%E7%BD%AE%E5%86%85%E6%A0%B8%E5%8F%82%E6%95%B0)
  - [:point_right:kdump - 系统崩溃时记录日志](#point_rightkdump---%E7%B3%BB%E7%BB%9F%E5%B4%A9%E6%BA%83%E6%97%B6%E8%AE%B0%E5%BD%95%E6%97%A5%E5%BF%97)
- [文件管理/目录管理](#%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E7%9B%AE%E5%BD%95%E7%AE%A1%E7%90%86)
  - [:point_right:chown - 更改文件用户、属组](#point_rightchown---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E7%94%A8%E6%88%B7%E5%B1%9E%E7%BB%84)
  - [:point_right:chmod - 更改文件权限](#point_rightchmod---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E6%9D%83%E9%99%90)
  - [:point_right:touch - 创建文件或修改文件访问时间](#point_righttouch---%E5%88%9B%E5%BB%BA%E6%96%87%E4%BB%B6%E6%88%96%E4%BF%AE%E6%94%B9%E6%96%87%E4%BB%B6%E8%AE%BF%E9%97%AE%E6%97%B6%E9%97%B4)
  - [:point_right:tree - 树状图列出目录的内容](#point_righttree---%E6%A0%91%E7%8A%B6%E5%9B%BE%E5%88%97%E5%87%BA%E7%9B%AE%E5%BD%95%E7%9A%84%E5%86%85%E5%AE%B9)
  - [:point_right:vi/vim - 编辑文件内容](#point_rightvivim---%E7%BC%96%E8%BE%91%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [:point_right:ls - 列出文件目录](#point_rightls---%E5%88%97%E5%87%BA%E6%96%87%E4%BB%B6%E7%9B%AE%E5%BD%95)
  - [:point_right:dir - 列出文件](#point_rightdir---%E5%88%97%E5%87%BA%E6%96%87%E4%BB%B6)
  - [:point_right:cd - 切换工作目录](#point_rightcd---%E5%88%87%E6%8D%A2%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [:point_right:pwd - 显示当前工作目录](#point_rightpwd---%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [:point_right:dirs - 显示当前工作目录](#point_rightdirs---%E6%98%BE%E7%A4%BA%E5%BD%93%E5%89%8D%E5%B7%A5%E4%BD%9C%E7%9B%AE%E5%BD%95)
  - [:point_right:cp - 文件文件或者目录](#point_rightcp---%E6%96%87%E4%BB%B6%E6%96%87%E4%BB%B6%E6%88%96%E8%80%85%E7%9B%AE%E5%BD%95)
  - [:point_right:scp - 基于SSH协议远程复制文件或目录](#point_rightscp---%E5%9F%BA%E4%BA%8Essh%E5%8D%8F%E8%AE%AE%E8%BF%9C%E7%A8%8B%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [rcp - 远程复制文件或目录](#rcp---%E8%BF%9C%E7%A8%8B%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [:point_right:mkdir - 创建文件或者目录](#point_rightmkdir---%E5%88%9B%E5%BB%BA%E6%96%87%E4%BB%B6%E6%88%96%E8%80%85%E7%9B%AE%E5%BD%95)
  - [rmdir - 删除一个空文件夹](#rmdir---%E5%88%A0%E9%99%A4%E4%B8%80%E4%B8%AA%E7%A9%BA%E6%96%87%E4%BB%B6%E5%A4%B9)
  - [:point_right:rm - 删除文件或目录](#point_rightrm---%E5%88%A0%E9%99%A4%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95)
  - [:point_right:mv - 移动或改名文件](#point_rightmv---%E7%A7%BB%E5%8A%A8%E6%88%96%E6%94%B9%E5%90%8D%E6%96%87%E4%BB%B6)
  - [:point_right:cat - 查看文件内容](#point_rightcat---%E6%9F%A5%E7%9C%8B%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [more - 分页显示文件内容](#more---%E5%88%86%E9%A1%B5%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [:point_right:less - 分页显示文件内容](#point_rightless---%E5%88%86%E9%A1%B5%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [:point_right:head -  显示文件开头的内容](#point_righthead----%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%BC%80%E5%A4%B4%E7%9A%84%E5%86%85%E5%AE%B9)
  - [:point_right:tail - 显示文件结尾的内容](#point_righttail---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E7%BB%93%E5%B0%BE%E7%9A%84%E5%86%85%E5%AE%B9)
  - [:point_right:grep/egrep - 文本过滤](#point_rightgrepegrep---%E6%96%87%E6%9C%AC%E8%BF%87%E6%BB%A4)
  - [:point_right:awk - 文本和数据进行处理的编程语言](#point_rightawk---%E6%96%87%E6%9C%AC%E5%92%8C%E6%95%B0%E6%8D%AE%E8%BF%9B%E8%A1%8C%E5%A4%84%E7%90%86%E7%9A%84%E7%BC%96%E7%A8%8B%E8%AF%AD%E8%A8%80)
  - [:point_right:sed -  批量编辑文本文件](#point_rightsed----%E6%89%B9%E9%87%8F%E7%BC%96%E8%BE%91%E6%96%87%E6%9C%AC%E6%96%87%E4%BB%B6)
  - [:point_right:ln - 创建链接](#point_rightln---%E5%88%9B%E5%BB%BA%E9%93%BE%E6%8E%A5)
  - [:point_right:diff - 比较文件内容差异](#point_rightdiff---%E6%AF%94%E8%BE%83%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9%E5%B7%AE%E5%BC%82)
  - [which - 找查命令文件路径](#which---%E6%89%BE%E6%9F%A5%E5%91%BD%E4%BB%A4%E6%96%87%E4%BB%B6%E8%B7%AF%E5%BE%84)
  - [:point_right:whereis - 找查命令文件路径](#point_rightwhereis---%E6%89%BE%E6%9F%A5%E5%91%BD%E4%BB%A4%E6%96%87%E4%BB%B6%E8%B7%AF%E5%BE%84)
  - [:point_right:find - 查找文件位置](#point_rightfind---%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
  - [:point_right:locate/slocate - 查找文件位置](#point_rightlocateslocate---%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
  - [:point_right:sort - 将文件进行排序并输出](#point_rightsort---%E5%B0%86%E6%96%87%E4%BB%B6%E8%BF%9B%E8%A1%8C%E6%8E%92%E5%BA%8F%E5%B9%B6%E8%BE%93%E5%87%BA)
  - [:point_right:uniq - 去除文件中的重复内容行](#point_rightuniq---%E5%8E%BB%E9%99%A4%E6%96%87%E4%BB%B6%E4%B8%AD%E7%9A%84%E9%87%8D%E5%A4%8D%E5%86%85%E5%AE%B9%E8%A1%8C)
  - [:point_right:split - 文件分割](#point_rightsplit---%E6%96%87%E4%BB%B6%E5%88%86%E5%89%B2)
  - [:point_right:shuf - 打乱顺序产生随机的排列](#point_rightshuf---%E6%89%93%E4%B9%B1%E9%A1%BA%E5%BA%8F%E4%BA%A7%E7%94%9F%E9%9A%8F%E6%9C%BA%E7%9A%84%E6%8E%92%E5%88%97)
  - [:point_right:tar - 归档使用工具](#point_righttar---%E5%BD%92%E6%A1%A3%E4%BD%BF%E7%94%A8%E5%B7%A5%E5%85%B7)
  - [:point_right:zip - zip格式压缩文件](#point_rightzip---zip%E6%A0%BC%E5%BC%8F%E5%8E%8B%E7%BC%A9%E6%96%87%E4%BB%B6)
  - [:point_right:unzip - 解压zip包](#point_rightunzip---%E8%A7%A3%E5%8E%8Bzip%E5%8C%85)
  - [gzip 压缩和解压文件（.gz文件）](#gzip-%E5%8E%8B%E7%BC%A9%E5%92%8C%E8%A7%A3%E5%8E%8B%E6%96%87%E4%BB%B6gz%E6%96%87%E4%BB%B6)
  - [bzip2 - 压缩和解压文件](#bzip2---%E5%8E%8B%E7%BC%A9%E5%92%8C%E8%A7%A3%E5%8E%8B%E6%96%87%E4%BB%B6)
  - [dd - 转换和复制文件](#dd---%E8%BD%AC%E6%8D%A2%E5%92%8C%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6)
  - [:point_right:chattr - 更改文件隐藏属性](#point_rightchattr---%E6%9B%B4%E6%94%B9%E6%96%87%E4%BB%B6%E9%9A%90%E8%97%8F%E5%B1%9E%E6%80%A7)
  - [:point_right:lsattr - 显示文件隐藏属性](#point_rightlsattr---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E9%9A%90%E8%97%8F%E5%B1%9E%E6%80%A7)
  - [cksum - 检查文件](#cksum---%E6%A3%80%E6%9F%A5%E6%96%87%E4%BB%B6)
  - [:point_right:md5sum - 检查文件md5值](#point_rightmd5sum---%E6%A3%80%E6%9F%A5%E6%96%87%E4%BB%B6md5%E5%80%BC)
  - [cmp - 比较文件差异](#cmp---%E6%AF%94%E8%BE%83%E6%96%87%E4%BB%B6%E5%B7%AE%E5%BC%82)
  - [file - 命令用于辨识文件类型](#file---%E5%91%BD%E4%BB%A4%E7%94%A8%E4%BA%8E%E8%BE%A8%E8%AF%86%E6%96%87%E4%BB%B6%E7%B1%BB%E5%9E%8B)
  - [:point_right:cut - 按列提取文件内容](#point_rightcut---%E6%8C%89%E5%88%97%E6%8F%90%E5%8F%96%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [od - 八进制输出文件内容](#od---%E5%85%AB%E8%BF%9B%E5%88%B6%E8%BE%93%E5%87%BA%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9)
  - [hexdump - 显示文件十六进制格式](#hexdump---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E5%8D%81%E5%85%AD%E8%BF%9B%E5%88%B6%E6%A0%BC%E5%BC%8F)
  - [strings - 查找可打印的字符串](#strings---%E6%9F%A5%E6%89%BE%E5%8F%AF%E6%89%93%E5%8D%B0%E7%9A%84%E5%AD%97%E7%AC%A6%E4%B8%B2)
  - [stat - 显示文件或文件系统的详细信息](#stat---%E6%98%BE%E7%A4%BA%E6%96%87%E4%BB%B6%E6%88%96%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F%E7%9A%84%E8%AF%A6%E7%BB%86%E4%BF%A1%E6%81%AF)
  - [diff3 - 比较3个文件的不同之处](#diff3---%E6%AF%94%E8%BE%833%E4%B8%AA%E6%96%87%E4%BB%B6%E7%9A%84%E4%B8%8D%E5%90%8C%E4%B9%8B%E5%A4%84)
  - [vimdiff - 同时对比编辑多个文件](#vimdiff---%E5%90%8C%E6%97%B6%E5%AF%B9%E6%AF%94%E7%BC%96%E8%BE%91%E5%A4%9A%E4%B8%AA%E6%96%87%E4%BB%B6)
  - [paste - 按对应行合并两个文件](#paste---%E6%8C%89%E5%AF%B9%E5%BA%94%E8%A1%8C%E5%90%88%E5%B9%B6%E4%B8%A4%E4%B8%AA%E6%96%87%E4%BB%B6)
  - [tmpwatch - 删除暂存文件](#tmpwatch---%E5%88%A0%E9%99%A4%E6%9A%82%E5%AD%98%E6%96%87%E4%BB%B6)
  - [comm - 命令用于比较两个已排过序的文件](#comm---%E5%91%BD%E4%BB%A4%E7%94%A8%E4%BA%8E%E6%AF%94%E8%BE%83%E4%B8%A4%E4%B8%AA%E5%B7%B2%E6%8E%92%E8%BF%87%E5%BA%8F%E7%9A%84%E6%96%87%E4%BB%B6)
  - [:point_right:tr - 字符转换](#point_righttr---%E5%AD%97%E7%AC%A6%E8%BD%AC%E6%8D%A2)
  - [:point_right:expr - 算术表达式](#point_rightexpr---%E7%AE%97%E6%9C%AF%E8%A1%A8%E8%BE%BE%E5%BC%8F)
  - [:point_right:let - 算术表达式](#point_rightlet---%E7%AE%97%E6%9C%AF%E8%A1%A8%E8%BE%BE%E5%BC%8F)
  - [:point_right:wc -  统计文件的字节数、单词数、行数](#point_rightwc----%E7%BB%9F%E8%AE%A1%E6%96%87%E4%BB%B6%E7%9A%84%E5%AD%97%E8%8A%82%E6%95%B0%E5%8D%95%E8%AF%8D%E6%95%B0%E8%A1%8C%E6%95%B0)
  - [zcat/zgrep - 过滤压缩包里面的内容](#zcatzgrep---%E8%BF%87%E6%BB%A4%E5%8E%8B%E7%BC%A9%E5%8C%85%E9%87%8C%E9%9D%A2%E7%9A%84%E5%86%85%E5%AE%B9)
  - [tac - 反向打印文本](#tac---%E5%8F%8D%E5%90%91%E6%89%93%E5%8D%B0%E6%96%87%E6%9C%AC)
  - [:point_right:dos2unix - 将文本文件转成unix格式](#point_rightdos2unix---%E5%B0%86%E6%96%87%E6%9C%AC%E6%96%87%E4%BB%B6%E8%BD%AC%E6%88%90unix%E6%A0%BC%E5%BC%8F)
- [进程和监控](#%E8%BF%9B%E7%A8%8B%E5%92%8C%E7%9B%91%E6%8E%A7)
  - [:point_right:ps - 查看进程](#point_rightps---%E6%9F%A5%E7%9C%8B%E8%BF%9B%E7%A8%8B)
  - [:point_right:top - 实时显示系统运行状态](#point_righttop---%E5%AE%9E%E6%97%B6%E6%98%BE%E7%A4%BA%E7%B3%BB%E7%BB%9F%E8%BF%90%E8%A1%8C%E7%8A%B6%E6%80%81)
  - [iotop - 监视磁盘I/O状态](#iotop---%E7%9B%91%E8%A7%86%E7%A3%81%E7%9B%98io%E7%8A%B6%E6%80%81)
  - [iftop - 套接字及进程的网络利用率](#iftop---%E5%A5%97%E6%8E%A5%E5%AD%97%E5%8F%8A%E8%BF%9B%E7%A8%8B%E7%9A%84%E7%BD%91%E7%BB%9C%E5%88%A9%E7%94%A8%E7%8E%87)
  - [iostat - 监视系统输入输出设备和CPU的使用情况](#iostat---%E7%9B%91%E8%A7%86%E7%B3%BB%E7%BB%9F%E8%BE%93%E5%85%A5%E8%BE%93%E5%87%BA%E8%AE%BE%E5%A4%87%E5%92%8Ccpu%E7%9A%84%E4%BD%BF%E7%94%A8%E6%83%85%E5%86%B5)
  - [:point_right:kill - 杀死进程](#point_rightkill---%E6%9D%80%E6%AD%BB%E8%BF%9B%E7%A8%8B)
  - [pkill - 按照进程名杀死进程](#pkill---%E6%8C%89%E7%85%A7%E8%BF%9B%E7%A8%8B%E5%90%8D%E6%9D%80%E6%AD%BB%E8%BF%9B%E7%A8%8B)
  - [killall - 使用进程名称来杀死一组进程](#killall---%E4%BD%BF%E7%94%A8%E8%BF%9B%E7%A8%8B%E5%90%8D%E7%A7%B0%E6%9D%A5%E6%9D%80%E6%AD%BB%E4%B8%80%E7%BB%84%E8%BF%9B%E7%A8%8B)
  - [vmstat - 显示虚拟内存状态](#vmstat---%E6%98%BE%E7%A4%BA%E8%99%9A%E6%8B%9F%E5%86%85%E5%AD%98%E7%8A%B6%E6%80%81)
  - [:point_right:dstat - 全能系统信息统计工具](#point_rightdstat---%E5%85%A8%E8%83%BD%E7%B3%BB%E7%BB%9F%E4%BF%A1%E6%81%AF%E7%BB%9F%E8%AE%A1%E5%B7%A5%E5%85%B7)
  - [:point_right:netstat - 显示网络状态](#point_rightnetstat---%E6%98%BE%E7%A4%BA%E7%BD%91%E7%BB%9C%E7%8A%B6%E6%80%81)
  - [:point_right:ss - 显示活动套接字信息](#point_rightss---%E6%98%BE%E7%A4%BA%E6%B4%BB%E5%8A%A8%E5%A5%97%E6%8E%A5%E5%AD%97%E4%BF%A1%E6%81%AF)
  - [:point_right:free - 显示系统内存使用量情况](#point_rightfree---%E6%98%BE%E7%A4%BA%E7%B3%BB%E7%BB%9F%E5%86%85%E5%AD%98%E4%BD%BF%E7%94%A8%E9%87%8F%E6%83%85%E5%86%B5)
  - [:point_right:lsof - 查看文件的进程信息](#point_rightlsof---%E6%9F%A5%E7%9C%8B%E6%96%87%E4%BB%B6%E7%9A%84%E8%BF%9B%E7%A8%8B%E4%BF%A1%E6%81%AF)
- [文件系统和磁盘](#%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F%E5%92%8C%E7%A3%81%E7%9B%98)
  - [:point_right:fsck/fsck.ext2/fsck.ext3/fsck.ext4/fsck.xfs - 检查与修复文件系统](#point_rightfsckfsckext2fsckext3fsckext4fsckxfs---%E6%A3%80%E6%9F%A5%E4%B8%8E%E4%BF%AE%E5%A4%8D%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F)
  - [:point_right:mount - 把文件系统挂载到目录](#point_rightmount---%E6%8A%8A%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F%E6%8C%82%E8%BD%BD%E5%88%B0%E7%9B%AE%E5%BD%95)
  - [:point_right:umount - 卸载文件系统](#point_rightumount---%E5%8D%B8%E8%BD%BD%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F)
  - [:point_right:du - 查看文件或目录的大小](#point_rightdu---%E6%9F%A5%E7%9C%8B%E6%96%87%E4%BB%B6%E6%88%96%E7%9B%AE%E5%BD%95%E7%9A%84%E5%A4%A7%E5%B0%8F)
  - [:point_right:df - 显示磁盘空间使用情况](#point_rightdf---%E6%98%BE%E7%A4%BA%E7%A3%81%E7%9B%98%E7%A9%BA%E9%97%B4%E4%BD%BF%E7%94%A8%E6%83%85%E5%86%B5)
  - [parted - 磁盘分区工具](#parted---%E7%A3%81%E7%9B%98%E5%88%86%E5%8C%BA%E5%B7%A5%E5%85%B7)
  - [:point_right:fdisk - 管理磁盘分区](#point_rightfdisk---%E7%AE%A1%E7%90%86%E7%A3%81%E7%9B%98%E5%88%86%E5%8C%BA)
  - [:point_right:lsblk - 查看块设备](#point_rightlsblk---%E6%9F%A5%E7%9C%8B%E5%9D%97%E8%AE%BE%E5%A4%87)
- [文件传输](#%E6%96%87%E4%BB%B6%E4%BC%A0%E8%BE%93)
  - [:point_right:ftp - ftp协议文件传送](#point_rightftp---ftp%E5%8D%8F%E8%AE%AE%E6%96%87%E4%BB%B6%E4%BC%A0%E9%80%81)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 系统管理

## :point_right:groupadd - 添加用户组

:point_right:用户文件/etc/group。

```bash
groupadd [options] ${group_name}

#	常用options
-g, --gid GID # 用户组 组id
```

## :point_right:groupmod - 修改用户组

## :point_right:groupdel - 删除用户组

 ## :point_right:useradd - 添加用户

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

## :point_right:usermod - 修改用户

```bash
usermod [options] ${user_name}
# 和useradd一致
# 例子
usermod -g 1002 stonebird
```

## :point_right:userdel - 删除用户

```bash
userdel [options] ${user_name}
# options
-r, --remove 删除用户目录

# 例子
userdel stonebird
userdel -r stonebird
```

## :point_right:passwd - 修改用户密码

:point_right:用户文件/etc/shadow。

```bash
passwd ${user_name}

# 非交互模式 root 
--stdin             read new tokens from stdin (root only)
echo "123456"|passwd --stdin stonebird
```

## :point_right:su - 切换用户

中间带 `-` 使用用户的环境变量

```bash
# options
-c	执行完指定的指令后，即恢复原来的身份
```

## chpasswd - 修改当前用户

## :point_right:date - 显示或设置系统日期与时间

```bash
date [OPTION]... [+FORMAT]

## 例子
date  +"%Y-%m-%d %H:%M:%S"
date +%s
```

## finger - 查询其他使用者的资料

```bash
finger root
```

## :point_right:who/whoami/w - 查看当前登录用户信息

## :point_right:sleep - 延迟当前命令的执行(s)

```bash
## 常用options
number 	时间长度，后面可接 s、m、h 或 d
<数字>s	秒数
<数字>m	分钟
<数字>h	小时
<数字>d	日期

## 例子
sleep 10  # 默认 s
sleep 3m
```

## usleep - 延迟当前命令的执行(us)

```bash
# 延迟0.1秒
sleep 0.1
usleep 100000
 
# 延迟 10 毫秒
sleep 0.01
usleep 10000
```

## :point_right:crontab - 管理定时计划任务

```bash
# For details see man 4 crontabs
# Example of job definition:
# .---------------- minute (0 - 59)
# | .------------- hour (0 - 23)
# | | .---------- day of month (1 - 31)
# | | | .------- month (1 - 12) OR jan,feb,mar,apr ...
# | | | | .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# | | | | |
# * * * * * user-name command to be executed

"*"代表所有的取值范围内的数字，如月份字段为*，则表示1到12个月；
"/"代表每一定时间间隔的意思，如分钟字段为*/10，表示每10分钟执行1次。
"-"代表从某个区间范围，是闭区间。如“2-5”表示“2,3,4,5”，小时字段中0-23/2表示在0~23点范围内每2个小时执行一次。
","分散的数字（不一定连续），如1,2,3,4,7,9。

## 常用options
-e	编辑任务
-l	列出任务
-r	删除任务
-u	指定用户名字

## 例子
3,15   *    *    *    *  command  # 每小时的第3和第15分钟执行command
3,15  8-11  *  *  *  command # 8-10点，每小时的第3和第15分钟执行command
*  */1  *  *  *  /etc/init.d/smb restart # 每小时重启一次
```

## at - 一次性定时计划任务

```bash
## 常用options
atq	查看系统中的等待作业
-d	删除系统中的等待作业(等效于atrm命令)
```

## batch - 指定时间执行任务

## :point_right:alias - 设置命令别名

```bash
## 常用options
-p	打印已经设置的命令别名

## 例子
alias ll=ls -lt
alias -p
```

## :point_right:time - 指令执行时所消耗的时间

```bash
time command
```

## declare - 声明shell变量

```bash
## 常用options
-a	声明数组变量
-f	仅显示函数
-F	不显示函数定义
-i	先计算表达式，把结果赋给所声明变量
-p	显示给定变量的定义的方法和值，当使用此选项时，其他的选项将被忽略
-r	定义只读变量
-x	将指定的Shell变量转换成环境变量

## 例子
declare -x file_name="test.txt"
```

## :point_right:export - 查看或设置环境变量

推荐使用，内部会转成declare

```bash
-f	指定函数名称
-n	删除指定的变量
-p	列出所有的环境变量
## 例子
export file_name="test.txt"
export |grep file_name
```

## :point_right:systemctl - 管理系统服务

```bash
##	常用options
start	启动服务
stop	停止服务
restart	重启服务
enable	使某服务开机自启
disable	关闭某服务开机自启
status	查看服务状态
list -units --type=service	列举所有已启动服务

## 例子
systemctl start httpd
```

## :point_right:service - 管理系统服务

```bash
## 例子
systemctl httpd [stop|start|restart|stauts]
```

## :point_right:clear - 清除屏幕

原理是向后翻页

## :point_right:dmesg - 显示开机信息

排查系统开机问题的重要参数 /var/log/dmesg

## :point_right:halt - 关闭当前服务器系统

```bash
## 常用options
-w	模拟关机，把过程写入到日志文件
-d	不写入日志纪录
-f	强制关机或重启
-i	关机或重启前关掉所有的网络服务
```

## shutdown - 关闭服务器的系统

```bash
-r	将系统重启
-t	送出警告信息和删除信息之间要延迟多少秒
```

## :point_right:reboot - 重启系统

## lsmod - 加载kernel模块管理

lsmod命令的指定结果共有三列。
Module：模块名。
Size：模块大小。
Used by：模块是否被其他模块调用。

## :point_right:modprobe - kernel模块智能加载工具

```bash
## 常用options
-a	加载命令行给出的全部的模块
-c	显示所有模块的设置信息
-d	使用排错模式
-l	显示可用的模块
-r	从内核中移除模块
-t	指定模块类型
-s	记录错误信息到系统日志中
```

## insmod - 用于载入kernel模块

install mod

```bash
-f 　不检查目前kernel版本与模块编译时的kernel版本是否一致，强制将模块载入。
-k 　将模块设置为自动卸除。
-m 　输出模块的载入信息。
-o<模块名称> 　指定模块的名称，可使用模块文件的文件名。
-p 　测试模块是否能正确地载入kernel。
-s 　将所有信息记录在系统记录文件中。
-v 　执行时显示详细的信息。
-x 　不要汇出模块的外部符号。
-X 　汇出模块所有的外部符号，此为预设置
```

## rmmod - 用于删除kernel模块

```bash
rmmod [-as][模块名称...]
```

## modinfo - 显示kernel模块的信息

```bash
## 常用options
-a	显示模块开发人员
```

## :point_right:sysctl - 配置内核参数

配置内核参数，sysctl命令被用于在内核运行时动态地修改内核的运行参数，可用的内核参数在目录“/proc/sys”中。

sysctl命令对内核参数的修改仅在当前生效，重启系统后参数丢失。如果希望参数永久生效可以修改配置文件“/etc/sysctl.conf”。

~~~shell
-n	打印值时不打印关键字
-e	忽略未知关键字错误
-N	仅打印名称
-w	当改变sysctl设置时使用此项
-p	从配置文件“/etc/sysctl.conf”加载内核参数设置
-a	打印当前所有可用的内核参数变量和值
-A	以表格方式打印当前所有可用的内核参数变量和值

## 读取
sysctl net.ipv6.neigh.lo.locktime
net.ipv6.neigh.lo.locktime = 0

## 修改
sysctl net.ipv6.neigh.lo.locktime=1
net.ipv6.neigh.lo.locktime = 1 
~~~

## :point_right:kdump - 系统崩溃时记录日志

# 文件管理/目录管理

## :point_right:chown - 更改文件用户、属组

```bash
 chown [OPTION]... [OWNER][:[GROUP]] FILE
 
 # 常用options
 -R	递归目录
 
 # 例子
 chown root test.txt
 chown -R stonebird:stonebird test.txt
```

## :point_right:chmod - 更改文件权限

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

## :point_right:touch - 创建文件或修改文件访问时间

```bash
touch ${file_name}
```

## :point_right:tree - 树状图列出目录的内容

```bash
tree path
```

## :point_right:vi/vim - 编辑文件内容

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

## :point_right:ls - 列出文件目录

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

## :point_right:dir - 列出文件

```bash
dir [OPTION]... [FILE]...

# 常用和 ls 一样 
```

## :point_right:cd - 切换工作目录

```bash
cd dir

# 常用例子
cd # 切换工作目录
cd dir # 切断到dir
cd - # 切换到之前的目录
cd . # 当前
cd .. # 切换到上层
```

## :point_right:pwd - 显示当前工作目录

## :point_right:dirs - 显示当前工作目录

## :point_right:cp - 文件文件或者目录

```bash
cp [OPTION]... [-T] SOURCE DEST

## 常用options 
-f	若目标文件已存在，则会直接覆盖原文件
-i	若目标文件已存在，则会询问是否覆盖
-p	保留源文件或目录的所有属性
-r	递归复制文件和目录
```

## :point_right:scp - 基于SSH协议远程复制文件或目录

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

## :point_right:mkdir - 创建文件或者目录

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

## :point_right:rm - 删除文件或目录

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

## :point_right:mv - 移动或改名文件

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

## :point_right:cat - 查看文件内容

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

## :point_right:less - 分页显示文件内容

```bash
less  [options] <file>...

## 常用键
空格键 滚动一页
回车键 滚动一行
[pagedown]： 向下翻动一页
[pageup]： 向上翻动一页
```

## :point_right:head -  显示文件开头的内容

```bash
head [OPTION]... [FILE]...
 
## 常用options
-n <数字>	定义显示行数
 
## 例子
head -n 50 run.txt
```

## :point_right:tail - 显示文件结尾的内容

```bash
tail [OPTION]... [FILE]...
 
## 常用options
-f	持续显示文件最新追加的内容
-n <N>	输出文件的尾部N（N位数字）行内容

## 例子
tail -n 50 run.txt
tail -f run.log
```

## :point_right:grep/egrep - 文本过滤

```BASH
grep [OPTION]... PATTERNS [FILE]...

## 常用options
-i	忽略大小写
-n	列出所有的匹配行，显示行号
-v	显示不包含匹配文本的所有行
-o	仅显示匹配的行的非空部分
-E	支持扩展的正则表达式
```

## :point_right:awk - 文本和数据进行处理的编程语言

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

## :point_right:sed -  批量编辑文本文件

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

## :point_right:ln - 创建链接

软连接：L开始，删除源文件，会影响链接文件
硬链接：和源文件一样的基本信息，删除原文件对链接文件没影响

```bash
ln [OPTION]... [-T] TARGET LINK_NAME

## 常用options
-s  创建软连接
```

## :point_right:diff - 比较文件内容差异

```bash
diff [OPTION]... FILES

## 常用options
-a	逐行比较文本文件
-y	以并列的方式显示文件的异同之处
```

## which - 找查命令文件路径

## :point_right:whereis - 找查命令文件路径

```bash
## 常用options
-b	查找二进制程序或命令
-B	从指定目录下 查找二进制程序或命令
-m	查找man手册文件
```

## :point_right:find - 查找文件位置

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

## :point_right:locate/slocate - 查找文件位置

```bash
locate ${file_name}

## 常用options
-d 指定目录
```

## :point_right:sort - 将文件进行排序并输出

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

## :point_right:uniq - 去除文件中的重复内容行

```bash
uniq [OPTION]... [INPUT [OUTPUT]]

## 常用options
-c	打印每行在文本中重复出现的次数
-d	每个重复纪录只出现一次
-u	只显示没有重复的纪录
-i, --ignore-case   忽略大小写差异
```

## :point_right:split - 文件分割

```bash
split [OPTION]... [FILE [PREFIX]]

##  常用options
-b	指定每多少字节切成一个小文件
-l  指定多少行
```

## :point_right:shuf - 打乱顺序产生随机的排列

```bash
-e	将每个ARG视为输入行
```

## :point_right:tar - 归档使用工具

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

## :point_right:zip - zip格式压缩文件

```bash
## 常用options
-d	更新压缩包内文件

# 例子
zip -r backup1.zip /etc
```

## :point_right:unzip - 解压zip包

```bash
unzip backup1.zip
```

## gzip 压缩和解压文件（.gz文件）

gzip 只能针对普通文件（regular file）进行压缩和解压，对于文件夹、符号链接等是不支持的。

```shell
-a	使用ASCII文字模式
-d	解开压缩文件  
-f	强行压缩文件
-l	列出压缩文件的相关信息
-c	把压缩后的文件输出到标准输出设备，不去更动原始文件
-r	递归处理，将指定目录下的所有文件及子目录一并处理 # 对目录下的单个文件
-q	不显示警告信息

gzip hero.avi
gzip -d hero.avi.gz
```

## bzip2 - 压缩和解压文件

由于 bzip2 与 gzip 相比，其压缩稳定性和效果都更好，对应单个文件bzip2 命令和 bunzip2 命令，就可以实现了

```shell
 bzip2 abc1.txt 
 bunzip2 A.txt.bz2
 
 tar -xjvf curl-7.47.1.tar.bz2 /dir
 tar -zvf curl-7.47.1.tar.bz2
```

## dd - 转换和复制文件

```bash
dd OPTION

## 例子
dd if=anaconda-ks.cfg of=ana.cfg count=1 bs=50
```

## :point_right:chattr - 更改文件隐藏属性

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

## :point_right:lsattr - 显示文件隐藏属性

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

## :point_right:md5sum - 检查文件md5值

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

## :point_right:cut - 按列提取文件内容

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

## hexdump - 显示文件十六进制格式

```shell
-n length	只格式化输入文件的前length个字节
-C	输出规范的十六进制和ASCII码
-b	单字节八进制显示
-c	单字节字符显示
-d	双字节十进制显示
-o	双字节八进制显示
-x	双字节十六进制显示
-s	从偏移量开始输出
-e	指定格式字符串，格式字符串包含在一对单引号中
-v	显示所有输入数据

hexdump testfile
```

## strings - 查找可打印的字符串

在对象文件或二进制文件中

```bash
ls |strings
```

## stat - 显示文件或文件系统的详细信息

```shell
-L	支持符号链接
-f	显示文件系统的信息
-t	以简洁的方式输出

stat hurl.go
  File: hurl.go
  Size: 938             Blocks: 8          IO Block: 4096   regular file
Device: fc01h/64513d    Inode: 929074      Links: 1
Access: (0664/-rw-rw-r--)  Uid: (  500/  ubuntu)   Gid: (  500/  ubuntu)
Access: 2021-12-05 12:05:42.491584506 +0800
Modify: 2021-12-05 10:50:02.472892197 +0800
Change: 2021-12-05 12:05:41.559580684 +0800
 Birth: -
```

## diff3 - 比较3个文件的不同之处

~~~shell
-A	全部显示，有冲突内容用括号括起来
-a	将所有文件视为文本
-T	使制表符对齐

diff3 file1 file2 file3
~~~

## vimdiff - 同时对比编辑多个文件

```shell
vimdiff file1 file2 
```

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

## :point_right:tr - 字符转换

```bash
## 常用options
-c ——complerment：取代所有不属于第一字符集的字符；
-d ——delete：删除所有属于第一字符集的字符；
-s --squeeze-repeats：把连续重复的字符以单独一个字符表示；
-t --truncate-set1：先删除第一字符集较第二字符集多出的字符。

## 例子
echo "HELLO WORLD" | tr 'A-Z' 'a-z'
```

## :point_right:expr - 算术表达式

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

## :point_right:let - 算术表达式

```bash
## 例子
a=1
let a++ # a=`expr $a + 1`
```

## :point_right:wc -  统计文件的字节数、单词数、行数

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

```bash
zcat ${tar_name}
```

## tac - 反向打印文本

```bash
tac ${file_name}
```

 ## :point_right:dos2unix - 将文本文件转成unix格式

```bash
dos2unix ${file_name}
```

# 进程和监控

## :point_right:ps - 查看进程

```bash
ps [options]

## 常用options
a	显示现行终端机下的所有程序，包括其他用户的程序
e	列出程序时，显示每个程序所使用的环境变量
f	用ASCII字符显示树状结构，表达程序间的相互关系
g	显示现行终端机下的所有程序，包括所属组的程序
-G <群组识别码>	列出属于该群组的程序的状况
h	不显示标题列
-H	显示树状结构，表示程序间的相互关系
-l	采用详细的格式来显示程序状况
L	列出栏位的相关信息
u	以用户为主的格式来显示程序状况
-U <用户识别码>	列出属于该用户的程序的状况
U <用户名称>	列出属于该用户的程序的状况
v	采用虚拟内存的格式显示程序状况
x	显示所有程序，不以终端机来区分

## 例子
ps -ef
ps -auxl
```

## :point_right:top - 实时显示系统运行状态

```bash
top [options]

## 常用options
-d <秒>	改变显示的更新速度
-p pid(s)  查看指定pid
-o field 
-w [cols]

## 例子
top
top -p 1
```

## iotop - 监视磁盘I/O状态

```bash
## 常用options
-o	只显示有io操作的进程
-n NUM	显示NUM次，主要用于非交互式模式
-d SEC	间隔SEC秒显示一次
-p PID	监控的进程pid
-u USER	监控的进程用户
```

## iftop - 套接字及进程的网络利用率

```bash
## 常用options
-i	指定要监控的网卡
```

## iostat - 监视系统输入输出设备和CPU的使用情况

```bash
## 常用options
-c	仅显示CPU使用情况
-d	仅显示设备利用率
```

## :point_right:kill - 杀死进程

```bash
## 常用options
-l 列出信号量

## 常用信号量 -9 -15
```

## pkill - 按照进程名杀死进程

```bash
## 常用options
-o	仅向找到的最小（起始）进程号发送信号
-n	仅向找到的最大（结束）进程号发送信号
-P	指定父进程号发送信号
-g	指定进程组
-t	指定开启进程的终端

## 例子
pkill httpd
pkill -o
pkill -n
```

## killall - 使用进程名称来杀死一组进程
```bash
## 常用options
-u	杀死指定用户的进程

## 例子
killall -9 nginx
```

## vmstat - 显示虚拟内存状态

```bash
## 常用options
-a	显示活动内页
-f	显示启动后创建的进程总数
-m	显示slab信息
-n	头信息仅显示一次
-s	以表格方式显示事件计数器和内存状态
-d	报告磁盘状态
-p	显示指定的硬盘分区状态

## 例子
vmstat -p /dev/vdb1
```

## :point_right:dstat - 全能系统信息统计工具
```bash
## 常用options
-c	显示CPU系统占用，用户占用，空闲，等待，中断，软件中断等信息
-d	显示磁盘读写数据大小
-n	显示网络状态
-l	显示系统负载情况
-m	显示内存使用情况
-g	显示页面使用情况
-p	显示进程状态
-s	显示交换分区使用情况
-r	I/O请求情况
-y	系统状态

## 例子
dstat -n
dstat -d
```

## :point_right:netstat - 显示网络状态

```bash
## 	常用options
-a	显示所有连线中的Socket
-p	显示正在使用Socket的程序识别码和程序名称
-l	仅列出在监听的服务状态
-t	显示TCP传输协议的连线状况
-u	显示UDP传输协议的连线状况
-i	显示网络界面信息表单
-r	显示路由表信息
-n	直接使用IP地址，不通过域名服务器

## 例子
netstat -a
```

## :point_right:ss - 显示活动套接字信息

```bash
## 常用options
-n	不解析服务名称，已数字方式显示
-a	显示所有套接字
-l	显示处于监听状态的套接字
-o	显示计时器信息
-e	显示详细的套接字信息
-m	显示套接字的内存使用情况
-p	显示使用套接字的进程
-i	显示内部的TCP信息
-s	显示套接字使用概况
-4	仅显示ipv4的套接字
-6	仅显示ipv6的套接字
-0	显示PACKET套接字
-t	只显示TCP套接字
-u	只显示UDP套接字
-d	只显示DCCP套接字
-w	只显示RAW套接字
-x	只显示 Unix套接字
-D	将原始TCP套接字信息转储到文件

## 例子
ss -t
```

## :point_right:free - 显示系统内存使用量情况

```bash
## 常用options
-b	以Byte显示内存使用情况
-k	以kb为单位显示内存使用情况
-m	以mb为单位显示内存使用情况
-g	以gb为单位显示内存使用情况

## 例子
free -m
```

## :point_right:lsof - 查看文件的进程信息

```bash
## 常用options
-a	列出打开文件存在的进程
-c <进程名>	列出指定进程所打开的文件
-g	列出GID号进程详情
-d <文件号>	列出占用该文件号的进程
+d <目录>	列出目录下被打开的文件
+D <目录>	递归列出目录下被打开的文件
-n <目录>	列出使用NFS的文件
-i <条件>	列出符合条件的进程
-p <进程号>	列出指定进程号所打开的文件
-u	列出UID号进程详情

## 例子
lsof -a
```

# 文件系统和磁盘

1、XFS是一个具有非常高性能且可扩展的文件系统，同时在大多数要求的应用程序中都会进行常规部署。XFS提供了一种健壮的、优秀的以及功能丰富的文件系统，它具有的可伸缩性能够满足最苛刻的存储需求。
2、ext4：ext3的升级版本，ext4对ext3做了很多深层次的改进，设计更合理、性能更好、更可靠，同时还引入了一些新功能。
3、ext3：ext2的升级版本，其主要优点是在ext2的基础上加入了记录数据的日志功能。
4、ext2：支持标准Unix文件类型，可用于多种存储介质，向上兼容性好。

## :point_right:fsck/fsck.ext2/fsck.ext3/fsck.ext4/fsck.xfs - 检查与修复文件系统

```bash
## 常用options
-a	自动修复文件系统
-f	强制检查
-A	依照/etc/fstab文件来检查全部文件系统
-N	不执行指令，仅列出实际执行会进行的动作
-r	采用互动模式，在执行修复时询问问题
-R	略过指定的文件系统不予检查
-t	指定要检查的文件系统类型
-T	执行fsck指令时，不显示标题信息
-V	显示指令执行过程
```

## :point_right:mount - 把文件系统挂载到目录

```bash
## 常用options
-t	指定挂载类型
-a	加载文件“/etc/fstab”中描述的所有文件系统
-r  以只读的形式挂载
-rw 以读写的形式挂载

## 例子
mount /dev/vdb /mnt/stonebird
```

## :point_right:umount - 卸载文件系统

```bash
## 常用options
-a	加载文件“/etc/fstab”中描述的所有文件系统

## 例子
umount /dev/sdb
```

## :point_right:du - 查看文件或目录的大小

```bash
## 常用options
-a	显示目录中所有文件大小
-k	以KB为单位显示文件大小
-m	以MB为单位显示文件大小
-g	以GB为单位显示文件大小
-h	以易读方式显示文件大小
--max-depth=N 指定统计深度
-s	仅显示总计

## 例子
du -sh . |sort -n
```

## :point_right:df - 显示磁盘空间使用情况

```bash
## 常用options
-a	显示所有系统文件
-h	以容易阅读的方式显示
-H	以1000字节为换算单位来显示
-t <文件系统类型>	只显示指定类型的文件系统
-T	输出时显示文件系统类型
## 例子
df -h
```

## parted - 磁盘分区工具

```bash
parted [options] [device [command [options...]...]]

## 常用options
-a  为新创建的分区设置对齐方式
-s  脚本模式
-v  显示版本号
-l  列出所有块设备上的分区布局
-m  显示机器可解析的输出
```

## :point_right:fdisk - 管理磁盘分区

```bash
## 常用options
-l	列出指定的外围设备的分区表状况

## 菜单操作说明
m ：显示菜单和帮助信息
a ：活动分区标记/引导分区
d ：删除分区
l ：显示分区类型
n ：新建分区
p ：显示分区信息
q ：退出不保存
t ：设置分区号
v ：进行分区检查
w ：保存修改
x ：扩展应用，高级功能
```

## :point_right:lsblk - 查看块设备

```bash
-a	显示所有设备
-t	显示拓扑结构信息
```



# 文件传输

## :point_right:ftp - ftp协议文件传送

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




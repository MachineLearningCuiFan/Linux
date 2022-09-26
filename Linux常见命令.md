**计算机中，一个正在执行的程序或命令，被叫做“进程”（process）。** 

**启动之后一只存在、常驻内存的进程，一般被称作“服务”（service）。**

systemctl start | stop | restart | status  服务名  （Centos7）




**1、Vim编辑器的使用**(默认模式)

yy 					 复制光标当前一行

dd				 	删除光标当前行

shift+g             移动到页尾


**2、查看网络配置**

ifconfig :network interfaces configuring 	  显示所有网络接口的配置信息

vim /etc/sysconfig/network-scripts/ifcfg-ens33     	查看IP配置文件       

systemctl stop NetworkManager      	启动/关闭网络服务

systemctl disable NetworkManager      	网络服务开机关闭自启动

vim  /etc/hostname     查看当前服务器主机名称


**3、关机重启**

（1）**sync**   （功能描述：将数据由内存同步到硬盘中） 

（2）halt   （功能描述：停机，关闭系统，但不断电） 

（3）poweroff   （功能描述：关机，断电） 

（4）reboot  （功能描述：就是重启，等同于 shutdown -r now）

（4）shutdown [选项] 时间


**4、文件目录类:**

pwd     		print working directory 打印工作目录 

ls				list 列出目录内容(-a:全部文件，-l行列出)

cd				Change Directory 切换路径

mkdir			Make directory 建立目录

rmdir			Remove directory 移除目录

touch  文件名称    	创建空文件

cp [选项] source dest			复制文件或目录  (-r 递归复制整个文件夹)

rm [选项] deleteFile  （功能描述：递归删除目录中所有内容）

-r 		递归删除目录中所有内容 

-f 		强制执行删除操作，而不提示用于进行确认。

mv /temp/movefile /targetFolder 			移动文件与目录或重命名

cat     		查看文件内容，从第一行开始显示。

more			指令是一个基于 VI 编辑器的文本过滤器，它以全屏幕的方式按页显示文本文件 

的内容。more 指令中内置了若干快捷键，详见操作说明。

less			分屏显示文件内容

echo			输出内容到控制台

输出重定向和 >> 追加


**4、用户管理命令**

useradd 		添加新用户

useradd -g 组名 用户名 （功能描述：添加新用户到某个组）

passwd 设置用户密码

su: swith user 切换用户

userdel 删除用户

usermod 修改用户			usermod -g 用户组 用户名

chmod 改变文件权限

chown 改变文件所有者

chgrp 改变所属组


**5、搜索查找类**

find 查找文件或者目录			find [搜索范围] [选项

locate 快速定位文件路径

grep 过滤查找及“		|”管道符


**6、压缩解压**

tar -zcvf xiyou.tar.gz xiyou/      压缩 xiyou/

tar -zxvf houma.tar.gz          解压到当前路径

tar -zxvf xiyou.tar.gz -C /opt     解压到/opt


**7 、磁盘查看和分区类**

du: disk usage 磁盘占用情况

df: disk free 空余磁盘


**8、进程系统资源管理类**

ps:process status 进程状态

ps aux | grep xxx 		（功能描述：查看系统中所有进程） 

ps -ef | grep xxx 			（功能描述：可以查看子父进程之间的关系）

kill [选项] 进程号 

（功能描述：通过进程号杀死进程，-9表示强迫进程立即停止） 

killall 进程名称 

（功能描述：通过进程名称杀死进程，也支持通配符，这 

在系统因负载过大而变得很慢时很有用）

pstree 查看进程树

top 实时监控系统进程状态

netstat 显示网络状态和端口占用信息


**9、安装包管理**

rpm -qa （功能描述：查询所安装的所有 rpm 软件包）

（1）rpm -e RPM软件包 

（2） rpm -e --nodeps 软件包

（--nodeps 	卸载软件时，不检查依赖。这样的话，那些使用该软件包的软件）

（3） rpm -ivh RPM 包全名  		 RPM 安装命令

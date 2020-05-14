# Linux 学习笔记

## 在 CentOS 8 上安装和使用 Apache Web 服务器

### 安装

```
sudo yum install httpd
```

### 启动

```
sudo systemctl start httpd
```

### 查看状态
```
sudo systemctl status httpd
```

### 停止
```
sudo systemctl stop httpd
```

参考：[如何在CentOS 7上安装Apache Web服务器
](https://www.howtoing.com/how-to-install-the-apache-web-server-on-centos-7)

## 利用 nohup 后台运行 jar 文件包程序

Linux 运行 jar 包命令如下：

### 方式一：

```
java -jar XXX.jar
```

特点：当前 ssh 窗口被锁定，可按`CTRL + C`打断程序运行，或直接关闭窗口，程序退出

那如何让窗口不锁定？

### 方式二

```
java -jar XXX.jar &
```

`&`代表在后台运行。

特点：当前 ssh 窗口不被锁定，但是当窗口关闭时，程序中止运行。

继续改进，如何让窗口关闭时，程序仍然运行？



### 方式三

```
nohup java -jar XXX.jar &
```

`nohup`意思是不挂断运行命令,当账户退出或终端关闭时,程序仍然运行

当用`nohup`命令执行作业时，缺省情况下该作业的所有输出被重定向到`nohup.out`的文件中，除非另外指定了输出文件。



### 方式四

```
nohup java -jar XXX.jar >temp.txt &
```

解释下`>temp.txt`

`command >out.file`是将`command`的输出重定向到`out.file`文件，即输出内容不打印到屏幕上，而是输出到`out.file`文件中。



可通过`jobs`命令查看后台运行任务

那么就会列出所有后台执行的作业，并且每个作业前面都有个编号。 
如果想将某个作业调回前台控制，只需要`fg + 编号`即可。

---
版权声明：本文为CSDN博主「一汪清水」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。 
原文链接：https://blog.csdn.net/tang9140/java/article/details/38899345

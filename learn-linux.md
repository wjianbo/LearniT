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

[参考](https://www.howtoing.com/how-to-install-the-apache-web-server-on-centos-7)

## 利用 nohup 后台运行 jar 文件包程序


```
nohup java -jar XXX.jar >temp.txt &
```

解释下：

`command >out.file`是将`command`的输出重定向到`out.file`文件，即输出内容不打印到屏幕上，而是输出到`out.file`文件中。

可通过`jobs`命令查看后台运行任务

那么就会列出所有后台执行的作业，并且每个作业前面都有个编号。 
如果想将某个作业调回前台控制，只需要`fg + 编号`即可。

[参考](https://blog.csdn.net/tang9140/java/article/details/38899345)

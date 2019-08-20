# 系统更新

更新操作系统，有两种方案。一种是启动AWS控制台门户的更新管理解决方案，另外一种是手动方案。

## AWS门户更新

AWS提供一套完整的[AWS Systems Manager](https://www.amazonaws.cn/systems-manager/)解决方案，可以帮助您自动收集软件清单、应用操作系统补丁、创建系统映像以及配置 Windows 和 Linux 操作系统。

1. 登录AWS门户
2. 打开：管理与监管->System Manager，进入如下的相关管理界面
![启用更新管理](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-sysmupdate-websoft9.png)
3. 补丁管理器就是基本的更新方案


## 系统中更新

所谓系统中是指通过登录EC2，通过输入更新命令或操作更新功能而实现更新，区别于AWS门户的更新管理功能。

### Linux更新

Linux服务器的更新，只需要运行一条更新命令，即可安装大部分更新

```shell
#CentOS or Redhat
sudo yum update -y

#Ubuntu
apt update && apt upgrade -y
```

实际上，Websoft9提供的镜像已经将以上更新命令通过计划任务定期执行。

### Windows更新

Windows服务器的更新与本地电脑类似，手动找到更新管理程序，设置自动下载自动更新即可。
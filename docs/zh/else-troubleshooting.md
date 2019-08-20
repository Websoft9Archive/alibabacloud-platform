# 故障处理

下面列出最常见的故障或设置错误导致的问题。

如果您已经明确问题原因是云服务器产生的，那么请直接阅读[AWS实例故障排查](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/ec2-instance-troubleshoot.html)。

#### SFTP无法登录？

检查账号和密码是正确，请保证[服务器安全组](/zh/network-safegroup.md)的22端口是开启的

#### Windows远程桌面连接失败？

检查账号和密码是正确，请保证[服务器安全组](/zh/network-safegroup.md)的3389端口是开启的

#### 实例无法重启？

请联系AWS官方修复

#### http://公网IP 无法打开软件的初始化界面？

检查是否安装了所需的软件，请保证[服务器安全组](/zh/network-safegroup.md)的80端口是开启的
# 连接Windows

1. 选择一种打开本地电脑远程桌面的方式（三选一）: 
   - 打开 **开始菜单** -> **远程桌面连接**
   - 打开 **开始菜单**，输入”mstsc“ ，系统会搜索远程桌面连接工具
   - 通过 **Windows Logo** + **R** 打开系统的命令窗口，输入”mstsc“来启动远程桌面连接工具

2. 打开远程桌面连接，输入公网IP地址
   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/zh/windows/windows-remote.png)

3. 通过更多选项，设置默认用户名，例如”Administrator“，并勾选”允许我保存凭据“
   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/zh/windows/windows-remote-login.png)

4. 点击连接，成功后会看到Windows界面
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-windows2019desktop-websoft9.png)

5. 远程登录后，就可以直接从本地**拷贝**文件，然后**粘贴**文件到服务器上。
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-copyfilewin-websoft9.png)

6. 如果需要使用FTP，需要自行安装FTP软件（推荐使用FileZilla Server）
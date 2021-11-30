# 连接Windows

1. 首先登录到阿里云控制台，获取云服务器等公网 IP 地址

2. 通过阿里云 **WorkBench** 远程连接 Windows（可选）

   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-remoteconnectweb-websoft9.png)
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-rdpremote-websoft9.png)

3. 通过本地电脑的远程桌面工具，连接 Windows（推荐）: 

   - 方式一：打开 **开始菜单** -> **远程桌面连接**
   - 方式二：打开 **开始菜单**，输入【mstsc】，系统会搜索远程桌面连接工具
   - 方式三：通过 **Windows Logo** + **R** 打开系统的命令窗口，输入【mstsc】来启动远程桌面连接工具

4. 打开远程桌面连接，输入公网 IP 地址
   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/zh/windows/windows-remote.png)

5. 通过更多选项，设置默认用户名，例如”Administrator“，并勾选”允许我保存凭据“
   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/zh/windows/windows-remote-login.png)

6. 点击连接，成功后会看到Windows界面
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-windows2019desktop-websoft9.png)

7. 远程登录后，就可以直接从本地**拷贝**文件，然后**粘贴**文件到服务器上。
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-copyfilewin-websoft9.png)

8. 如果需要使用FTP，需要自行安装FTP软件（推荐使用FileZilla Server）
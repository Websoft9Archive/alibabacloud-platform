# 安全组

安全组是管理ECS端口的功能，端口是服务器上应用程序与外部访问出入访问的通道。下面以**开启80端口为例**，为您介绍安全组的使用

1. 登录到阿里云控制台->ECS

2. 打开实例下：网络和安全组->安全组配置
   ![ecs更改安全组](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-modifysg-websoft9.png)

3. 编辑安全组规则，选择“入方向”标签，然后点击“快速创建规则”
   ![ecs更改安全组入](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-modifysg80-websoft9.png)

4. 授权对象一般为`0.0.0.0/0`较为合适

3. 点击“确认”按钮即可生效
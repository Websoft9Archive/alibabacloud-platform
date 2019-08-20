# 安全组

安全组是管理EC2端口的功能，端口是服务器上应用程序与外部访问出入访问的通道。下面以**开启80端口为例**，为您介绍安全组的使用

1. 登录AWS控制台，打开EC2->实例
2. 打开实例下的“描述”标签，然后点击安全组名称
   ![ec2更改安全组](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-changesg-websoft9.png)
3. 进入所属安全组的设置后，打开“入站”标签页，点击编辑
   ![ec2更改安全组入](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-sfin-websoft9.png)
4. 编辑入站规则，增加一个新的规则（下图以80为例）
   ![ec2更改安全组入](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-set80sg-websoft9.png)
3. 点击“保存”按钮即可生效
# 公网IP地址

## 查看

1. 登录到阿里云控制台->ECS
2. 打开要查看公网IP的实例，我们会看到 **IP地址（公）** 
   ![查看公网IP](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-getpublicip-websoft9.png)
3. 如果实例没有公网IP地址项（或为空），需挂载一个弹性公网IP（[参考文档](https://help.aliyun.com/document_detail/72125.html)）

## 更换

在创建后六小时内的ECS可以更换公网IP。具体操作步骤如下：

1. 登录ECS管理控制台。
2. 在左侧导航栏，选择实例与镜像 > 实例。
3. 找到更换公网IP地址的实例，停止
4. 然后选择：更多-> 网络和安全组 -> 更换公网IP
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-changeip-websoft9.jpg)
5. 根据提示完成后续操作
# 公网IP地址

## 查看

1. 登录AWS控制台
2. 打开要查看公网IP的实例，我们会看到 **公有IP** 和 **公有DNS**
   ![查看公网IP](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-getip-websoft9.png)
3. 如果实例没有公网IP地址项（或为空），就需要参考下一个小节挂载一个公网IP

## 挂载

当创建的实例没有公网IP地址，只要有空闲（或新购）的公网IP地址，AWS控制台是可以给实例挂载上公网IP地址的。具体操作步骤如下：

1. 登录到AWS控制台
2. 打开所需的实例，查看：操作->联网->管理IP地址
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-manageip-websoft9.png)

3. 在管理IP地址操作栏中，点击“分配弹性IP”
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-assignip-websoft9.png)

4. 根据提示完成后续操作
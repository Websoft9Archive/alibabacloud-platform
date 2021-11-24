# 快照与镜像

之所以我们把快照和镜像放在一起描述，是因为这两者有一定的关联，甚至说有互生关系。

## 关系

此处不对快照和镜像进行抽象概念描述，只列出如下几个关键信息点：

* 基于磁盘可以创建一个快照。

  快照是对磁盘进行“拍照”，顾名思义就是备份某个时间点卷（磁盘）的数据，是一种备份手段

* 基于快照可以创建一个镜像，而镜像无法直接转换成快照。

* 基于镜像可以直接创建一个实例，基于实例也可以直接创建一个镜像

总结：（磁盘-->快照） --> （镜像--实例）

## 创建快照

对于阿里云来说，基于磁盘来创建快照

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**

2. 点击“创建快照”操作
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-disktosnapshot-websoft9.png)
   
3. 根据提示完成后续步骤

## 创建镜像

前面讲过，基于快照可以创建镜像，基于实例也可以创建镜像

### 实例创建镜像

1. 登录到阿里云控制台->ECS，找到需要操作的目标实例

2. 依次打开：更多->磁盘和镜像->创建自定义镜像
   ![创建自定义镜像](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createimage-websoft9.png)

3. 根据提示完成后续操作

### 快照创建镜像

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**快照**

2. 选择所需的快照，对它进行“创建自定义镜像”操作
   ![打开快照](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-snapshottoimage-websoft9.png)

3. 根据提示完成后续操作

### 文件创建镜像

阿里云支持将本地镜像文件上传到 OSS 存储之后，再基于这个已上传的文件创建镜像。

1. 登陆到阿里云控制台，依次打开：【实例与镜像】>【镜像】

2. 选择右侧的【导入镜像】功能
   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/alibabacloud-importimage001-websoft9.png)

3. 根据实际情况填写。**操作系统/平台**的选择需特别慎重，它决定控制台是否会通过 Cloud-init 对云服务器初始化工作，以及初始化工作的程度。

   > 【Others Linux】和【Customized Linux】区别阅读：（[非标准平台Linux镜像](https://help.aliyun.com/document_detail/48226.html)）

   ![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/alibabacloud-importimage002-websoft9.png)



> **操作系统/平台** 尽量避免选择 Others Linux 或 Customized Linux。例如： OracleLinux 建议选择 CentOS 更为合适 
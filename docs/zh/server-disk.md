# 卷（磁盘）

对于AWS平台来说，卷（磁盘）可以是单独的一种计算资源（单独创建、单独计费、单独管理等），同时也可以被集成到服务器实例，作为其中的一个组件。

## 增加卷

1. 登录AWS云控制台，打开EC2 Dashboard
2. 点开ELASTIC BLOCK STORE下的“卷”操作，点击“创建卷”
   ![创建卷](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-createvolume-websoft9.png)
3. 设置卷类型，大小等，确认无误后开始创建
   ![设置卷规格](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-createvolume2-websoft9.png)
4. 将创建好的卷，挂载到EC2实例
   ![挂载卷](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-volumeaddec2-websoft9.png)
5. 登录到EC2实例，完成初始化磁盘操作，使卷可用：
    - Windows, 请参考AWS官方文档 [使 Amazon EBS 卷可在 Windows 上使用](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/WindowsGuide/ebs-using-volumes.html)
    - Linux，请参考请参考文档 [使 Amazon EBS 卷可在 Linux 上使用](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/ebs-using-volumes.html) 
5. 完成所有设置后方可使用磁盘

## 分离卷

将卷从EC2中解除绑定关系，操作如下

1. 登录AWS云控制台，打开EC2 Dashboard
2. 在左侧菜单中，选择“实例” ，选择具有要分离的数据磁盘的实例，并单击“停止” 
3. 点开ELASTIC BLOCK STORE下的“卷”操作，对所要解绑的卷进行“Detach Volume”操作
   ![创建卷](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-detachvolume-websoft9.png)

> 磁盘分离后，会保留在存储中，不会被删除

## 容量修改

当卷没有附加到EC2时，可以调整卷的容量

1. 登录AWS控制台，依次打开：EC2->ELASTIC BLOCK STORE->卷
2. 选择所需修改的卷，依次打开：操作->修改
   ![修改卷](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-ddiskin-websoft9.png)
3. 设置新的大小

> 大多数情况下，卷只能增加大小，而不能降低大小
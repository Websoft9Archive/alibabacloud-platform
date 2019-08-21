# 云盘

对于阿里云平台来说，云盘（磁盘）可以是单独的一种计算资源（单独创建、单独计费、单独管理等），同时也可以被集成到服务器实例，作为其中的一个组件。

## 增加云盘

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**
2. 点击“创建云盘”按钮
   ![创建云盘](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-createdisk-websoft9.png)
3. 设置磁盘类型，大小等，确认无误后开始创建
   ![设置磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-createdisk2-websoft9.png)
4. 将创建好的磁盘，挂载到ECS实例
   ![挂载磁盘](http://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-attachdisk-websoft9.png)
5. “磁盘挂载”执行成功后，需登录本实例对挂载的磁盘进行“分区格式化和挂载新分区”的操作：
    - Windows, 请参考阿里云官方文档 [Windows格式化数据盘](https://help.aliyun.com/document_detail/25418.html)
    - Linux，请参考阿里云官方文档 [Linux格式化数据盘](https://help.aliyun.com/document_detail/25426.html) 
5. 以上所有设置后方可使用磁盘

## 卸载云盘

将磁盘从ECS中解除绑定关系(卸载)，操作如下

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**
2. 找到所需卸载的磁盘，依次打开：更多->卸载
   ![卸载磁盘](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-ditachdisk-websoft9.png)
3. 根据提示完成后续操作

> 磁盘卸载后，会保留，不会被删除，可以被其他ECS挂载

## 容量修改

阿里云支持在线扩容**系统盘**和**数据盘**，即无需重启ECS实例便可以完成扩容。

1. 登录到阿里云控制台->ECS，点击**存储与快照**下的**云盘**
2. 找到所需卸载的磁盘，依次打开：更多->磁盘扩容
   ![修改卷](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-changedisks-websoft9.png)
3. 根据提示完成后续操作

> 大多数情况下，磁盘只能增加大小，而不能降低大小
# 部署镜像

Websoft9已经在 阿里云云市场 上提供了多款镜像（**镜像是云上的一种软件产品交付形态**），覆盖常用的云场景，收到用户的良好反馈。

>  是不是想了解有哪些优质的镜像呢？点击 [此处](https://shop658hlt17.market.aliyun.com) 查看Websoft9在AlibabaCloud上发布的所有镜像。

那么如何在阿里云上使用这些镜像呢？有两种方法：

## 云市场部署

1. 访问 [阿里云云市场](https://aws.amazon.com/marketplace) 网站 或 [Websoft9店铺地址](https://shop658hlt17.market.aliyun.com/)

2. 搜索关键字"websoft9"，网站会列出所有相关的镜像
   ![搜索Websoft9镜像](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-buywebsoft9.gif) 

3. 点击您所需的产品，进入产品详情页后点击"立即购买"按钮，镜像已经购买完成
7. 接下来系统会自动要求购买一台新服务器：选择计费方式、实例类型、网络和安全组等设置
8. 等待几分钟，ECS创建完成后，镜像会作为ECS实例的系统盘启动，即镜像自动部署到实例中


## 创建实例部署

购买ECS或控制台创建实例过程中，可以选择Websoft9的镜像作为系统启动盘

1. 登录到阿里云管理控制台->ECS，点击“创建实例”，
   ![进入ecs控制台](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-createecs-websoft9.png)
2. 在镜像一栏，选择镜像市场->从镜像市场获取更多选择（含操作系统）。
3. 然后搜索关键件词“websoft9”，列出相关镜像
   ![选择Websoft9镜像](http://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-images-2-websoft9.png)

4. 选择一个你所需的镜像，开始创建ECS实例
5. 后续动作基本都会要求用户完成：选择计费方式、实例类型、网络和安全组等设置
6. 等待几分钟，ECS创建完成后，镜像会作为ECS实例的系统盘启动，即镜像自动部署到实例中

## 更换系统盘部署

镜像除了可以在创建新服务器之时购买，针对已有服务器，也可以通过更换系统盘的方式使用镜像。

> 需要注意的是，重装系统意味着系统数据全部会格式化，所以请注意做好数据的备份。

1. 登录到阿里云管理控制台，在”实例“中先停止服务器，依次选择：更多->磁盘和镜像->更换系统盘 
   ![更换系统盘](https://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-changesysdisk-websoft9.png)

2. 确认更换后，镜像类型选择“镜像市场”，然后输入搜索关键字”websoft9“，根据提示设置新密码
   ![选择Websoft9镜像](http://libs.websoft9.com/Websoft9/DocsPicture/en/alicloud/aliyun-images-2-websoft9.png)

3. 请耐心等待几分钟，直至更换完成

除了镜像订阅部署之外，你还可以通过我们发布到 [Github](https://github.com/websoft9)上的 Ansible 脚本，来实现自动部署。
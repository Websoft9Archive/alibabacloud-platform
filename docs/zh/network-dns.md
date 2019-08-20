# 域名

申请域名，解析域名等通用技术，本文档不会讨论。

这里我们介绍一个AWS比较实用的域名功能：AWS针对于每个实例提供了DNS服务。

## EC2之DNS

AWS给每台EC2实例都配置了一个公有DNS

当EC2配置的是动态IP时，每次重启实例，IP地址都可能会发生变化，导致需要重新解析域名，给运维带来不必要的麻烦。AWS的DNS功能，就是帮我们避免这个问题的。

1. 在AWS门户，打开实例->描述
   ![查看DNS](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-getip-websoft9.png)
2. 找到公有DNS，复制下来

## Route 53

Route 53就是AWS的域名购买、解析与管理平台，通过使用 Amazon Route 53，您可以注册新域、转移现有域、将域流量路由到 AWS 和外部资源，还可以监控您的资源的运行状况。

1. 在AWS门户，在联网与内容分发类别找到Route 53服务
   ![打开Route 53](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aws/aws-route53-websoft9.png)
2. 开始域名相关操作
   ![Route 53界面](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-route53start-websoft9.png)

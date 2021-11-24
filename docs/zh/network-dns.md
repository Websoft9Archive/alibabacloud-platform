# 域名

域名的目的是通过一段容易识别的文字段来指向服务器上的网站。如果没有域名，网站就只能通过IP地址访问，这样不便于记忆和识别。

为了使网站可以通过域名访问，有三个工作：

## 域名解析

阿里云给每台ECS实例都配置了一个公有DNS

当ECS配置的是动态IP时，每次重启实例，IP地址都可能会发生变化，导致需要重新解析域名，给运维带来不必要的麻烦。阿里云的DNS功能，就是帮我们避免这个问题的。

1. 购买域名(也称之为注册域名)，并完成实名制认证

2. 登录阿里云控制台，打开域名列表，在所需操作的域名上点击“解析”
   ![A记录解析](http://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-dns-websoft9.png)

3. 增加一个A记录：将域名（或子域名）指向IP的操作(下图示例)
   ![A记录解析](http://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-dnsrev-websoft9.png)

2. 保存并等待生效

## 域名绑定

域名绑定指一台服务器在多网站部署的时候，通过**虚拟主机配置文件**，将每个域名绑定到其对应的网站目录，从而达到每个网站都可以通过域名访问且相会不会干扰的效果。

下面是一个虚拟配置文件范例（LAMP环境）：

   ~~~ 
   <VirtualHost *:80>
   ServerName www.mydomain.com
   ServerAlias other.mydomain.com
   DocumentRoot "/data/wwwroot/default/mysite2"
   ErrorLog "/var/log/httpd/www.mydomain.com_error_apache.log"
   CustomLog "/var/log/httpd/www.mydomain.com_apache.log" common
   <Directory "/data/wwwroot/default/mysite1">
   Options Indexes FollowSymlinks
   AllowOverride All
   Require all granted
   </Directory>
   </VirtualHost>
   ~~~

通过**登录云服务器**，然后修改配置文件中域名相关的值（ServerName,ServerAlias等）实现绑定域名

> 配置文件主要包括域名与网站的对应的关系，即某个域名应该对应访问哪个目录。如果服务器上有多个网站，就必须对应多个配置文件。

## 域名备案

阿里云的备案政策简述：

- 购买服务器2个月或以上，就可以由阿里云免费提供备案服务。  
- 备案过程请通过[阿里云备案系统](https://beian.aliyun.com/order/index.htm)全程操作
- 备案是纯粹的商务流程活动，没有任何技术门槛，建议用户自行完成
   ![阿里云备案](https://libs.websoft9.com/Websoft9/DocsPicture/zh/aliyun/aliyun-beian-websoft9.png)
- 服务器地区在中国大陆的对应的域名需要备案

> 阿里云 7*24小时备案专线：95187转3 确保您的备案咨询能够得到及时回复



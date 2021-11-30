# Domain

[Domains](https://www.alibabacloud.com/help/product/35473.html) is a domain name management platform that provides domain name registration, transaction, monitoring, and protection services. 

Below steps is need for you to enable domains visit of your application:  

## Resolve Domain 

Resolve Domain mean that you set a mapping relations between domain and ECS's IP

1. Buy your Domain and register it

2. Login to console, lis all domains by 【Alibaba Cloud DNS】
   ![Add a record](http://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-dns-websoft9.png)

3. Add an **Add Record** for it
   ![Add a record](http://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-dnsrev-websoft9.png)

2. Save it and wait for 2-10 minute, then your DNS is take effect

## Bind Domain

The precondition for binding a domain is that MingDao can accessed by domain name.

When there is only one website on the server, you can visit the website without binding domain. While considering the server security and subsequent maintenance, **Binding Domain** is necessary.

Steps for binding MingDao domain are as follows:

1. Connect your Cloud Server;
2. Modify [Nginx vhost configuration file](/stack-components.md#nginx),and change the **server_name** and **proxy_pass** if you want.
   ```text
   server
   {
   listen 80;
   server_name mingdao.yourdomain.com;  # Set your domain
       location / {
        proxy_pass  http://127.0.0.1:8880; # Set your port
   ...
   }
   ```
3. Restart Nginx service
   ```
   sudo systemctl restart nginx
   ```

## Domain Beian

If you ECS is created in China, and you want to use Domain for application, you must complete the **Domain Beian** for Government governance.

Refer to: [Domain Beian](https://beian.aliyun.com/order/index.htm)
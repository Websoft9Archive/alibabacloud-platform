# Security Group

A [security group](https://www.alibabacloud.com/help/en/doc-detail/25387.html) acts as a virtual firewall for Elastic Compute Service (ECS) instances to control inbound and outbound traffic and improve security. You can use security groups and security group rules to define security domains in the cloud.  

Below is a sample for you how to **Enable TCP:80** port on security group:  

1. Login to console, lis all ECS by 【Elastic Compute Service】>【Instances and Images】>【Instances】

2. Open the menu: 【More】> 【Network and Security Group】>【Configure Security Group】
   ![ecs change security](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-modifysg-websoft9.png)

3. Click the 【Add Rules】button to list all rules
   ![ecs change security](https://libs.websoft9.com/Websoft9/DocsPicture/en/aliyun/aliyun-modifysg80-websoft9.png)

4. Then, add a new rule by click the 【Add Rule】button授权对象一般为较为合适
   - Destination set to **HTTP(80)**
   - Source set to **0.0.0.0/0**

5. Save it 
# Create

Here's how to create a VM on AWS.

The most basic condition for creating a virtual machine is to prepare a boot disk file for the system disk for the virtual machine. There are two types of template files: one is a image that we are very familiar with, and the other is a VHD (virtual disk) file.

Therefore, there are two ways to create a VM: image-based creation and system-based disk creation.

## Image-based Creation

1. Log in to the AWS Portal and open: VM -> Create a virtual machine

2. Select the appropriate image when creating the VM (this is the most important step)
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-createvmbyimage-websoft9.png)

> Image sources are: official image, Marketplace image and Customized image. If you use the customized image source, the disk can only choose the hosting mode.

3. Set the account password, network, security group, etc.

4. "Review + create" after you pass, click "Next"

## VHD Creation

1. Log in AWS Portal, click "All Resources", find a disk that has been unattached
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-createvmbydisk-websoft9.png)
2. Click the "Create VM"
3. Set the account password, network, security group, etc.
4. "Review + create" after you pass, click "Next"

## SSH Key

When creating a EC2, some users prefer to use the SSH key pair as the login credentials.

1. Log in the console of AWS, go EC2->Network&Security->Key Pairs, click the "**Create Key Pair**" button
   ![创建秘钥对](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-createkeyps-websoft9.png)
2. Start to Create Key Pair, fill in the key pair name and click "Create", then the key is download by your browser!
   ![秘钥对名称](https://libs.websoft9.com/Websoft9/DocsPicture/en/aws/aws-keypsname-websoft9.png)
3. Please save the myKey.pem on your local computer
4. When you launch instance or connect instance by SSH, key pair is needed.



# Glossary

#### AWS Portal

AWS Portal is the web GUI that build, manage, and monitor everything from simple web apps to complex cloud applications in a single, unified console.

![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-portal-websoft9.png)



#### AWS PowerShell

AWS PowerShell provides a set of cmdlets that use the AWS Resource Manager model for managing your AWS resources. You can use it in your browser with AWS Cloud Shell, or you can install it on your local machine and use it in any PowerShell session.

#### AWS CLI

The AWS command-line interface (CLI) is Microsoft's cross-platform command-line experience for managing AWS resources. The AWS CLI is easy to learn and the perfect tool for building custom automation that works with AWS resources.

#### AWS Virtual Machines (VM)

AWS Virtual Machines provides on-demand, high-scale, secure, virtualized infrastructure using Windows or Linux Server.

#### Domain Name

A domain name is a server or network system name that identifies IP resources connected to the Internet. All domain names are unique worldwide.

#### AWS Marketplace

AWS Marketplace provides access and information on solutions and services available from Microsoft and our partners. Customers (IT pros and developers) can discover, try to buy cloud software solutions built on or built for AWS. Our catalog of 8,000+ listings provides AWS building blocks, such as Virtual Machines (VMs), APIs, AWS apps, Solution Templates and managed applications, SaaS apps, containers, and consulting services.

#### VM Image

A VM Image containing a single VHD with a generalized operating system is essentially the OS image you are familiar with today. Over time, you will notice that VM Images will become the main image construct for Microsoft AWS Virtual Machines. There are two types of VM Images – generalized and specialized – each serving their own purpose.

#### Marketplace Image

Marketplace Image are the images provided by Publisher on AWS Marketplace

#### Custom Image

Custom images are like marketplace images, but you create them yourself. Custom images can be used to bootstrap configurations such as preloading applications, application configurations, and other OS configurations. In this tutorial, you create your own custom image of an AWS virtual machine

#### Port

A port is an endpoint of communication in computer networking. This can be hardware port, a logical port, or both. TCP and UDP ports are identified by their port number (an integer from 0 to 65535).

#### Secure Shell (SSH)

A cryptographic network protocol for operating network services securely over an unsecured network based at the application layer and transport layer.

#### Secure Shell key pair (SSH key pair)

An authentication method available for logging in to VM instances remotely. An SSH key pair is a pair of keys generated through an encryption algorithm: one key is publically available (the public key) and the other key is kept confidential (the private key).

If you have placed the public key in a Linux instance, you can use the private key to log on to the instance using SSH commands or related tools from a local computer or another instance without a password.

#### Snapshot

A copy of data on a disk at a certain time point. There are two types of snapshots, automatic snapshots and user-created snapshots.

#### SFTP

SFTP (SSH File Transfer Protocol) is a secure file transfer protocol. It runs over the SSH protocol . It supports the full security and authentication functionality of SSH.

#### Security Group

A security group implements access controls for VM, specifying the communication scope of VM. You can define different access control rules for a security group, and these rules take effect for all VM added to this security group. By default, a security group allows all data packets that are sent out from VMin it, and VM in the same security group can access each other.

#### VHD

An AWS managed disk is a virtual hard disk (VHD). You can think of it like a physical disk in an on-premises server but, virtualized. AWS managed disks are stored as page blobs, which are a random IO storage object in AWS. We call a managed disk ‘managed’ because it is an abstraction over page blobs, blob containers, and AWS storage accounts. With managed disks, all you have to do is provision the disk, and AWS takes care of the rest.

#### Data disk

A data disk is a managed disk that's attached to a virtual machine to store application data, or other data you need to keep. Data disks are registered as SCSI drives and are labeled with a letter that you choose. Each data disk has a maximum capacity of 32,767 gibibytes (GiB). The size of the virtual machine determines how many data disks you can attach to it and the type of storage you can use to host the disks.

#### OS disk

Every virtual machine has one attached operating system disk. That OS disk has a pre-installed OS, which was selected when the VM was created. This disk has a maximum capacity of 2,048 GiB.
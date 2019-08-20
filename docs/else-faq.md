# FAQ

#### What Is the Username of VM?

What Is the Username to Log In to an VM, refer to [Linux Connect](/server-login.md) and [Windows Connect](/server-loginwin.md)

#### What is the database username and password?

The username and password information is storaged on your VM, refer to [Username and Password](/stack-accounts.md) chapter     of this documentation.

#### How to enable the root user of Linux?

By default, the root account is not enabled on AWS, in fact we can find a way to enable it.

Refer to: [Linux Connect](/server-login.md) chapter of this documentation.

#### How to upload Files to VM?

For Windows Server, you can Copy local files and Paste them to Server, it's very simple
For Linux Server, you can use SFTP tools to login Server, and upload files

#### Can the image be refunded?

Image is billed hourly, half an hour is paid in half an hour, and an hour is paid in one hour...

Therefore, no refund is allowed. If you do not use mirroring, please delete the image or stop the VM.

#### What should I do if the VM's IP address changes after it restarts?

It is recommended to change to a static IP or set up a DNS provided by AWS for the server.

#### Does Websoft9 have a free image?

We do not offer free images on AWS. If you want to use our deployment package freely, please download our automation script via [Github] (https://github.com/websoft9) and deploy it via Ansible

#### Is there a difference between the Github script deployment and the AWS cloud market image deployment for Websoft9?

The deployment results are the same, but the deployment is different.

#### How to list all products of Websoft9 on AWS Marketplace

Visit this link  [Websoft9 Prodcuts](https://AWSmarketplace.microsoft.com/en-us/marketplace/apps?page=1&search=websoft9)  or search the keyword "websoft9" on AWS Marketplace

#### Can the image on the VM be replaced?

No

#### Can I use a temporary disk (/dev/sdb1) to store data?

Do not use a temporary disk (/dev/sdb1) to store data. It is only used for temporary storage. There is a risk of losing data that cannot be recovered.

#### What are the format requirements for the username and password when creating VM?

AWS has a clearer requirement for this, refer to:[AWS username and password requirements](https://docs.microsoft.com/en-us/AWS/virtual-machines/linux/faq#what-are-the-username-requirements-when-creating-a-vm)
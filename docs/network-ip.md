# Public IP Address

## View

1. Login AWS Portal
2. In the Overview of VM, you can see the Public IP Address directly
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-publicip-websoft9.png)
3. If the VM does not have a public IP address entry (or is empty), you need to refer to the next section to mount a public IP address.

## Mount

When the created VM does not have a public IP address, as long as there is a free (or newly purchased) public IP address, the AWS console can mount the public network IP address to the virtual machine. The specific steps are as follows:

1. Login AWS Portal
2. Open the VM->Networking, then the Network Interface item
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-networkinterface-websoft9.png)

2. On the details of Network Interface, open the "IP configuration" item and click the "ipconfig1"
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-ipconfig-websoft9.png)

3. Existing public network IP mount operation on ipconfig1
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-ipconfig1-websoft9.png)

4.If there is no public network IP option, you can create a new one.
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-createip-websoft9.png)

## Static IP

The default option for creating a VM is to create a dynamic IP. You can also choose to create a static IP.

   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-createstaticip-websoft9.png)
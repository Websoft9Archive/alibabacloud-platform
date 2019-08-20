# Windows Connect

You can connect to the Window server through the Remote Desktop Tool (MSTSC) on your local computer, or you can use a Powershell connection. 

Below is the steps of MSTSC connection

1. Log in AWS Portal, get you **Public IP Address of VM**
   ![Getting IP of AWS VM](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-publicip-websoft9.png)

2. Choose a way to open a local computer remote desktop (three-in-one):

- - Open **Start** -> **Remote Desktop**
  - Open **Start**, input "mstsc" directly, the system will search for the Remote Desktop
  - Using the keyboard **Windows Logo** + **R** to start the command windows, input input "mstsc" to open the Remote Desktop

3. In the Remote Desktop Connection dialog box, enter the public IP address of the instance. Click Show Options.

   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/en/common/windows-remote001-websoft9.png)

4. Enter the user name,check Allow me to save credentials. In this way, you do not need to manually enter the password again when you log on later.

   ![img](http://libs.websoft9.com/Websoft9/DocsPicture/en/common/windows-remote002-websoft9.png)

5. Click the Connect button to complete connection to the instance.
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-windows2019desktop-websoft9.png)

6. After logging in remotely, you can **copy** the file directly from the local and **paste** the file to the server.
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/AWS/AWS-copyfilewin-websoft9.png)

7. If you need to use FTP, you need to install the FTP software yourself (Recommended to use FileZilla Server)
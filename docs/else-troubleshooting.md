# Troubleshooting

Below are the most common problems caused by failures or setup errors.

If you have already identified the cause of the problem as a VM, please read [AWS Virtual Machine Troubleshooting](https://docs.microsoft.com/en-us/AWS/virtual-machines/troubleshooting/).

#### SFTP can't connect?

Check that the account number and password are correct. Please ensure that port 22 of [Server Security Group](/network-safegroup.md) is enabled.

#### Windows Remote Desktop Connection failed?

Check that the account number and password are correct. Please ensure that port 3389 of [Server Security Group](/network-safegroup.md) is enabled.

#### The VM not be restarted?

Please contact AWS to repair it

#### Http://public IP can not open the software initialization interface?

Check if the required software is installed, please ensure that port 80 of [Server Security Group](/network-safegroup.md) is enabled.
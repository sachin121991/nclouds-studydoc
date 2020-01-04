# Create Your EC2 Resources and Launch Your EC2 Instance
## Steps to start with:
1. Before you can launch and connect to an Amazon EC2 instance For client, make sure you have correct keypair name so that respective team can login into it.
2. Open the Amazon EC2 console at [https://console.aws.amazon.com/ec2/](https://console.aws.amazon.com/ec2/)

3. Choose Launch Instance.

4. Choose an Amazon Machine Image (AMI), kindly confirm with client regarding which AMI to use and find that Amazon Linux AMI from the list and choose Select.

5. Choose an Instance Type, Please be very particular about instance type as client have to pay charges according to instance type. so kindly confirm with client and choose Next: Configure Instance Details.

6. Configure Instance Details, provide the following information:

  - For Network, choose the entry for the same VPC that you noted when you created your EFS file system in Step 1: Create Your Amazon EFS File System.

  - For Subnet, choose a default subnet in any Availability Zone.

  - For File systems, make sure that the EFS file system that you created in Step 1: Create Your Amazon EFS File System is selected. The path shown next to the file system ID is the mount point that the EC2 instance will use, which you can change. Choose Add to user data to mount the file system when the EC2 is launched.

  - Under Advanced Details, confirm that the user data is present in User data.

7. Choose Next: Add Storage. kindly confirm with client what type of storage and how much storage required as client is charged for this.
> Use separate Amazon EBS volumes for the operating system versus your data. Ensure that the volume with your data persists after instance termination. also check if client's want Encrypt EBS volumes.

8. Choose Next: Add Tags. chose proper tags according to enviroment so that resources can be easily identified.

9. Name your instance and choose Next: Configure Security Group.

- Configure Security Group, set Assign a security group to Select an existing security group. 
> please be very sure while chosing security group on prod env. as u are about to give access to diff. users and service to this ec2

10. Choose Review and Launch.

11. Choose Launch.

12. Select the check box for the key pair that you selected, and then choose Launch Instances.

<img src="icon.png" align="right" />


# Create Your EC2 Resources and Launch Your EC2 Instance
## Steps To Start With:
> Before you can launch and connect to an Amazon EC2 instance For client, make sure you have correct keypair name so that respective team can login into it.
1. Open the Amazon EC2 console at [https://console.aws.amazon.com/ec2/](https://console.aws.amazon.com/ec2/)

2. Choose **Launch Instance**.

3. Choose an **Amazon Machine Image (AMI)**, kindly confirm with client regarding which AMI to use and find that Amazon Linux AMI from the list and choose Select.

4. Choose an **Instance Type**, Please be very particular about instance type as client have to pay charges according to instance type. so kindly confirm with client and choose Next: Configure Instance Details.

5. Configure Instance Details, provide the following information:

  - For Network, choose the Correct *VPC* name according to enviroment.

  - For Subnet, choose a correct *Subnet* in any Availability Zone.
  > Here we need to be sure while making selection in subnet as there will be public and private subnet with different access granted to them by client. confirm from client once.

  - For File systems, make sure that you choose correct EFS file system with correct path shown next to the file system ID that is the mount point that the EC2 instance will use.

  - Under Advanced Details, confirm that the user data is present in User data.

6. Choose Next: **Add Storage**. kindly confirm with client what type of storage and how much storage required as client is charged for this.
> Use separate Amazon EBS volumes for the operating system versus your data. Ensure that the volume with your data persists after instance termination. also check if client's want Encrypt EBS volumes.

7. Choose Next: **Add Tags**. `chose proper tags according to enviroment so that resources can be easily identified.`

8. Name your instance and choose Next: **Configure Security Group**.

- Configure Security Group, set Assign a security group to Select an existing security group. 
> please be very sure while chosing security group on prod env. as u are about to give access to diff. users and service to this ec2

9. Choose **Review and Launch**.

10. Choose **Launch**.

11. Select the check box for the key pair that you selected, and then choose **Launch Instances**.

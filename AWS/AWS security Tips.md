## Important AWS Security Tips
> Most of the developers and system admins handle Clients Production Env.But,There were many hacking incidents for such accounts which ended up in huge monthly bills. This happens because of many reasons. For example, you may commit your code to a public code repository with your AWS access and secret keys and a hacker would get access to you account and he will launch high capacity instances for his computing needs. This would result in a huge monthly usage bill. You can avoid your account being getting hacked just by applying few security policies and following best practices. 
1. Create IAM user with admin privileges for you even if you have the root access. Do not use you root account except for billing purposes.

2. Put a strong password of more than 10 characters for your root account.

2. Enable strong password policy with password expiration for IAM users.

3. Enable MFA (Multi-Factor Authentication) for you root account and all IAM user accounts.

4. Do not create AWS access keys unless needed. Make the existing keys inactive when not used.

5. Never hard code your access keys in your code which would end up getting committed to any public repository.

6. Never store you access keys and secret key in ec2 instances or any other cloud storage. If you need to access AWS resources from an ec2 instance, you can always use IAM roles.

7. Never allow all ports in security groups for your instances. Allow only required ports for your applications.

8. Make use of NACL’s to provide an additional security layer.

9. Never send your AWS credentials over email. If you do, change the password as soon as possible.

10. If you are planning to host your website on a windows server, install a good antivirus.

11. If you have more instances in VPC, use a Jump Server to connect to those machines or use Virtual VPN appliances like OpenVPN.

12. Do not launch instances in public subnet unless required.

13. Use NAT instances to patch your private instances rather than attaching an internet gateway to the private subnet.

15. Set billing alerts and resource monitoring using cloudwatch and SNS.

16. Enable cloudtrial service  which logs all the actives for your AWS account including API requests. You can use cloudwatch in conjunction with cloudtrial to get notified for any suspicious activity. (For example data transfer of more than 10 GB).

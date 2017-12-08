# Iac Templates for AWS CloudFormation


Inorder to create this template please enter below parameters

DBAllocatedStorage:  (enter the size in gb by default it will take 5 gb)
DBClass: (select DB class from below options typedb.t2.microdb.t2.largedb.t2.xlargedb.t2.2xlargedb.t2.4xlarge) 
DBName: (Enter database name)
DBPassword: (Enter database password)
DBUsername: (Enter The database admin account username)
InstanceType:  (Enter instance type from the option t1.microt2.nanot2.microt2.smallt2.mediumt2.largem3.mediumm3.largem3.xlargem3.2xlargem4.largem4.xlargem4.2xlargem4.4xlargem4.10xlarge) 
KeyName select: (security key for the launchconfiguration)
OperatorEMail: (enter EMail address to notify if there are any scaling operations)
SSHLocationThe: (IP address range that can be used to SSH to the EC2 instances)

Stack create will be in progress once we add above information to the stack and create the stack.

This stack will Create a VPC with two private subnets and Two Public Subnets.
This stack will create autoscaling group called webservergroup which will create two instaces and install httpd in it.
This stack will create autoscaling group called bastiongroup which will create a bastion host and it can connect to the ec2 instances which are created by webserver autoscaling group
This stack will create a s3 bucket and create a vpc endpoint to s3 bucket from the vpc.
Cloudfront is not created as part of the stack.
This Stack will create RDS instance with postgres Engine.
Two web servers will have port 22  access only from bastion host wher as port 80 access only from ELB.
RDS instance only reached through webservers.


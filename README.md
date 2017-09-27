#CloudFormation Template

This Template is an attempt to create Subnets in Aws with three tiered architecture. It comprises cloudformation Template to create the stack. The automation is enabled through Cloudformationtemplate.yml starting from stack creation to creation of subnets and instances including Elastic IP..

Setup your AWS with Cloudformation, you can write the code using Cloudformation using Aws account or installing aws cli in your local.

If you are fluent with Cloudformation, you know where to look and what to do. If you are new to cloudformation, just follow along with step-by-step instructions below.

Pre-requisites

Create AWS account and generate security credentials.

Create and Download private key from AWS account which would be used to access Instances.

Simple installation

Clone or Download ZIp  of the repo:

git clone https://github.com/Shravan6488/Ansible.git

once you get the cloudformation.yml file in your local.

1) Logon to Aws account.
2) Create a keypair and dowload in local (to login to instances later at the time of app deployment)
3) Go to cloudformation services
4) click on create stack/Create new stack
5) In choose template section click on choose file to upload template to amazon S3. 
6)You can select instace (for this i selecte t2.micro which is free of charge.To reduce cost).
7) click Next give the Stack name and select key pair drop down which you have created earlier and next and create.
8) wait for few minutes till the status changes to CREATE_COMPLETE.

What happenes once the stack is created.See below.

This tempalte creates the following.
1)Creates VPC
2) Creates gateway and attach to VPC
3) Creates 3 subnets (Web,app and DB) which is associated to created VPC.
4) Creates 3 instaces which is associated with each subnet(WEB01,APP01,DB01)
5) Created elastic IP and attahced to Web01 instance
6) Creates Security groups where the ports are opened accordingly ( web port 22,80 and 443) (app and DB 22 )

To evaluate this app , please consider using the following boxes for best results:

Once the testing completes, you can delete the stack to save the extra cost on AWS.
-- TO do this select your stack go to actions tab and click DELET STACK.

simple 


Author:	Sravan Kumar
Copyright:	Sravan Kumar
License:	The MIT License (MIT)

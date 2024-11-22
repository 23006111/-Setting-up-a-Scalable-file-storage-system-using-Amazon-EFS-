 ## EX 4: SETTING UP A SCALABLE FILE STORAGE SYSTEM USING AMAZON ELASTIC FILE SYSTEM
 ## NAME : RAMYA P
 
 ## REGISTER NO : 212223230168
 
 ## AIM
   To  setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones. 
## PROBLEM STATEMENT
   This experiment demonstrates how to configure Amazon EFS to provide a shared storage solution for two Linux EC2 instances across different availability zones, enabling easy data sharing. The aim is to ensure both instances can mount and access the EFS file system and validate data consistency across instances.

## ALGORITHM
Step 1: Create two EC2 instances in different availability zones.
Step 2: Set up a security group that allows necessary communication between the instances and EFS.
Step 3: Create an EFS file system and mount it to both EC2 instances.
Step 4: Ensure that the EC2 instances can access the file system and share data between them.

## COMMANDS
# EC2 Instance 1

```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
vi file  # Create a file and add some text

```

# EC2 Instance 2

```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
ls
cat file  
```

## OUTPUT

![Screenshot (255)](https://github.com/user-attachments/assets/1333fbc9-8a86-4aca-affb-1dc845bffaba)


![Screenshot (253)](https://github.com/user-attachments/assets/fb2d0318-e59b-477e-ad23-fa6ba751f29b)


![Screenshot (254)](https://github.com/user-attachments/assets/0b2fe73c-eb65-43ad-98c7-1cb273c47953)


![Screenshot (260)](https://github.com/user-attachments/assets/aed1a283-62d4-4c8a-8c1a-08ce43a5eb22)


![Screenshot (261)](https://github.com/user-attachments/assets/08b52adf-74b0-42d2-b6df-cd90d2527b7c)


## RESULT
Thus, The setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones, enabling shared access to data is executed successfully. 

  



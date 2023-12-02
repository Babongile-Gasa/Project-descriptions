#Storing Big Data Part 1 

The goal of this project was to recreate an on-premise to cloud data migration scenario using AWS services. Specifically, I configured a connection between an on-premise file server and a cloud-based object storage repository to facilitate seamless data transfer. 

To accomplish this, I leveraged AWS CloudFormation and YAML templates to provision the necessary computing infrastructure, including an on-premise VPC with public and private subnets, security groups, a Windows-based "corporate" machine, and a Linux-based file server instance. 
I then setup an Amazon S3 bucket to act as the cloud storage repository and configured a file gateway using Storage Gateway to bridge the on-premise systems with the cloud. After creating an NFS file share through the gateway, I successfully mounted this share onto the on-premise Linux file server, allowing me to automatically transfer sample data files whenever the share was written to.
To monitor this data transfer, I implemented a CloudWatch alarm that would trigger SNS-based email notifications whenever the file share recorded activity exceeding a set threshold. Through testing, I validated the ability to automatically and securely migrate data from the simulated on-premise environment into cloud storage.

![SBD_P1](https://github.com/Babongile-Gasa/Project-descriptions/assets/124687095/bde425e1-fba8-48a1-a675-1bee8d98f326)

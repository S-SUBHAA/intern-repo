# Tickbig Project Infrastuture Understanding(SECURITY FOCUSED)
## Platform:AWS
## TOOLS: EC2,VPC,ALB,apache2,subnets,routetable,internet gateway,Target Group.




#### **Task Info:**
 1.EC2 (Elastic Compute Cloud): This is a scalable virtual server hosting service by AWS. It allows users to run instances of virtual machines, supporting various applications including web servers like 
           Apache2. EC2 instances are crucial for deploying web applications and managing workloads.
           ![ec2](https://github.com/user-attachments/assets/aac645f1-fbb4-4493-bf2f-75cc493556ba)
          
2.A VPC is a dedicated section of the AWS cloud that isolates network resources. Users can define their own IP address range my ip range(10.0.0.0/16), subnets, route tables, and security groups, ensuring a secure and 
         customizable network environment for their resources.
         ![sg-1](https://github.com/user-attachments/assets/e53bcc28-0ae4-4300-ac36-da2ed472241b)
         instance 1 security group
         ![sg-2](https://github.com/user-attachments/assets/99f38e16-05ba-41e1-b172-715a07da86bd)
         instance 2 security group
         ![vpc](https://github.com/user-attachments/assets/877c82b7-6a57-46f5-b6d6-81b0a1a2e0f9)
         here i created VPC.
         ![subnets](https://github.com/user-attachments/assets/b89424d5-e2fb-44f4-bdbf-8512e041f47d)
         then i created to public subnets(publicsubnet1 and publicsubnet2)
         ![route table](https://github.com/user-attachments/assets/aa1ab253-5dce-4ab2-b345-233f6215f16b)
         Route a subnets.
         ![route association](https://github.com/user-attachments/assets/e1c25a09-7428-47c3-9755-55d07ab3b001)
         here associate both subnets.
         ![sg-1](https://github.com/user-attachments/assets/0fdc9257-573b-47ac-918e-652f604436c9)
         ec2 instance1 i create a security group and open a http port 80 in inbound.
         ![sg-2](https://github.com/user-attachments/assets/bff6a15c-307a-4b2a-9c20-dec3157978a8)
         ec2 instance2 i create a security group and open a http port 80 in inbound.
         
 3.An ALB distributes incoming application traffic across multiple EC2 instances to enhance availability and fault tolerance.
         ![loadbalancer](https://github.com/user-attachments/assets/844560eb-6276-4e2b-b061-583cdf676d06)

 4.Subnets divide the VPC into smaller, manageable segments. Each subnet can be private or public, depending on its route table configuration. Route tables determine how traffic is directed within the VPC 
           and to the internet. 
           Public subnets use route tables with entries directing traffic through an Internet Gateway.
           ![internetgateway](https://github.com/user-attachments/assets/f4486157-53ba-4d84-9b1d-6ff2c125abca)

           
 5.An Internet Gateway connects the VPC to the public internet, allowing resources in public subnets (like web servers) to communicate externally. Target Groups are associated with ALBs, defining the EC2 
           instances or IP addresses that will receive traffic. They support health checks to ensure traffic is only sent to healthy instances.
           ![targetgroup](https://github.com/user-attachments/assets/c5d641a6-9c51-4e37-a31d-89dc5bf7fab0)
         target group.
public ip - 13.233.236.154
         ![ec21-op](https://github.com/user-attachments/assets/c862f42a-9ec7-4b8d-b017-16ce72078fef)
public ip-3.108.238.169
         ![ec22-op](https://github.com/user-attachments/assets/9ead65e1-f1fc-4901-9eb2-e49a92ad02c3)
load balancer DNS:![final op1](https://github.com/user-attachments/assets/cbab731d-0101-4be5-85ab-6b8390972316)
                  ![final-op2](https://github.com/user-attachments/assets/77c02299-9fc2-4a19-845a-8a3157326657)
instance 1 apache2 installation page:
![cmd 1](https://github.com/user-attachments/assets/fbe0a4c4-9776-47b7-973f-36a182f9c139)
![cmd2](https://github.com/user-attachments/assets/3471e7b3-4e14-4148-8b50-675c7ab6c6cd)
![cmd3](https://github.com/user-attachments/assets/4cd3448f-5f2e-4e96-a702-ba87686c6929)
instance 2 apache2 installation page:
![2 cmd 1](https://github.com/user-attachments/assets/63c2d4c4-5611-4512-8b9a-07b7716285ed)
![2 cmd 2](https://github.com/user-attachments/assets/b77f8e3c-899d-47ce-8d14-f5255a9c68a7)
![2 cmd 3](https://github.com/user-attachments/assets/957b1bf3-425c-4243-8220-f5dd1df378a3)







         

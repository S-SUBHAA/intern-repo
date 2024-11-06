date:05-11-24
OBJECTIVE: Tickbig Project Infrastuture Understanding(SECURITY FOCUSED)
Platform:AWS
TOOLS: EC2,VPC,ALB,apache2,subnets,routetable,internet gateway,Target Group.
task info:
         1.EC2 (Elastic Compute Cloud): This is a scalable virtual server hosting service by AWS. It allows users to run instances of virtual machines, supporting various applications including web servers like 
           Apache2. EC2 instances are crucial for deploying web applications and managing workloads.
           ![ec2](https://github.com/user-attachments/assets/aac645f1-fbb4-4493-bf2f-75cc493556ba)












           
         2.A VPC is a dedicated section of the AWS cloud that isolates network resources. Users can define their own IP address range, subnets, route tables, and security groups, ensuring a secure and customizable 
           network environment for their resources.
         3.An ALB distributes incoming application traffic across multiple EC2 instances to enhance availability and fault tolerance.
         4.Subnets divide the VPC into smaller, manageable segments. Each subnet can be private or public, depending on its route table configuration. Route tables determine how traffic is directed within the VPC 
           and to the internet. Public subnets use route tables with entries directing traffic through an Internet Gateway.
         5.An Internet Gateway connects the VPC to the public internet, allowing resources in public subnets (like web servers) to communicate externally. Target Groups are associated with ALBs, defining the EC2 
           instances or IP addresses that will receive traffic. They support health checks to ensure traffic is only sent to healthy instances.
         

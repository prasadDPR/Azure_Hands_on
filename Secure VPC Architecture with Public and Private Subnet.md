# Secure VPC Architecture with Public and Private Subnets for Production Environment

## Overview
This project aims to create a secure Virtual Private Cloud (VPC) architecture on AWS with public and private subnets to host production workloads. The architecture will ensure isolation, scalability, and high availability for critical applications.

![Secure AWS Environment](https://github.com/prasadDPR/AWS/assets/121819069/d76aeb87-315c-4780-b9a3-1da4052031c5)

## Step 1: Design VPC Architecture
- Create a new VPC with appropriate CIDR block.
- Divide the IP address range into public and private subnets.
- Allocate subnets across multiple availability zones.

![VPC,Subnet,Route table](https://github.com/prasadDPR/AWS/assets/121819069/c0ae5c2e-4764-4e85-ace3-664e9e3f3ec7)

## Step 2: Create Subnets
- Create public and private subnets within the VPC.
- Associate subnets with specific availability zones.
- Configure routing tables for subnets to route traffic appropriately.

## Step 3: Set Up Internet Gateway (IGW)
- Attach an internet gateway to the VPC.
- Update routing tables for public subnets to route traffic to the internet gateway.

## Step 4: Configure NAT Gateway or NAT Instance
- Deploy a NAT gateway or NAT instance in the public subnet.
- Configure routing tables for private subnets to route outbound traffic through the NAT gateway or NAT instance.

![NAT](https://github.com/prasadDPR/AWS/assets/121819069/6326b6a0-63b0-4698-9703-d6d6b5dec851)

## Step 5: Implement Security Measures
- Configure security groups to control inbound and outbound traffic.
- Apply network ACLs to control traffic at the subnet level.

![Security Group](https://github.com/prasadDPR/AWS/assets/121819069/c2f327df-1f9b-458c-9224-45072dbf39fa)

## Step 6: Set Up Application Load Balancer (ALB)
- Create an Application Load Balancer (ALB) in the public subnets.
- Configure target groups to distribute traffic to instances in private subnets.
- Update security groups to allow traffic from ALB to instances.

![loadbalancer](https://github.com/prasadDPR/AWS/assets/121819069/79a68639-a254-4625-b833-ac74c38947a7)

## Step 7: Implement Auto Scaling Group
- Set up an Auto Scaling group to automatically adjust the number of EC2 instances based on demand.
- Configure scaling policies and health checks for the Auto Scaling group.
- Associate the Auto Scaling group with the target group of the ALB.

## Step 8: Install NGINX and Apache on Private VMs
- Launch two EC2 instances in the private subnets.
- Install NGINX on one instance and Apache on the other.
- Configure NGINX and Apache to serve web pages.

## Step 9: Test Load Balancing
- Access the ALB DNS name from a web browser.
- Observe how traffic is distributed between NGINX and Apache instances.
- Monitor ALB metrics to ensure load balancing is working as expected.

## Step 10: Test and Monitor
- Test connectivity and functionality of deployed resources.
- Monitor ALB metrics, Auto Scaling group metrics, and instance health.
- Set up alarms and notifications for any issues or scaling events.

![private ping](https://github.com/prasadDPR/AWS/assets/121819069/b24ae3d0-345f-4aaf-82bd-a64d17b45ce5)

## Conclusion
By following these steps, you'll have a secure and scalable VPC architecture with public and private subnets for hosting production workloads on AWS, utilizing an Application Load Balancer to distribute traffic and an Auto Scaling group to ensure high availability and scalability of EC2 instances. Additionally, NGINX and Apache instances installed on private VMs demonstrate load balancing functionality.

# Lab 6 – Scale and Load Balance Your Architecture
## Name: Sushil Shiva R
## Register Number: 212224250017

## Title

Scale and Load Balance Your Architecture


---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

1. I reviewed the existing EC2-based application architecture that I had created in previous experiments to understand how the instances were configured and how the application was being accessed.

2. I created a Launch Template by defining the EC2 configuration, including the Amazon Machine Image (AMI), instance type, key pair, security group, and user data script for automatic application setup during instance launch.

3. Using the launch template, I created an Auto Scaling Group. I configured the minimum, maximum, and desired capacity values to control how many EC2 instances should run based on demand. I also selected the appropriate VPC and subnets.

4. Next, I created an Application Load Balancer and configured a target group. I set the protocol and port (HTTP/HTTPS) and defined health check settings to monitor the EC2 instances.

5. I attached the Auto Scaling Group to the target group so that any instances launched by the Auto Scaling Group would automatically register with the Load Balancer.

6. I configured scaling policies based on CPU utilization. I created Amazon CloudWatch alarms to automatically increase the number of instances when CPU usage was high and decrease them when CPU usage was low.

7. Finally, I tested the setup by generating traffic to the Load Balancer DNS name. I observed that the traffic was distributed evenly across instances and that additional instances were launched automatically when the CPU utilization threshold was exceeded.

---

## Output Screenshots 
## Created LoadBalancer:
<img width="1919" height="866" alt="Screenshot 2026-03-13 090624" src="https://github.com/user-attachments/assets/54b3e88a-e896-491a-a8a0-c16600e85cf8" />

---
## Created LabConfig:
<img width="1919" height="858" alt="Screenshot 2026-03-13 091102" src="https://github.com/user-attachments/assets/533485f5-ebe2-4331-bad4-c63c8134008a" />

---
## Dynamic Scaling Policy created:
<img width="1919" height="862" alt="Screenshot 2026-03-13 091949" src="https://github.com/user-attachments/assets/101e996f-30da-40e3-9d35-e6560dc119de" />

---

## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.

## Introducing Today's Project!

### ✍️ What are we here to do today?

In this project, I will demonstrate VPC Traffic Flow and Security.

### ✍️ What are we doing in this step?

In this step, I will create VPC, subnet and Internet Gateway because I deleted it after earlier projects to not pay money for something I don't use.

### ✍️ What are we doing in this step?

In this step, I will create a route table because resources in subnet have to know the route to access the Internet.

### What is Amazon VPC?

Amazon VPC is a service that lets you launch AWS resources in a logically isolated virtual network that you define.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to set different network ACLs, security groups, subnets in different regions.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was deploying instances in different regions.

### This project took me...

This project took me 1 hour.

## Route tables

Route tables are rules that decide where the data in my network should go.

Routes tables are needed to make a subnet public because they provide a set of addresses where the network traffic should go.

## Route destination and target

Routes are defined by their destination and target.\
The destination is the physical address of the resource the traffic wants to access.\
The target is the specific "door" or "gateway" the traffic has to go through and it points to the right destination.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of Internet Gateway (setted up before).

### ✍️ What are we doing in this step?

In this step, I will create security group because I have to secure what protocols are allowed to what resources.

![Route destination and target](https://nextwork.ai/adam/uploads/fe5ed473-5874-57e1-a58f-d9b3d652330c_0a07b191)

## Security groups

Security groups are a set of rules that decide about inbound and outbound traffic.

### Inbound vs Outbound rules

Inbound rules are rules that decide about access to specific resource. I configured an inbound rule that let's http traffic into this security group.

Outbound rules are rules that decide about the traffic that goes out of reasource. By default, my security group's outbound rule is set to allow all traffic out.

### ✍️ What are we doing in this step?

In this step, I will create network ACL's to manage the network access to my resources in VPC.

![Security groups](https://nextwork.ai/adam/uploads/fe5ed473-5874-57e1-a58f-d9b3d652330c_92b0b0b4)

## Network ACLs

Network ACLs act at the subnet boundary. They are stateless. They support both allow and deny rules.

### Security groups vs. network ACLs

The difference between a security group and a network ACL is that:\
ACLs act as the subnet boundry. Security groups act at the resource level.\
Network ACLs are stateless both directions. Security groups are stateful.\
Network ACLs support both allow and deny rules. Security groups only support allow rules.

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will allow all inboud and outbound traffic.

In contrast, a custom ACL’s inbound and outbound rules are automatically set to deny all traffic.

![Default vs Custom Network ACLs](https://nextwork.ai/adam/uploads/fe5ed473-5874-57e1-a58f-d9b3d652330c_4faeb056)

## Tracking VPC Resources

I created additional VPC, Internet Gateway and security group. Instead of my usual region, I used eu-central-1. Teams would use multiple regions to:\
1\. Improve latency for their end users, which means apps run faster because resources are physically closer to the users' location.\
2\. Protect themselves from natural disasters and other risks - if one Region experiences an outage, other Regions can maintain operations.

EC2 Global View is a tool where you can find your EC2 and VPC resources aggregated from all enabled AWS Regions on your account onto a single dashboard. I could even narrow down my search by filtering by a specific region, resource type and tags. Without EC2 Global View, you'd have to manually switch your active region one-by-one using dropdown menu.

Now that I've learnt about EC2 Global View, I'd use it again to verify that all resources exist in specific regions.

![Tracking VPC Resources](https://nextwork.ai/adam/uploads/fe5ed473-5874-57e1-a58f-d9b3d652330c_b03ea6162)

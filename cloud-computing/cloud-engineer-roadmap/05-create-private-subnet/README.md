## Introducing Today's Project!

### ✍️ What are we here to do today?

In this project, I will demonstrate how to create Private Subnet in VPC. I'm doing this project to learn Cloud Computing.

### ✍️ What are we doing in this step?

In this step, I will create a VPC, subnets, an Internet Gateway, a route table, security group and a network ACLs.

### ✍️ What are we doing in this step?

In this step, I will set up a private subnet because some resources have to be kept private.

### What is Amazon VPC?

Amazon VPC is one of the most fundamental services in AWS. VPC - you have absolute power over your network configuration. You can secure your network using multiple security layers.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to set up a private and public subnets. I secured them with Network ACLs and security groups.

### One thing I didn't expect in this project was...

Nothing.

### This project took me...

This project took me approximately 1 hour.

## Private vs Public Subnets

The difference between public and private subnets is that public subnet is shared to all traffic and private is kept to specific traffic.

Having private subnets are useful because it reduces attack surface.

My private and public subnets cannot have the same CIDR block.

### ✍️ What are we doing in this step?

In this step, I will crate a private route table because the subnet has to connect to IG.

![Private vs Public Subnets](https://nextwork.ai/adam/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_afe1fdbd)

## A dedicated route table

By default, my private subnet is associated with my VPC's main route table.

I had to set up a new route table because my main route table contains a route pointing to my Internet gateway. This route allows two-way communication with the public internet. By default, any new subnet automatically links to main route table. If I leave my private subnet associated with it, my "private" subnet would actually be public, because it would inherit that route to Internet Gateway. To keep my private subnet truly private, I had to create a separate, custom route table that does not contain a route to the Internet Gateway.

My new route table contains only one active route. It targets my VPC's CIDR block with the target set to local. This route is what allows internal communication between different resources and subnets inside my VPC. Unlike my public route table, the table does not contain a route with a destination of 0.0.0.0/0 targeting an Internet Gateway.

### ✍️ What are we doing in this step?

In this step, I will set up a private Network ACL because I have to keep the traffic private.

![A dedicated route table](https://nextwork.ai/adam/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_b4b904b5)

## A new network ACL

Just like with route tables, when I create a new subnet in a VPC, AWS automatically associates it with the VPC's default Network ACL. The default Network ACL is configured to allow all inbound and outbound traffic. This means that if another part of my network gets compromised, an attacker could freely access resources in my private subnet because there are no firewall rules blocking them at this layer.

The default NACL is completely wide open and it allows all traffic to enter and leave the subnet. Leaving this default rule active on my private subnet defeats the purpose of making it private. A network ACL acts as a stateless firewall controlling traffic entering and exiting my subnet. By creating a custom one, you can write specific rules to block unwanted traffic before it can reach my backend instances.

My new custom Network ACL deny any traffic inbound and outbound.

![A new network ACL](https://nextwork.ai/adam/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_1ed2cb07)

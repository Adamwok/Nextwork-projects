<picture><source media="(prefers-color-scheme: dark)" srcset="https://nextwork.ai/static/nextwork-logo-paper.svg" /><img src="https://nextwork.ai/static/nextwork-logo-leather.svg" alt="NextWork" width="300" /></picture>

# Launching VPC Resources

**Project Link:** [View Project](https://nextwork.ai/projects/8f49d756-9e51-58c0-856a-e71e54f064ab)

**Author:** Adam

---

## Introducing Today's Project!

### ✍️ What are we here to do today?

In this project, I will demonstrate Launching VPC Resources. I'm doing this project to learn Cloud Computing.

### ✍️ What are we doing in this step?

In this step, I will create a VPC, subnets, an Internet Gateway, a route table, a security group, a network ACLs and private resources.

### ✍️ What are we doing in this step?

In this step, I will create a Public EC2 Instance.

### What is Amazon VPC?

Amazon VPC is Virtual Private Cloud and it is useful because it gives an absolute control over virtual networkign environment.

### How I used Amazon VPC in this project

I used Amazon VPC to create a secure, logically isolated network environment featuring both a public subnet for an internet-facing web sercer and a private subnet for a protected backend server. I configured route tables, security groups and network gateways to carefully control the flow of traffic and utilized VPC and more setup tool to rapidly deploy a redundant, high-availability architecture visualized on a resource map.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how visual and intuitive the VPC resource map actually is.

### This project took me...

This project took me approximately 1 hour.

## Setting Up Direct VM Access

Directly accessing a virtual machine means to establish a network connection straight from local computer to the virtual server running in AWS, without special middleman server or special private network tunnel.

### SSH is a key method for directly accessing a VM

SSH traffic means Secure SHell. It is a secure cryptographic network protocol that allows to establish an encrypted connection and remotely manage a virtual server over an unsecured network using a command-line interface.

### To enable direct access, I set up key pairs

Key pairs are a secure authentication method used to log into virtual servers in the cloud, like EC2 instances, without needing a traditional password.

A private key's file format means the specific technical structure and encoding standard used to save security credendtials on your computer, which ensures that your connection tools can read and process the cryptographic key correctly. My private key's file format was .pem, which is the industry-standard, text-based format natively supported by Linux-based EC2 instances and modern Windows terminals like PowerShell

## Launching a public server

Start your response with 'I had to change my EC2 instance's networking settings by clicking the Edit button on the Network settings panel, switching the VPC selection from the default VPC to NextWork VPC, assigning the instance to my public subnet, and then choosing Select existing security group to apply the pre-created NextWork Public Security Group instead of creating a new one.

### ✍️ What are we doing in this step?

In this step, I will launch a Private EC2 Instance.

![Launching a public server](https://nextwork.ai/adam/uploads/8f49d756-9e51-58c0-856a-e71e54f064ab_88727bef)

## Launching a private server

My private server has its own dedicated security group because it requires a completely different and far more restrictive set of access rules than public server. To maintain high security backend resources must be isolated from the outside world.

My private server's security group's source is the NextWork Public Security Group, which means only virtual servers or resources that are associated that specific public security group are allowed to communicate with private server.

### ✍️ What are we doing in this step?

In this step, I will launch VPC setup in minutes.

![Launching a private server](https://nextwork.ai/adam/uploads/8f49d756-9e51-58c0-856a-e71e54f064ab_4a9e8014)

## Speeding up VPC creation

I used an alternative way to set up an Amazon VPC! This time, I selected the VPC and more option instead of just VPC only, when creating my network. This allowed me to configure and spin up my entire network architecture, including multiple subnets, route tables and network connections at the exact same time from a single page, while visualizing it all through the interactive VPC resource map.

A VPC resource map is an interactive, visual representation tool within the Amazon VPC console that displays the layout, relationships and routing paths of all my network resources in real time.

My new VPC has a CIDR block of 10.0.0.0/16. It is possible for my new VPC to have the same IPv4 CIDR block as my existing VPC because each VPC is a completely isolated, logically distinct virtual network within my AWS account.

![Speeding up VPC creation](https://nextwork.ai/adam/uploads/8f49d756-9e51-58c0-856a-e71e54f064ab_1cbb1b88)

## Speeding up VPC creation

### Tips for using the VPC resource map

When determining the number of public subnets in my VPC, I only had two options: 0 or 2. This was because the VPC wizard enforces AWS cloud best practices for high availability and redundancy. Because I selected 2 Availability Zones for my setup, AWS ensures that if I choose to create public subnets, there must be one public subnet deployed in each AZ.

The set up page also offered to create NAT gateways, which are managed network address translation services that enable resources in a private subnet to connect to the internet while completely preventing the public internet from initiating any direct incoming connections with them.

![Speeding up VPC creation](https://nextwork.ai/adam/uploads/8f49d756-9e51-58c0-856a-e71e54f064ab_8ee57662)

## Introducing Today's Project!

In this project, I will demonstrate a use of VPC. I'm doing this project to learn Virtual Private Clouds, subnetting and connecting them to Internet via Internet Gateway.

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create the VPC in the AWS and access it through the AWS console.

### How VPCs work

VPCs are Virtual Private Clouds, they are created to divide cloud into the private sectors.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because some services by default need an VPC e.g. EC2 instances.

![Virtual Private Clouds (VPCs)](https://nextwork.ai/adam/uploads/7f907ac7-2473-5c15-a8be-edb36581cdba_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a way to assign a block of IP adresses.

## Subnets

### What I did in this step

In this step, I will launch a subnet inside my VPC.

### Creating and configuring subnets

Subnets are a way to divide network into smaller blocks, these blocks - subnet is like a city in a country or a neighbourhood in city. There are already subnets existing in my account, one for every Avalibility Zone.

### Public vs private subnets

The difference between public and private subnets are the public is connected to Internet Gateway. For a subnet to be considered public, it has to connect to Internet Gateway.

![Subnets](https://nextwork.ai/adam/uploads/7f907ac7-2473-5c15-a8be-edb36581cdba_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses. This setting makes sure any EC2 instance or other service that I launch for public.

## Internet gateways

### What I did in this step

In this step, I will connect my VPC to Internet using Internet Gateway.

### Setting up internet gateways

Internet gateways are a bridge between my VPC and Internet.

Attaching an internet gateway to a VPC means connecting the VPC to Internet. If I missed this step, other people wouldn't be able to connect to services working in VPC.

![Internet gateways](https://nextwork.ai/adam/uploads/7f907ac7-2473-5c15-a8be-edb36581cdba_4ae90410)

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will run AWS CLI commands to set up a VPC because I want to learn more efficient way to do this project.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which is shell in my management Console it's a space to run my code. CLI is is a software that let's me create, delete and update AWS resources faster than clicking through all options.

### Debugging my setup

To set up a VPC or a subnet, you can use the command I have to select CIDR block. Make sure to avoid errors by including --cidr-block.

![Using the AWS CLI](https://nextwork.ai/adam/uploads/7f907ac7-2473-5c15-a8be-edb36581cdba_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is it is faster than AWS Console. An advantage of using the Console is that there are all options displayed and when something is missing I know where to put it. Overall, I preferred AWS Console, because I am not experienced yet.

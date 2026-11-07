## Introducing Today's Project!

### Project overview

In this project, I will demonstrate Cloud Security with AWS IAM. I'm doing this project to learn Cloud Computing.

### Tools and concepts

Services I used were EC2, IAM Policies, IAM Policy Simulation. Key concepts I learnt include launching EC2 instances, using tags for easy identification. Also I learnt how to set up IAM Policies, create an IAM user and test IAM access without running it on live instances.

### Project reflection

This project took me approximately an hour. The most challenging part was switching between accounts. It was most rewarding to test permissions.

### ❤️ Thanks for doing this project!

I chose to do this project today because I want to break into Cloud Computing and Cybersecurity.

## Tags

### What I did in this step

In this step, I will launch two Amazon EC2 instances, because I want to train securing access to EC2 instance.

### Understanding tags

Tags are names to differ EC2 instances.

### My tag configuration

The tag I’ve used on my EC2 instances is called "env". The value I’ve assigned for my instances are "production" and "developement".

![Tags](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_2e0e5a5d)

## IAM Policies

### What I did in this step

In this step, I will set up an IAM policy, because I want to secure access to EC2.

### Understanding IAM policies

IAM Policies are Identity and Account Management, that control permissions and policies.

### The policy I set up

For this project, I’ve set up a policy using IAM and JSON policy.

### Policy effect

I’ve created a policy that allow access to Env - developement.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy define a list of permissions.

## My JSON Policy

![My JSON Policy](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_1c864649)

## Account Alias

### What I did in this step

In this step, I will set up an Account Alias for my root account to simplify user login to my AWS account.

### Understanding account aliases

An account alias is a friendly name for my AWS account that I can use instead of my account ID.

### Setting up my account alias

Creating an account alias took me 30 seconds. Now, my new AWS console sign-in URL is https://nextwork-alias-adam-wojtkowiak.signin.aws.amazon.com/console/

![Account Alias](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_0eb4439b)

## IAM Users and User Groups

### What I did in this step

In this step, I will set an IAM group and dedicate users to these groups.

### Understanding user groups

IAM user groups are a way to manage permissions of these users.

### Attaching policies to user groups

I attached the policy I created to this user group, which means users in this group can access developement EC2.

### Understanding IAM users

IAM users are accounts to represent a specific person or application that needs to interact with AWS resources.

## Logging in as an IAM User

### Sharing sign-in details

The first way is to download a .csv file to my computer. The other option is to copy credentials and text them into an email or other communication methods.

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that some of my dashboard panels are showing access denied. This was because group policy denies access.

![Logging in as an IAM User](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_6f2ab446)

## Testing IAM Policies

### What I did in this step

In this step, I will log into the AWS using the intern's IAM user. Also I will test the intern's access to my production and development instances.

### Testing policy actions

I tested my JSON IAM policy by trying to stop both of the instances at once and it blocked IAM user from stopping production instance.

### Stopping the production instance

When I tried to stop the production instance I have got an error. This was because the account is not authorized.

![Testing IAM Policies](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance JSON IAM Policy worked and allowed IAM user to stop the instance.

![Testing IAM Policies](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_1811801c)

## IAM Policy Simulator

To extend my project, I'm going to test IAM Policy Simulation. I'm doing this because I don't want to test Policies on live instances.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is a tool used for testing IAM Policies, without actually testing Policies on live services, that other people might use.

### How I used the simulator

I set up a simulation for EC2 instances. The access was denied, I had to adjust the condition which the simulation run with. I had to set development tag, to run the simulation only for development instance. After that result for stopping the instance was "allowed".

![IAM Policy Simulator](https://nextwork.ai/adam/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_069d8a621)

## Introducing Today's Project!

### Project overview

In this project I will demonstrate the use of a S3 bucket - service on AWS and I will set my own S3 bucket.

### Tools and concepts

Services I used were S3, ACL and policies. Key concepts I learnt include managing permissions and access.

### Time, challenges, and wins

This project took me approximately 30 minutes.

### ❤️ Thanks for doing this project!

I chose to do this project today because I want to learn cloud computing.

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create S3 bucket because I am learning cloud computing. I want to expand my competences and knowledge.

### How long it took to create the bucket

Creating an S3 bucket took me 5 minutes with a walkthrough.

### Region selection

The Region I picked for my S3 bucket was eu-north-1 because it was the closest one to where I live.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means the name of the S3 bucket must be unique.

![How I Set Up an S3 Bucket](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_ba6d42ad)

## Upload Website Files to S3

### What I did in this step

In this step, I will download an HTML file that will set up my website. Upload the files to my S3 bucket.

### Files I uploaded

I uploaded two files to my S3 bucket - they were an index.html file and the whole folder with the rest of the data.

### How the files work together

Both files are necessary for this project as the main page of the website and all the media.

![Upload Website Files to S3](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_a265af88)

## Static Website Hosting on S3

### What I did in this step

In this step, I will statis host a website on my S3 bucket.

### Understanding website hosting

Website hosting means letting other people visit the website.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went to the properties of the S3 bucket, scrolled all the way down and setted up the static host.

### Access Control Lists (ACLs)

An ACL is an Access Control List. They control the access to a computer system or a network. They decide which resource users can access.

![Static Website Hosting on S3](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_c22c54c0)

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is an access to the website hosted on the S3 bucket.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw the 403 error. The reason for this error was that the objects by default are private. No one except the root has the access to them.

![Bucket Endpoints](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_22ce4daf)

## Success!

### What I did in this step

In this step, I will make my website files publicly accessible.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I made the objects public in my S3 bucket.

### ✅ What were the key services and concepts you learnt in this project?

Services I used were Amazon S3, ACL and policies. Key concepts I learnt include managing access to the resources.

### ✅ How long did it take you to complete this project?

This project took me approximately 30 minutes. The most challenging part was downloading the correct index.html file (I downloaded it the wrong way). It was most rewarding to potentially setting up a static website.

### ❤️ Thanks for doing this project!

I chose to do this project today because I want to learn cloud computing.

![Success!](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Bucket Policies

### What I did in this extension

In this project extension I'm about to protect my resources from deleting. I'm doing this so that no one from outside can delete files in my bucket.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are permissions for the resources.

![Bucket Policies](https://nextwork.ai/adam/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_sm2sm2sm)

### What my bucket policy does

My bucket policy denies anyone from deleting the index.html file. I tested this by trying to delete the file and saw the deletion error.

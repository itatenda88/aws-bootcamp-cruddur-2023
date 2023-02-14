# Week 0 — Billing and Architecture

This week's tasks are mainly around billing for the AWS services we will use during the course.

I'm aware that the pricing of AWS services heavily depends on the regions you choose, with Nothern Virginia and Ohio being the cheapest, followed by Oregon and Mumbai. There are many other considerations when picking regions but I will be basing my decision on pricing and availability of the services I know we will be using. There are tools in AWS that are useful for tracking usage and cost. I have chosen billing alerts and CloudWatch alarms for this purpose.

My Account is fairly new, it's still eligible for the free tier on all services with the offering. Alerts and Alarms will notify me if I go near and over limits I have set for myself.

## Completed Assignments:

Not making excuses but I'm juggling this boot camp and a heavy work schedule while also preparing for an SAA exam. I won't have much time to journal in detail but rather just summarize tasks in the order that I complete them. This week's homework was divided into "would be great ifs" and "must dos". There is a list of tasks that you MUST complete and optional tasks that would be great if you can do them as they will provide you a better understanding of the project and knowledge of AWS's best practices. I plan on completing as much time allows.

##### Setting up Account & Billing Alerts

###### IAM

Instructors have sort of left security concerns and considerations to us, it's not a super high priority for the project we are building but certainly shouldn't be ignored. Best to build it into the architectural design and account set up from the jump. I have chosen a few security services available in AWS, IAM for access control, Cognito for user authentication and use of public and private subnets. I will touch on cognito and subnets later, first here is how I set up the account:

1. Like I mentioned, I already have an AWS account that has a single IAM User I created a while ago. This is the IAM  account I will be using throughout the course. Permissions will be granted to the account as and when needed and this week only billing permission is required. To achieve this, I created a Role and attached it to an admin group that I added the user to. See the images below.

2. Created Access Keys to give users programmatic access to the account. This is the key I'm using in gitpod to access and control my AWS environment

###### Billing Alerts

1. My monthly budget is currently set at $20, pretty low, will change it if needed. Have also set up a usage alarm for EC2 instances (insert image)
2. The budget alert can function as a billing alarm, but wanted to get some practice on CloudWatch to see how it works and how it's configured. I set up a single billing alarm and opted for SNS for notification. May disable this if it drives costs up. (insert image)

Installed gitpod extension. A new revelation I was super happy to learn about! Thank you!

Installed cloudshell in termainal. I'm now able to access my AWS account from the terminal in gitpod(insert image)

Completed conceptual architecture diagram. This is one task I struggle with as I'm still trying to wrap my head around the project, deciding components without going overboard and leaving out important stuff has been challenging. I ended up going almost 1:1 with Andrew's diagram from class. Click the link below.
[https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720](https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720)

Went with Andrew's architectural design again here. Tried to think about security and added public and private subnets for security [https:lucid.app/lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56](lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56)

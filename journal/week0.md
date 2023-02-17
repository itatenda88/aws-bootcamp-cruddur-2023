# Week 0 — Billing and Architecture

Hey there! So for this week has been about billing for the AWS services we'll be using throughout the bootcamp. And let me tell you, the pricing of these services really depends on which region you select. I did some digging and found out that Northern Virginia and Ohio are the cheapest, followed by Oregon and Mumbai. Of course, there are other things to consider when making this decision, but I will be basing my decision on  pricing and service availability.

Now, to make sure I don't go over our usage and costs, I've set up some handy tools within AWS, like Budget Alerts and a CloudWatch Alarm with SNS to send me notifications. And the best part? Since my account is still pretty new, I can use some of these services for free under the free tier! But just in case, these alerts and the alarm will keep me in the loop so there won't be any unexpected surprises. Unless, of course, I forget to check my email :D

## Completed Assignments:

##### Setting up Account & Billing Alerts

###### IAM & Access Keys

We're responsible for considering security concerns, even if it's not a top priority. It's better to have it built into the design from the start. For me, I chose some AWS security services like IAM for access control, Cognito for user authentication, and public and private subnets. I'll go into detail on Cognito and subnets later, but first let me explain how I set up my account:

I had an existing AWS account with a single IAM User that I created a while back. I'll be using this account throughout the course and have add permissions as needed. For now, I only needed billing permission, so I created a Role and attached it to an admin group, then added my user to that group. Oh, and enabled MFA for extra layer of security.


![](assets/20230217_191830_IAM_User with MFA enabled.png)


I also created Access Keys, which give programmatic access to the account. I'm using these keys in gitpod to control my AWS environment.


![](assets/20230217_191921_ProgrammaticAccess_For IAM.png)


###### Billing Alerts

1. I set my monthly budget at $20, which is pretty low, but I can always adjust it if needed. I also set up a usage alarm for EC2 instances to keep track of any unexpected spikes.

![](assets/20230217_192442_Cost_Usage Budgets.png)

1. While the budget alert can also function as a billing alarm, I wanted to practice using CloudWatch and see how it works. So, I set up a single billing alarm and opted for SNS for notification. I may disable it if it drives up costs, but for now, it's good to have some extra visibility.

![](assets/20230217_192325_CloudWatchBillingAlarm.png)


###### Gitpod

So listen, gitpod was a revelation that I was super chuffed to learn about ! Had not heard or used it until this point. To be fair though, I'm new to this field, I have a lot to learn and discover but damn I love this one! If you are just hearing about this tool like me, Gitpod is a cloud-based integrated development environment (IDE) that allows developers to write, test, and deploy code from a web browser. Some of it's advantages include:

* Quick and easy setup
* Centralized development environment
* Scalable and flexible
* Accessible from anywhere with an internet connection
* Easy collaboration with team members

To get Gitpod extension on your GitHub, just head over to the GitHub Marketplace, look up the Gitpod extension, and install it. After that, you can simply click the "Gitpod" button in any repository to start a fully functional development environment in your web browser. Gitpod automates the configuration process and offers various tools, including automatic workspace backups, collaborative editing, and workspace sharing, to provide a smooth and streamlined development experience.

Cloudshell 

Installed cloudshell in termainal. I'm now able to access my AWS account from the terminal in gitpod(insert image)

Completed conceptual architecture diagram. This is one task I struggle with as I'm still trying to wrap my head around the project, deciding components without going overboard and leaving out important stuff has been challenging. I ended up going almost 1:1 with Andrew's diagram from class. Click the link below.
[https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720](https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720)

Went with Andrew's architectural design again here. Tried to think about security and added public and private subnets for security [https:lucid.app/lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56](lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56)

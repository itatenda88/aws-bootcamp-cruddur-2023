# Week 0 — Billing and Architecture

Hey there! So for this week has been about billing for the AWS services we'll be using throughout the bootcamp. And let me tell you, the pricing of these services really depends on which region you select. I did some digging and found out that Northern Virginia and Ohio are the cheapest, followed by Oregon and Mumbai. Of course, there are other things to consider when making this decision, but I will be basing my decision on  pricing and service availability.

Now, to make sure I don't go over our usage and costs, I've set up some handy tools within AWS, like Budget Alerts and a CloudWatch Alarm with SNS to send me notifications. And the best part? Since my account is still pretty new, I can use some of these services for free under the free tier! But just in case, these alerts and the alarm will keep me in the loop so there won't be any unexpected surprises. Unless, of course, I forget to check my email :D

## Completed Assignments:

##### Setting up Account & Billing Alerts

###### IAM & Access Keys

We're responsible for considering security concerns, even if it's not a top priority. It's better to have it built into the design from the start. For me, I chose some AWS security services like IAM for access control, Cognito for user authentication, and public and private subnets. I'll go into detail on Cognito and subnets later, but first let me explain how I set up my account:

I had an existing AWS account with a single IAM User that I created a while back. I'll be using this account throughout the course and have add permissions as needed. For now, I only needed billing permission, so I created a Role and attached it to an admin group, then added my user to that group. Oh, and enabled MFA for extra layer of security.

![IAM User with MFA enabled](https://user-images.githubusercontent.com/65119027/219777870-0c2c318d-e611-47f1-b74e-0da741f205b0.png)


I also created Access Keys, which give programmatic access to the account. I'm using these keys in gitpod to control my AWS environment.

![ProgrammaticAccess For IAM](https://user-images.githubusercontent.com/65119027/219777245-cf34d7c6-6028-457b-9629-7b898906479b.png)

###### Billing Alerts

1. I set my monthly budget at $20, which is pretty low, but I can always adjust it if needed. I also set up a usage alarm for EC2 instances to keep track of any unexpected spikes.

![Cost Usage Budgets](https://user-images.githubusercontent.com/65119027/219778524-d6e3e833-366c-4b9b-bc3c-2037f0de0c24.png)

2. While the budget alert can also function as a billing alarm, I wanted to practice using CloudWatch and see how it works. So, I set up a single billing alarm and opted for SNS for notification. I may disable it if it drives up costs, but for now, it's good to have some extra visibility.

![CloudWatchBillingAlarm](https://user-images.githubusercontent.com/65119027/219780203-0675cf0b-ff89-47a6-9371-9ffea340cffe.png)


###### Gitpod

Gitpod is such a game-changer for me. It's basically a cloud-based IDE that lets you do all your coding, testing, and deployment from the comfort of your web browser! The best part is that it's super easy to use and has some amazing features like workspace sharing, automated backups, and collaboration tools. Plus, it integrates with all the fav tools like GitHub, GitLab and whatnot! Clutch!

* Quick and easy setup
* Centralized development environment
* Scalable and flexible
* Accessible from anywhere with an internet connection
* Easy collaboration with team members

To get Gitpod on GitHub, go to GitHub Marketplace and install the Gitpod extension. Click "Gitpod" button in any repo to start a fully functional environment in your web browser and viola! Try it if you are just hearing about it too.

![Gitpod extension](https://user-images.githubusercontent.com/65119027/219779314-681eb93f-2ab6-4ff5-98a5-bf9519929d27.png)

Cloudshell 

Installed cloudshell in termainal. I'm now able to access my AWS account from the terminal in gitpod(insert image)

Completed conceptual architecture diagram. This is one task I struggle with as I'm still trying to wrap my head around the project, deciding components without going overboard and leaving out important stuff has been challenging. I ended up going almost 1:1 with Andrew's diagram from class. Click the link below.
[https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720](https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720)

Went with Andrew's architectural design again here. Tried to think about security and added public and private subnets for security [https:lucid.app/lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56](lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56)

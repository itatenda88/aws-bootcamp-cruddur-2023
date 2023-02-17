# Week 0 — Billing and Architecture

Hey there! So for this week has been about billing for the AWS services we'll be using throughout the bootcamp. And let me tell you, the pricing of these services really depends on which region you select. I did some digging and found out that Northern Virginia and Ohio are the cheapest, followed by Oregon and Mumbai. Of course, there are other things to consider when making this decision, but I will be basing my decision on  pricing and service availability.

Now, to make sure I don't go over our usage and costs, I've set up some handy tools within AWS, like Budget Alerts and a CloudWatch Alarm with SNS to send me notifications. And the best part? Since my account is still pretty new, I can use some of these services for free under the free tier! But just in case, these alerts and the alarm will keep me in the loop so there won't be any unexpected surprises. Unless, of course, I forget to check my email :D

## Completed Assignments:

## Setting up Account & Billing Alerts

### IAM & Access Keys

We're responsible for considering security concerns, even if it's not a top priority. It's better to have it built into the design from the start. For me, I chose some AWS security services like IAM for access control, Cognito for user authentication, and public and private subnets. I'll go into detail on Cognito and subnets later, but first let me explain how I set up my account:

I had an existing AWS account with a single IAM User that I created a while back. I'll be using this account throughout the course and have add permissions as needed. For now, I only needed billing permission, so I created a Role and attached it to an admin group, then added my user to that group. Oh, and enabled MFA for extra layer of security.

![IAM User with MFA enabled](https://user-images.githubusercontent.com/65119027/219781915-258d9f65-d816-47a1-ac41-95d52b6f115b.png)

I also created Access Keys, which give programmatic access to the account. I'm using these keys in gitpod to control my AWS environment. AWS access keys are like a username and password, used to interact with AWS services and resources programmatically, such as through the AWS CLI or SDKs. They consist of an access key ID and secret access key, and can be generated and managed through the AWS Management Console, CLI, or SDKs. Access keys should be kept secure and not shared with unauthorized individuals or applications.

![ProgrammaticAccess For IAM](https://user-images.githubusercontent.com/65119027/219777245-cf34d7c6-6028-457b-9629-7b898906479b.png)

### Billing Alerts

1. I set my monthly budget at $20, which is pretty low, but I can always adjust it if needed. I also set up a usage alarm for EC2 instances to keep track of any unexpected spikes.

![Cost Usage Budgets](https://user-images.githubusercontent.com/65119027/219778524-d6e3e833-366c-4b9b-bc3c-2037f0de0c24.png)

2. While the budget alert can also function as a billing alarm, I wanted to practice using CloudWatch and see how it works. So, I set up a single billing alarm and opted for SNS for notification. I may disable it if it drives up costs, but for now, it's good to have some extra visibility.

![CloudWatchBillingAlarm](https://user-images.githubusercontent.com/65119027/219780203-0675cf0b-ff89-47a6-9371-9ffea340cffe.png)

### Gitpod

Gitpod is such a game-changer for me. It's basically a cloud-based IDE that lets you do all your coding, testing, and deployment from the comfort of your web browser! The best part is that it's super easy to use and has some amazing features like workspace sharing, automated backups, and collaboration tools. Plus, it integrates with all the fav tools like GitHub, GitLab and whatnot! Clutch!

* Quick and easy setup
* Centralized development environment
* Scalable and flexible
* Accessible from anywhere with an internet connection
* Easy collaboration with team members

To get Gitpod on GitHub, go to GitHub Marketplace and install the Gitpod extension. Click "Gitpod" button in any repo to start a fully functional environment in your web browser and viola! Try it if you are just hearing about it too.

![Gitpod extension](https://user-images.githubusercontent.com/65119027/219779314-681eb93f-2ab6-4ff5-98a5-bf9519929d27.png)

### Cloudshell

Next task, Cloudshell. Since attempting a Linux course (which I will get back to at some point), I have been obsessed with doing EVERYTHING in the in CLI. Not a reason to base a career choice on but it's one of the main reasons I want to get into DevOps lol. Anyway...AWS Cloudshell. What is it you may (not) ask?

It's a super cool environment provided by AWS that offers a preconfigured shell for the AWS CLI and other tools, making it easy to run AWS CLI commands without having to install and configure anything on your local machine. Using CloudShell in Gitpod terminal is as simple as opening the terminal, installing it (see AWS documentation for this) and typing in your AWS CLI commands. Just remember that you'll need to have your Access keys on hand to access your AWS environment.

# Architecture Diagrams

Alright, buckle up folks, because we're about to dive into the heart of this project. We're talking about an ephemeral-first micro-blogging platform, designed for those who want to make a statement without a permanent online presence.This platform is all about embracing the moment, with anything you upload expiring after just a few days. It's the perfect solution for those who want to share their thoughts and experiences without leaving a digital footprint behind.

Now is probably the best time for a disclaimer: I AM NOT A SOLUTIONS ARCHITECT... YET, I AM HERE TO LEARN! So, if you see anything that looks wonky, just remember - I'm not a professional yet.

Now, I may have taken a few liberties with these diagrams and borrowed some (most **cough**) ideas from class demos, but hey, imitation is the sincerest form of flattery, right? On the real though, our instructors are super chill, not only do they not mind, they encouraged the plagerism lol

Anyways, we move...

#### Requirements

* Micro services
* Frontend using JS with React
* Backend using Python with flask
* APIs
* User Authentication
* Caching system of sorts

####The concept?

![Conceptual Diagram](https://user-images.githubusercontent.com/65119027/219788115-00b208b8-03db-4a40-88b5-bca73cf64fce.png)

#### And the Logic?

![Logical Diagram](https://user-images.githubusercontent.com/65119027/219790466-46f4f103-57e2-4606-9060-ef189bfb043a.png)


# Up next?

Docker and Containerization. Let's do it!!


Thanks again Andrew..

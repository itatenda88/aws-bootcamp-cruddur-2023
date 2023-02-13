# Week 0 — Billing and Architecture

## Completed Assignments:

1. I already had an AWS account with a single user I created a few days ago. This is the IAM  account I will be using throughout the course. Permissions will be granted to the account as and when needed, this week only billing permission is required. For this, I created a role and attached it to an admin group that I added the user to. See images Below.
2. Created Access Keys to give user programmatic access to the account. This is the key I'm using in gitpod to acess and control my AWS environment (insert image)
3. I plan on keeping costs at minimal for the duration of the bootcamp, a tricky thing to achieve but not entirely imporssible since it's a fairly new account that's still eligible to free tier on a lot of services. My monthly budge is currently set at $20, pretty low, will change it if needed. Have also set up a usage alarm for EC2 instances (insert image)
4. The budget alert doubles as a billing alarm, but wanted to get some practice on CloudWatch to see how it works and how to configure it. I set up a single billing alarm and opted for SNS for notification. May disable this if it drives costs up. (insert image)
5. Installed gitpod extension. A new revelation I was super happy to learn about! Thank you!
6. Installed cloudshell in termainal. I'm now able to access my AWS account from the terminal in gitpod(insert image)
7. Completed conceptual architecture diagram. This is one task I struggles with as I'm still trying to wrap my head around the project, deciding components without going overboard and leaving out important stuff has been challenging. I eneded going almost 1:1 with Andrew's driagram from class. Click link below.
   [https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720](https://lucid.app/documents/view/fdebe2bb-0e59-4cf9-a574-2bdbc290720)
8. Went with Andrew's architectural design again here. Tried to think about security and added public and private subnets for security [https:lucid.app/lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56](lucidchart/78f59885-480f-4b05-80f9-c67ae7411633/edit?viewport_loc=-7%2C55%2C1869%2C1532%2C0_0&invitationId=inv_d811feb0-e127-4b3d-bc7f-511d31276c56)

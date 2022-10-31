# 1.1.1- AWS Cloud Essentials
## Introduction
#### What is best way to use AWS?
##### Amazon Web Services has a lot of pieces to it and can be hard to figure out just where to get started. AWS account might be like the Starship Enterprise with many different decks and hundreds of rooms tying together a multitude of AWS services while being commanded by several engineering, science and security teams

#### Course objectives
##### Amazon Web Services has over 100 different services and it just seems like they're adding more and more each year. It's important that you start learning what kinds of services offers, what AWS has named that service, and the architecture icon for that servicethat you'll find in the documentation, blogs and in other courses 
- Summary of the service
- Service name
- Architecture icon

#### What you need to know
- Have basic understanding of how a computer works
- How devices talk to each other in an IP network
- You should have a basic undestanding of how a web server works and how a domain name, like linkedin.com points to an IP address for serving up that site to your web browser
- You should be familiar with what a database does and how you would use it in your application to read and store user data
- If you have any familiarity with a modern programming language you shouldn't have too much trouble reading the code samples
##### This course is going to introduce cloud computing concepts using computer parts that you would find on the shelves of any big box electronics store. Such as CPUs and RAM and networking switches and routers. So it helps if you've used these components before and you're at least a little familiar with what they do. I'll introduce you to some cloud concepts by showing you a few ways you can host a website with AWS such as one build on WordPress

## 1. AWS Essential Setup
#### The AWS root account
##### If you signed up your account this way, or someone in your organization only sent you username and password. Then you have an AWS root account. If you have an AWS root account, you are using a special account within AWS and you should only sign into AWS using the root account under certain circumstances

| Root Account |
| ----- |
| Username |
| Password |

##### If you were sent a username, password , and an account ID, or an account alias, or maybe someone sent you a special link to click on to sign in. Then you have an IAM user account. IAM stands for indentity and acces management. And this is how AWS controls who has access to your organization's account. If you have an IAM user account, then your login screen will include a field at the top that says account ID or alias and it should already be filled in for you

| IAM User |
| ----- |
| Username |
| Password |
| Account ID/alias |

##### When you sign in with the AWS root account, you become captain of your starship. And the captain of the starship has special abilities. You can promote and demote your officers. You can even tell your ship to self destruct when you interact with AWS using the root account imagine yourself wearing the captain's uniform, and the great responsabilities that come with uniform. There's a complete list of the special privileges the root user has in the documentation, but the most common uses are:
- First IAM user (Creating your first IAM user)
- Root password (Changing the login credentials of the root user itself)
- Support plans (Changing your plan with AWS)
- Account closure (Deleting the entire AWS account)

##### Note: You never want to give out your AWS root account and you should only log into the AWS root account when you absolutely have to, make sure your AWS root account has a strong password and if you want to take extra precautions
AWS recommends that you secure the root account by using a **physical multi-factor authentication key**
##### AWS Recommends
- Physical MFA (root) - Using the physical MFA key for the AWS root account
- Virtual MFA (IAM user) - Using the virtual MFA option to secure your individual IAM user account 

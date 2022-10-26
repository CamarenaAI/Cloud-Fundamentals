# DevOps Foundations: Continuous Delivery/Continuous Integration

## Introduction
### Wellcome
| Continuous Integration | Continuous Deployment |
| --- | --- |
| The practice of automatically building and unit testing an entire application frequently, ideally on every source code check-in| The practice of automatically deploying every build to production after it passes its automated test |

### What you should know
#### DevOps Fundamentals
- Infraestructure automation
- Continuous delivery
- Reliability engineering 

#### Requeriments
- Bash (OS X Terminal, win-bash, and Linux)
- Basic understanding of coded applications

#### Following along with the demos
[DevOps Foundations: Continuous Delivery/Continuous Integration](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/following-along-with-the-demos?autoSkip=true&autoplay=true&resume=false&u=2154233)

## 1. Continuous Integration and Continuous Delivery
#### DevOps core concept: CI/CD
| Continuous Integration | Continuous Delivery | Continuous Deployment |
| --- | --- | --- |
| The practice of automatically building and unit testing an entire application frequently, ideally on every source code check-in| The practice of deploying every build to a production-like environment and performing automated integration and acceptance testing | The practice of automatically deploying every build to production after it passes its automated test |
| Those check-ins are frequent. You don't use long-running parallel code branches that'll cause large, messy merge effort the older they get. Or if you do, you at least set up builds for them in the meantime to continually validate that they work| This can involve small-scale deployment on a single server using mock enviroments created with Docker containers or virtual machines to mimic a production environment so that you can run those integration test Testing should generally end up with a deployment to aproduction-like environment | Large-scale web properties like Facebook, Etsy, adn Wealthfront use continuous deployment as a key component behind their succes. Even at my work we use continuous deployment for the microservices that backup or Open Threat Exchange website |
| Ideally developers will build and test their application on their local desktop, even before submitting to a shared build system. It's all about shortening the feedback loop for every change| This allows us to validate the deployment process and to see what functionality and performance look like in a real deployment enviroment | Once you're making one change at a time, and you have trustworthy tests that can find issues in your application, then you can remove all the manual gates that get in the way of a continuous flow to production |
###### In most situations, CI and CD is a huge improvement for products and teams of any sort.

#### Benefits of continuous delivery
- Empowering Teams: By nature our pipeline is a self-service system that makes the process of software delivery transparent and understandable to entire team
- Lowered Cycle Times: This is the time from code commit to running in production. Using older methods this time was generally measured in weeks or months, Now it's measured in hours, or even minutes
- Better Security: It might seem odd that security gets better if you are moving faster. It's tempting to think that it's important to go slower to do security
- Rhythm of Practice: Removes stress from teams, both in development and operations. No longer release date's a stressful event
- More Time to Be Productive: This goes hand in hand with the ability to deliver value faster as we discussed earlier. Organiations and teams doing Continuos Delivery find that they spend less time doing unplanned work or rework and more time adding new features

#### Build pipelines in practice
##### A build pipeline is your sequence of operations and the tools that perform them between your source code and your deployment system
![DevOps-Img1](https://raw.githubusercontent.com/IsmaelCamna/WingsElevate-1/main/Wings%20%3A%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img1.png?token=GHSAT0AAAAAAB2K6N2RD573LQKPIM46VRH6Y2YJZOQ "DevOps-Img1")

## 2. Build Your Own Pipeline
#### Introduction our delivery pipeline
![DevOps-Img2](https://raw.githubusercontent.com/IsmaelCamna/WingsElevate-1/main/Wings%20%3A%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img2.png?token=GHSAT0AAAAAAB2K6N2Q5YMCLX2SB7RYU2IWY2YJXBA "DevOps-Img2")
##### Note: No one's pipeline looks the same 

#### Version control practices
![DevOps-Version Control](https://raw.githubusercontent.com/IsmaelCamna/WingsElevate-1/main/Wings%20%3A%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-Version%20Control.png?token=GHSAT0AAAAAAB2K6N2QXOAXY4ZPJGRBIBLCY2YJVXQ "DevOps-Version Control")
##### Version control contains all the source code for your project and maintains the current and historical state of the code. Version control needs to be used by all teams who tocuh the software
##### Best practices for version control
- Always use version control
- Put in all in version control
- Commit often
- Use easy-to-understand commit messages
- Don't commit broken code
- Consider using a master branch approach
- Developing off trunk or master generally offers better performance
- Commit hooks enforce quality
- Be careful with secrets
###### Branch by Abstraction
![DevOps-Branches](https://raw.githubusercontent.com/IsmaelCamna/WingsElevate-1/main/Wings%20%3A%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-Branches.png?token=GHSAT0AAAAAAB2K6N2RRDUY35F46HKP7MMIY2YJV2Q "DevOps-Branches")

#### Version control in action with Git
##### Note: Is necesary have a GitHub account and SSH keys
##### In the command line let's clone our repo
``` 
git clone git@github.com:wickett//word-cloud-generator
cd word-cloud-generator/
git log
git show "commit ideas"
```
###### I'll just change the project description in the readme. I'll open them to edit the readme file and type
``` 
vim README.md 
git status
git diff
```

``` 
cat./hooks/git-pre-commit.hook
make git-hooks
git add.
git commit -m"adding more text to our README"
git status
git push
```

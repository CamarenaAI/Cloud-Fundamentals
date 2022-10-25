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
[DevOps Foundations: Continuous Delivery/Continuous Integration][https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/following-along-with-the-demos?autoSkip=true&autoplay=true&resume=false&u=2154233]

## 1. Continuous Integration and Continuous Delivery
#### DevOps core concept: CI/CD
| Continuous Integration | Continuous Delivery | Continuous Deployment |
| --- | --- | --- |
| The practice of automatically building and unit testing an entire application frequently, ideally on every source code check-in| The practice of deploying every build to a production-like environment and performing automated integration and acceptance testing | The practice of automatically deploying every build to production after it passes its automated test |
| Those check-ins are frequent. You don't use long-running parallel code branches that'll cause large, messy merge effort the older they get. Or if you do, you at least set up builds for them in the meantime to continually validate that they work| This can involve small-scale deployment on a single server using mock enviroments created with Docker containers or virtual machines to mimic a production environment so that you can run those integration test Testing should generally end up with a deployment to aproduction-like environment | Large-scale web properties like Facebook, Etsy, adn Wealthfront use continuous deployment as a key component behind their succes. Even at my work we use continuous deployment for the microservices that backup or Open Threat Exchange website |
| Ideally developers will build and test their application on their local desktop, even before submitting to a shared build system. It's all about shortening the feedback loop for every change| This allows us to validate the deployment process and to see what functionality and performance look like in a real deployment enviroment | Once you're making one change at a time, and you have trustworthy tests that can find issues in your application, then you can remove all the manual gates that get in the way of a continuous flow to production |
###### In most situations, CI and CD is a huge improvement for products and teams of any sort.

#### Benefits of continuous delivery


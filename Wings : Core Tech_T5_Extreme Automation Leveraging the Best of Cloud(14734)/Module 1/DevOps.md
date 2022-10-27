# DevOps Foundations: Continuous Delivery/Continuous Integration

## Introduction
#### Welcome
| Continuous Integration | Continuous Deployment |
| --- | --- |
| The practice of automatically building and unit testing an entire application frequently, ideally on every source code check-in| The practice of automatically deploying every build to production after it passes its automated test |

#### What you should know
##### DevOps Fundamentals
- Infraestructure automation
- Continuous delivery
- Reliability engineering 

##### Requeriments
- Bash (OS X Terminal, win-bash, and Linux)
- Basic understanding of coded applications

#### Following along with the demos
[Linkedin: DevOps Foundations: Continuous Delivery/Continuous Integration](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/following-along-with-the-demos?autoSkip=true&autoplay=true&resume=false&u=2154233)

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
![DevOps-Img1](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img1.png?raw=true)

## 2. Build Your Own Pipeline
#### Introduction our delivery pipeline
![DevOps-Img2](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img2.png?raw=true)
##### Note: No one's pipeline looks the same 

#### Version control practices
![DevOps-Version Control](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-Version%20Control.png?raw=true)
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
![DevOps-Branches](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-Branches.png?raw=true)

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
[Linkedin: Version control in action with Git](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/version-control-in-action-with-git?autoplay=true&resume=false&u=2154233)

#### Continuous integration systems
- Open Source
- Commercial (purchased)
- CI as a service
##### Continuous integration is a practice
##### Several important principles and practices to consider when using a CI system
- Start with a clean environment
- Build to pass the coffe test
##### A CI Culture
- Run test locally before committing
- Don't commit new code to broken builds
- Don't leave the build broken
- Don't remove test that fail
##### Use notifications to update your build progress

#### CI in actions with Jenkins
##### CI system looks like in practice. For that, we're going to use Jenkins
##### Jenkins is a free, open-source tool (It´s written in Java so it runs on any platform from Linux to Windows to Mac)
[Download Jenkins](https://jenkins.io/download/)
[Linkedin: CI in actions with Jenkins](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/ci-in-action-with-jenkins?autoplay=true&resume=false&u=2154233)

#### Build artifacts
##### Benefits of Artifacts
- Reliability
- Composability
- Security
- Shareability
##### Plan Ahead
- Packaging format(s)
- Dependency managment
- Artifact repo

#### Artifacts in action with Nexus
- Nexus (2 and 3)
- JFrog Artifactory
- Apache Archiva
- And many more, See https://binary-repositories-comparison-github.io

#### Testing and continuous delivery
##### Good Test
- Are fast
- Are reliable
- Isolate failures for you
##### Types of testing
- Unit testing: Performed at build time on a single unit of code and/or artifact without use of external dependencies or deployment
Example tools: JUnitX, XUnit, and Rspec
- Integration testing: Performed as your bring together pieces of your application and as it needs to use external dependencies
Example tools: Abao/RAML and Serverspec 
- End-to-end (E2E) testing: Performed to excercise the full flow of your application in the same way an end user would
- Security testing: Performed to look for flaws in your code and runtime to prevent compromises ans leaking of data in production
- Shift left: Move testing early as possible in the development process, ideally to the dev desktop
- Text fixture: A set objects used to run a test in a well-known environment
- System under test (SUT): The application and system on wich you are running your test
- Cycle time: The time from when an item (feature or bug fix) is worked on until it is delivered into production
- Lead time: The time taken from when an item (feature or bug fix) is requested until it is delivered into production
- Mock: Code designed to stand in for a piece of code that contains dependencies to enable unit tests

#### Testing philosophy
- Tets-driven development (TDD): The practice of wiritng a failing test first, and then writing the code that causes the test to pass
- Behavior-driven development (BDD): The practice test in a simple end-user-behavior-centric language
- Acceptance test-driven development (ATDD): The practice of agreeing on acceptance test before development to establish what is to be delivered
##### The Big Three Testing Metrics
- Cycle Time - time from the start of work to delivery
- Velocity - value delivered per unit time
- Customer satistafaction - how well a product/service met the customer's needs. NPS scores and bug reports work well here
![DevOps-Img4](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img4.png?raw=true)

#### Unit testing in action
##### Whit good unit testing practices, a safety is built up around your code, making changes in the future a breeze. Additionally, they build confidence in development team to deliver faster
##### For Go, I can use GoConvey it's easy setup and works with the native Go testing package
##### Mocks are way to test with fake data for a provider
[Linkedin: Unit testing in action](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/unit-testing-in-action?autoSkip=true&autoplay=true&resume=false&u=2154233)

#### Application deploy and release
##### Deploy with
- The same artifact
- The same way
- The same (similar) environment
- The same smoke tests
##### Separate Deploy and Release
- Blue/green deployments
- Feature flag
##### Deployment Options
- Source pulls
- CM systems
- Orchestration Systems
- Build 
- And any more
##### Product Update Deploys to Customer
![DevOps-img3](https://github.com/IsmaelCamna/WingsElevate-1/blob/main/Wings%20:%20Core%20Tech_T5_Extreme%20Automation%20Leveraging%20the%20Best%20of%20Cloud(14734)/Module%201/Img/DevOps-img3.png?raw=true)

#### Deployment in action with Chef
[Linkedin: Deployment in action with Chef](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/deployment-in-action-with-chef?autoSkip=true&autoplay=true&resume=false&u=2154233)

#### Integration testing in action with Abao
- Integration testing: Testing performed to expose defects in the interfaces and in the interactions between integrated components or systems
##### Don't mix your unit tests with your integration test
[Linkedin: Integration testing in action with Abao](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/integration-testing-in-action-with-abao?autoSkip=true&autoplay=true&resume=false&u=2154233)

#### UI testing in action with Robot
##### UI testting has it's advantages and disadvantages. On the one hand, it totally simulates the user experience on a UI application. Level of testing below it just aren't complete. But one the other hand it's slow and usually pretty touchy UI tests requiere a lot of mainteance in the face of app changes
- Regression testing: A test conducted to verify that software that was previously developed and tested still performs the same way after it is changed or iterfaced with other software
- Acceptance testing: A test to determine whether the requirements of a specification or contract have been met

[Linkedin: UI testing in action with Robot](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/ui-testing-in-action-with-robot?autoSkip=true&autoplay=true&resume=false&u=2154233)

#### Security testing in action with gauntlt
##### The main types of tests are static and dynamic
- Dynamic Security Testing
    - Pros
        - Test actual attack payloads
        - Collaboration between Dev, Sec, and Ops
    - Cons
        - Requires system to be running
        - Can be slow    
        
[Linkedin: Security testing in action with gauntlt](https://www.linkedin.com/learning/devops-foundations-continuous-delivery-continuous-integration-2017/security-testing-in-action-with-gauntlt?autoSkip=true&autoplay=true&resume=false&u=2154233)

## 3. Putting It All Together
#### CI/CD best practices
- **Each developer** is responsible for their check-in through deployment
- **Small** changes. Build quality in
- **Don´t** check in broken builds
- **Automate** high-quality testing
- Run tests **before** check-in
- **Fix** flaky tests
- **Don't** ignore or disable tests
- **Automate** deployments
- Keep the build and deploy **fast**
##### Own Your Build
- Take responsibility for your build
- Immediately address a broken build
- Revert if fixing takes time
- No check-ins while the builds broken--the line stops

#### Continuous delivery in real life
- The most important thing to watch is total cycle time
- You'll need to balance the benefits of fast feedback with the speed of a single build
##### Problems in real life
- Builds are not reliable
- Quality goes down
- Deploys take a long time
- There will be tradeoffs

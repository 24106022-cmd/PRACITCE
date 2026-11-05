[ASDD_Ubuntu_Practical_Steps.pdf](https://github.com/user-attachments/files/34386995/ASDD_Ubuntu_Practical_Steps.pdf)


**Experiment 1: Jira Board and Sprint Management**

Theory:
Agile Software Development is an iterative and incremental approach to software development in which a project is divided into smaller parts called iterations or sprints. It focuses on customer satisfaction, teamwork, continuous feedback, and delivering working software frequently.

Jira is a project management tool used by Agile teams to plan, track, and manage their work. It supports Scrum and Kanban methodologies.

In Scrum, work is organized into Product Backlog and Sprint Backlog. The Product Backlog contains all the features, requirements, and improvements needed for the product. The Sprint Backlog contains selected tasks that the team plans to complete during a particular sprint.

A Sprint is a fixed period, usually 1–4 weeks, during which the development team works to complete a set of tasks and deliver a working product increment.

Jira provides a board to visualize the progress of tasks through different stages such as:
- To Do: Task is yet to be started.
- In Progress: Task is currently being worked on.
- In Review: Task is being checked or tested.
- Done: Task has been completed.
Jira helps teams improve collaboration, track progress, identify problems, and complete projects efficiently.

Q1. Differentiate between Product Backlog and Sprint Backlog.
Product Backlog	Sprint Backlog
Contains all requirements of the product.	Contains tasks selected for a particular sprint.
Managed by the Product Owner.	Managed by the Developers/Scrum Team.
Covers the entire product.	Covers only the current sprint.
Continuously updated.	Updated as work progresses during the sprint.
Includes features, bugs, and improvements.	Includes selected items and the plan to complete them.

Q2. Define Product Backlog and Sprint Backlog.
Product Backlog: A prioritized list of all features, requirements, bug fixes, and improvements needed in a product.
Sprint Backlog: A list of Product Backlog items selected for a sprint, along with the tasks required to achieve the Sprint Goal.

Q3. How is the Sprint Process carried out in an Agile Team?
1. Sprint Planning     : The team selects tasks from the Product Backlog.
2. Sprint Execution    : Developers work on the selected tasks.
3. Daily Scrum         : Team members discuss progress and obstacles.
4. Sprint Review       : The completed work is demonstrated to stakeholders.
5. Sprint Retrospective: The team discusses improvements for the next sprint.
6. Next Sprint         : The process repeats with the updated backlog.

**Experiment 2: Jira and GitHub Integration**

Theory:
Jira and GitHub Integration connects Jira project management with GitHub version control. Jira is used to manage issues and tasks, while GitHub is used to store and manage source code.
Every Jira issue has a unique issue key, such as ASDD-101. Developers can include this issue key in their GitHub branch names, commit messages, and pull requests.

For example, a branch can be created using:
ASDD-101-login-feature

When developers make changes and commit them with the Jira issue key, Jira can display related development activities.
This integration helps team members understand which code changes are associated with which tasks. It improves collaboration, traceability, transparency, and project management.

Q1. How can Jira issues be linked to GitHub branches and commits? How is it useful for others to track changes?
Jira issues can be linked to GitHub branches and commits by including the Jira issue key in the branch name and commit message.

Example:
- Jira Issue: ASDD-101
- Branch: ASDD-101-login-feature
- Commit: git commit -m "ASDD-101 Add login feature"
After integration, Jira can display associated branches, commits, and pull requests.

Benefits:
1. Helps track code changes related to Jira issues.
2. Improves collaboration between developers.
3. Provides transparency in development.
4. Makes it easier to identify completed tasks.
5. Helps developers review and understand changes.



**Experiment 3: Git Commands and Version Control**

Theory:
Git is a distributed version control system used to track changes in source code. It allows multiple developers to work on the same project and maintain different versions of files.

GitHub is a cloud-based platform used to host Git repositories and collaborate with other developers.

Git helps developers maintain project history, manage code changes, create branches, and collaborate efficiently.

A repository is a storage location for project files and their version history. A branch is an independent line of development that allows developers to work on features without affecting the main branch.

The basic Git workflow consists of:
1. Working Directory: Files are created or modified.
2. Staging Area: Changes are selected using git add.
3. Local Repository: Changes are saved using git commit.
4. Remote Repository: Changes are uploaded using git push.
Git is widely used in Agile and DevOps for collaboration, version control, and continuous integration.

Q1. Explain the purpose of Git commands.
Command      	Purpose
git add     :	Adds modified files to the staging area.
git commit  :	Saves staged changes in the local repository.
git push    :	Uploads local commits to the remote repository.
git branch	: Lists existing branches or helps create new branches.
git status	: Displays the current state of the working directory and staging area.

Additional useful commands:
Command	                     Purpose
git clone                   : URL	Copies a remote repository to the local machine.
git checkout -b branch_name :	Creates and switches to a new branch.
git pull                    :	Downloads and integrates changes from a remote repository.
git log	                    : Displays commit history.

Q2. Explain GitHub Actions.
GitHub Actions is a CI/CD automation platform provided by GitHub. It automatically builds, tests, and deploys software whenever specified events occur in a repository.

It uses workflow files written in YAML and stored in the .github/workflows directory.

Main components:
- Workflow: Automated process triggered by an event.
- Event: Action that triggers a workflow, such as a push or pull request.
- Job: A group of steps executed on a runner.
- Step: An individual task or command.
- Runner: A machine that executes the workflow.
  
Advantages:
1. Automates software testing and building.
2. Reduces manual effort.
3. Detects errors early.
4. Supports continuous integration and delivery.
5. Improves software quality.



**Experiment 4: Docker Image Management and Container Execution**

Theory:
Docker is an open-source platform used to develop, package, and run applications inside containers. Containers provide an isolated environment containing the application and its dependencies.

Docker uses images as templates to create containers. A Docker image contains the application code, libraries, dependencies, and configuration required to run an application.

A Docker container is a running instance of a Docker image. Containers are lightweight, portable, and isolated from the host system.

Docker allows applications to run consistently across different environments, such as development, testing, and production.

Common Docker commands include:
- docker pull   – Downloads an image from Docker Hub.
- docker images – Lists available images.
- docker run    – Creates and starts a container.
- docker ps     – Displays running containers.
- docker ps -a  – Displays all containers, including stopped ones.

Docker is widely used in DevOps for application deployment, testing, and containerization.
Theory Questions and Answers

Q1. Differentiate between a Docker image and a Docker container.
Docker Image	Docker Container
A template used to create containers.	An instance of a Docker image.
Generally read-only.	Has a writable layer.
Contains application and dependencies.	Runs the application in an isolated environment.
Can create multiple containers.	Created from an image.
Stored in image repositories.	Managed by the Docker engine.
Example: A Docker image is like a recipe, while a container is the actual dish prepared using that recipe.

Q2. Explain the Docker Build command.
The docker build command is used to create a Docker image from a Dockerfile.
Syntax:
docker build -t image_name .
Explanation:
- docker build: Builds the image.
- -t: Assigns a name or tag to the image.
- image_name: Name of the image.
- .: Specifies the current directory as the build context.
The Docker engine reads the Dockerfile instructions, executes them, and creates a Docker image.



**Experiment 5: Dockerfile Creation and Image Building**

Theory:
A Dockerfile is a text file containing instructions used to build a Docker image. It defines the application environment, dependencies, files, and commands required to run an application inside a Docker container.

Docker uses the Dockerfile to automatically build images, making application deployment consistent and repeatable.

The Dockerfile contains instructions such as FROM, COPY, RUN, EXPOSE, and CMD.

The docker build command reads the Dockerfile and creates an image. The image can then be used to run a container using the docker run command.

Dockerfiles are useful because they automate application setup, reduce manual configuration, and simplify deployment across different environments.

Q1. What is a Dockerfile? Explain the purpose of FROM, COPY, RUN, EXPOSE, and CMD.
A Dockerfile is a text file containing instructions to build a Docker image.
Instruction	      Purpose
FROM	      : Specifies the base image used to build the image.
COPY	      :  Copies files from the host system into the image.
RUN         :	Executes commands during image building, such as installing packages.
EXPOSE	    : Documents the port on which the application listens inside the container.
CMD	        : Specifies the default command executed when the container starts.

Example:
FROM python:3.12
WORKDIR /app
COPY . .
RUN pip install flask
EXPOSE 5000
CMD ["python", "app.py"]


This Dockerfile creates a Python environment, copies application files, installs Flask, documents port 5000, and runs the application.



**Experiment 6: Terraform and GitHub Actions**

Theory:
Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp. It is used to create, manage, and provision infrastructure such as virtual machines, networks, and cloud resources using configuration files.

Terraform uses HashiCorp Configuration Language (HCL) to define infrastructure in a declarative manner. This means the user specifies the desired infrastructure, and Terraform determines the steps required to achieve it.

Terraform maintains a state file that tracks the resources it manages. It compares the desired configuration with the current state and identifies necessary changes.

Terraform can be integrated with GitHub Actions to automate infrastructure validation and deployment.

Advantages of Terraform:
1. Automates infrastructure provisioning.
2. Reduces manual configuration.
3. Supports multiple cloud providers.
4. Enables infrastructure version control.
5. Provides consistent and repeatable deployments.

Q1. What is Terraform? List the Terraform commands and explain their purpose briefly.
Terraform is an Infrastructure as Code tool used to provision and manage infrastructure through configuration files.

Command	              Purpose
terraform init	    : Initializes the working directory and downloads required providers.
terraform plan	    : Shows the changes Terraform will make.
terraform apply	    : Applies the planned changes and creates or modifies infrastructure.
terraform destroy	  : Destroys infrastructure managed by Terraform.
terraform validate  :	Checks whether configuration files are syntactically valid.
terraform fmt	      : Formats Terraform configuration files.
terraform show	    : Displays the current state or a saved plan.
terraform output	  : Displays output values defined in the configuration.

Basic Terraform workflow:

terraform init
terraform validate
terraform plan
terraform apply

terraform destroy is used when the managed infrastructure needs to be removed.



**Experiment 7: Grafana Using Docker**

Theory:
Grafana is an open-source monitoring and data visualization platform used to analyze and display data through interactive dashboards.

It helps DevOps engineers monitor applications, servers, infrastructure, and system performance.

Grafana supports multiple data sources, such as Prometheus, InfluxDB, and MySQL. It collects data from these sources and presents it using graphs, charts, tables, and gauges.

In DevOps, Grafana is commonly used to monitor CPU utilization, memory usage, network traffic, application performance, and system health.

Grafana can be deployed using Docker, which makes installation and execution easier.

The Docker container port can be mapped to a local machine port to access Grafana through a web browser.

Advantages of Grafana:
1. Provides real-time monitoring and visualization.
2. Supports multiple data sources.
3. Offers customizable dashboards.
4. Helps identify performance issues.
5. Supports alerts and notifications.
6. Simplifies infrastructure monitoring.

Q1. What is Grafana, and how is it used for monitoring and visualization in DevOps?
Grafana is an open-source monitoring and visualization tool used to display system and application metrics through interactive dashboards.

Uses in DevOps:
1. Monitors CPU, memory, and network utilization.
2. Displays application and infrastructure performance.
3. Integrates with Prometheus and other data sources.
4. Helps identify errors and performance issues.
5. Provides dashboards for real-time monitoring.
6. Supports alerting when configured with suitable rules and notification systems.
Example: Grafana can display Kubernetes pod CPU and memory usage using metrics collected by Prometheus.

**Quick Revision: Important Concepts**

Agile	      : Iterative software development approach focused on collaboration and continuous delivery.

Scrum	      : Agile framework that organizes work into sprints.

Sprint      : Fixed period during which a team completes selected work.

Velocity    :	Amount of work a Scrum team completes in a sprint, commonly measured in story points.

Jira        :	Project management tool used to track tasks and Agile workflows.

Git	        : Distributed version control system.

GitHub      :	Platform for hosting Git repositories and collaboration.

CI          :	Continuous Integration; automatically integrates and tests code changes.

CD	        : Continuous Delivery or Continuous Deployment; automates software release processes.

Docker      :	Platform for building and running applications in containers.

Image	      : Template used to create Docker containers.

Container   :	Isolated running instance of an image.

Dockerfile  :	File containing instructions to build a Docker image.

Terraform	  : Infrastructure as Code tool used to provision infrastructure.

Grafana	    : Monitoring and visualization platform.

**Most Important Commands for Practical Exam**
Git
git clone URL
git checkout -b branch_name
git branch
git status
git add .
git commit -m "Changes"
git push


Docker
docker pull ubuntu
docker images
docker run -it ubuntu bash
docker ps
docker ps -a


Dockerfile
docker build -t myapp .
docker run -it myapp


Terraform
terraform init
terraform validate
terraform plan
terraform apply


Grafana
docker pull grafana/grafana
docker run -d -p 3001:3000 grafana/grafana



1. Agile Software Development
Q1. What is Agile?
Agile is a software development approach in which software is developed in small increments with continuous testing, feedback, and improvement.
Q2. What is the Agile Manifesto?
The Agile Manifesto is a document that defines the values and principles of Agile software development.

It has 4 values and 12 principles.

Four values:
1. Individuals and interactions over processes and tools.
2. Working software over comprehensive documentation.
3. Customer collaboration over contract negotiation.
4. Responding to change over following a plan.

   
Q3. What are the 12 principles of Agile?
1. Satisfy customers through early and continuous delivery.
2. Welcome changing requirements, even late in development.
3. Deliver working software frequently.
4. Business people and developers work together daily.
5. Build projects around motivated individuals.
6. Face-to-face communication is the most effective.
7. Working software is the main measure of progress.
8. Maintain a sustainable development pace.
9. Focus on technical excellence and good design.
10. Keep things simple.
11. Self-organizing teams produce the best designs.
12. Regularly reflect and improve the process.

    
Q4. What is the Waterfall Model?
The Waterfall Model is a traditional software development model in which development happens sequentially, and each phase is completed before the next phase begins.

Stages of Waterfall:
1. Requirement Analysis
2. System Design
3. Implementation (Coding)
4. Testing
5. Deployment
6. Maintenance
Q5. What is Feature-Driven Development (FDD)?
FDD is an Agile methodology that develops software by focusing on small, client-valued features.

Example: In an online shopping application, login, payment, and product search are separate features.

2. Scrum
Q6. What is Scrum?
Scrum is an Agile framework used to develop software in small iterations called Sprints.
Q7. What are the Scrum models or frameworks?
Scrum is an Agile framework. Its main elements are:
- Scrum roles
- Scrum events
- Scrum artifacts
It works through iterative development using Sprints.
Q8. Who are the members of a Scrum team?
There are three main Scrum roles:
1. Product Owner: Defines requirements and prioritizes the product backlog.
2. Scrum Master: Ensures Scrum is followed and removes obstacles.
3. Developers: Develop, test, and deliver the product.

   
Q9. What is a Sprint?
A Sprint is a fixed period, usually 1–4 weeks, during which the team completes selected work and delivers a usable product increment.

Q10. What is the Sprint Process?

1. Sprint Planning
2. Sprint Backlog Creation
3. Development and Daily Scrum
4. Testing
5. Sprint Review
6. Sprint Retrospective
Then the next Sprint begins.
Q11. What is a Product Backlog?
The Product Backlog is a prioritized list of all features, requirements, and improvements needed in a product.
Q12. What is a Sprint Backlog?
The Sprint Backlog is a list of tasks selected from the Product Backlog that the team plans to complete during a Sprint.

Difference:
Product Backlog	Sprint Backlog
Contains all product requirements.	Contains work for the current Sprint.
Managed by Product Owner.	Managed by Developers.
Changes continuously.	Focuses on the current Sprint.

Q13. What is Velocity in Scrum?
Velocity is the amount of work a team completes during one Sprint, usually measured in story points.

It helps estimate the work for future Sprints.
Q14. What is Planning Poker?
Planning Poker is an Agile estimation technique used to estimate the effort or complexity of tasks.

Team members select cards with numbers, often Fibonacci numbers, and discuss differences in estimates.
Q15. What is a User Story?
A User Story describes a software feature from the user's perspective.

Format:

"As a [user], I want [feature], so that [benefit]."

Example: As a student, I want to view my attendance so that I can track my attendance percentage.

3. Jira, Git, GitHub, and CI/CD
Q16. What is Jira?
Jira is a project management and issue-tracking tool used to manage tasks, bugs, and Agile Sprints.
Q17. What is Git?
Git is a distributed version control system used to track changes in source code and manage different versions of a project.
Q18. What is GitHub?
GitHub is an online platform used to host Git repositories and collaborate with other developers.

Difference between Git and GitHub:
Git	GitHub
Version control system.	Online code hosting platform.
Works locally.	Works mainly online.
Tracks code changes.	Stores repositories and supports collaboration.

Q19. What is CI/CD?
CI/CD stands for:
- CI – Continuous Integration: Frequently merging and testing code changes.
- CD – Continuous Delivery/Deployment: Automatically preparing or deploying software updates.
Q20. What is a CI/CD Pipeline?
A CI/CD pipeline is an automated process that takes code from development to testing and deployment.

Basic stages:
1. Code
2. Build
3. Test
4. Deploy

4. Docker
Q21. What is Docker?
Docker is a platform used to package and run applications inside containers.

Containers make applications easier to run consistently across different environments.
Q22. What is a Docker Image?
A Docker Image is a read-only template containing the application, dependencies, and instructions required to create a container.
Q23. What is a Docker Container?
A Docker Container is a running instance of a Docker Image.

Difference:
Docker Image	Docker Container
Template or blueprint.	Running instance of the image.
Read-only.	Has a writable layer.
Used to create containers.	Used to run applications.


5. DevOps
Q24. What is DevOps?
DevOps is a combination of Development and Operations practices that improves collaboration and automates software development, testing, and deployment.

Q25. What are the 7 Cs of DevOps?
The commonly taught 7 Cs are:
1. Continuous Development: Frequently develop and update code.
2. Continuous Integration: Regularly merge and integrate code.
3. Continuous Testing: Test software continuously.
4. Continuous Deployment: Deploy software automatically.
5. Continuous Delivery: Keep software ready for release.
6. Continuous Monitoring: Monitor application performance and errors.
7. Continuous Feedback: Collect feedback for improvement.
Note: Some textbooks use slightly different versions of the 7 Cs.



Q26. What is the DevOps Lifecycle?
The DevOps lifecycle consists of:
1. Plan
2. Code
3. Build
4. Test
5. Release
6. Deploy
7. Operate
8. Monitor
It is a continuous cycle of development and improvement.

6. Extreme Programming (XP)
Q27. What is Extreme Programming (XP)?
Extreme Programming is an Agile software development methodology that focuses on high-quality software, frequent releases, and customer satisfaction.

Q28. What are the main practices of XP?
- Pair Programming
- Test-Driven Development (TDD)
- Continuous Integration
- Small Releases
- Simple Design
- Refactoring
- Customer Feedback
  
Q29. What is Pair Programming?
Pair Programming is a technique in which two programmers work together on the same computer.
One writes the code (Driver), while the other reviews it (Navigator).

Q30. What is Test-Driven Development (TDD)?
TDD is a development approach in which developers write tests before writing the actual code.

Process: Write Test → Write Code → Refactor.

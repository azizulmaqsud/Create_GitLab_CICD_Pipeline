# Create GitLab CICD Pipeline
## Why GitLab?
- GitLab CI builds and tests the software automatically whenever a developer pushes code to the application
- GitLab CD places the changes of each code in the production in day2day deployment of the production

## GitLab Architecture
- Gitlab instance or Gitlab server hosts application code and pipelines altogether
- GitLab Runners: The Gitlab instance may have multiple GitLab runners connected to the Gitlab server machine. Runners are executing the pipelines

## Pipeline Configuration .gitlab-ci.yml
- Configuration as a Code (CaaC) or Pipeline as Code (PaaC), the total pipeline is written in the code and hosted in the git repository as a YAML file
- using .gitlab-ci.yml, Gitlab detects the pipeline code and executes it immediately
- YAML file is created at the root of the project repository. All the pipeline configuration is written inside
- Write the YAML file once in the GitLab UI then NO need to go back and forth for editing your Gitlab 

## Jobs
- Tasks in the CICD pipeline as running tests, building an image, and deploying to the server are configured as GitLab 'jobs’
- Each job has a name and inside the job, there are a couple of parameters or a couple of attributes or things that require to configure for the job
- The first or required attribute of a job is called script. Following the script, commands are executed for the jobs

## Let's Start a LAB! Pre-requisite:
• CREATE ACCOUNT - https://gitlab.com/
• CREATE ORG/REPO – DevOps or any name
• CREATE PROJECT REPO - GitlabCICD or any name

## Runner Setup in Shell [Here I am using AWS EC2 UBUNTU, Debian commands bellow]
- sudo su
- sudo apt-get update -y
- exec commands:
• curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh > script.deb.sh
• sudo bash script.deb.sh
• sudo apt install gitlab-runner
• systemctl status gitlab-runner
- For REGISTRATION_TOKEN go to Project settings -> CICD -> Runners -> Copy the token and paste the command
• sudo gitlab-runner register --url https://gitlab.com/ --registration-token $REGISTRATION_TOKEN

- GitLab Runner becomes active with EC2 IPv4 IP address here
- Push a dummy change to the Repo and go to https://gitlab.com/yourRepo. Refresh it.

## GitLab Executors
- GitLab Runner implements a number of executors that can be used to run your builds in a different scenario. Types of Runners are:
- Shell
- Docker
- Kubernetes

## Create .gitlab-ci.yml file, Steps:
- On the left side pane of Gitlab UI, select Repository > Files > select branch to commit. If you are not sure then just leave it as master or main
- Then select the plus icon () and new file
- create Filename .gitlab-ci.yml > in the larger window, paste sample code (code I shared in the snapshot)

## Thank You! 
# Stay Connected !!

https://www.youtube.com/channel/UCNwP7KEElaJ7cdDTLP-KbBg

https://www.linkedin.com/in/azizul-maqsud/

https://azizulmaqsud-1684501031000.hashnode.dev/

https://medium.com/@azizulmaqsud

https://twitter.com/Sohail2me

https://github.com/azizulmaqsud
